+++
tags = ["devexpress","treelist","code","c#","development"]
categories = ["development","code","c#"]
date = "2011-07-09T00:00:00Z"
title = "Using Devexpress Winforms Treelist Control"
keywords = ["development","code","c#"]

+++

I have been using the DevExpress WinForms & ASP.Net controls at work. I have been surprised by the many useful features that you get straight out of the box. I mostly work with the ASP.Net controls, but recently I have been using the DevExpress TreeList WinForm controls. 

<!--more-->

I needed to and when the user clicks the third level it displays relevant information to the user.
One of the things that I found really interesting was that your business object can implement the IVirtualTreeListData interface, this will then allow you to create the hierarchical structure for your business objects and then you will be able to directly bind a list of these objects to the tree list. For my current project I did not want to implement this interface directly in my entities. I thought it would be better to define a class that only catered to the concerns related to the tree list and did not expose all the details of the entity. Below is the TreeNode class that implements the IVirtualTreeListData.

```
public class TreeNode : TreeList.IVirtualTreeListData
{
 protected TreeNode parentNode;
 protected List childrenNodes = new List();
 protected string _name;
 protected int _id;</code>
 
 public TreeNode (TreeNode parent, string name, int id)
 {
  this.parentNode = parent;
 
  _name = name;
  _id = id;
 
  if(this.parentNode != null)
  this.parentNode.childrenNodes.Add(this);
 } 
 
 public void VirtualTreeGetCellValue(VirtualTreeGetCellValueInfo info)
 {
  if (info.Column.AbsoluteIndex == 0)
   info.CellData = _name;
  else
   info.CellData = _id;
 }
 
 public void VirtualTreeGetChildNodes(VirtualTreeGetChildNodesInfo info)
 {
  info.Children = childrenNodes;
 }
 
 public void VirtualTreeSetCellValue(VirtualTreeSetCellValueInfo info)
 {
  if (info.Column.AbsoluteIndex == 0)
   _name = info.NewCellData.ToString();
  else
   _id = (int)info.NewCellData;
 }
}
```

Below is the method that populates the TreeNodes with data from your entities and binds to the treelist.

```
private void SetupControls()
{
 //This sections sets up the tree list columns. I only display the fist column to the user. The second is used to  retrieve the additional information for the user.
 TreeListColumn col1 = new TreeListColumn();
 col1.Caption = "Name";
 col1.VisibleIndex = 0;
 TreeListColumn col2 = new TreeListColumn();
 col2.Caption = "Id";
 col2.VisibleIndex = 1;
 col2.Visible = false;
 treeList1.Columns.AddRange(new TreeListColumn[] { col1, col2 });
 //Here we create the root node for the treelist
 TreeNode datasource = new TreeNode(null, null, 0);
 //Iterate through the list of your entities to create the level 1, level 2 and level 3 nodes for
 tree list.
 foreach (TreeBusinessObject treenode in GetNodeObjects())
 {
  TreeNode node = new TreeNode(datasource, treenode.Node, 0);
  TreeNode subnode = new TreeNode(node, treenode.SubNode, 0);</code>
 
  foreach (var item in treenode.GetChildSubNodes())
  {
   TreeNode childnode = new TreeNode(subnode, item, treenode.Id);
  }
 }
 //Bind to the tree list
 treeList1.DataSource = datasource;
}
```

I am also adding the code for my business object.

```
public class TreeBusinessObject
{
 public int Id { get; set; }
 public string Node { get; set; }
 public string SubNode { get; set; }</code>
 
 private List childSubNode;
 
 public TreeBusinessObject()
 {
  childSubNode = new List();
 }
 
 public TreeBusinessObject(int id)
 {
  Id = id;
  Node = String.Format("Node {0}", id.ToString());
  SubNode = String.Format("Sub Node {0}", id.ToString());
 
  childSubNode = new List();
  AddChildNode(String.Format("Child A1_{0}", id.ToString()));
  AddChildNode(String.Format("Child A2_{0}", id.ToString()));
  AddChildNode(String.Format("Child A3_{0}", id.ToString()));
 }
 
 public void AddChildNode(string childnode)
 {
  childSubNode.Add(childnode);
 }
 
 public List GetChildSubNodes()
 {
  return childSubNode;
 }
 
 public void RemoveChildNode(string childnode)
 {
  childSubNode.Remove(childnode);
 }
 
 public void ClearAllChildNodes()
 {
  childSubNode.Clear();
 }
}
```

### Conclusion
I really liked that your business object can implement an interface and then directly bind a list of business objects to the tree list. Initially when I was working with the control I did not realise that there was a difference between selected nodes and focused nodes, but after using the control the difference is clear. The only thing I couldn’t figure out was setting the state of the tree list i.e. whether is was expanded or collapsed.
For for more information about binding a treelist to your business objects refer to the DevExpress documentation.
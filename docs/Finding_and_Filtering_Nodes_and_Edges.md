[Finding and Filtering Nodes and Edges](http://wiki.cytoscape.org/Cytoscape_3/UserManual/Cytoscape_3/UserManual/Filters)
========================================================================================================================

Search Bar
----------

You can search for nodes and edges by column value directly through
Cytoscape's tool bar. For example, to select nodes or edges with a
column value that starts with "STE", type `ste*` in the search bar. The
search is case-insensitive. The `*` is a wildcard character that matches
zero or more characters, while "?" matches exactly one character. So
`ste?` would match "STE2" but would not match "STE12". Searching for
`ste*` would match both.

![searchbar.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Filters?action=AttachFile&do=get&target=searchbar.png)

To search a specific column, you can prefix your search term with the
column name followed by a `:`. For example, to select nodes and edges
that have a "COMMON" column value that starts with "STE", use
`common:ste*`. If you don't specify a particular column, all columns
will be searched.

Columns with names that contain spaces, quotes, or characters other than
letters and numbers currently do not work when searching a specific
column. This will be fixed in a future release.

To search for column values that contain special characters you need to
escape those characters using a "\\". For example, to search for
"GO:1232", use the query `GO\:1232`. The complete list of special
characters is:

    + - & | ! ( ) { } [ ] ^ " ~ * ? : \

**Note:** Escaping characters only works when searching all columns. It
currently does not work for column-specific searching. This will be
fixed in a future release.

Filters
-------

Cytoscape 3 provides a new user interface for filtering nodes and edges.
These tools can be found in the **Select** panel:

![select-panel.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Filters?action=AttachFile&do=get&target=select-panel.png)

There are two main types of filters: narrowing filters, which can be
combined into a tree; and chainable filters, which can only be combined
in a linear chain. These can be found in the **Filter**, and **Chain**
tabs of the **Select** panel, respectively.

### Narrowing Filters

Narrowing filters select nodes and edges based on user-specified
constraints. For example, you can use these filters to find edges with a
weight between 0 and 5.5, or nodes with degree less than 3. A filter can
contain an arbitrary number of sub-filters. To add one to your filter,
click on the "+" button.

#### Interactive Filter Application Mode

Due to the nature of narrowing filters, Cytoscape can apply them to a
network efficiently and interactively. Some filters even provide slider
controls to quickly explore different thresholds. This is the default
behavior on smaller networks. For larger networks, Cytoscape
automatically disables this interactivity. You can override this by
manually checking the **Apply Automatically** box above the **Apply**
button:

![apply-automatically.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Filters?action=AttachFile&do=get&target=apply-automatically.png)

Cytoscape comes packaged with the following narrowing filters:

#### Column Filter

This filter will match nodes or edges that have particular column
values. For numeric columns, sliders are provided to set thresholds in
interactive mode. Otherwise, minimum and maximum values can be keyed in.

From string columns, a variety of matching options are provided:

![string-column.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Filters?action=AttachFile&do=get&target=string-column.png)

For example, column values can be checked if they contain or match
exactly a particular string. The filter can also match against
Java-style regular expressions. A checkbox controls whether the matching
is done in a case-sensitive way.

#### Degree Filter

The degree filter matches nodes with a degree that falls within the
given minimum and maximum values, inclusive. You can choose whether the
filter operates on the in-degree, out-degree or overall (in + out)
degree.

#### Topology Filter

The topology filter matches nodes with a certain number of neighbors
which are within a fixed distance away. The thresholds for the
neighborhood size and distance can be set independently.

#### Grouping and Organizing Filters

By default, nodes and edges need to satisfy the constraints of all your
filters. You can change this so that instead, only the constraints of at
least one filter needs to be met in order to match a node or edge. This
behavior is controlled by the **Match all/any** drop-down box. This
appears once your filter has more than one sub-filter. For example,
suppose you wanted to match nodes with column *COMMON* containing `ste`
or `cdc`, but you only want nodes with degree 5 or more, you'd first
construct a filter that looks like this:

![sample-group2.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Filters?action=AttachFile&do=get&target=sample-group2.png)

This filter will match nodes where **COMMON** contains `ste` **and**
`cdc`. To change this to a logical **or** operation, drag either of the
column filters by its handle onto the other column filter to create a
new group. Now change the group's matching behavior to **Match any**:

![sample-group1.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Filters?action=AttachFile&do=get&target=sample-group1.png)

You can also reorder filters by dropping them in-between existing
filters.

### Chainable Filters

Chainable filters are a more general case of narrowing filters. These
filters take nodes and edges, from your selection or a narrowing filter,
as input. The nodes and edges in the output of the filter become the
input of the next filter in the chain. The output of the last filter
becomes the new selection.

Chainable filters can also be reordered by dragging one by the handle
and dropping it between existing filters.

Cytoscape currently bundles the following chainable filter:

#### Interaction Transformer

This transformer will go through all the input edges and add their
source nodes, target nodes, or both, to the output. This is useful for
selecting nodes that are connected to edges that match a particular
filter.

### Working with Narrowing and Chainable Filters

The name of active filter appears in the drop-down box at the top of
**Select** panel. Beside this is the options button which will allow you
to rename, remove or export the active filter. It also lets you create a
new filter, or import filters.

![select-panel-options.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Filters?action=AttachFile&do=get&target=select-panel-options.png)

At the bottom of the **Select** panel, there is an **Apply** button that
will re-apply the active filter. On the opposite side of the progress
bar is the cancel button, which will let you interrupt a long-running
filter.

The Select Menu
---------------

The **Select → Nodes** and **Select → Edges** menus provide several
mechanisms for selecting nodes and edges. Most options are fairly
straightforward; however, some need extra explanation.

**Select → Nodes → From ID List File...** selects nodes based on node
identifiers found in a specified file. The file format is simply one
node id per line:

    Node1
    Node2
    Node3
    ...

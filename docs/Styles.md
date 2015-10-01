[Styles](http://wiki.cytoscape.org/Cytoscape_3/UserManual/Cytoscape_3/UserManual/Styles)
========================================================================================

What are Styles?
----------------

One of Cytoscape's strengths in network visualization is the ability to
allow users to encode any table data (name, type, degree, weight,
expression data, etc.) as a property (such as color, size of node,
transparency, or font type) of the network. A set of these encoded or
mapped table data sets is called a **Style** and can be created or
edited in the **Style** panel of the **Control Panel**. In this
interface, the appearance of your network is easily customized. For
example, you can:

**Specify a default color and shape for all nodes.**

-   ![NodeShape.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=NodeShape.png)

**Set node sizes based on the degree of connectivity of the nodes. You
can visually see the hub of a network...**

-   ![DegreeSize.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=DegreeSize.png)

**...or, set the font size of the node labels instead.**

-   ![DegreeLabelSize.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=DegreeLabelSize.png)

**Visualize gene expression data along a color gradient.**

-   ![ColorGradient.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=ColorGradient.png)

**Encode specific physical entities as different node shapes.**

-   ![NodeShapeMapping.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=NodeShapeMapping.png)

**Use specific line types to indicate different types of interactions.**

-   ![edge\_types.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=edge_types.png)

**Control edge transparency (opacity) using edge weights.**

-   ![OpacityForEdges.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=OpacityForEdges.png)

**Control multiple edge properties using edge score.**

-   ![MultipleEdgeMapping.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=MultipleEdgeMapping.png)

**Browse extremely-dense networks by controlling the opacity of nodes.**

-   ![OpacityForNodesAndEdges.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=OpacityForNodesAndEdges.png)

**Show highly-connected region by edge bundling and opacity.**

-   ![Bundling.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=Bundling.png)

**Add photo/image/graphics on top of nodes.**

-   ![CustomGraphics1.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=CustomGraphics1.png)
    ![CustomGraphics4.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=CustomGraphics4.png)
    ![CustomGraphics5.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=CustomGraphics5.png)

Cytoscape 3 has several sample styles. Below are a few examples of these
applied to the *galFiltered.sif* network :

![default\_style.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=default_style.png)
![solid\_style.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=solid_style.png)
![ripple\_style.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=ripple_style.png)
![universe\_style.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=universe_style.png)

Introduction to the Style interface
-----------------------------------

The **Style** interface is located under the **Style** panel of the
**Control Panel**.

-   ![StylesInterface.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=StylesInterface.png)

This interface allows you to create/delete/view/switch between different
styles using the Current Style options. The panel displays the mapping
details for a given style and is used to edit these details as well.

-   At the top of the interface, there is a drop-down menu for selecting
    a pre-defined style. There is also an **Options** drop-down with
    options to rename, remove, create and copy a Style, and an option to
    create a legend for the selected Style.

-   The main area of the interface is composed of three tabs, for Node,
    Edge and Network.

-   Each tab contains a list of properties relevant to the
    current style. At the top of the list a **Properties** drop-down
    allows you to add additional properties to the list.

-   Each property entry in the list has 3 columns:

    -   The **Default Value** shows just that, the default value for
        the property. Clicking on the **Default Value** column for any
        property allows you to change the default value.

    -   **Mapping** displays the type of mapping currently in use for
        the property. Clicking on the **Mapping** column for any
        property expands the property entry to show the interface for
        editing the mapping. Details on the mapping types provided
        [here](#mappers).

    -   **Bypass** displays any style bypass for a selected node
        or edge. Note that a node/edge or subset of nodes/edges must be
        selected to activate the **Bypass** column. Clicking on the
        **Bypass** column for selected node(s)/edge(s) allows you to
        enter a bypass for that property for selected node(s)/edge(s).

The **Default Value** is used when no mapping is defined for a property,
or for nodes/edges not covered by a mapping for a particular property.
If a **Mapping** is defined for a property, this defines the style for
all or a subset of nodes/edges, depending on how the mapping is defined.
A **Bypass** on a specific set of nodes/edges will bypass and override
both the default value and defined mapping.

Introduction to Style
---------------------

The Cytoscape distribution includes several predefined styles to get you
started. To examine a few styles, try out the following example:

**Step 1. Load some sample data**

-   Load a sample session file: From the main menu, select **File →
    Open**, and select the file *sampleData/galFiltered.cys*.

-   The session file includes a network, some annotations, and
    sample styles. By default, the **Sample for galFiltered** style
    is selected. Gene expression values for each node are colored along
    a color gradient between red and green (where red represents a low
    expression ratio and green represents a high expression ratio, using
    thresholds set for the gal4RGexp experiment bundled with Cytoscape
    in the *sampleData/galExpData.csv* file). Also, node size is mapped
    to the degree of the node (number of edges connected to the node)
    and you can see the hubs of the network as larger nodes. See the
    sample screenshot below:

-   ![galFilteredSessionDefault.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=galFilteredSessionDefault.png)

**Step 2. Switch between different styles**

You can change the style by making a selection from the **Current
Style** drop-down list, found at the top of the **Style** panel.

For example, if you select **Sample1**, a new style will be applied to
your network, and you will see a white background and round blue nodes.
If you zoom in closer, you can see that protein-DNA interactions
(specified with the label "pd") are drawn with dashed edges, whereas
protein-protein interactions (specified with the label "pp") are drawn
with solid edges (see sample screenshot below).

-   ![VizMapperSample1Style26.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=VizMapperSample1Style26.png)

Finally, if you select **Solid**, you can see the graphics below:

-   ![VizMapperSolidStyle.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=VizMapperSolidStyle.png)

This style does not have mappings except node/edge labels, but you can
modify the network graphics by editing the *Default Value* for any
property.

Additional sample styles are available in the `sampleStyles.xml` file in
the *sampleData* directory. You can import the sample file from **File →
Import → Style File...**.

### List of Node, Edge and Network Properties

Cytoscape allows a wide variety of properties to be controlled. These
are summarized in the tables below.

  ------------------------------------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
  **Node Properties**                         **Description**
  *Border Line Type*                          The type of line used for the border of the node.
  *Border Transparency*                       The opacity of the color of the border of the node. Allows for transparency.
  *Border Width*                              The width of the node border.
  *Label*                                     The text used for the node label.
  *Label Font Face*                           The font used for the node label.
  *Label Font Size*                           The size of the font used for the node label.
  *Label Position*                            The position of the node label relative to the node.
  *Label Transparency*                        The transparency of the color of the node label. Allows for transparency.
  *Label Width*                               The maximum width of the node label. If the node label is wider than the specified width, Cytoscape will automatically wrap the label on space characters. Cytoscape will not hyphenate words, meaning that if a single word (i.e. no spaces) is longer than maximum width, the word will be displayed beyond the maximum width.
  *Nested Network Image Visible*              A boolean value that indicates whether a nested network should be visualized (assuming a nested network is present for the specified node).
  *Paint &gt; Paint*                          The color of the node.
  *Paint &gt; Border Paint*                   The color of the border of the node.
  *Paint &gt; Custom Graphics 1-9*            A user-defined custom graphic that is displayed on the node.
  *Paint &gt; Custom Graphics Position 1-9*   The position of each custom graphic.
  *Paint &gt; Fill Color*                     The color of the node.
  *Paint &gt; Label Color*                    The color of the node label.
  *Paint &gt; Selected Paint*                 The color of the node when selected.
  *Shape*                                     The shape of the node.
  *Size &gt; Size*                            The size of the node. Width and height will be equal. This property is mutually exclusive of *Node Height* and *Node Width*.
  *Size &gt; Custom Graphics Size 1-9*        A user-defined custom graphic size that is displayed on the node.
  *Size &gt; Height*                          The height of the node. Height will be independent of width. This property is mutually exclusive of *Node Size*.
  *Size &gt; Width*                           The width of the node. Width will be independent of height. This property is mutually exclusive of *Node Size*.
  *Size &gt; Fit Custom Graphics to node*     Toggle to fit Custom Graphics size to node size.
  *Size &gt; Lock node width and height*      Toggle to ignore *Width* and *Height*, and to use *Size* for both values.
  *Tooltip*                                   The text of the tooltip that appears when a mouse hovers over the node.
  *Transparency*                              The opacity of the color of the node. Zero means totally transparent, and 255 is most opaque.
  *Visible*                                   Node is visible or not. By default, this value is set to *true*.
  *X Location*                                X location of the node. Default value of this will be ignored. The value will be used only when mapping function is defined.
  *Y Location*                                Y location of the node. Default value of this will be ignored. The value will be used only when mapping function is defined.
  *Z Location*                                Z location of the node. Default value of this will be ignored. The value will be used only when mapping function is defined.
  ------------------------------------------- ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

  -------------------------------------------------------------------- -----------------------------------------------------------------------------------------------------------------------------------------------------
  **Edge Properties**                                                  **Description**
  *Bend*                                                               The edge bend. Defines how the edge is rendered. Users can add multiple handles to define how to bend the edge line.
  *Curved*                                                             If *Egde Bend* is defined, edges will be rendered as straight or curved lines. If this value is set to *true*, edges will be drawn as curved lines.
  *Label*                                                              The text used for the edge label.
  *Label Font Face*                                                    The font used for the edge label.
  *Label Font Size*                                                    The size of the font used for the edge label.
  *Label Transparency*                                                 The opacity of the color of the edge label. Allows for transparency.
  *Line Type*                                                          The type of stoke used to render the line (solid, dashed, etc.)
  *Paint &gt; Paint*                                                   The color of the edge.
  *Paint &gt; Color (Selected) &gt; Color (Selected)*                  The color of the edge.
  *Paint &gt; Color (Selected) &gt; Source Arrow Selected Paint*       The selected color of the arrow on the source node end of the edge.
  *Paint &gt; Color (Selected) &gt; Stroke Color (Selected)*           The color of the edge when selected.
  *Paint &gt; Color (Selected) &gt; Target Arrow Selected Paint*       The selected color of the arrow on the target node end of the edge.
  *Paint &gt; Color (Unselected) &gt; Color (Unselected)*              The color of the edge.
  *Paint &gt; Color (Unselected) &gt; Source Arrow Unselected Paint*   The color of the arrow on the source node end of the edge.
  *Paint &gt; Color (Unselected) &gt; Stroke Color (Unselected)*       The color of the edge.
  *Paint &gt; Color (Unselected) &gt; Target Arrow Unselected Paint*   The color of the arrow on the target node end of the edge.
  *Paint &gt; Label Color*                                             The color of the edge label.
  *Source Arrow Shape*                                                 The shape of the arrow on the source node end of the edge.
  *Target Arrow Shape*                                                 The shape of the arrow on the target node end of the edge.
  *Tooltip*                                                            The text of the tooltip that appears when a mouse hovers over the edge.
  *Transparency*                                                       The opacity of the color of the edge. Allows for transparency.
  *Visible*                                                            Edge is visible or not. By default, this value is set to *true*.
  *Width*                                                              The width of the line.
  -------------------------------------------------------------------- -----------------------------------------------------------------------------------------------------------------------------------------------------

  ------------------------ -----------------------------------------------------------------------------
  **Network Properties**   **Description**
  *Background Paint*       The background color of the network view.
  *Center X Location*      The X location of network view center.
  *Center Y Location*      The Y location of network view center.
  *Edge Selection*         Edges are selectable or not. If this is *false*, users cannot select edges.
  *Node Selection*         Nodes are selectable or not. If this is *false*, users cannot select nodes.
  *Scale Factor*           The zoom level of the network view.
  *Size &gt; Size*         The size of the network view.
  *Size &gt; Height*       The height of the network view.
  *Size &gt; Width*        The width of the network view.
  *Title*                  The title of the network view.
  ------------------------ -----------------------------------------------------------------------------

### Available Shapes and Line Styles

  -------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------------
  **Available Shapes and Line Styles**   **Sample**
  *Node Shapes*                          ![NodeShapeOptions.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=NodeShapeOptions.png)
  *Line Types*                           ![BorderLineOptions.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=BorderLineOptions.png)
  *Arrow Shapes*                         ![ArrowShapeOptions.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=ArrowShapeOptions.png)
  -------------------------------------- ------------------------------------------------------------------------------------------------------------------------------------------

### How Mappings Work

For each property, you can specify a default value or define a dynamic
mapping. Cytoscape currently supports three different types of mappings:

1.  **Passthrough Mapping**

    -   The values of network column data are passed directly through
        to properties. A passthrough mapping is typically used to
        specify node/edge labels. For example, a passthrough mapping can
        label all nodes with their common gene names.

2.  **Discrete Mapping**

    -   Discrete column data are mapped to discrete properties. For
        example, a discrete mapping can map different types of molecules
        to different node shapes, such as rectangles for gene products
        and ellipses for metabolites.

3.  **Continuous Mapping**

    -   Continuous data are mapped to properties. Depending on the
        property, there are three kinds of continuous mapping:

        i.  **Continuous-to-Continuous Mapping**: for example, you can
            map a continuous numerical value to node size.

        ii. **Color Gradient Mapping**: This is a special case of
            continuous-to-continuous mapping. Continuous numerical
            values are mapped to a color gradient.

        iii. **Continuous-to-Discrete Mapping**: for example, all values
            below 0 are mapped to square nodes, and all values above 0
            are mapped to circular nodes.

    -   However, note that there is no way to smoothly morph between
        circular nodes and square nodes.

The table below shows mapping support for each property.

**Legend**

  ------------ -----------------------------------------------------------------------------------------------------------------------------
  **Symbol**   **Description**
  -            Mapping is not supported for the specified property.
  +            Mapping is fully supported for the specified property.
  o            Mapping is partially supported for the specified property. Support for “continuous to continuous” mapping is not supported.
  ------------ -----------------------------------------------------------------------------------------------------------------------------

**Node Mappings**

  -------------------------------- ------------------------- ---------------------- ------------------------ ---
  **Node Property**                **Passthrough Mapping**   **Discrete Mapping**   **Continuous Mapping**
  Color                            *Fill Color*              +                      +                        +
  *Transparency*                   +                         +                      +
  *Border Paint*                   +                         +                      +
  *Border Transparency*            +                         +                      +
  *Label Color*                    +                         +                      +
  *Label Transparency*             +                         +                      +
  Numeric                          *Size/Width/Height*       +                      +                        +
  *Label Font Size*                +                         +                      +
  *Border Width*                   +                         +                      +
  *Label Width*                    +                         +                      +
  Other                            *Border Line Type*        +                      +                        o
  *Shape*                          +                         +                      o
  *Label*                          +                         +                      o
  *Tooltip*                        +                         +                      o
  *Label Font Face*                +                         +                      o
  *Label Position*                 o                         +                      o
  *Nested Network Image Visible*   +                         +                      o
  -------------------------------- ------------------------- ---------------------- ------------------------ ---

**Edge Mappings**

  ---------------------- ------------------------- ---------------------- ------------------------ ---
  **Edge Properties**    **Passthrough Mapping**   **Discrete Mapping**   **Continuous Mapping**
  Color                  *Color*                   +                      +                        +
  *Transparency*         +                         +                      +
  *Target Arrow Color*   +                         +                      +
  *Source Arrow Color*   +                         +                      +
  *Label Color*          +                         +                      +
  *Label Transparency*   +                         +                      +
  Numeric                *Width*                   +                      +                        +
  *Label Font Size*      +                         +                      +
  *Label Width*          +                         +                      +
  Other                  *Line Type*               +                      +                        o
  *Source Arrow Shape*   +                         +                      o
  *Target Arrow Shape*   +                         +                      o
  *Label*                +                         +                      o
  *Tooltip*              +                         +                      o
  *Label Font Face*      o                         +                      o
  ---------------------- ------------------------- ---------------------- ------------------------ ---

#### Text Passthrough Mapping

In Cytoscape 2.8.0 and later versions, the Passthrough Mapping can
recognize some text representations of values. This means, if you have a
string column named *Node Size Values*, you can directly map those
values as the Node Size by setting **Node Size Values** as controlling
column with **Node Size Passthrough** mapping. The following value types
are supported:

-   Color: [Standard color names supported by all
    browsers](http://www.w3schools.com/html/html_colornames.asp) or RGB
    representation in hex

-   Numerical Values: Automatically mapped to the specified property.

-   Custom Graphics: URL String. If the URL is valid and an actual image
    data exists there, Cytoscape automatically downloads the image and
    maps it to the node.

##### Examples

1.  Color Passthrough Mapping

    -   ![ColorPassthrough.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=ColorPassthrough.png)
        ![colorPt2.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=colorPt2.png)

2.  Node Size Passthrough Mapping

    -   ![SizePassthrough.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=SizePassthrough.png)
        ![sizePt2.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=sizePt2.png)

3.  Custom Graphics Passthrough Mapping

    -   ![CustomGraphicsPassthrough.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=CustomGraphicsPassthrough.png)
        ![cglorPt2.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=cglorPt2.png)

Custom Graphics
---------------

For Cytoscape 2.8.0 and later versions, Cytoscape supports **Custom
Graphics** for nodes. Using the Style interface, you can map Custom
Graphics to nodes like any other property. Cytoscape has a set of
graphics and you can also add your own graphics in the **Custom Graphics
Manager**, as well as remove or modify existing graphics.

[Taxonomy
Icon](http://biosciencedbc.jp/taxonomy_icon/taxonomy_icon.cgi?lng=en)
set used in this section is created by Database Center for Life Science
(DBCLS) and is distributed under Creative Commons License ([CC BY
2.1.](http://creativecommons.org/licenses/by/2.1/jp/deed.en))

### Managing Images with the Custom Graphics Manager

The **Custom Graphics Manager** is available under **View → Open Custom
Graphics Manager**:

-   ![cgManager1.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=cgManager1.png)

-   You can add images by drag-and-drop of image files and URLs. If you
    want to add images from a web browser or local file system, you can
    drag images from them and drop those images onto the list of images
    on the left.

    -   **Note:** When you drag and drop images from web browser, make
        sure that you are actually dragging the URL for the image. In
        some cases, images are linked to an HTML page or scripts, and in
        such cases, this drag and drop feature may not work.

-   If you want to add all images in a folder, press the **+** button on
    the bottom of the Custom Graphics Manager window.

-   ![add\_custom\_graphics.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=add_custom_graphics.png)

-   To remove images from the current session's **Custom Graphics**
    library, simply select graphics from the list and press the
    **-** button.

-   Images can be resized by defining specific **Width** and
    **Height** information. If the *Aspect Ratio* box is checked, the
    width-height ratio is always synchronized. You can resize the image
    to the original size by pressing **Original** button.

### Using Custom Graphics in Styles

-   ![CustomGraphicsVizMapper.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=CustomGraphicsVizMapper.png)
    ![CustomGraphicsNodes.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=CustomGraphicsNodes.png)

**Custom Graphics** is used and defined like any other property, through
the **Style** interface. There are nine **Custom Graphics** properties.

-   To select a custom graphic, first add the Custom Graphics property
    to the **Properties** list in the **Style** interface (on the
    **Node** tab, select **Properties → Paint → Custom Paint *n* →
    Custom Graphics *n***). Next, click the **Default Value** column of
    the Custom Graphics property to bring up the Graphics dialog. Select
    an image, a chart or a gradient and then click **Apply**.

    -   By default, custom graphics objects are automatically resized to
        be consistent with the Node Size property.

-   To remove a custom graphics, click the **Remove Graphics** button on
    the Graphics dialog.

-   ![CustomGraphicsSelector.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=CustomGraphicsSelector.png)

-   Cytoscape provides three kinds of Custom Graphics, selectable via
    tabs on the Custom Graphics dialog:

    -   **Images:** You can select one of the provided images or add
        your own (use the **Custom Graphics Manager** to add more images
        to the list).

    -   **Charts:** The following chart types are available:
        ![BarChartIcon.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=BarChartIcon.png)
        *Bar* ,
        ![BoxChartIcon.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=BoxChartIcon.png)
        *Box*,
        ![HeatMapChartIcon.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=HeatMapChartIcon.png)
        *Heat Map*,
        ![LineChartIcon.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=LineChartIcon.png)
        *Line*,
        ![PieChartIcon.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=PieChartIcon.png)
        *Pie*,
        ![RingChartIcon.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=RingChartIcon.png)
        *Ring*.

    -   **Gradients:** You can also set *Linear* and *Radial* gradients
        to nodes.

![BarChartEditor.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=BarChartEditor.png)
![RadialGradientEditor.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=RadialGradientEditor.png)

#### Custom Graphics Positions

Each custom graphics property is associated with a position. You can
edit their positions by using the UI available in the **Default Value**
column for any **Custom Graphics Position** property.

-   **Note:** Setting custom graphics positions for *Linear* or *Radial*
    gradients has no effect, as they are always centered on the node.

#### Z-Ordering

The number that appears with the custom graphics property represents an
ordering of layers. Basic node color and shape are always rendered
first, then node custom graphics 1, 2, ..., through 9.

### Saving and Loading Custom Graphics

In general, saving and loading Custom Graphics is automatic. When you
quit Cytoscape, all of the Custom Graphics in the manager will be saved
automatically. There are two types of saving:

1.  To session file

    -   When you save the current session to a file, the Custom Graphics
        **used in Style** will be saved to that file. For example, if
        you have a style with a discrete mapping for *Custom Graphics*,
        all custom graphics used in the style will be saved to the
        session file. Other graphics will **not** be saved in your
        session file. This is because your image library can be huge
        when you add thousands of images to the Custom Graphics Manager
        and it takes very long time to save and load the session file.

2.  Automatic saving to `CytoscapeConfiguration/images3` directory

    -   When you select **File → Quit**, all of Custom Graphics in the
        Manager will be saved automatically to your Cytoscape
        setting directory. Usually, it's
        `YOUR_HOME_DIRECTORY/CytoscapeConfiguration/images3`.

In any case, Custom Graphics will be saved automatically to your system
or session and will be restored when you restart Cytoscape or load a
session.

Styles Tutorials
----------------

The following tutorials demonstrate some of the basic **Style**
features. Each tutorial is independent of the others.

### Tutorial 1: Create a Basic Style and Set Default Values

The goal of this tutorial is to learn how to create a new Style and set
some default values.

1.  **Load a sample network.** From the main menu, select **File →
    Import → Network → File...**, and select
    `sampleData/galFiltered.sif`.

2.  **Create some node/edge statistics by Network Analyzer.** Network
    Analyzer calculates some basic statistics for nodes and edges. From
    the main menu, select **Tools → Network Analyzer → Network Analysis
    → Analyze Network**, and click **OK**. Once the result is displayed,
    simply close the window. All statistics are stored as regular
    table data.

3.  Select the **Style** panel in the Control Panel.

    ![StylesInterface.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=StylesInterface.png)

4.  **Create a new style.** Click the **Options**
    ![OptionsDropDown.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=OptionsDropDown.png)
    drop-down, and select **Create New Style**. Enter a name for your
    new style when prompted.

    ![NewStyle.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=NewStyle.png)

Since no mappings are set up yet, only default values are defined for
some of the properties. From this panel, you can create node/edge
mappings for all properties.

1.  **Change the default node color and shape.** To set the default node
    shape to triangles, click the **Default Value** column for **Node
    Shape**. A list of available node shapes will be shown. Select the
    **Round Rectangle** icon and click the **Apply** button. You can
    edit other default values in the same way. In the example shown
    below, the node shape is set to **Round Rectangle**, while the
    **Node Fill Color** is set to white. The new Style is automatically
    applied to the current network, as shown below.

    ![Tutorial1-final.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=Tutorial1-final.png)

### Tutorial 2: Creating a New Style with a Discrete Mapping

Now you have a network with new Style. The following section
demonstrates how to create a new style using a discrete mapping. The
goal is to draw protein-DNA interactions as dashed lines, and
protein-protein interactions as solid lines.

1.  **Choose a property.** In the Edge tab of the Style panel, find the
    **Stroke Color (Unselected)** property.

2.  **Choose a data column to map to.** Expand the entry for **Stroke
    Color (Unselected)** by clicking the arrow icon to the right. Click
    the **Column** entry and select "interaction" from the drop-down
    list that appears.

3.  **Choose a mapping type.** Under **Mapping Type**, select **Discrete
    Mapping**. All available column values for "interaction" will be
    displayed, as shown below.

    ![DiscreteMapper.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=DiscreteMapper.png)

4.  **Set the mapping relationship.** Click the empty cell next to "pd"
    (protein-DNA interactions). On the right side of the cell, click on
    the **...** button that appears. A popup window will appear; select
    green or similar, and the change will immediately appear on the
    network window.

    ![EdgeColorTut2.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=EdgeColorTut2.png)

Repeat step 4 for "pp" (protein-protein interactions), but select a
darker color as edge stroke color. Then repeat steps 3 through 4 for the
*Edge Line Type* property, by selecting the correct line style ("Dash"
or "Solid") from the list.

Now your network should show "pd" interactions as dashed green lines and
"pp" interactions as solid lines. A sample screenshot is provided below.

![Tutorial2-final.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=Tutorial2-final.png)

### Tutorial 3: Creating a New Style with a Continuous Mapping

At this point, you have a network with some edge mappings. Next, let's
create mappings for nodes. The following section demonstrates how to
create a new style using a continuous mapping. The goal is to
superimpose node statistics (in this example, node degree) onto a
network and display it along a color gradient.

1.  **Choose a property.** In the Node tab of the Style panel, find the
    **Fill Color** property.

2.  **Choose a node table column.** Expand the entry for **Fill Color**
    by clicking the arrow icon to the right. Click the **Column** entry
    and select "Degree" from the drop-down list that appears.

3.  **Choose a mapping type.** Set the "Continuous Mapping" option as
    the *Mapping Type*. This automatically creates a default mapping.

    ![DefaultContinous.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=DefaultContinous.png)

4.  **Define the points where colors will change.** Double-click on the
    black-and-white gradient rectangle next to Current Mapping to open
    the Color Gradient Mapping. Note the two smaller triangles at the
    top of the gradient. Move the left-side one all the way to the left,
    and the right-side one all the way to the right.

    ![DefaultColorGradient.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=DefaultColorGradient.png)

5.  **Define the colors between points.** Double-click on the larger
    leftmost triangle (facing left) and a color palette will appear. Set
    the color white and repeat for the smaller left-side triangle. For
    the triangle at the right, set its color to green and then choose
    the same green color for the smaller right-side triangle.

    ![GreenWhiteGradient.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=GreenWhiteGradient.png)

The color gradients will immediately appear on the network. All nodes
with degree 1 will be set to white, and all values between 1 and 18 will
be painted with a white/green color gradient. A sample screenshot is
below.

-   ![Tutorial3-final.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=Tutorial3-final.png)

-   **Repeat for other properties.** You can create some more mappings
    for other numeric table data. For example, edge data table column
    "EdgeBetweenness" is a number, so you can use it for
    continuous mapping. The following is an example visualization by
    mapping *Edge Width* to "EdgeBetweenness".

    ![Tutorial3-EdgeThickness.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=Tutorial3-EdgeThickness.png)

### Tutorial 4: How to Use Utilities for Discrete Mapping

The following tutorial demonstrates utilities for editing discrete
mappings. The goal of this section is learning how to set and adjust
values for discrete mappings automatically.

1.  Switch the Current Style to **Minimal**. Now your network looks like
    the following:

    ![Minimal.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=Minimal.png)

2.  Create a discrete Node Color mapping. Select
    "AverageShortestPathLength" (generated by Network Analyzer) as the
    controlling property.

3.  Click the **Fill Color** cell, then right-click it and select
    **Mapping Value Generators → Rainbow**. Cytoscape will automatically
    generate different colors for different property values as shown
    below:

    ![RainbowDiscreteMapping.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=RainbowDiscreteMapping.png)

4.  Create a discrete Node Label Font Size mapping. Select
    "AverageShortestPathLength" as controlling property.

5.  Click the **Node Label Font Size** cell, then right-click it and
    select **Mapping Value Generators → Number Series**. Type **3** for
    the first value and click OK. Enter *3* for increment.

6.  Apply **Layout → yFiles Layouts → Organic**. The final view is shown
    below:

    ![Tutorial4-final.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=Tutorial4-final.png)

This mapping generator utility is useful for categorical data. The
following example is created by adding node color discrete mapping from
species column to color.

-   ![tutorial4\_sample.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=tutorial4_sample.png)

### Tutorial 5: Using Custom Graphics in Styles

This tutorial is a quick introduction to Custom Graphics feature. You
can assign up to nine images per node as a part of a Style.

1.  In this first example, we will use the presets that Cytoscape 3 has.
    In general, you can use any type of bitmap graphics. Custom images
    should be added to the **Custom Graphics Manager** before using them
    in a Style.

2.  If you are continuing from the previous tutorials, skip to the
    next step. Otherwise, load a network and run the Network Analyzer
    (**Tools → Network Analyzer → Network Analysis → Analyze Network**).
    This creates several new table columns (statistics for nodes
    and edges).

3.  Click the **Style** panel in the **Control Panel**, and select the
    **Solid** style.

4.  Under **Properties**, add **Custom Graphics 1** from **Paint →
    Custom Paint 1 → Custom Graphics 1**.

5.  In the **Default Value** cell of the **Custom Graphics 1** entry,
    click to open the **Graphics** dialog, and select any of the custom
    graphics from the list.

6.  In the **Default Value** cell of **Transparency**, set the value
    to zero.

7.  Set the **Default Value** of node **Size** to 80. Also change the
    edge width to 6 and the node label font size to 10, to
    increase readability.

8.  Press *Apply*. Now your network looks like the following:

    ![CustomGraphicsNodes.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=CustomGraphicsNodes.png)

9.  Open the Custom Graphics Manager under **View → Open Custom Graphics
    Manager**. Drag and Drop this
    ![sampleImage.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=sampleImage.png)
    icon to the image list which automatically adds it to the manager.

    ![cgTutorial4.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=cgTutorial4.png)

10. Create a continuous mapping for **Node Custom Graphics 2**. Select
    "BetweennessCentrality" as controlling property. In the **Continuos
    Mapping Editor**, add a handle position by clicking in the **Add**
    button, and move the handle to *0.2*. Double-click the region over
    **0.2** and set the new icon you have just added in the last step.

    ![cgTutorial5.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=cgTutorial5.png)

11. Press **Apply**. Under **Properties**, add **Custom Graphics
    Position 2** from **Paint → Custom Paint 2 → Custom Graphics
    Position 2**. Change the **Default Value** and move the position of
    the graphics to upper left.

    ![cgTutorial6.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=cgTutorial6.png)

12. Press **Apply**. Now the important nodes in the network (nodes with
    high [betweenness
    centrality](http://en.wikipedia.org/wiki/Betweenness_centrality))
    are annotated with the icon.

    ![CustomGraphicsNodes2.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=CustomGraphicsNodes2.png)

### Tutorial 6: Creating Node Charts

The goal of this tutorial is learning how to create and customize node
charts from data stored in the Node tables.

1.  Start a new session and load a sample network. From the main menu,
    select **File → Import → Network → File...**, and select
    `sampleData/galFiltered.sif`.

2.  Create some node/edge statistics by Network Analyzer. Network
    Analyzer calculates some basic statistics for nodes and edges. From
    the main menu, select **Tools → Network Analyzer → Network Analysis
    → Analyze Network**, and click **OK**. Once the result is displayed,
    simply close the window. All statistics are stored as regular
    table data.

3.  Select the **Style** panel in the Control Panel.

4.  **Create a new style.** Click the **Options**
    ![OptionsDropDown.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=OptionsDropDown.png)
    drop-down, and select **Create New Style**. Enter a name for your
    new style when prompted.

5.  Add **Custom Graphics 1** to the properties list. Click
    **Properties** and select **Paint → Custom Paint 1 → Custom Graphics
    1**.

6.  In the **Default Value** cell of the **Custom Graphics 1** property
    entry, click to open the **Graphics** dialog.

7.  Click the **Charts** tab and make sure the **Bar Chart** option
    is selected.

    ![BarChartPanel\_6\_1.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=BarChartPanel_6_1.png)

8.  **Select data columns.** Now you have to choose the columns in the
    Node table that contains the data you want to be displayed
    as charts. The **Available Columns** list displays all node columns
    that can be used as chart data (i.e. *single* or *list* columns of
    numerical types).

    -   First click the **Remove All** button to remove the current
        selected columns (by default, Cytoscape selects the first column
        in the **Available Columns** list).

        ![BarChartPanel\_6\_2.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=BarChartPanel_6_2.png)

    -   Now select all *centrality* and *coefficient* columns from
        **Available Columns** list and click the **Add
        Selected** button.

        ![BarChartPanel\_6\_3.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=BarChartPanel_6_3.png)

9.  Click the **Apply** button to create bar charts with the selected
    data columns and default options.

    ![BarChartPanel\_6\_4.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=BarChartPanel_6_4.png)
    ![BarChartsNetwork\_6\_1.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=BarChartsNetwork_6_1.png)

10. The network view doesn't look so good yet, so let's make a few
    changes to its Style before we continue. In the example shown below,
    the node **Shape** is set to *Rectangle*, while the node **Fill
    Color** is set to *white*. It's also a good idea to apply another
    layout (e.g. select **Layout → yFiles Layouts → Organic**).

    ![BarChartsNetwork\_6\_2.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=BarChartsNetwork_6_2.png)

11. Focus on one node to see the chart details. For example search for
    and then focus on node "YMR043W".

    ![BarChartsNode\_6\_1.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=BarChartsNode_6_1.png)

12. **Change other chart options.** Click the **Default Value** cell of
    the **Custom Graphics 1** property again in order to open the
    **Graphics** dialog and then select the **Options** tab on the Bar
    Chart editor.

    ![BarChartPanel\_6\_5.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=BarChartPanel_6_5.png)

    On this panel, you can:

    -   Choose another **Color Scheme** or set all the colors
        individually (just click each color).

    -   Show/Hide Value and Domain **Labels** and also set the **Domain
        Label Position**.

    -   Change the chart **Orientation**.

    -   Show/Hide Axes.

    -   Change the line width and color for axes and bars.

    -   Increase or reduce the separation between bars (up to 50% of the
        total chart width).

    -   **Note:** Other charts provides different options

13. Check both **Show Domain Axis** and **Show Range Axis** and apply
    the graphics again. Now the node chart should look like this:

    ![BarChartsNode\_6\_2.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=BarChartsNode_6_2.png)

14. The default domain labels are not very useful, so let's set better
    labels:

    -   On the **Node Table** (Table Panel), create a new *List Column*
        of type *String* and name it "domain\_labels".

    -   Edit any of the cells of the created column (double-click it)
        and type
        `["Bet. Cent.","Closen. Cent","Clust. Coeff.","Topol. Coeff."]`.

    -   Right-click the same cell and select the option **Apply to
        entire column**.
        ![BarChartsNetwork\_6\_3.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=BarChartsNetwork_6_3.png)

    -   Open the chart editor again and select the **Options** panel.

    -   Select "domain\_labels" on the **Domain Labels Column**
        drop-down button.

    -   Select "Up 45^o^" on the **Domain Labels Position**
        drop-down button. The labels should look like this now:

    ![BarChartsNode\_6\_3.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=BarChartsNode_6_3.png)

Advanced Topics
---------------

### Discrete Mappings

Several utility functions are available for Discrete Mappings. You can
use those functions by right-clicking on any property (shown below.)

![MappingValueGenerators.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=MappingValueGenerators.png)

#### Automatic Value Generators

-   **Mapping Value Generators** - Functions in this menu category are
    value generators for discrete mappings. Users can set values for
    discrete mappings automatically by these functions.

    -   **Rainbow** and **Rainbow OSC** - These functions try to assign
        as diverse a set of colors as possible for each data value.

        -   ![RainbowMapper.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=RainbowMapper.png)

    -   **Random Numbers** and **Random Colors** - Randomized numbers
        and colors.

    -   **Number Series** - Set a series of numbers to the
        specified mapping. Requires a starting number and increment.

        -   ![NumberSeriesNodeSize.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=NumberSeriesNodeSize.png)

    -   **Fit label width** - This function is only for node width
        and height. When the node size is **unlocked** AND **Node
        Width/Height** discrete mappings are available, you can fit the
        size of each node to its label automatically by selecting
        this function. See the example below:

        -   ![NodeLabelFit.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=NodeLabelFit.png)

#### Edit Selected Values at Once

You can set multiple values at once. First, you need to select rows in
which you want to change values then right-click and select **Edit →
Edit Selected Discrete Mapping Values**. A dialog pops up and you can
enter the new value for the selected rows.

#### Property Dependencies

A Property Dependency can be established between different properties.
Currently there are two dependencies: **Lock node width and height**
(available in the **Node** tab) and **Edge color to arrows** (available
in the **Edge** tab).

-   **Lock Node with and height** - If this menu item is checked, **Node
    Width** and **Node Height** mappings are ignored and **Node Size**
    overrides them. If you want to use the **Fit label width** function,
    you need to unlock this.

-   **Edge color to arrows** - If this menu item is checked then
    **Source Arrow Color** and **Target Arrow Color** for edges are
    overridden and **Edge Color** is used in both cases.

### Working with Continuous Mapping Editors

There are three kinds of **Continuous Mapping Editors**. Each of them
are associated with a specific properties:

  ---------------------------------- ------------------------- -------------------------------
  **Editor Type**                    **Supported Data Type**   **Properties**
  **Color Gradient Editor**          Color                     node/edge/border/label colors
  **Continuous-Continuous Editor**   Numbers                   size/width/opacity
  **Continuous-Discrete Editor**     All others                font/shape/text
  ---------------------------------- ------------------------- -------------------------------

#### Range Setting Panel

![RangeSetting26.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=RangeSetting26.png)

Each editor has a common section named **Range Setting**.

1.  **Handle Value Box** - This box displays the current value for the
    selected slider handle. You can also directly type the value in this
    box to move the slider to an exact location.

2.  **Min/Max Button** - Set the overall range of this editor. The first
    time you open the editor, the *Min* and *Max* values are set by the
    range of the data column you selected, i.e., minimum and maximum
    value of the column will be set to the range of this editor. You can
    change this range anytime you want by pressing this button.

3.  **Add Handle Button** - Add a new handle to the editor.

4.  **Delete Handle Button** - Delete the selected handle from the
    slider widget.

5.  **Handle Value Editor Button** - Edit value assigned to the
    selected handle.

#### Gradient Editor

![GradientEditorSample26.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=GradientEditorSample26.png)

The Gradient Editor is an editor for creating continuous mappings for
colors. To change the color of each region, just double-click the
handles (small triangles on the top). A Color gradient will be created
only when the editor has two or more handles (see the example below).

  -------------------------------------------------------------------------------------------------------------------------- ----------------------------------------------------------------------------------------------------------------------------
  1 handle (no gradient)                                                                                                     2 handles
  ![OneSlider.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=OneSlider.png)   ![TwoSliders.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=TwoSliders.png)
  -------------------------------------------------------------------------------------------------------------------------- ----------------------------------------------------------------------------------------------------------------------------

#### Continuous-Continuous Editor

![C2CEditor26.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=C2CEditor26.png)

The Continuous-Continuous Editor is for creating mappings between
numerical data and numerical properties (size/opacity). To change the
value assigned on the Y-axis (the property shown in the example above is
node size), drag the red squares or double-click on the squares to
directly type an exact value.

#### Continuous-Discrete Editor

![C2DEditor26.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=C2DEditor26.png)

The Continuous-Discrete Editor is used to create mappings from numerical
column values to discrete properties, such as font, shape, or line
style. To edit a value for a specific region, double click on the icon
on the track.

Managing Styles
---------------

All Cytoscape Style settings are initially loaded from a default file
that cannot be altered by users. When users make changes to the
properties, a `session_syle.xml` file is saved in the session file. This
means that if you save your session, you will not lose your properties.
No other style files are saved during normal operation.

### Saving Styles

Styles are automatically saved with the session they were created in.
Before Cytoscape exits, you will be prompted to make sure you save the
session before quitting. It is also possible to save your styles in a
file separate from the session file. To do this, navigate to the **File
→ Export → Style...** menu option and save the properties as a file.
This feature can be used to share styles with other users.

You can also change the default list of styles for all future sessions
of Cytoscape. To do this, click the **Options**
![OptionsDropDown.png](http://wiki.cytoscape.org//Cytoscape_3/UserManual/Styles?action=AttachFile&do=get&target=OptionsDropDown.png)
drop-down in the Style section, and select **Make Current Styles
Default**. This will save the current styles as a `default_vizmap.xml`
file to your `CytoscapeConfiguration` directory (found in your home
directory). These styles will then be loaded each time Cytoscape is
started.

#### Style File Formats

The Cytoscape-native Style format is Style XML. If you want to share
Style files with other Cytoscape users, you need to export them to this
format.

From version 3.1.0 on, Cytoscape can export
[Cytoscape.js](http://cytoscape.github.io/cytoscape.js/#style)
compatible JSON file. Since Cytoscape.js is an independent
[JavaScript](http://wiki.cytoscape.org/Cytoscape_3/UserManual/JavaScript#)
library, and there are some differences between Cytoscape and
Cytoscape.js, not all properties are mapped to JSON. The following
properties are not supported by the exporter:

-   Custom Graphics and their locations

-   Edge Bends

-   Nested Networks

-   Network Background (Note: This can be set manually as standard CSS
    in Cytoscape.js)

The Continuous-Discrete Editor is used to create mappings from numerical
data values to discrete properties, such as font, shape, or line style.
To edit a value for a specific region, double-click on the icon on the
track.

### Importing Styles

To import existing styles, navigate to the **File → Import → Style...**
menu option and select a `styles.xml` (Cytoscape 3 format) file.
Imported properties will supplement existing properties or override
existing properties if the properties have the same name. You can also
specify a style file using the -V command line option. Properties loaded
from the command line will override any default properties. Note that
legacy `.props` files can only be loaded via the **File → Import →
Style...** menu option, but not by command line.


# Data socket Object

> Inherits from dsock.Object
  
<sub>go to [index](../index.md)</sub>



## Methods

- [geometry](#geometry) : Sockets      [location (Vector), rotation (Vector), scale (Vector), geometry (Geometry)]
- [info](#info) : Sockets      [location (Vector), rotation (Vector), scale (Vector), geometry (Geometry)]
- [location](#location) : Sockets      [location (Vector), rotation (Vector), scale (Vector), geometry (Geometry)]
- [rotation](#rotation) : Sockets      [location (Vector), rotation (Vector), scale (Vector), geometry (Geometry)]
- [scale](#scale) : Sockets      [location (Vector), rotation (Vector), scale (Vector), geometry (Geometry)]
- [switch](#switch) : output (Object)

## switch
```{eval-rst}
Geometry node [*Switch*].


  Args:
    switch: Boolean
    true: Object
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Object
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Switch`
  
  - input_type = 'OBJECT'
    
  Blender reference : `GeometryNodeSwitch <https://docs.blender.org/api/current/bpy.types.GeometryNodeSwitch.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Switch(false=self, switch=switch, true=true, input_type='OBJECT', label=node_label, node_color=node_color)
    

```
## info
```{eval-rst}

Geometry node [*Object Info*].


  Args:
    as_instance: Boolean
    transform_space (str): 'ORIGINAL' in [ORIGINAL, RELATIVE]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [location (Vector), rotation (Vector), scale (Vector), geometry (Geometry)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.ObjectInfo`
  
  
  Blender reference : `GeometryNodeObjectInfo <https://docs.blender.org/api/current/bpy.types.GeometryNodeObjectInfo.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.ObjectInfo(object=self, as_instance=as_instance, transform_space=transform_space, label=node_label, node_color=node_color)
    

```
## location
```{eval-rst}

Geometry node [*Object Info*].


  Args:
    as_instance: Boolean
    transform_space (str): 'ORIGINAL' in [ORIGINAL, RELATIVE]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    location in Sockets [location (Vector), rotation (Vector), scale (Vector), geometry (Geometry)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.ObjectInfo`
  
  
  Blender reference : `GeometryNodeObjectInfo <https://docs.blender.org/api/current/bpy.types.GeometryNodeObjectInfo.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.ObjectInfo(object=self, as_instance=as_instance, transform_space=transform_space, label=node_label, node_color=node_color).location
    

```
## rotation
```{eval-rst}

Geometry node [*Object Info*].


  Args:
    as_instance: Boolean
    transform_space (str): 'ORIGINAL' in [ORIGINAL, RELATIVE]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    rotation in Sockets [location (Vector), rotation (Vector), scale (Vector), geometry (Geometry)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.ObjectInfo`
  
  
  Blender reference : `GeometryNodeObjectInfo <https://docs.blender.org/api/current/bpy.types.GeometryNodeObjectInfo.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.ObjectInfo(object=self, as_instance=as_instance, transform_space=transform_space, label=node_label, node_color=node_color).rotation
    

```
## scale
```{eval-rst}

Geometry node [*Object Info*].


  Args:
    as_instance: Boolean
    transform_space (str): 'ORIGINAL' in [ORIGINAL, RELATIVE]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    scale in Sockets [location (Vector), rotation (Vector), scale (Vector), geometry (Geometry)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.ObjectInfo`
  
  
  Blender reference : `GeometryNodeObjectInfo <https://docs.blender.org/api/current/bpy.types.GeometryNodeObjectInfo.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.ObjectInfo(object=self, as_instance=as_instance, transform_space=transform_space, label=node_label, node_color=node_color).scale
    

```
## geometry
```{eval-rst}

Geometry node [*Object Info*].


  Args:
    as_instance: Boolean
    transform_space (str): 'ORIGINAL' in [ORIGINAL, RELATIVE]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    geometry in Sockets [location (Vector), rotation (Vector), scale (Vector), geometry (Geometry)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.ObjectInfo`
  
  
  Blender reference : `GeometryNodeObjectInfo <https://docs.blender.org/api/current/bpy.types.GeometryNodeObjectInfo.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.ObjectInfo(object=self, as_instance=as_instance, transform_space=transform_space, label=node_label, node_color=node_color).geometry
    
```
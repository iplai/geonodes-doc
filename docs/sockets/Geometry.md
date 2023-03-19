
# Data socket Geometry

> Inherits from dsock.Geometry
  
<sub>go to [index](../index.md)</sub>



## Static methods

- [is_viewport](#is_viewport) : is_viewport (Boolean)

## Properties

- [bound_box](#bound_box) : Sockets      [bounding_box (Geometry), min (Vector), max (Vector)]
- [box](#box) : bounding_box (Geometry) = bound_box.bounding_box
- [box_max](#box_max) : max (Vector) = bound_box.max
- [box_min](#box_min) : min (Vector) = bound_box.min
- [components](#components) : Sockets      [mesh (Mesh), point_cloud (Geometry), curve (Curve), volume (Volume), instances (Instances)]
- [curve_component](#curve_component) : curve (Curve) = components.curve
- [instances_component](#instances_component) : instances (Instances) = components.instances
- [mesh_component](#mesh_component) : mesh (Mesh) = components.mesh
- [points_component](#points_component) : point_cloud (Geometry) = components.point_cloud
- [volume_component](#volume_component) : volume (Volume) = components.volume

## Methods

- [capture_attribute](#capture_attribute) : attribute (data_type dependant)
- [convex_hull](#convex_hull) : convex_hull (Geometry)
- [delete_geometry](#delete_geometry) : geometry (Geometry)
- [duplicate_elements](#duplicate_elements) : Sockets      [geometry (Geometry), duplicate_index (Integer)]
- [join](#join) : geometry (Geometry)
- [merge_by_distance](#merge_by_distance) : geometry (Geometry)
- [proximity](#proximity) : Sockets      [position (Vector), distance (Float)]
- [remove_named_attribute](#remove_named_attribute) : geometry (Geometry)
- [replace_material](#replace_material) : geometry (Geometry)
- [scale_elements](#scale_elements) : geometry (Geometry)
- [separate_geometry](#separate_geometry) : Sockets      [selection (Geometry), inverted (Geometry)]
- [set_ID](#set_id) : geometry (Geometry)
- [set_material](#set_material) : geometry (Geometry)
- [set_material_index](#set_material_index) : geometry (Geometry)
- [set_position](#set_position) : geometry (Geometry)
- [set_shade_smooth](#set_shade_smooth) : geometry (Geometry)
- [store_named_attribute](#store_named_attribute) : geometry (Geometry)
- [store_named_boolean](#store_named_boolean) : geometry (Geometry)
- [store_named_byte_color](#store_named_byte_color) : geometry (Geometry)
- [store_named_color](#store_named_color) : geometry (Geometry)
- [store_named_float](#store_named_float) : geometry (Geometry)
- [store_named_integer](#store_named_integer) : geometry (Geometry)
- [store_named_vector](#store_named_vector) : geometry (Geometry)
- [switch](#switch) : output (Geometry)
- [to_instance](#to_instance) : instances (Instances)
- [transform](#transform) : geometry (Geometry)

## is_viewport
```{eval-rst}

Geometry node [*Is Viewport*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Boolean
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.IsViewport`
  
  
  Blender reference : `GeometryNodeIsViewport <https://docs.blender.org/api/current/bpy.types.GeometryNodeIsViewport.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.IsViewport(label=node_label, node_color=node_color)
    

```
## bound_box
```{eval-rst}

Geometry node [*Bounding Box*].



  Returns:
    Sockets [bounding_box (Geometry), min (Vector), max (Vector)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.BoundingBox`
  
  
  Blender reference : `GeometryNodeBoundBox <https://docs.blender.org/api/current/bpy.types.GeometryNodeBoundBox.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.BoundingBox(geometry=self, label=f"{self.node_chain_label}.bound_box")
    

```
## box
```{eval-rst}

Geometry node [*Bounding Box*].



  Returns:
    Sockets [bounding_box (Geometry), min (Vector), max (Vector)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.BoundingBox`
  
  
  Blender reference : `GeometryNodeBoundBox <https://docs.blender.org/api/current/bpy.types.GeometryNodeBoundBox.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.BoundingBox(geometry=self, label=f"{self.node_chain_label}.box")
    

```
## box_min
```{eval-rst}

Geometry node [*Bounding Box*].



  Returns:
    Sockets [bounding_box (Geometry), min (Vector), max (Vector)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.BoundingBox`
  
  
  Blender reference : `GeometryNodeBoundBox <https://docs.blender.org/api/current/bpy.types.GeometryNodeBoundBox.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.BoundingBox(geometry=self, label=f"{self.node_chain_label}.box_min")
    

```
## box_max
```{eval-rst}

Geometry node [*Bounding Box*].



  Returns:
    Sockets [bounding_box (Geometry), min (Vector), max (Vector)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.BoundingBox`
  
  
  Blender reference : `GeometryNodeBoundBox <https://docs.blender.org/api/current/bpy.types.GeometryNodeBoundBox.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.BoundingBox(geometry=self, label=f"{self.node_chain_label}.box_max")
    

```
## components
```{eval-rst}

Geometry node [*Separate Components*].



  Returns:
    Sockets [mesh (Mesh), point_cloud (Geometry), curve (Curve), volume (Volume), instances (Instances)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.SeparateComponents`
  
  
  Blender reference : `GeometryNodeSeparateComponents <https://docs.blender.org/api/current/bpy.types.GeometryNodeSeparateComponents.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.SeparateComponents(geometry=self, label=f"{self.node_chain_label}.components")
    

```
## mesh_component
```{eval-rst}

Geometry node [*Separate Components*].



  Returns:
    Sockets [mesh (Mesh), point_cloud (Geometry), curve (Curve), volume (Volume), instances (Instances)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.SeparateComponents`
  
  
  Blender reference : `GeometryNodeSeparateComponents <https://docs.blender.org/api/current/bpy.types.GeometryNodeSeparateComponents.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.SeparateComponents(geometry=self, label=f"{self.node_chain_label}.mesh_component")
    

```
## points_component
```{eval-rst}

Geometry node [*Separate Components*].



  Returns:
    Sockets [mesh (Mesh), point_cloud (Geometry), curve (Curve), volume (Volume), instances (Instances)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.SeparateComponents`
  
  
  Blender reference : `GeometryNodeSeparateComponents <https://docs.blender.org/api/current/bpy.types.GeometryNodeSeparateComponents.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.SeparateComponents(geometry=self, label=f"{self.node_chain_label}.points_component")
    

```
## curve_component
```{eval-rst}

Geometry node [*Separate Components*].



  Returns:
    Sockets [mesh (Mesh), point_cloud (Geometry), curve (Curve), volume (Volume), instances (Instances)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.SeparateComponents`
  
  
  Blender reference : `GeometryNodeSeparateComponents <https://docs.blender.org/api/current/bpy.types.GeometryNodeSeparateComponents.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.SeparateComponents(geometry=self, label=f"{self.node_chain_label}.curve_component")
    

```
## volume_component
```{eval-rst}

Geometry node [*Separate Components*].



  Returns:
    Sockets [mesh (Mesh), point_cloud (Geometry), curve (Curve), volume (Volume), instances (Instances)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.SeparateComponents`
  
  
  Blender reference : `GeometryNodeSeparateComponents <https://docs.blender.org/api/current/bpy.types.GeometryNodeSeparateComponents.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.SeparateComponents(geometry=self, label=f"{self.node_chain_label}.volume_component")
    

```
## instances_component
```{eval-rst}

Geometry node [*Separate Components*].



  Returns:
    Sockets [mesh (Mesh), point_cloud (Geometry), curve (Curve), volume (Volume), instances (Instances)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.SeparateComponents`
  
  
  Blender reference : `GeometryNodeSeparateComponents <https://docs.blender.org/api/current/bpy.types.GeometryNodeSeparateComponents.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.SeparateComponents(geometry=self, label=f"{self.node_chain_label}.instances_component")
    

```
## switch
```{eval-rst}

Geometry node [*Switch*].


  Args:
    switch: Boolean
    true: Geometry
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Geometry
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Switch`
  
  - input_type = 'GEOMETRY'
    
  Blender reference : `GeometryNodeSwitch <https://docs.blender.org/api/current/bpy.types.GeometryNodeSwitch.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Switch(false=self, switch=switch, true=true, input_type='GEOMETRY', label=node_label, node_color=node_color)
    

```
## capture_attribute
```{eval-rst}

Geometry node [*Capture Attribute*].


  Args:
    value: Float
    data_type (str): 'FLOAT' in [FLOAT, INT, FLOAT_VECTOR, FLOAT_COLOR, BOOLEAN]
    domain (str): 'POINT' in [POINT, EDGE, FACE, CORNER, CURVE, INSTANCE]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [geometry (Geometry), attribute (data_type dependant)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.CaptureAttribute`
  
  
  Blender reference : `GeometryNodeCaptureAttribute <https://docs.blender.org/api/current/bpy.types.GeometryNodeCaptureAttribute.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.CaptureAttribute(geometry=self, value=value, data_type=data_type, domain=domain, label=node_label, node_color=node_color)
    

```
## duplicate_elements
```{eval-rst}

Geometry node [*Duplicate Elements*].


  Args:
    selection: Boolean
    amount: Integer
    domain (str): 'POINT' in [POINT, EDGE, FACE, SPLINE, INSTANCE]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [geometry (Geometry), duplicate_index (Integer)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.DuplicateElements`
  
  
  Blender reference : `GeometryNodeDuplicateElements <https://docs.blender.org/api/current/bpy.types.GeometryNodeDuplicateElements.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.DuplicateElements(geometry=self, selection=selection, amount=amount, domain=domain, label=node_label, node_color=node_color)
    

```
## delete_geometry
```{eval-rst}

Geometry node [*Delete Geometry*].


  Args:
    selection: Boolean
    domain (str): 'POINT' in [POINT, EDGE, FACE, CURVE, INSTANCE]
    mode (str): 'ALL' in [ALL, EDGE_FACE, ONLY_FACE]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Geometry
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.DeleteGeometry`
  
  
  Blender reference : `GeometryNodeDeleteGeometry <https://docs.blender.org/api/current/bpy.types.GeometryNodeDeleteGeometry.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.DeleteGeometry(geometry=self, selection=selection, domain=domain, mode=mode, label=node_label, node_color=node_color)
    

```
## merge_by_distance
```{eval-rst}

Geometry node [*Merge by Distance*].


  Args:
    selection: Boolean
    distance: Float
    mode (str): 'ALL' in [ALL, CONNECTED]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Geometry
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.MergeByDistance`
  
  
  Blender reference : `GeometryNodeMergeByDistance <https://docs.blender.org/api/current/bpy.types.GeometryNodeMergeByDistance.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.MergeByDistance(geometry=self, selection=selection, distance=distance, mode=mode, label=node_label, node_color=node_color)
    

```
## replace_material
```{eval-rst}

Geometry node [*Replace Material*].


  Args:
    old: Material
    new: Material
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Geometry
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.ReplaceMaterial`
  
  
  Blender reference : `GeometryNodeReplaceMaterial <https://docs.blender.org/api/current/bpy.types.GeometryNodeReplaceMaterial.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.ReplaceMaterial(geometry=self, old=old, new=new, label=node_label, node_color=node_color)
    

```
## scale_elements
```{eval-rst}

Geometry node [*Scale Elements*].


  Args:
    selection: Boolean
    scale: Float
    center: Vector
    axis: Vector
    domain (str): 'FACE' in [FACE, EDGE]
    scale_mode (str): 'UNIFORM' in [UNIFORM, SINGLE_AXIS]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Geometry
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.ScaleElements`
  
  
  Blender reference : `GeometryNodeScaleElements <https://docs.blender.org/api/current/bpy.types.GeometryNodeScaleElements.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.ScaleElements(geometry=self, selection=selection, scale=scale, center=center, axis=axis, domain=domain, scale_mode=scale_mode, label=node_label, node_color=node_color)
    

```
## set_ID
```{eval-rst}

Geometry node [*Set ID*].


  Args:
    selection: Boolean
    ID: Integer
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Geometry
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.SetID`
  
  
  Blender reference : `GeometryNodeSetID <https://docs.blender.org/api/current/bpy.types.GeometryNodeSetID.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.SetID(geometry=self, selection=selection, ID=ID, label=node_label, node_color=node_color)
    

```
## set_material
```{eval-rst}

Geometry node [*Set Material*].


  Args:
    selection: Boolean
    material: Material
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Geometry
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.SetMaterial`
  
  
  Blender reference : `GeometryNodeSetMaterial <https://docs.blender.org/api/current/bpy.types.GeometryNodeSetMaterial.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.SetMaterial(geometry=self, selection=selection, material=material, label=node_label, node_color=node_color)
    

```
## set_material_index
```{eval-rst}

Geometry node [*Set Material Index*].


  Args:
    selection: Boolean
    material_index: Integer
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Geometry
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.SetMaterialIndex`
  
  
  Blender reference : `GeometryNodeSetMaterialIndex <https://docs.blender.org/api/current/bpy.types.GeometryNodeSetMaterialIndex.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.SetMaterialIndex(geometry=self, selection=selection, material_index=material_index, label=node_label, node_color=node_color)
    

```
## set_position
```{eval-rst}

Geometry node [*Set Position*].


  Args:
    selection: Boolean
    position: Vector
    offset: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Geometry
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.SetPosition`
  
  
  Blender reference : `GeometryNodeSetPosition <https://docs.blender.org/api/current/bpy.types.GeometryNodeSetPosition.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.SetPosition(geometry=self, selection=selection, position=position, offset=offset, label=node_label, node_color=node_color)
    

```
## set_shade_smooth
```{eval-rst}

Geometry node [*Set Shade Smooth*].


  Args:
    selection: Boolean
    shade_smooth: Boolean
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Geometry
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.SetShadeSmooth`
  
  
  Blender reference : `GeometryNodeSetShadeSmooth <https://docs.blender.org/api/current/bpy.types.GeometryNodeSetShadeSmooth.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.SetShadeSmooth(geometry=self, selection=selection, shade_smooth=shade_smooth, label=node_label, node_color=node_color)
    

```
## transform
```{eval-rst}

Geometry node [*Transform*].


  Args:
    translation: Vector
    rotation: Vector
    scale: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Geometry
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Transform`
  
  
  Blender reference : `GeometryNodeTransform <https://docs.blender.org/api/current/bpy.types.GeometryNodeTransform.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Transform(geometry=self, translation=translation, rotation=rotation, scale=scale, label=node_label, node_color=node_color)
    

```
## store_named_attribute
```{eval-rst}

Geometry node [*Store Named Attribute*].


  Args:
    name: String
    value: Float
    data_type (str): 'FLOAT' in [FLOAT, INT, FLOAT_VECTOR, FLOAT_COLOR, BYTE_COLOR, BOOLEAN]
    domain (str): 'POINT' in [POINT, EDGE, FACE, CORNER, CURVE, INSTANCE]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Geometry
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.StoreNamedAttribute`
  
  
  Blender reference : `GeometryNodeStoreNamedAttribute <https://docs.blender.org/api/current/bpy.types.GeometryNodeStoreNamedAttribute.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.StoreNamedAttribute(geometry=self, name=name, value=value, data_type=data_type, domain=domain, label=node_label, node_color=node_color)
    

```
## store_named_float
```{eval-rst}

Geometry node [*Store Named Attribute*].


  Args:
    name: String
    value: Float
    domain (str): 'POINT' in [POINT, EDGE, FACE, CORNER, CURVE, INSTANCE]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Geometry
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.StoreNamedAttribute`
  
  - data_type = 'FLOAT'
    
  Blender reference : `GeometryNodeStoreNamedAttribute <https://docs.blender.org/api/current/bpy.types.GeometryNodeStoreNamedAttribute.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.StoreNamedAttribute(geometry=self, name=name, value=value, data_type='FLOAT', domain=domain, label=node_label, node_color=node_color)
    

```
## store_named_integer
```{eval-rst}

Geometry node [*Store Named Attribute*].


  Args:
    name: String
    value: Integer
    domain (str): 'POINT' in [POINT, EDGE, FACE, CORNER, CURVE, INSTANCE]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Geometry
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.StoreNamedAttribute`
  
  - data_type = 'INT'
    
  Blender reference : `GeometryNodeStoreNamedAttribute <https://docs.blender.org/api/current/bpy.types.GeometryNodeStoreNamedAttribute.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.StoreNamedAttribute(geometry=self, name=name, value=value, data_type='INT', domain=domain, label=node_label, node_color=node_color)
    

```
## store_named_vector
```{eval-rst}

Geometry node [*Store Named Attribute*].


  Args:
    name: String
    value: Vector
    domain (str): 'POINT' in [POINT, EDGE, FACE, CORNER, CURVE, INSTANCE]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Geometry
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.StoreNamedAttribute`
  
  - data_type = 'FLOAT_VECTOR'
    
  Blender reference : `GeometryNodeStoreNamedAttribute <https://docs.blender.org/api/current/bpy.types.GeometryNodeStoreNamedAttribute.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.StoreNamedAttribute(geometry=self, name=name, value=value, data_type='FLOAT_VECTOR', domain=domain, label=node_label, node_color=node_color)
    

```
## store_named_color
```{eval-rst}

Geometry node [*Store Named Attribute*].


  Args:
    name: String
    value: Color
    domain (str): 'POINT' in [POINT, EDGE, FACE, CORNER, CURVE, INSTANCE]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Geometry
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.StoreNamedAttribute`
  
  - data_type = 'FLOAT_COLOR'
    
  Blender reference : `GeometryNodeStoreNamedAttribute <https://docs.blender.org/api/current/bpy.types.GeometryNodeStoreNamedAttribute.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.StoreNamedAttribute(geometry=self, name=name, value=value, data_type='FLOAT_COLOR', domain=domain, label=node_label, node_color=node_color)
    

```
## store_named_byte_color
```{eval-rst}

Geometry node [*Store Named Attribute*].


  Args:
    name: String
    value: Color
    domain (str): 'POINT' in [POINT, EDGE, FACE, CORNER, CURVE, INSTANCE]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Geometry
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.StoreNamedAttribute`
  
  - data_type = 'BYTE_COLOR'
    
  Blender reference : `GeometryNodeStoreNamedAttribute <https://docs.blender.org/api/current/bpy.types.GeometryNodeStoreNamedAttribute.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.StoreNamedAttribute(geometry=self, name=name, value=value, data_type='BYTE_COLOR', domain=domain, label=node_label, node_color=node_color)
    

```
## store_named_boolean
```{eval-rst}

Geometry node [*Store Named Attribute*].


  Args:
    name: String
    value: Boolean
    domain (str): 'POINT' in [POINT, EDGE, FACE, CORNER, CURVE, INSTANCE]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Geometry
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.StoreNamedAttribute`
  
  - data_type = 'BOOLEAN'
    
  Blender reference : `GeometryNodeStoreNamedAttribute <https://docs.blender.org/api/current/bpy.types.GeometryNodeStoreNamedAttribute.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.StoreNamedAttribute(geometry=self, name=name, value=value, data_type='BOOLEAN', domain=domain, label=node_label, node_color=node_color)
    

```
## remove_named_attribute
```{eval-rst}

Geometry node [*Remove Named Attribute*].


  Args:
    name: String
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Geometry
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.RemoveNamedAttribute`
  
  
  Blender reference : `GeometryNodeRemoveAttribute <https://docs.blender.org/api/current/bpy.types.GeometryNodeRemoveAttribute.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.RemoveNamedAttribute(geometry=self, name=name, label=node_label, node_color=node_color)
    

```
## separate_geometry
```{eval-rst}

Geometry node [*Separate Geometry*].


  Args:
    selection: Boolean
    domain (str): 'POINT' in [POINT, EDGE, FACE, CURVE, INSTANCE]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [selection (Geometry), inverted (Geometry)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.SeparateGeometry`
  
  
  Blender reference : `GeometryNodeSeparateGeometry <https://docs.blender.org/api/current/bpy.types.GeometryNodeSeparateGeometry.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.SeparateGeometry(geometry=self, selection=selection, domain=domain, label=node_label, node_color=node_color)
    

```
## convex_hull
```{eval-rst}

Geometry node [*Convex Hull*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Geometry
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.ConvexHull`
  
  
  Blender reference : `GeometryNodeConvexHull <https://docs.blender.org/api/current/bpy.types.GeometryNodeConvexHull.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.ConvexHull(geometry=self, label=node_label, node_color=node_color)
    

```
## to_instance
```{eval-rst}

Geometry node [*Geometry to Instance*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Instances
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.GeometryToInstance`
  
  
  Blender reference : `GeometryNodeGeometryToInstance <https://docs.blender.org/api/current/bpy.types.GeometryNodeGeometryToInstance.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.GeometryToInstance(self, *geometry, label=node_label, node_color=node_color)
    

```
## join
```{eval-rst}

Geometry node [*Join Geometry*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Geometry
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.JoinGeometry`
  
  
  Blender reference : `GeometryNodeJoinGeometry <https://docs.blender.org/api/current/bpy.types.GeometryNodeJoinGeometry.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.JoinGeometry(self, *geometry, label=node_label, node_color=node_color)
    

```
## proximity
```{eval-rst}

Geometry node [*Geometry Proximity*].


  Args:
    source_position: Vector
    target_element (str): 'FACES' in [POINTS, EDGES, FACES]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [position (Vector), distance (Float)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.GeometryProximity`
  
  
  Blender reference : `GeometryNodeProximity <https://docs.blender.org/api/current/bpy.types.GeometryNodeProximity.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.GeometryProximity(target=self, source_position=source_position, target_element=target_element, label=node_label, node_color=node_color)
    
```
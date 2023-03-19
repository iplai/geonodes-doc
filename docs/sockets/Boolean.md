
# Data socket Boolean

> Inherits from dsock.Boolean
  
<sub>go to [index](../index.md)</sub>



## Constructors

- [Random](#random) : value (Boolean)

## Methods

- [b_and](#b_and) : boolean (Boolean)
- [b_not](#b_not) : boolean (Boolean)
- [b_or](#b_or) : boolean (Boolean)
- [capture_attribute](#capture_attribute) : Sockets      [geometry (Geometry), attribute (Boolean)]
- [field_at_index](#field_at_index) : value (Boolean)
- [imply](#imply) : boolean (Boolean)
- [nand](#nand) : boolean (Boolean)
- [nimply](#nimply) : boolean (Boolean)
- [nor](#nor) : boolean (Boolean)
- [raycast](#raycast) : Sockets      [is_hit (Boolean), hit_position (Vector), hit_normal (Vector), hit_distance (Float), attribute (Boolean)]
- [switch](#switch) : output (Boolean)
- [xnor](#xnor) : boolean (Boolean)
- [xor](#xor) : boolean (Boolean)

## Random
```{eval-rst}
Geometry node [*Random Value*].


  Args:
    probability: Float
    ID: Integer
    seed: Integer
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Boolean
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.RandomValue`
  
  - data_type = 'BOOLEAN'
    
  Blender reference : `FunctionNodeRandomValue <https://docs.blender.org/api/current/bpy.types.FunctionNodeRandomValue.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.RandomValue(probability=probability, ID=ID, seed=seed, data_type='BOOLEAN', label=node_label, node_color=node_color)
```    

## capture_attribute
```{eval-rst}
Geometry node [*Capture Attribute*].


  Args:
    geometry: Geometry
    domain (str): 'POINT' in [POINT, EDGE, FACE, CORNER, CURVE, INSTANCE]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [geometry (Geometry), attribute (Boolean)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.CaptureAttribute`
  
  - data_type = 'BOOLEAN'
    
  Blender reference : `GeometryNodeCaptureAttribute <https://docs.blender.org/api/current/bpy.types.GeometryNodeCaptureAttribute.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.CaptureAttribute(value=self, geometry=geometry, data_type='BOOLEAN', domain=domain, label=node_label, node_color=node_color)
    
```
## field_at_index
```{eval-rst}
Geometry node [*Field at Index*].


  Args:
    index: Integer
    domain (str): 'POINT' in [POINT, EDGE, FACE, CORNER, CURVE, INSTANCE]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Boolean
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.FieldAtIndex`
  
  - data_type = 'BOOLEAN'
    
  Blender reference : `GeometryNodeFieldAtIndex <https://docs.blender.org/api/current/bpy.types.GeometryNodeFieldAtIndex.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.FieldAtIndex(value=self, index=index, data_type='BOOLEAN', domain=domain, label=node_label, node_color=node_color)
    
```
## raycast
```{eval-rst}
Geometry node [*Raycast*].


  Args:
    target_geometry: Geometry
    source_position: Vector
    ray_direction: Vector
    ray_length: Float
    mapping (str): 'INTERPOLATED' in [INTERPOLATED, NEAREST]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [is_hit (Boolean), hit_position (Vector), hit_normal (Vector), hit_distance (Float), attribute (Boolean)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Raycast`
  
  - data_type = 'BOOLEAN'
    
  Blender reference : `GeometryNodeRaycast <https://docs.blender.org/api/current/bpy.types.GeometryNodeRaycast.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Raycast(attribute=self, target_geometry=target_geometry, source_position=source_position, ray_direction=ray_direction, ray_length=ray_length, data_type='BOOLEAN', mapping=mapping, label=node_label, node_color=node_color)
    
```
## switch
```{eval-rst}
Geometry node [*Switch*].


  Args:
    false: Boolean
    true: Boolean
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Boolean
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Switch`
  
  - input_type = 'BOOLEAN'
    
  Blender reference : `GeometryNodeSwitch <https://docs.blender.org/api/current/bpy.types.GeometryNodeSwitch.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Switch(switch=self, false=false, true=true, input_type='BOOLEAN', label=node_label, node_color=node_color)
    
```
## b_and
```{eval-rst}
Geometry node [*Boolean Math*].


  Args:
    boolean1: Boolean
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Boolean
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.BooleanMath`
  
  - operation = 'AND'
    
  Blender reference : `FunctionNodeBooleanMath <https://docs.blender.org/api/current/bpy.types.FunctionNodeBooleanMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.BooleanMath(boolean0=self, boolean1=boolean1, operation='AND', label=node_label, node_color=node_color)
    
```
## b_or
```{eval-rst}
Geometry node [*Boolean Math*].


  Args:
    boolean1: Boolean
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Boolean
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.BooleanMath`
  
  - operation = 'OR'
    
  Blender reference : `FunctionNodeBooleanMath <https://docs.blender.org/api/current/bpy.types.FunctionNodeBooleanMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.BooleanMath(boolean0=self, boolean1=boolean1, operation='OR', label=node_label, node_color=node_color)
    
```
## b_not
```{eval-rst}
Geometry node [*Boolean Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Boolean
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.BooleanMath`
  
  - operation = 'NOT'
    
  Blender reference : `FunctionNodeBooleanMath <https://docs.blender.org/api/current/bpy.types.FunctionNodeBooleanMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.BooleanMath(boolean0=self, operation='NOT', label=node_label, node_color=node_color)
    
```
## nand
```{eval-rst}
Geometry node [*Boolean Math*].


  Args:
    boolean1: Boolean
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Boolean
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.BooleanMath`
  
  - operation = 'NAND'
    
  Blender reference : `FunctionNodeBooleanMath <https://docs.blender.org/api/current/bpy.types.FunctionNodeBooleanMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.BooleanMath(boolean0=self, boolean1=boolean1, operation='NAND', label=node_label, node_color=node_color)
    
```
## nor
```{eval-rst}
Geometry node [*Boolean Math*].


  Args:
    boolean1: Boolean
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Boolean
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.BooleanMath`
  
  - operation = 'NOR'
    
  Blender reference : `FunctionNodeBooleanMath <https://docs.blender.org/api/current/bpy.types.FunctionNodeBooleanMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.BooleanMath(boolean0=self, boolean1=boolean1, operation='NOR', label=node_label, node_color=node_color)
    
```
## xnor
```{eval-rst}
Geometry node [*Boolean Math*].


  Args:
    boolean1: Boolean
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Boolean
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.BooleanMath`
  
  - operation = 'XNOR'
    
  Blender reference : `FunctionNodeBooleanMath <https://docs.blender.org/api/current/bpy.types.FunctionNodeBooleanMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.BooleanMath(boolean0=self, boolean1=boolean1, operation='XNOR', label=node_label, node_color=node_color)
    
```
## xor
```{eval-rst}
Geometry node [*Boolean Math*].


  Args:
    boolean1: Boolean
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Boolean
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.BooleanMath`
  
  - operation = 'XOR'
    
  Blender reference : `FunctionNodeBooleanMath <https://docs.blender.org/api/current/bpy.types.FunctionNodeBooleanMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.BooleanMath(boolean0=self, boolean1=boolean1, operation='XOR', label=node_label, node_color=node_color)
    
```
## imply
```{eval-rst}
Geometry node [*Boolean Math*].


  Args:
    boolean1: Boolean
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Boolean
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.BooleanMath`
  
  - operation = 'IMPLY'
    
  Blender reference : `FunctionNodeBooleanMath <https://docs.blender.org/api/current/bpy.types.FunctionNodeBooleanMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.BooleanMath(boolean0=self, boolean1=boolean1, operation='IMPLY', label=node_label, node_color=node_color)
    
```
## nimply
```{eval-rst}
Geometry node [*Boolean Math*].


  Args:
    boolean1: Boolean
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Boolean
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.BooleanMath`
  
  - operation = 'NIMPLY'
    
  Blender reference : `FunctionNodeBooleanMath <https://docs.blender.org/api/current/bpy.types.FunctionNodeBooleanMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.BooleanMath(boolean0=self, boolean1=boolean1, operation='NIMPLY', label=node_label, node_color=node_color)
    
```
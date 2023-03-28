
# Data socket Integer

> Inherits from dsock.Integer
  
<sub>go to [index](../index.md)</sub>



## Constructors

- [Random](#random) : value (Integer)

## Methods

- [abs](#abs) : value (Float)
- [accumulate_field](#accumulate_field) : Sockets      [leading (Integer), trailing (Integer), total (Integer)]
- [arccos](#arccos) : value (Float)
- [arcsin](#arcsin) : value (Float)
- [arctan](#arctan) : value (Float)
- [arctan2](#arctan2) : value (Float)
- [capture_attribute](#capture_attribute) : Sockets      [geometry (Geometry), attribute (Integer)]
- [ceil](#ceil) : value (Float)
- [compare](#compare) : value (Float)
- [cos](#cos) : value (Float)
- [cosh](#cosh) : value (Float)
- [degrees](#degrees) : value (Float)
- [equal](#equal) : result (Boolean)
- [exp](#exp) : value (Float)
- [field_at_index](#field_at_index) : value (Integer)
- [floor](#floor) : value (Float)
- [fract](#fract) : value (Float)
- [greater_equal](#greater_equal) : result (Boolean)
- [greater_than](#greater_than) : result (Boolean)
- [inverse_sqrt](#inverse_sqrt) : value (Float)
- [less_equal](#less_equal) : result (Boolean)
- [less_than](#less_than) : result (Boolean)
- [log](#log) : value (Float)
- [math_greater_than](#math_greater_than) : value (Float)
- [math_less_than](#math_less_than) : value (Float)
- [max](#max) : value (Float)
- [min](#min) : value (Float)
- [modulo](#modulo) : value (Float)
- [multiply_add](#multiply_add) : value (Float)
- [not_equal](#not_equal) : result (Boolean)
- [pingpong](#pingpong) : value (Float)
- [pow](#pow) : value (Float)
- [radians](#radians) : value (Float)
- [raycast](#raycast) : Sockets      [is_hit (Boolean), hit_position (Vector), hit_normal (Vector), hit_distance (Float), attribute (Integer)]
- [round](#round) : value (Float)
- [sign](#sign) : value (Float)
- [sin](#sin) : value (Float)
- [sinh](#sinh) : value (Float)
- [smooth_max](#smooth_max) : value (Float)
- [smooth_min](#smooth_min) : value (Float)
- [snap](#snap) : value (Float)
- [sqrt](#sqrt) : value (Float)
- [switch](#switch) : output (Integer)
- [tan](#tan) : value (Float)
- [tanh](#tanh) : value (Float)
- [trunc](#trunc) : value (Float)
- [wrap](#wrap) : value (Float)

## Random
```{eval-rst}

Geometry node [*Random Value*].


  Args:
    min: Integer
    max: Integer
    ID: Integer
    seed: Integer
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Integer
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.RandomValue`
  
  - data_type = 'INT'
    
  Blender reference : `FunctionNodeRandomValue <https://docs.blender.org/api/current/bpy.types.FunctionNodeRandomValue.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.RandomValue(min=min, max=max, ID=ID, seed=seed, data_type='INT', label=node_label, node_color=node_color)
    

```
## accumulate_field
```{eval-rst}

Geometry node [*Accumulate Field*].


  Args:
    group_index: Integer
    domain (str): 'POINT' in [POINT, EDGE, FACE, CORNER, CURVE, INSTANCE]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [leading (Integer), trailing (Integer), total (Integer)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.AccumulateField`
  
  - data_type = 'INT'
    
  Blender reference : `GeometryNodeAccumulateField <https://docs.blender.org/api/current/bpy.types.GeometryNodeAccumulateField.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.AccumulateField(value=self, group_index=group_index, data_type='INT', domain=domain, label=node_label, node_color=node_color)
    

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
    Sockets [geometry (Geometry), attribute (Integer)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.CaptureAttribute`
  
  - data_type = 'INT'
    
  Blender reference : `GeometryNodeCaptureAttribute <https://docs.blender.org/api/current/bpy.types.GeometryNodeCaptureAttribute.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.CaptureAttribute(value=self, geometry=geometry, data_type='INT', domain=domain, label=node_label, node_color=node_color)
    

```
## field_at_index
```{eval-rst}

Geometry node [*Field at Index*].


  Args:
    value: Integer
    domain (str): 'POINT' in [POINT, EDGE, FACE, CORNER, CURVE, INSTANCE]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Integer
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.FieldAtIndex`
  
  - data_type = 'INT'
    
  Blender reference : `GeometryNodeFieldAtIndex <https://docs.blender.org/api/current/bpy.types.GeometryNodeFieldAtIndex.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.FieldAtIndex(index=self, value=value, data_type='INT', domain=domain, label=node_label, node_color=node_color)
    

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
    Sockets [is_hit (Boolean), hit_position (Vector), hit_normal (Vector), hit_distance (Float), attribute (Integer)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Raycast`
  
  - data_type = 'INT'
    
  Blender reference : `GeometryNodeRaycast <https://docs.blender.org/api/current/bpy.types.GeometryNodeRaycast.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Raycast(attribute=self, target_geometry=target_geometry, source_position=source_position, ray_direction=ray_direction, ray_length=ray_length, data_type='INT', mapping=mapping, label=node_label, node_color=node_color)
    

```
## switch
```{eval-rst}

Geometry node [*Switch*].


  Args:
    switch: Boolean
    true: Integer
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Integer
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Switch`
  
  - input_type = 'INT'
    
  Blender reference : `GeometryNodeSwitch <https://docs.blender.org/api/current/bpy.types.GeometryNodeSwitch.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Switch(false=self, switch=switch, true=true, input_type='INT', label=node_label, node_color=node_color)
    

```
## less_than
```{eval-rst}

Geometry node [*Compare*].


  Args:
    b: Integer
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Boolean
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Compare`
  
  - data_type = 'INT'
  - mode = 'ELEMENT'
  - operation = 'LESS_THAN'
    
  Blender reference : `FunctionNodeCompare <https://docs.blender.org/api/current/bpy.types.FunctionNodeCompare.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Compare(a=self, b=b, data_type='INT', mode='ELEMENT', operation='LESS_THAN', label=node_label, node_color=node_color)
    

```
## less_equal
```{eval-rst}

Geometry node [*Compare*].


  Args:
    b: Integer
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Boolean
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Compare`
  
  - data_type = 'INT'
  - mode = 'ELEMENT'
  - operation = 'LESS_EQUAL'
    
  Blender reference : `FunctionNodeCompare <https://docs.blender.org/api/current/bpy.types.FunctionNodeCompare.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Compare(a=self, b=b, data_type='INT', mode='ELEMENT', operation='LESS_EQUAL', label=node_label, node_color=node_color)
    

```
## greater_than
```{eval-rst}

Geometry node [*Compare*].


  Args:
    b: Integer
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Boolean
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Compare`
  
  - data_type = 'INT'
  - mode = 'ELEMENT'
  - operation = 'GREATER_THAN'
    
  Blender reference : `FunctionNodeCompare <https://docs.blender.org/api/current/bpy.types.FunctionNodeCompare.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Compare(a=self, b=b, data_type='INT', mode='ELEMENT', operation='GREATER_THAN', label=node_label, node_color=node_color)
    

```
## greater_equal
```{eval-rst}

Geometry node [*Compare*].


  Args:
    b: Integer
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Boolean
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Compare`
  
  - data_type = 'INT'
  - mode = 'ELEMENT'
  - operation = 'GREATER_EQUAL'
    
  Blender reference : `FunctionNodeCompare <https://docs.blender.org/api/current/bpy.types.FunctionNodeCompare.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Compare(a=self, b=b, data_type='INT', mode='ELEMENT', operation='GREATER_EQUAL', label=node_label, node_color=node_color)
    

```
## equal
```{eval-rst}

Geometry node [*Compare*].


  Args:
    b: Integer
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Boolean
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Compare`
  
  - data_type = 'INT'
  - mode = 'ELEMENT'
  - operation = 'EQUAL'
    
  Blender reference : `FunctionNodeCompare <https://docs.blender.org/api/current/bpy.types.FunctionNodeCompare.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Compare(a=self, b=b, data_type='INT', mode='ELEMENT', operation='EQUAL', label=node_label, node_color=node_color)
    

```
## not_equal
```{eval-rst}

Geometry node [*Compare*].


  Args:
    b: Integer
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Boolean
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Compare`
  
  - data_type = 'INT'
  - mode = 'ELEMENT'
  - operation = 'NOT_EQUAL'
    
  Blender reference : `FunctionNodeCompare <https://docs.blender.org/api/current/bpy.types.FunctionNodeCompare.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Compare(a=self, b=b, data_type='INT', mode='ELEMENT', operation='NOT_EQUAL', label=node_label, node_color=node_color)
    

```
## multiply_add
```{eval-rst}

Geometry node [*Math*].


  Args:
    value1: Float
    value2: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'MULTIPLY_ADD'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, value1=value1, value2=value2, operation='MULTIPLY_ADD', label=node_label, node_color=node_color)
    

```
## pow
```{eval-rst}

Geometry node [*Math*].


  Args:
    value1: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'POWER'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, value1=value1, operation='POWER', label=node_label, node_color=node_color)
    

```
## log
```{eval-rst}

Geometry node [*Math*].


  Args:
    value1: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'LOGARITHM'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, value1=value1, operation='LOGARITHM', label=node_label, node_color=node_color)
    

```
## sqrt
```{eval-rst}

Geometry node [*Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'SQRT'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, operation='SQRT', label=node_label, node_color=node_color)
    

```
## inverse_sqrt
```{eval-rst}

Geometry node [*Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'INVERSE_SQRT'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, operation='INVERSE_SQRT', label=node_label, node_color=node_color)
    

```
## abs
```{eval-rst}

Geometry node [*Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'ABSOLUTE'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, operation='ABSOLUTE', label=node_label, node_color=node_color)
    

```
## exp
```{eval-rst}

Geometry node [*Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'EXPONENT'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, operation='EXPONENT', label=node_label, node_color=node_color)
    

```
## min
```{eval-rst}

Geometry node [*Math*].


  Args:
    value1: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'MINIMUM'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, value1=value1, operation='MINIMUM', label=node_label, node_color=node_color)
    

```
## max
```{eval-rst}

Geometry node [*Math*].


  Args:
    value1: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'MAXIMUM'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, value1=value1, operation='MAXIMUM', label=node_label, node_color=node_color)
    

```
## math_less_than
```{eval-rst}

Geometry node [*Math*].


  Args:
    value1: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'LESS_THAN'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, value1=value1, operation='LESS_THAN', label=node_label, node_color=node_color)
    

```
## math_greater_than
```{eval-rst}

Geometry node [*Math*].


  Args:
    value1: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'GREATER_THAN'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, value1=value1, operation='GREATER_THAN', label=node_label, node_color=node_color)
    

```
## sign
```{eval-rst}

Geometry node [*Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'SIGN'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, operation='SIGN', label=node_label, node_color=node_color)
    

```
## compare
```{eval-rst}

Geometry node [*Math*].


  Args:
    value1: Float
    value2: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'COMPARE'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, value1=value1, value2=value2, operation='COMPARE', label=node_label, node_color=node_color)
    

```
## smooth_min
```{eval-rst}

Geometry node [*Math*].


  Args:
    value1: Float
    value2: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'SMOOTH_MIN'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, value1=value1, value2=value2, operation='SMOOTH_MIN', label=node_label, node_color=node_color)
    

```
## smooth_max
```{eval-rst}

Geometry node [*Math*].


  Args:
    value1: Float
    value2: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'SMOOTH_MAX'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, value1=value1, value2=value2, operation='SMOOTH_MAX', label=node_label, node_color=node_color)
    

```
## round
```{eval-rst}

Geometry node [*Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'ROUND'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, operation='ROUND', label=node_label, node_color=node_color)
    

```
## floor
```{eval-rst}

Geometry node [*Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'FLOOR'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, operation='FLOOR', label=node_label, node_color=node_color)
    

```
## ceil
```{eval-rst}

Geometry node [*Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'CEIL'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, operation='CEIL', label=node_label, node_color=node_color)
    

```
## trunc
```{eval-rst}

Geometry node [*Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'TRUNC'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, operation='TRUNC', label=node_label, node_color=node_color)
    

```
## fract
```{eval-rst}

Geometry node [*Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'FRACT'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, operation='FRACT', label=node_label, node_color=node_color)
    

```
## modulo
```{eval-rst}

Geometry node [*Math*].


  Args:
    value1: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'MODULO'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, value1=value1, operation='MODULO', label=node_label, node_color=node_color)
    

```
## wrap
```{eval-rst}

Geometry node [*Math*].


  Args:
    value1: Float
    value2: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'WRAP'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, value1=value1, value2=value2, operation='WRAP', label=node_label, node_color=node_color)
    

```
## snap
```{eval-rst}

Geometry node [*Math*].


  Args:
    value1: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'SNAP'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, value1=value1, operation='SNAP', label=node_label, node_color=node_color)
    

```
## pingpong
```{eval-rst}

Geometry node [*Math*].


  Args:
    value1: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'PINGPONG'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, value1=value1, operation='PINGPONG', label=node_label, node_color=node_color)
    

```
## sin
```{eval-rst}

Geometry node [*Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'SINE'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, operation='SINE', label=node_label, node_color=node_color)
    

```
## cos
```{eval-rst}

Geometry node [*Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'COSINE'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, operation='COSINE', label=node_label, node_color=node_color)
    

```
## tan
```{eval-rst}

Geometry node [*Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'TANGENT'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, operation='TANGENT', label=node_label, node_color=node_color)
    

```
## arcsin
```{eval-rst}

Geometry node [*Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'ARCSINE'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, operation='ARCSINE', label=node_label, node_color=node_color)
    

```
## arccos
```{eval-rst}

Geometry node [*Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'ARCCOSINE'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, operation='ARCCOSINE', label=node_label, node_color=node_color)
    

```
## arctan
```{eval-rst}

Geometry node [*Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'ARCTANGENT'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, operation='ARCTANGENT', label=node_label, node_color=node_color)
    

```
## arctan2
```{eval-rst}

Geometry node [*Math*].


  Args:
    value1: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'ARCTAN2'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, value1=value1, operation='ARCTAN2', label=node_label, node_color=node_color)
    

```
## sinh
```{eval-rst}

Geometry node [*Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'SINH'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, operation='SINH', label=node_label, node_color=node_color)
    

```
## cosh
```{eval-rst}

Geometry node [*Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'COSH'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, operation='COSH', label=node_label, node_color=node_color)
    

```
## tanh
```{eval-rst}

Geometry node [*Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'TANH'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, operation='TANH', label=node_label, node_color=node_color)
    

```
## radians
```{eval-rst}

Geometry node [*Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'RADIANS'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, operation='RADIANS', label=node_label, node_color=node_color)
    

```
## degrees
```{eval-rst}

Geometry node [*Math*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'DEGREES'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=self, operation='DEGREES', label=node_label, node_color=node_color)
    
```
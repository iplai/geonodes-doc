
# geonodes functions

> global functions
  
<sub>go to [index](../index.md)</sub>

Example of use:
            
```python
import geonodes as gn
value = gn.Float(14.) # A float value
v = gn.sin(v)         # The sine of this value
```



## Functions

- [abs](#abs) : value (Float)
- [add](#add) : value (Float)
- [arccos](#arccos) : value (Float)
- [arcsin](#arcsin) : value (Float)
- [arctan](#arctan) : value (Float)
- [arctan2](#arctan2) : value (Float)
- [b_and](#b_and) : boolean (Boolean)
- [b_not](#b_not) : boolean (Boolean)
- [b_or](#b_or) : boolean (Boolean)
- [ceil](#ceil) : value (Float)
- [compare](#compare) : result (Boolean)
- [compare](#compare) : value (Float)
- [corners_of_face](#corners_of_face) : Sockets      [corner_index (Integer), total (Integer)]
- [corners_of_vertex](#corners_of_vertex) : Sockets      [corner_index (Integer), total (Integer)]
- [cos](#cos) : value (Float)
- [cosh](#cosh) : value (Float)
- [cross](#cross) : vector (Vector)
- [curve_of_point](#curve_of_point) : Sockets      [curve_index (Integer), index_in_curve (Integer)]
- [degrees](#degrees) : value (Float)
- [distance](#distance) : value (Float)
- [divide](#divide) : value (Float)
- [dot](#dot) : value (Float)
- [edges_of_corner](#edges_of_corner) : Sockets      [next_edge_index (Integer), previous_edge_index (Integer)]
- [edges_of_vertex](#edges_of_vertex) : Sockets      [edge_index (Integer), total (Integer)]
- [exp](#exp) : value (Float)
- [face_of_corner](#face_of_corner) : Sockets      [face_index (Integer), index_in_face (Integer)]
- [faceforward](#faceforward) : vector (Vector)
- [floor](#floor) : value (Float)
- [fract](#fract) : value (Float)
- [fraction](#fraction) : vector (Vector)
- [imply](#imply) : boolean (Boolean)
- [inverse_sqrt](#inverse_sqrt) : value (Float)
- [join_strings](#join_strings) : string (String)
- [length](#length) : value (Float)
- [log](#log) : value (Float)
- [math_greater_than](#math_greater_than) : value (Float)
- [math_less_than](#math_less_than) : value (Float)
- [max](#max) : value (Float)
- [min](#min) : value (Float)
- [modulo](#modulo) : value (Float)
- [multiply](#multiply) : value (Float)
- [multiply_add](#multiply_add) : value (Float)
- [nand](#nand) : boolean (Boolean)
- [nimply](#nimply) : boolean (Boolean)
- [nor](#nor) : boolean (Boolean)
- [normalize](#normalize) : vector (Vector)
- [offset_corner_in_face](#offset_corner_in_face) : corner_index (Integer)
- [pingpong](#pingpong) : value (Float)
- [pow](#pow) : value (Float)
- [project](#project) : vector (Vector)
- [radians](#radians) : value (Float)
- [reflect](#reflect) : vector (Vector)
- [refract](#refract) : vector (Vector)
- [round](#round) : value (Float)
- [scale](#scale) : vector (Vector)
- [scene](#scene) : Sockets      [seconds (Float), frame (Float)]
- [sign](#sign) : value (Float)
- [sin](#sin) : value (Float)
- [sinh](#sinh) : value (Float)
- [smooth_max](#smooth_max) : value (Float)
- [smooth_min](#smooth_min) : value (Float)
- [snap](#snap) : value (Float)
- [sqrt](#sqrt) : value (Float)
- [subtract](#subtract) : value (Float)
- [switch](#switch) : output (input_type dependant)
- [tan](#tan) : value (Float)
- [tanh](#tanh) : value (Float)
- [trunc](#trunc) : value (Float)
- [vector_absolute](#vector_absolute) : vector (Vector)
- [vector_add](#vector_add) : vector (Vector)
- [vector_ceil](#vector_ceil) : vector (Vector)
- [vector_cos](#vector_cos) : vector (Vector)
- [vector_divide](#vector_divide) : vector (Vector)
- [vector_floor](#vector_floor) : vector (Vector)
- [vector_max](#vector_max) : vector (Vector)
- [vector_min](#vector_min) : vector (Vector)
- [vector_modulo](#vector_modulo) : vector (Vector)
- [vector_multiply](#vector_multiply) : vector (Vector)
- [vector_multiply_add](#vector_multiply_add) : vector (Vector)
- [vector_sin](#vector_sin) : vector (Vector)
- [vector_snap](#vector_snap) : vector (Vector)
- [vector_subtract](#vector_subtract) : vector (Vector)
- [vector_tan](#vector_tan) : vector (Vector)
- [vector_wrap](#vector_wrap) : vector (Vector)
- [vertex_of_corner](#vertex_of_corner) : vertex_index (Integer)
- [wrap](#wrap) : value (Float)
- [xnor](#xnor) : boolean (Boolean)
- [xor](#xor) : boolean (Boolean)

## compare
```{eval-rst}

Geometry node [*Compare*].


  Args:
    a: Float
    b: Float
    epsilon: Float
    data_type (str): 'FLOAT' in [FLOAT, INT, VECTOR, STRING, RGBA]
    mode (str): 'ELEMENT' in [ELEMENT, LENGTH, AVERAGE, DOT_PRODUCT, DIRECTION]
    operation (str): 'GREATER_THAN' in [LESS_THAN, LESS_EQUAL, GREATER_THAN, GREATER_EQUAL, EQUAL, NOT_EQUAL]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Boolean
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Compare`
  
  
  Blender reference : `FunctionNodeCompare <https://docs.blender.org/api/current/bpy.types.FunctionNodeCompare.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Compare(a=a, b=b, epsilon=epsilon, data_type=data_type, mode=mode, operation=operation, label=node_label, node_color=node_color)
    

```
## join_strings
```{eval-rst}

Geometry node [*Join Strings*].


  Args:
    strings: <m>String
    delimiter: String
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    String
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.JoinStrings`
  
  
  Blender reference : `GeometryNodeStringJoin <https://docs.blender.org/api/current/bpy.types.GeometryNodeStringJoin.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.JoinStrings(*strings, delimiter=delimiter, label=node_label, node_color=node_color)
    

```
## scene
```{eval-rst}

Geometry node [*Scene Time*].


  Args:
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [seconds (Float), frame (Float)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.SceneTime`
  
  
  Blender reference : `GeometryNodeInputSceneTime <https://docs.blender.org/api/current/bpy.types.GeometryNodeInputSceneTime.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.SceneTime(label=node_label, node_color=node_color)
    

```
## switch
```{eval-rst}

Geometry node [*Switch*].


  Args:
    switch: Boolean
    false: Geometry
    true: Geometry
    input_type (str): 'GEOMETRY' in [FLOAT, INT, BOOLEAN, VECTOR, STRING,... , COLLECTION, TEXTURE, MATERIAL]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    input_type dependant
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Switch`
  
  
  Blender reference : `GeometryNodeSwitch <https://docs.blender.org/api/current/bpy.types.GeometryNodeSwitch.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Switch(switch=switch, false=false, true=true, input_type=input_type, label=node_label, node_color=node_color)
    

```
## b_and
```{eval-rst}

Geometry node [*Boolean Math*].


  Args:
    boolean0: Boolean
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
    nodes.BooleanMath(boolean0=boolean0, boolean1=boolean1, operation='AND', label=node_label, node_color=node_color)
    

```
## b_or
```{eval-rst}

Geometry node [*Boolean Math*].


  Args:
    boolean0: Boolean
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
    nodes.BooleanMath(boolean0=boolean0, boolean1=boolean1, operation='OR', label=node_label, node_color=node_color)
    

```
## b_not
```{eval-rst}

Geometry node [*Boolean Math*].


  Args:
    boolean0: Boolean
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
    nodes.BooleanMath(boolean0=boolean0, operation='NOT', label=node_label, node_color=node_color)
    

```
## nand
```{eval-rst}

Geometry node [*Boolean Math*].


  Args:
    boolean0: Boolean
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
    nodes.BooleanMath(boolean0=boolean0, boolean1=boolean1, operation='NAND', label=node_label, node_color=node_color)
    

```
## nor
```{eval-rst}

Geometry node [*Boolean Math*].


  Args:
    boolean0: Boolean
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
    nodes.BooleanMath(boolean0=boolean0, boolean1=boolean1, operation='NOR', label=node_label, node_color=node_color)
    

```
## xnor
```{eval-rst}

Geometry node [*Boolean Math*].


  Args:
    boolean0: Boolean
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
    nodes.BooleanMath(boolean0=boolean0, boolean1=boolean1, operation='XNOR', label=node_label, node_color=node_color)
    

```
## xor
```{eval-rst}

Geometry node [*Boolean Math*].


  Args:
    boolean0: Boolean
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
    nodes.BooleanMath(boolean0=boolean0, boolean1=boolean1, operation='XOR', label=node_label, node_color=node_color)
    

```
## imply
```{eval-rst}

Geometry node [*Boolean Math*].


  Args:
    boolean0: Boolean
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
    nodes.BooleanMath(boolean0=boolean0, boolean1=boolean1, operation='IMPLY', label=node_label, node_color=node_color)
    

```
## nimply
```{eval-rst}

Geometry node [*Boolean Math*].


  Args:
    boolean0: Boolean
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
    nodes.BooleanMath(boolean0=boolean0, boolean1=boolean1, operation='NIMPLY', label=node_label, node_color=node_color)
    

```
## add
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
    value1: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'ADD'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=value0, value1=value1, operation='ADD', label=node_label, node_color=node_color)
    

```
## subtract
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
    value1: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'SUBTRACT'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=value0, value1=value1, operation='SUBTRACT', label=node_label, node_color=node_color)
    

```
## multiply
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
    value1: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'MULTIPLY'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=value0, value1=value1, operation='MULTIPLY', label=node_label, node_color=node_color)
    

```
## divide
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
    value1: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Math`
  
  - operation = 'DIVIDE'
    
  Blender reference : `ShaderNodeMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Math(value0=value0, value1=value1, operation='DIVIDE', label=node_label, node_color=node_color)
    

```
## multiply_add
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, value1=value1, value2=value2, operation='MULTIPLY_ADD', label=node_label, node_color=node_color)
    

```
## pow
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, value1=value1, operation='POWER', label=node_label, node_color=node_color)
    

```
## log
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, value1=value1, operation='LOGARITHM', label=node_label, node_color=node_color)
    

```
## sqrt
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, operation='SQRT', label=node_label, node_color=node_color)
    

```
## inverse_sqrt
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, operation='INVERSE_SQRT', label=node_label, node_color=node_color)
    

```
## abs
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, operation='ABSOLUTE', label=node_label, node_color=node_color)
    

```
## exp
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, operation='EXPONENT', label=node_label, node_color=node_color)
    

```
## min
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, value1=value1, operation='MINIMUM', label=node_label, node_color=node_color)
    

```
## max
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, value1=value1, operation='MAXIMUM', label=node_label, node_color=node_color)
    

```
## math_less_than
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, value1=value1, operation='LESS_THAN', label=node_label, node_color=node_color)
    

```
## math_greater_than
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, value1=value1, operation='GREATER_THAN', label=node_label, node_color=node_color)
    

```
## sign
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, operation='SIGN', label=node_label, node_color=node_color)
    

```
## compare
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, value1=value1, value2=value2, operation='COMPARE', label=node_label, node_color=node_color)
    

```
## smooth_min
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, value1=value1, value2=value2, operation='SMOOTH_MIN', label=node_label, node_color=node_color)
    

```
## smooth_max
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, value1=value1, value2=value2, operation='SMOOTH_MAX', label=node_label, node_color=node_color)
    

```
## round
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, operation='ROUND', label=node_label, node_color=node_color)
    

```
## floor
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, operation='FLOOR', label=node_label, node_color=node_color)
    

```
## ceil
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, operation='CEIL', label=node_label, node_color=node_color)
    

```
## trunc
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, operation='TRUNC', label=node_label, node_color=node_color)
    

```
## fract
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, operation='FRACT', label=node_label, node_color=node_color)
    

```
## modulo
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, value1=value1, operation='MODULO', label=node_label, node_color=node_color)
    

```
## wrap
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, value1=value1, value2=value2, operation='WRAP', label=node_label, node_color=node_color)
    

```
## snap
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, value1=value1, operation='SNAP', label=node_label, node_color=node_color)
    

```
## pingpong
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, value1=value1, operation='PINGPONG', label=node_label, node_color=node_color)
    

```
## sin
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, operation='SINE', label=node_label, node_color=node_color)
    

```
## cos
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, operation='COSINE', label=node_label, node_color=node_color)
    

```
## tan
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, operation='TANGENT', label=node_label, node_color=node_color)
    

```
## arcsin
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, operation='ARCSINE', label=node_label, node_color=node_color)
    

```
## arccos
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, operation='ARCCOSINE', label=node_label, node_color=node_color)
    

```
## arctan
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, operation='ARCTANGENT', label=node_label, node_color=node_color)
    

```
## arctan2
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, value1=value1, operation='ARCTAN2', label=node_label, node_color=node_color)
    

```
## sinh
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, operation='SINH', label=node_label, node_color=node_color)
    

```
## cosh
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, operation='COSH', label=node_label, node_color=node_color)
    

```
## tanh
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, operation='TANH', label=node_label, node_color=node_color)
    

```
## radians
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, operation='RADIANS', label=node_label, node_color=node_color)
    

```
## degrees
```{eval-rst}

Geometry node [*Math*].


  Args:
    value0: Float
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
    nodes.Math(value0=value0, operation='DEGREES', label=node_label, node_color=node_color)
    

```
## vector_add
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    vector1: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'ADD'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, vector1=vector1, operation='ADD', label=node_label, node_color=node_color)
    

```
## vector_subtract
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    vector1: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'SUBTRACT'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, vector1=vector1, operation='SUBTRACT', label=node_label, node_color=node_color)
    

```
## vector_multiply
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    vector1: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'MULTIPLY'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, vector1=vector1, operation='MULTIPLY', label=node_label, node_color=node_color)
    

```
## vector_divide
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    vector1: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'DIVIDE'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, vector1=vector1, operation='DIVIDE', label=node_label, node_color=node_color)
    

```
## vector_multiply_add
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    vector1: Vector
    vector2: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'MULTIPLY_ADD'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, vector1=vector1, vector2=vector2, operation='MULTIPLY_ADD', label=node_label, node_color=node_color)
    

```
## cross
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    vector1: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'CROSS_PRODUCT'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, vector1=vector1, operation='CROSS_PRODUCT', label=node_label, node_color=node_color)
    

```
## project
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    vector1: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'PROJECT'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, vector1=vector1, operation='PROJECT', label=node_label, node_color=node_color)
    

```
## reflect
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    vector1: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'REFLECT'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, vector1=vector1, operation='REFLECT', label=node_label, node_color=node_color)
    

```
## refract
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    vector1: Vector
    scale: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'REFRACT'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, vector1=vector1, scale=scale, operation='REFRACT', label=node_label, node_color=node_color)
    

```
## faceforward
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    vector1: Vector
    vector2: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'FACEFORWARD'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, vector1=vector1, vector2=vector2, operation='FACEFORWARD', label=node_label, node_color=node_color)
    

```
## dot
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    vector1: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'DOT_PRODUCT'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, vector1=vector1, operation='DOT_PRODUCT', label=node_label, node_color=node_color)
    

```
## distance
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    vector1: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'DISTANCE'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, vector1=vector1, operation='DISTANCE', label=node_label, node_color=node_color)
    

```
## length
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'LENGTH'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, operation='LENGTH', label=node_label, node_color=node_color)
    

```
## scale
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    scale: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'SCALE'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, scale=scale, operation='SCALE', label=node_label, node_color=node_color)
    

```
## normalize
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'NORMALIZE'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, operation='NORMALIZE', label=node_label, node_color=node_color)
    

```
## vector_absolute
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'ABSOLUTE'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, operation='ABSOLUTE', label=node_label, node_color=node_color)
    

```
## vector_min
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    vector1: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'MINIMUM'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, vector1=vector1, operation='MINIMUM', label=node_label, node_color=node_color)
    

```
## vector_max
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    vector1: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'MAXIMUM'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, vector1=vector1, operation='MAXIMUM', label=node_label, node_color=node_color)
    

```
## vector_floor
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'FLOOR'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, operation='FLOOR', label=node_label, node_color=node_color)
    

```
## vector_ceil
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'CEIL'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, operation='CEIL', label=node_label, node_color=node_color)
    

```
## fraction
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'FRACTION'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, operation='FRACTION', label=node_label, node_color=node_color)
    

```
## vector_modulo
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    vector1: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'MODULO'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, vector1=vector1, operation='MODULO', label=node_label, node_color=node_color)
    

```
## vector_wrap
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    vector1: Vector
    vector2: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'WRAP'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, vector1=vector1, vector2=vector2, operation='WRAP', label=node_label, node_color=node_color)
    

```
## vector_snap
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    vector1: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'SNAP'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, vector1=vector1, operation='SNAP', label=node_label, node_color=node_color)
    

```
## vector_sin
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'SINE'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, operation='SINE', label=node_label, node_color=node_color)
    

```
## vector_cos
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'COSINE'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, operation='COSINE', label=node_label, node_color=node_color)
    

```
## vector_tan
```{eval-rst}

Geometry node [*Vector Math*].


  Args:
    vector0: Vector
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Vector
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VectorMath`
  
  - operation = 'TANGENT'
    
  Blender reference : `ShaderNodeVectorMath <https://docs.blender.org/api/current/bpy.types.ShaderNodeVectorMath.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VectorMath(vector0=vector0, operation='TANGENT', label=node_label, node_color=node_color)
    

```
## corners_of_face
```{eval-rst}

Geometry node [*Corners of Face*].


  Args:
    face_index: Integer
    weights: Float
    sort_index: Integer
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [corner_index (Integer), total (Integer)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.CornersOfFace`
  
  
  Blender reference : `GeometryNodeCornersOfFace <https://docs.blender.org/api/current/bpy.types.GeometryNodeCornersOfFace.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.CornersOfFace(face_index=face_index, weights=weights, sort_index=sort_index, label=node_label, node_color=node_color)
    

```
## corners_of_vertex
```{eval-rst}

Geometry node [*Corners of Vertex*].


  Args:
    vertex_index: Integer
    weights: Float
    sort_index: Integer
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [corner_index (Integer), total (Integer)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.CornersOfVertex`
  
  
  Blender reference : `GeometryNodeCornersOfVertex <https://docs.blender.org/api/current/bpy.types.GeometryNodeCornersOfVertex.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.CornersOfVertex(vertex_index=vertex_index, weights=weights, sort_index=sort_index, label=node_label, node_color=node_color)
    

```
## edges_of_corner
```{eval-rst}

Geometry node [*Edges of Corner*].


  Args:
    corner_index: Integer
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [next_edge_index (Integer), previous_edge_index (Integer)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.EdgesOfCorner`
  
  
  Blender reference : `GeometryNodeEdgesOfCorner <https://docs.blender.org/api/current/bpy.types.GeometryNodeEdgesOfCorner.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.EdgesOfCorner(corner_index=corner_index, label=node_label, node_color=node_color)
    

```
## edges_of_vertex
```{eval-rst}

Geometry node [*Edges of Vertex*].


  Args:
    vertex_index: Integer
    weights: Float
    sort_index: Integer
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [edge_index (Integer), total (Integer)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.EdgesOfVertex`
  
  
  Blender reference : `GeometryNodeEdgesOfVertex <https://docs.blender.org/api/current/bpy.types.GeometryNodeEdgesOfVertex.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.EdgesOfVertex(vertex_index=vertex_index, weights=weights, sort_index=sort_index, label=node_label, node_color=node_color)
    

```
## face_of_corner
```{eval-rst}

Geometry node [*Face of Corner*].


  Args:
    corner_index: Integer
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [face_index (Integer), index_in_face (Integer)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.FaceOfCorner`
  
  
  Blender reference : `GeometryNodeFaceOfCorner <https://docs.blender.org/api/current/bpy.types.GeometryNodeFaceOfCorner.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.FaceOfCorner(corner_index=corner_index, label=node_label, node_color=node_color)
    

```
## offset_corner_in_face
```{eval-rst}

Geometry node [*Offset Corner in Face*].


  Args:
    corner_index: Integer
    offset: Integer
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Integer
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.OffsetCornerInFace`
  
  
  Blender reference : `GeometryNodeOffsetCornerInFace <https://docs.blender.org/api/current/bpy.types.GeometryNodeOffsetCornerInFace.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.OffsetCornerInFace(corner_index=corner_index, offset=offset, label=node_label, node_color=node_color)
    

```
## vertex_of_corner
```{eval-rst}

Geometry node [*Vertex of Corner*].


  Args:
    corner_index: Integer
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Integer
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VertexOfCorner`
  
  
  Blender reference : `GeometryNodeVertexOfCorner <https://docs.blender.org/api/current/bpy.types.GeometryNodeVertexOfCorner.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VertexOfCorner(corner_index=corner_index, label=node_label, node_color=node_color)
    

```
## curve_of_point
```{eval-rst}

Geometry node [*Curve of Point*].


  Args:
    point_index: Integer
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [curve_index (Integer), index_in_curve (Integer)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.CurveOfPoint`
  
  
  Blender reference : `GeometryNodeCurveOfPoint <https://docs.blender.org/api/current/bpy.types.GeometryNodeCurveOfPoint.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.CurveOfPoint(point_index=point_index, label=node_label, node_color=node_color)
    
```
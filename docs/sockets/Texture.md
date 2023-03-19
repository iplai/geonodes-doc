
# Data socket Texture

> Inherits from dsock.Texture
  
<sub>go to [index](../index.md)</sub>



## Static methods

- [Brick](#brick) : Sockets      [color (Color), fac (Float)]
- [Checker](#checker) : Sockets      [color (Color), fac (Float)]
- [Gradient](#gradient) : Sockets      [color (Color), fac (Float)]
- [Image](#image) : Sockets      [color (Color), alpha (Float)]
- [Magic](#magic) : Sockets      [color (Color), fac (Float)]
- [Musgrave](#musgrave) : fac (Float)
- [Noise](#noise) : Sockets      [fac (Float), color (Color)]
- [Voronoi](#voronoi) : Sockets      [distance (Float), color (Color), position (Vector), w (Float), radius (Float)]
- [Wave](#wave) : Sockets      [color (Color), fac (Float)]
- [WhiteNoise](#whitenoise) : Sockets      [value (Float), color (Color)]

## Methods

- [switch](#switch) : output (Texture)

## Brick
```{eval-rst}

Geometry node [*Brick Texture*].


  Args:
    vector: Vector
    color1: Color
    color2: Color
    mortar: Color
    scale: Float
    mortar_size: Float
    mortar_smooth: Float
    bias: Float
    brick_width: Float
    row_height: Float
    offset (float): 0.5
    offset_frequency (int): 2
    squash (float): 1.0
    squash_frequency (int): 2
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [color (Color), fac (Float)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.BrickTexture`
  
  
  Blender reference : `ShaderNodeTexBrick <https://docs.blender.org/api/current/bpy.types.ShaderNodeTexBrick.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.BrickTexture(vector=vector, color1=color1, color2=color2, mortar=mortar, scale=scale, mortar_size=mortar_size, mortar_smooth=mortar_smooth, bias=bias, brick_width=brick_width, row_height=row_height, offset=offset, offset_frequency=offset_frequency, squash=squash, squash_frequency=squash_frequency, label=node_label, node_color=node_color)
    

```
## Checker
```{eval-rst}

Geometry node [*Checker Texture*].


  Args:
    vector: Vector
    color1: Color
    color2: Color
    scale: Float
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [color (Color), fac (Float)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.CheckerTexture`
  
  
  Blender reference : `ShaderNodeTexChecker <https://docs.blender.org/api/current/bpy.types.ShaderNodeTexChecker.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.CheckerTexture(vector=vector, color1=color1, color2=color2, scale=scale, label=node_label, node_color=node_color)
    

```
## Gradient
```{eval-rst}

Geometry node [*Gradient Texture*].


  Args:
    vector: Vector
    gradient_type (str): 'LINEAR' in [LINEAR, QUADRATIC, EASING, DIAGONAL, SPHERICAL, QUADRATIC_SPHERE, RADIAL]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [color (Color), fac (Float)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.GradientTexture`
  
  
  Blender reference : `ShaderNodeTexGradient <https://docs.blender.org/api/current/bpy.types.ShaderNodeTexGradient.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.GradientTexture(vector=vector, gradient_type=gradient_type, label=node_label, node_color=node_color)
    

```
## Magic
```{eval-rst}

Geometry node [*Magic Texture*].


  Args:
    vector: Vector
    scale: Float
    distortion: Float
    turbulence_depth (int): 2
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [color (Color), fac (Float)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.MagicTexture`
  
  
  Blender reference : `ShaderNodeTexMagic <https://docs.blender.org/api/current/bpy.types.ShaderNodeTexMagic.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.MagicTexture(vector=vector, scale=scale, distortion=distortion, turbulence_depth=turbulence_depth, label=node_label, node_color=node_color)
    

```
## Musgrave
```{eval-rst}

Geometry node [*Musgrave Texture*].


  Args:
    vector: Vector
    w: Float
    scale: Float
    detail: Float
    dimension: Float
    lacunarity: Float
    offset: Float
    gain: Float
    musgrave_dimensions (str): '3D' in [1D, 2D, 3D, 4D]
    musgrave_type (str): 'FBM' in [MULTIFRACTAL, RIDGED_MULTIFRACTAL, HYBRID_MULTIFRACTAL, FBM, HETERO_TERRAIN]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Float
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.MusgraveTexture`
  
  
  Blender reference : `ShaderNodeTexMusgrave <https://docs.blender.org/api/current/bpy.types.ShaderNodeTexMusgrave.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.MusgraveTexture(vector=vector, w=w, scale=scale, detail=detail, dimension=dimension, lacunarity=lacunarity, offset=offset, gain=gain, musgrave_dimensions=musgrave_dimensions, musgrave_type=musgrave_type, label=node_label, node_color=node_color)
    

```
## Noise
```{eval-rst}

Geometry node [*Noise Texture*].


  Args:
    vector: Vector
    w: Float
    scale: Float
    detail: Float
    roughness: Float
    distortion: Float
    noise_dimensions (str): '3D' in [1D, 2D, 3D, 4D]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [fac (Float), color (Color)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.NoiseTexture`
  
  
  Blender reference : `ShaderNodeTexNoise <https://docs.blender.org/api/current/bpy.types.ShaderNodeTexNoise.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.NoiseTexture(vector=vector, w=w, scale=scale, detail=detail, roughness=roughness, distortion=distortion, noise_dimensions=noise_dimensions, label=node_label, node_color=node_color)
    

```
## Voronoi
```{eval-rst}

Geometry node [*Voronoi Texture*].


  Args:
    vector: Vector
    w: Float
    scale: Float
    smoothness: Float
    exponent: Float
    randomness: Float
    distance (str): 'EUCLIDEAN' in [EUCLIDEAN, MANHATTAN, CHEBYCHEV, MINKOWSKI]
    feature (str): 'F1' in [F1, F2, SMOOTH_F1, DISTANCE_TO_EDGE, N_SPHERE_RADIUS]
    voronoi_dimensions (str): '3D' in [1D, 2D, 3D, 4D]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [distance (Float), color (Color), position (Vector), w (Float), radius (Float)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.VoronoiTexture`
  
  
  Blender reference : `ShaderNodeTexVoronoi <https://docs.blender.org/api/current/bpy.types.ShaderNodeTexVoronoi.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.VoronoiTexture(vector=vector, w=w, scale=scale, smoothness=smoothness, exponent=exponent, randomness=randomness, distance=distance, feature=feature, voronoi_dimensions=voronoi_dimensions, label=node_label, node_color=node_color)
    

```
## Wave
```{eval-rst}

Geometry node [*Wave Texture*].


  Args:
    vector: Vector
    scale: Float
    distortion: Float
    detail: Float
    detail_scale: Float
    detail_roughness: Float
    phase_offset: Float
    bands_direction (str): 'X' in [X, Y, Z, DIAGONAL]
    rings_direction (str): 'X' in [X, Y, Z, SPHERICAL]
    wave_profile (str): 'SIN' in [SIN, SAW, TRI]
    wave_type (str): 'BANDS' in [BANDS, RINGS]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [color (Color), fac (Float)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.WaveTexture`
  
  
  Blender reference : `ShaderNodeTexWave <https://docs.blender.org/api/current/bpy.types.ShaderNodeTexWave.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.WaveTexture(vector=vector, scale=scale, distortion=distortion, detail=detail, detail_scale=detail_scale, detail_roughness=detail_roughness, phase_offset=phase_offset, bands_direction=bands_direction, rings_direction=rings_direction, wave_profile=wave_profile, wave_type=wave_type, label=node_label, node_color=node_color)
    

```
## WhiteNoise
```{eval-rst}

Geometry node [*White Noise Texture*].


  Args:
    vector: Vector
    w: Float
    noise_dimensions (str): '3D' in [1D, 2D, 3D, 4D]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [value (Float), color (Color)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.WhiteNoiseTexture`
  
  
  Blender reference : `ShaderNodeTexWhiteNoise <https://docs.blender.org/api/current/bpy.types.ShaderNodeTexWhiteNoise.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.WhiteNoiseTexture(vector=vector, w=w, noise_dimensions=noise_dimensions, label=node_label, node_color=node_color)
    

```
## Image
```{eval-rst}

Geometry node [*Image Texture*].


  Args:
    image: Image
    vector: Vector
    frame: Integer
    extension (str): 'REPEAT' in [REPEAT, EXTEND, CLIP]
    interpolation (str): 'Linear' in [Linear, Closest, Cubic]
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Sockets [color (Color), alpha (Float)]
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.ImageTexture`
  
  
  Blender reference : `GeometryNodeImageTexture <https://docs.blender.org/api/current/bpy.types.GeometryNodeImageTexture.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.ImageTexture(image=image, vector=vector, frame=frame, extension=extension, interpolation=interpolation, label=node_label, node_color=node_color)
    

```
## switch
```{eval-rst}

Geometry node [*Switch*].


  Args:
    switch: Boolean
    true: Texture
    node_label (str): Node label
    node_color (color): Node background color
    
  Returns:
    Texture
    
  **Node creation**
  
  Node :class:`~geonodes.nodes.nodes.Switch`
  
  - input_type = 'TEXTURE'
    
  Blender reference : `GeometryNodeSwitch <https://docs.blender.org/api/current/bpy.types.GeometryNodeSwitch.html>`_
  
  .. code-block:: python
  
    from geonodes import nodes
    nodes.Switch(false=self, switch=switch, true=true, input_type='TEXTURE', label=node_label, node_color=node_color)
    
```
                    RENDERING
Rendering is the process of generating a visual representation of a 2D or 3D model to communicate its appearance, structure, materials, lighting and environment.
In engineering and product design, rendering helps designers visualize how a product, component, building or mechanical assembly will look before it is manufactured or constructed.
  Main purposes:
- Visualize product appearance and form.
- Communicate design concepts to clients and manufacturers.
- Evaluate colours, materials, textures and finishes.
- Present realistic product prototypes.
- Identify visual design problems before production.
- Support marketing, presentations and technical documentation.

 Types of Rendering
  Based on Visual Style;
1. Wireframe rendering: Displays only the edges and vertices of a model. Useful for understanding geometry and structure.
2. Hidden-line rendering: Shows visible edges while concealing edges blocked by surfaces.
3. Shaded rendering: Uses surface shading to communicate shape and depth.
4. Flat-shaded rendering: Gives each polygon a uniform appearance, without smooth transitions.
5. Smooth-shaded rendering: Interpolates surface normals to create continuous-looking surfaces.
6. Photorealistic rendering: Produces images that closely resemble real photographs using realistic materials, lighting and camera settings.
7. Non-photorealistic rendering (NPR): Uses artistic styles such as sketches, cartoons, illustrations and technical drawings.
  Based on Rendering Method;
1. Real-time rendering: Generates images rapidly, often at interactive frame rates. Used in games, simulations, interactive product visualization and virtual reality.
2. Offline rendering: Uses more computational time to produce higher-quality images. Used in product presentations, animation and architectural visualization.
3. Rasterization: Converts 3D geometry into pixels. It is generally fast and widely used in real-time graphics.
4. Ray tracing: Simulates light rays to calculate reflections, shadows, refraction and other lighting effects.
5. Path tracing: Uses many simulated light paths to approximate realistic global illumination. It can produce highly realistic images but is computationally expensive.

 Rendering Pipeline;
A rendering pipeline converts a digital 3D scene into a final 2D image.
  Main stages:
1. 3D modelling: Create the object's geometry using vertices, edges, faces and surfaces.
2. Scene preparation: Arrange objects, backgrounds, cameras and environmental elements.
3. Material assignment: Define the physical appearance of surfaces.
4. Lighting setup: Add light sources and control their intensity, direction and colour.
5. Camera setup: Choose the viewing position, orientation, projection and focal length.
6. Rendering: Process geometry, materials, lighting and camera information to generate pixels.
7. Post-processing: Adjust colour, contrast, brightness, sharpness and other image properties.
8. Output: Export the final image or animation.

 Materials and Textures
A material defines how a surface interacts with light. A texture provides surface detail or modifies material properties.
  Important material properties:
- Base colour (albedo): The basic colour of a surface.
- Roughness: Determines how smooth or rough a surface appears. Low roughness produces sharper reflections; high roughness produces blurred reflections.
- Metallic: Controls whether a material behaves like a metal.
- Transparency/opacity: Determines how much light passes through a surface.
- Index of refraction (IOR): Determines how light bends when entering a transparent material.
- Normal map: Simulates small surface details by modifying shading normals without changing the actual geometry.
- Bump map: Creates an apparent surface relief effect through shading.
- Displacement map: Changes actual surface geometry based on texture values.
Examples:
- Polished steel: metallic, low roughness.
- Rubber: non-metallic, relatively high roughness.
- Glass: transparent, with an appropriate IOR.
- Wood: non-metallic, with colour and grain textures.

 Lighting in Rendering
Lighting determines the visibility, depth, mood and realism of a rendered scene.
  Common light sources:
- Directional light: Simulates light from a distant source, such as sunlight.
- Point light: Emits light in all directions from one position.
- Spotlight: Directs light within a cone.
- Area light: Emits light from a surface, producing softer shadows.
- Environment lighting: Uses surrounding environmental illumination, often from an image-based environment map.
  Important lighting concepts:
- Direct illumination: Light reaching a surface directly from a source.
- Indirect illumination: Light reaching a surface after bouncing off other surfaces.
- Shadows: Areas where light is blocked by objects.
- Ambient occlusion: Approximates darkening in areas where nearby surfaces restrict ambient light.
- Global illumination: Accounts for direct and indirect light interactions throughout a scene.
- Reflection: Light bouncing off a surface.
- Refraction: Bending of light as it passes between materials with different refractive indices.
  Three-point lighting:
1. Key light – main light source.
2. Fill light – reduces harsh shadows.
3. Back light – separates the object from the background.

 Cameras and Projection
A virtual camera determines how a 3D scene is viewed and converted into a 2D image.
  Camera parameters:
- Position and orientation.
- Focal length.
- Field of view (FOV).
- Aperture and depth of field.
- Aspect ratio.
- Focus distance.
  Projection types:
1. Orthographic projection: Parallel projection in which object size does not change with distance. Useful for engineering and technical visualization.
2. Perspective projection: Parallel lines may converge toward vanishing points, creating realistic depth.
3. Isometric view: Shows three principal axes equally inclined to the viewing plane, useful for communicating 3D engineering geometry.
Field of view: Determines how much of the scene is visible through the camera.
A wider field of view shows more of the scene but can exaggerate perspective distortion.

 Rendering Quality and Performance
The quality of a rendered image depends on several factors:
- Resolution: Number of pixels in the image, e.g. 1920 × 1080.
- Sampling: Number of samples used to estimate pixel colour and lighting.
- Anti-aliasing: Reduces jagged edges.
- Shadow quality: Determines shadow sharpness and accuracy.
- Reflection quality: Determines how accurately reflected objects and environments appear.
- Global illumination: Improves realistic indirect lighting.
- Denoising: Reduces noise caused by limited rendering samples.
- Texture resolution: Determines the detail available in surface textures.
Common image-quality trade-off: Increasing resolution and sample count generally improves quality but increases memory usage and rendering time.

 Basic Rendering Mathematics
  Perspective Projection;
For a simplified pinhole camera:[
x'=f x/z, y'=f y/z
Where:
- (x,y) = point coordinates in camera space.
- (z) = depth from the camera.
- (f) = focal length.
- (x',y') = projected image coordinates.
Objects farther from the camera appear smaller.
  Reflection Law;
    \theta_i=\theta_r
The angle of incidence equals the angle of reflection, measured from the surface normal.
  Refraction – Snell's Law;
    n_1\sin\theta_1=n_2\sin\theta_2
Where:
- (n_1,n_2) = refractive indices.
- (\theta_1,\theta_2) = angles measured from the normal.
  Lambertian Diffuse Lighting;
    I_d=k_d I_L\max(0,\mathbf{N}\cdot\mathbf{L})
Where:
- (I_d) = diffuse reflected intensity.
- (k_d) = diffuse reflectivity.
- (I_L) = light intensity.
- (\mathbf{N}) = unit surface normal.
- (\mathbf{L}) = unit direction toward the light.
A surface receives maximum diffuse illumination when it faces the light directly.
  Image Resolution;
    N=W\times H
Where:
- (N) = total number of pixels.
- (W) = image width in pixels.
- (H) = image height in pixels.
For example, a 1920 × 1080 image contains 2,073,600 pixels.

 Rendering in Engineering and Product Design
   Rendering is used to:
- Visualize mechanical components, machines and assemblies.
- Present industrial and consumer product designs.
- Examine surface finishes, colours and materials.
- Visualize buildings and engineering structures.
- Communicate designs to clients and manufacturing teams.
- Produce product catalogues, manuals and promotional images.
- Support design reviews before physical prototyping.
  Engineering rendering versus artistic rendering:
- Engineering rendering prioritizes dimensional accuracy, correct geometry, materials and design communication.
- Artistic rendering prioritizes visual expression, style, mood and composition.
A visually realistic render does not automatically prove that a design is structurally safe or manufacturable. Engineering analysis and physical testing may still be required.

 Rendering Software and Tools
  Common tools include:
- Blender: 3D modelling, materials, animation and rendering.
- Autodesk 3ds Max: Product and architectural visualization.
- Autodesk Maya: 3D modelling, animation and rendering.
- KeyShot: Product-focused photorealistic rendering.
- SolidWorks Visualize: Rendering of CAD models.
- Autodesk VRED: Automotive and industrial visualization.
- Unreal Engine: Real-time rendering and interactive visualization.
- V-Ray: Photorealistic rendering plugin used with several 3D applications.

 Common Rendering Problems and Solutions
Problem| Possible solution
Grainy/noisy image| Increase samples or use denoising
Jagged edges| Enable anti-aliasing
Unrealistic materials| Adjust roughness, metallic and texture settings
Flat-looking objects| Improve lighting and shadows
Overexposed image| Reduce light intensity or exposure
Slow rendering| Optimize geometry, textures and sample settings
Missing textures| Relink or correctly package texture files
Incorrect reflections| Check materials, lighting and environment maps

 Practical Rendering Workflow
1. Create or import a dimensionally accurate 3D model.
2. Clean the geometry and correct modelling errors.
3. Assign appropriate materials and textures.
4. Set up the scene and background.
5. Position the camera to communicate the design clearly.
6. Add and adjust lighting.
7. Generate a low-quality test render.
8. Correct materials, lighting, composition and camera settings.
9. Increase resolution and rendering quality.
10. Apply post-processing where necessary.
11. Export the final image in an appropriate format.

  Common output formats:
- PNG – high-quality images; supports transparency.
- JPEG/JPG – compressed images for presentations and web use.
- TIFF – high-quality image storage and professional workflows.
- EXR – high-dynamic-range rendering data.
- MP4 – rendered animation or video.

 Important Tips
- Start with an accurate 3D model; rendering cannot correct incorrect geometry.
- Use realistic materials rather than relying only on colour.
- Avoid excessive lighting, reflections and visual effects.
- Use appropriate camera angles to communicate important design features.
- Test with low-quality renders before producing final images.
- Use sufficient resolution for the intended presentation.
- Keep engineering dimensions and proportions accurate.
- Distinguish visual appearance from engineering performance.
- Save materials, textures, lighting and camera settings with the project.

Key distinction: 
3D modelling creates the object, material assignment defines its surface properties, lighting illuminates it, and rendering generates the final visual image.
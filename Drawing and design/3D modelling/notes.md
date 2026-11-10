                3D MODELLING
3D modelling is the process of creating a mathematical or digital representation of an object in three-dimensional space using specialized computer software.
  A 3D model represents an object's:
- Length (X-axis).
- Width (Y-axis).
- Height (Z-axis).
- Shape and geometry.
- Surface characteristics.
- Material properties, where assigned.
- Spatial position and orientation.
  Importance of 3D modelling;
- Visualizes engineering designs before physical production.
- Supports product design, prototyping, and manufacturing.
- Enables engineering analysis and simulation.
- Helps detect design errors and geometric interference.
- Supports CNC machining and additive manufacturing (3D printing).
- Facilitates assembly design and component integration.
- Reduces development time and production costs.
  Applications;
- Mechanical component and machine design.
- Automotive and aerospace engineering.
- Robotics and automation.
- Architecture and structural engineering.
- Electronics enclosure design.
- Medical device design.
- Product development and industrial design.

 FUNDAMENTALS OF 3D SPACE AND GEOMETRY
A 3D model exists within a Cartesian coordinate system.
  Cartesian coordinates;
A point in 3D space is represented by:
    P = (x, y, z)
Where:
- x = position along the X-axis.
- y = position along the Y-axis.
- z = position along the Z-axis.
Distance between two points
For points P₁(x₁,y₁,z₁) and P₂(x₂,y₂,z₂):
    d = √[(x₂−x₁)² + (y₂−y₁)² + (z₂−z₁)²]
Vector magnitude
For vector A = (Ax, Ay, Az):
    |A| = √(Ax² + Ay² + Az²)
  Basic geometric solids;
- Cube: Six equal square faces.
- Cuboid: Six rectangular faces.
- Cylinder: Two circular ends and a curved surface.
- Cone: Circular base and a vertex.
- Sphere: All surface points are equidistant from its centre.
- Prism: Two parallel, congruent polygonal ends.
- Pyramid: Polygonal base with triangular faces meeting at an apex.
  Important volume equations;
Cube:
    V = a³
Cuboid:
    V = lwh
Cylinder:
    V = πr²h
Cone:
    V = ⅓πr²h
Sphere:
    V = ⁴⁄₃πr³
These equations are useful for checking model dimensions, material quantities, and approximate manufacturing requirements.

 TYPES OF 3D MODELLING
  Solid modelling;
Represents an object as a complete, enclosed volume.
Characteristics:
- Defines the object's interior and exterior.
- Supports volume and mass-property calculations.
- Useful for mechanical components and assemblies.
- Supports manufacturing and engineering simulation workflows.
Examples: Shafts, gears, brackets, housings, and machine components.
  Surface modelling;
Represents an object using its external surfaces without necessarily defining a closed solid.
Characteristics:
- Provides control over complex curved surfaces.
- Useful for aerodynamic and aesthetic shapes.
- Common in automotive and aerospace design.
Examples: Vehicle body panels, aircraft surfaces, and product casings.
  Wireframe modelling;
Represents an object using points, lines, and curves that define its edges.
Characteristics:
- Shows the skeletal structure of an object.
- Uses relatively simple geometric representations.
- Does not inherently define solid volume or enclosed surfaces.
  Mesh modelling;
Represents an object using interconnected polygonal faces, usually triangles or quadrilaterals.
Characteristics:
- Commonly uses vertices, edges, and faces.
- Suitable for complex organic shapes.
- Widely used in 3D printing, animation, scanning, and visualization.
  Parametric modelling;
Creates models using dimensions, constraints, parameters, and relationships.
Characteristics:
- Design changes can automatically update dependent features.
- Supports design intent and controlled modifications.
- Useful for engineering components and assemblies.
  Direct modelling;
Allows geometry to be modified directly by moving faces, edges, or vertices without depending primarily on a feature history.
Useful for:
- Rapid design modifications.
- Editing imported CAD geometry.
- Concept development.

 CORE 3D MODELLING OPERATIONS
These are the fundamental operations used to construct 3D objects.
  Sketching;
Creates 2D profiles on a plane before converting them into 3D geometry.
Common sketch elements:
- Lines.
- Circles.
- Arcs.
- Rectangles.
- Polygons.
- Splines.
Sketch constraints:
- Horizontal.
- Vertical.
- Coincident.
- Parallel.
- Perpendicular.
- Tangent.
- Equal.
- Concentric.
- Symmetric.
A fully constrained sketch has no remaining unintended degrees of freedom.
  Extrusion
Extends a 2D profile along a specified direction to create a 3D feature.
Example: Extruding a rectangle produces a cuboid.
For a constant cross-sectional area:
    V = Ah
Where:
- A = cross-sectional area.
- h = extrusion distance.
  Revolving;
Rotates a 2D profile around an axis to create a 3D object.
Applications:
- Shafts.
- Pulleys.
- Bushings.
- Cylindrical housings.
- Pressure-vessel components.
For a solid cylinder produced by revolution:
    V = πr²h
  Sweeping;
Moves a 2D profile along a defined path to generate a 3D feature.
Applications:
- Pipes.
- Tubes.
- Handles.
- Curved ducts.
- Cable conduits.
  Lofting;
Creates a 3D shape by connecting two or more profiles positioned on different planes.
Applications:
- Aircraft transitions.
- Duct transitions.
- Complex product housings.
- Aerodynamic components.
  Filleting;
Rounds sharp edges or corners using a specified radius.
Applications:
- Reducing stress concentrations.
- Improving ergonomics.
- Improving manufacturability.
- Removing sharp edges.
  Chamfering;
Creates an angled or bevelled edge by removing material from a corner.
Applications:
- Bolt and shaft ends.
- Assembly lead-ins.
- Edge finishing.
- Removing sharp corners.
  Shelling;
Removes internal material from a solid while maintaining a specified wall thickness.
Applications:
- Enclosures.
- Containers.
- Plastic housings.
- Lightweight components.
  Boolean operations'
Combines or modifies solid objects using set operations.
- Union: Combines two or more solids.
- Difference: Subtracts one solid from another.
- Intersection: Retains only the common volume.
If A and B represent two solid volumes:
Union: A ∪ B
Difference: A − B
Intersection: A ∩ B
  Patterning;
Repeats a feature or component according to a defined arrangement.
Types:
- Linear pattern.
- Circular pattern.
- Mirror pattern.
- Curve-driven pattern.
Applications include bolt holes, gear teeth, cooling fins, and repeated mounting features.

 TRANSFORMATIONS IN 3D MODELLING
Transformations change an object's position, orientation, or size.
  Translation;
Moves an object without changing its orientation or dimensions.
x' = x + Tx
y' = y + Ty
z' = z + Tz
  Scaling;
Changes the size of an object.
x' = Sx × x
y' = Sy × y
z' = Sz × z
Uniform scaling uses:
Sx = Sy = Sz
  Rotation;
Rotates an object around an axis.
For rotation about the Z-axis:
x' = x cosθ − y sinθ
y' = x sinθ + y cosθ
z' = z
Where θ is the rotation angle.
  Homogeneous transformation matrices;
A 3D transformation can be represented using a 4 × 4 matrix:
    P' = TP
Where:
T = [ R  t ]
[ 0  1 ]
R represents the 3 × 3 rotation matrix, while t represents the translation vector.
Homogeneous transformations are especially important in robotics, CAD, computer graphics, and assembly positioning.

 PARAMETRIC AND FEATURE-BASED MODELLING
Parametric modelling uses dimensions, constraints, and mathematical relationships to control geometry.
  Important concepts;
Parameters: Variables that control model dimensions or properties.
Examples:
- Shaft diameter.
- Hole spacing.
- Wall thickness.
- Extrusion length.
Constraints: Define geometric relationships between sketch elements.
Features: Individual modelling operations such as extrusion, fillet, hole, and chamfer.
Feature history: Records the sequence of operations used to construct the model.
Design intent: Describes how the model should behave when dimensions or design requirements change.
Example
A shaft model may use:
- Diameter = 20 mm.
- Length = 100 mm.
- Chamfer = 2 mm.
- Material = Steel.
Changing the shaft diameter updates the dependent model geometry according to its constraints and feature relationships.

 ASSEMBLY MODELLING
Assembly modelling combines multiple 3D components into a functional mechanical system.
  Important concepts;
Components: Individual parts forming an assembly.
Mates or constraints: Define relationships between components.
Common assembly relationships:
- Coincident.
- Concentric.
- Parallel.
- Perpendicular.
- Distance.
- Angle.
- Tangent.
- Gear relationship.
  Degrees of freedom (DOF);
A free rigid body in 3D space has six degrees of freedom:
- Three translational: X, Y, Z.
- Three rotational: Rotation about X, Y, Z.
Assembly constraints restrict these degrees of freedom to produce the required motion or fixed position.
Assembly drawings and representations
- Exploded views show separated components and their assembly order.
- Sectional views reveal internal arrangements.
- Bills of materials (BOM) list components and quantities.
- Motion studies demonstrate component movement and interaction.
Applications include gearboxes, engines, robotic arms, pumps, and manufacturing machines.

 3D MODELLING AND ENGINEERING ANALYSIS
3D models provide geometry for several engineering analysis processes.
  Mass properties;
For a uniform-density solid:
Mass = Density × Volume
    m = ρV
Where:
- m = mass (kg).
- ρ = density (kg/m³).
- V = volume (m³).
  Centre of mass;
For discrete components:
x̄ = Σ(mᵢxᵢ)/Σmᵢ
ȳ = Σ(mᵢyᵢ)/Σmᵢ
z̄ = Σ(mᵢzᵢ)/Σmᵢ
The centre of mass is important in balancing, stability, and mechanical design.
  Moment of inertia;
For a system of discrete point masses about an axis:
    I = Σmᵢrᵢ²
Where rᵢ is the perpendicular distance from each mass to the axis.
For a solid cylinder about its central longitudinal axis:
    I = ½mr²
Moment of inertia is important in rotational dynamics and mechanical system design.
  Finite Element Analysis (FEA);
FEA divides a model into smaller elements connected at nodes to approximate its structural or physical behaviour.
Applications:
- Stress analysis.
- Deformation analysis.
- Thermal analysis.
- Vibration analysis.
- Buckling analysis.
Basic linear elastic relationship:
    σ = Eε
Where:
- σ = normal stress (Pa).
- E = Young's modulus (Pa).
- ε = normal strain (dimensionless).
For axial loading:
    σ = F/A
    ε = ΔL/L
FEA results depend on appropriate material properties, boundary conditions, loading, mesh quality, and model assumptions.
  Computational Fluid Dynamics (CFD);
CFD uses numerical methods to study fluid flow and heat transfer around or through 3D geometries.
Applications:
- Aerodynamics.
- Cooling systems.
- Pipe and duct flow.
- Turbomachinery.
- Thermal management.

 3D MODELLING FOR MANUFACTURING
A 3D model can be converted into manufacturing instructions.
  Computer-Aided Manufacturing (CAM);
CAM uses digital models and manufacturing data to plan and generate production operations.
Examples:
- CNC milling.
- CNC turning.
- Drilling.
- Toolpath generation.
- Laser cutting.
  Additive manufacturing (3D printing);
Creates physical objects by adding material layer by layer.
Common technologies:
- FDM/FFF: Fused filament deposition.
- SLA: Stereolithography.
- SLS: Selective laser sintering.
- Metal powder-bed fusion processes.
Important design considerations:
- Wall thickness.
- Support structures.
- Build orientation.
- Overhangs.
- Dimensional tolerances.
- Material selection.
- Shrinkage and warping.
  Subtractive manufacturing;
Removes material from a solid workpiece using cutting tools.
Examples:
- CNC milling.
- Turning.
- Grinding.
- Drilling.
Designs should consider tool access, machining allowances, workholding, and achievable tolerances.

 CAD SOFTWARE AND TOOLS
Common engineering 3D modelling software includes:
- SolidWorks: Mechanical part modelling, assemblies, and engineering drawings.
- Autodesk Fusion: 3D CAD, CAM, simulation, and product design.
- Autodesk Inventor: Mechanical design and assembly modelling.
- AutoCAD: Primarily 2D drafting, with 3D modelling capabilities.
- FreeCAD: Open-source parametric 3D CAD.
- CATIA: Complex product and surface design, especially aerospace and automotive.
- Siemens NX: Advanced product engineering, CAD, CAM, and CAE.
- Blender: Polygonal modelling, visualization, animation, and rendering; not primarily a parametric mechanical CAD system.
  Common file formats;
Format| Main purpose
STEP (.step/.stp)| 3D CAD model exchange
IGES (.iges/.igs)| CAD surface and geometry exchange
STL (.stl)| 3D printing mesh
OBJ (.obj)| Polygonal mesh and visual assets
3MF (.3mf)| 3D printing model exchange
DWG (.dwg)| CAD drawing and design data
DXF (.dxf)| 2D drawing exchange
Native CAD format| Editable model and feature history
Important: Exporting to a mesh format such as STL generally loses the original parametric feature history.

 3D MODELLING WORKFLOW
A typical engineering modelling process follows these steps:
1. Identify design requirements: Determine the object's function, dimensions, material, and operating conditions.
2. Create initial sketches: Draw the basic 2D profiles.
3. Apply constraints: Define geometric relationships and dimensions.
4. Generate 3D geometry: Use extrusion, revolution, sweep, and loft.
5. Add details: Create holes, fillets, chamfers, threads, and patterns.
6. Apply materials: Define material properties and appearance.
7. Create assemblies: Combine individual components and apply constraints.
8. Validate the design: Check dimensions, interference, mass properties, and manufacturability.
9. Perform engineering analysis: Conduct FEA, CFD, or motion analysis where necessary.
10. Generate technical drawings: Produce orthographic, sectional, and isometric views.
11. Export manufacturing files: Prepare suitable CAD, CAM, or 3D printing formats.
12. Revise and document: Save revisions and maintain design records.

 COMMON MODELLING ERRORS AND GOOD PRACTICES
  Common errors;
- Incorrect dimensions or units.
- Poorly constrained sketches.
- Overcomplicated feature histories.
- Self-intersecting or invalid geometry.
- Incorrect surface orientation.
- Unintended gaps in solid models.
- Interference between assembly components.
- Ignoring manufacturing limitations.
- Using inappropriate mesh resolution.
- Applying unrealistic simulation boundary conditions.
  Good practices;
1. Start with simple geometry and progressively add details.
2. Use fully constrained sketches where practical.
3. Use meaningful feature and component names.
4. Apply design parameters rather than arbitrary dimensions.
5. Maintain consistent units.
6. Use symmetry and patterns to reduce repetitive work.
7. Keep models organized and editable.
8. Check interference and clearances in assemblies.
9. Design according to manufacturing processes.
10. Save regular revisions and maintain backups.
11. Validate the final model before manufacturing.

 IMPORTANT FORMULAS SUMMARY
3D distance:
    d = √[(x₂−x₁)² + (y₂−y₁)² + (z₂−z₁)²]
Vector magnitude:
    |A| = √(Ax² + Ay² + Az²)
Cube volume:
    V = a³
Cuboid volume:
    V = lwh
Cylinder volume:
    V = πr²h
Cone volume:
    V = ⅓πr²h
Sphere volume:
    V = ⁴⁄₃πr³
Mass:
    m = ρV
Normal stress:  
    σ = F/A
Normal strain:
    ε = ΔL/L
Young's modulus:
    E = σ/ε
Rotational moment of inertia:
    I = Σmᵢrᵢ²
Solid cylinder moment of inertia about its longitudinal axis:
    I = ½mr²
Final principle: 
Effective 3D modelling combines geometric accuracy, design intent, engineering principles, material properties, and manufacturing requirements to create models that are not only visually correct but also functional, analyzable, and manufacturable.
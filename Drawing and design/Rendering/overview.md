Rendering is the process of generating a 2D image or animation from 3D or 2D scene data (such as geometry, lighting, materials, and camera settings) using computer software.

Overview & Core Concepts;
• What it does: Bridges the gap between raw mathematical 3D models and the visual pixels displayed on a screen.
• Inputs required: Geometry/meshes, textures and material properties, light sources, and a virtual camera.
• Real-time vs. Offline/Pre-rendering:
	• Real-time rendering: Generates 30 to 120+ frames per second, used in video games and interactive AR/VR where immediate feedback is required.
	• Offline (Pre-rendering): Takes minutes to days per frame, used in film VFX and high-end visualization to calculate strict physical light accuracy.

Key Techniques & Algorithms;
• Rasterization: Projects 3D triangles onto a 2D screen and uses a Z-buffer to track depth; extremely fast, making it standard for games, though shadows and reflections are often approximated.
• Ray Tracing / Path Tracing: Simulates the physical behavior of light rays bouncing off surfaces to compute true reflections, refractions, global illumination, and soft shadows.
• Rasterization + Ray Tracing (Hybrid): Combines fast rasterization for base scenes with ray-traced effects (like RT reflections or DLSS upscaling) for balanced performance and realism.
• Gaussian Splatting: Represents real-world 3D spaces using millions of small 3D Gaussians derived from photos to render high-framerate, photorealistic environments.
• Hardware Support: Accelerated via GPUs using parallel thread processing and dedicated ray-tracing cores, or offloaded to cloud-based render farms.
For a deep dive into pipeline stages, you can explore the Scratchapixel Rendering Overview.

Main Applications;
• Video Games & Interactive Media: Delivers high-speed real-time graphics and environments.
• Film & Visual Effects (VFX): Creates photorealistic CGI creatures, explosions, and digital stunt doubles.
• Architectural Visualization (ArchViz): Lets architects preview building exteriors, lighting conditions, and interior walkthroughs before construction begins.
• Product Design & E-Commerce: Replaces physical photography with digital twins, cutting prototyping costs and boosting online conversion rates.
• Augmented & Virtual Reality (AR/VR): Drives synchronized visual, spatial audio, and haptic signals to display gear.
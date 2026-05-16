### **Tier 1: NORMAL (Rasterized Graphics)**
*Focus: Speed and "Fake" Realism. Good for general gameplay.*
* **Shadow Maps:** Pre-calculated shadows that can look "blocky" or "jaggy" at low resolutions.
* **SSAO (Screen Space Ambient Occlusion):** Fakes contact shadows only for what is visible on your screen.
* **Dynamic Lighting (Vanilla-style):** Light updates in "chunks" or steps, not smooth gradients.
* **Basic Water:** Simple reflections (SSR) and a scrolling texture.
* **Standard Tone Mapping:** Basic brightness and contrast adjustments.
* **[PLUS] Volumetric Fog:** Simple "God Rays" that react to the sun's position.
* **[PLUS] Flat Puddles:** A simple "wetness" overlay that increases reflectivity on blocks.
* **[PLUS] Sprite Clouds:** 2D cloud layers that rotate with the sky.
* **[PLUS] Particle Smoke:** Standard Minecraft particles that don't cast shadows or react to light.

---

### **Tier 2: RAYTRACING (Hybrid Engine)**
*Focus: Physical accuracy for shadows and reflections. The "Pro" look.*
* **Ray-Traced Shadows:** Pixel-perfect shadows that eliminate "shadow acne" and "peter panning."
* **SSR (Screen Space Reflections):** Advanced reflections that handle mirrors and glossy blocks.
* **Point-Light Calculation:** Individual lights (like torches) act as single points in space.
* **Caustics:** Basic light patterns through water.
* **[PLUS] Variable Penumbra:** Shadows that are sharp near the base and get slightly softer far away.
* **[PLUS] PBR Support:** Full "Physical Based Rendering" (materials look like real metal, rock, or plastic).
* **[PLUS] Real-Time Puddles:** Uses a "noise" map to create varied wetness (some areas dry, some soaked) with ray-traced reflections.
* **[PLUS] Volumetric Haze (Basic):** A uniform "fog" that gets thicker in the distance and glows when the sun hits it.
* **[PLUS] Screen-Space Water Interaction:** Water ripples slightly when a player or entity moves through it (fake physics).
* **[PLUS] 2D Volumetric Clouds:** Clouds that have "thickness" but are still rendered on a flat plane.

---

### **Tier 3: PATHTRACING (The PTX Hyperrealist Engine)**
*Focus: Infinite light bounces and spectral physics. This is your "Huge" vision.*
* **PTGI (Path Traced Global Illumination):** Light bounces off walls to light up dark rooms (Indirect lighting).
* **Voxel-Based Tracer:** The engine "sees" every block as a physical object for 100% accurate light blocking.
* **[PLUS] Surface-Based Emission:** Light comes from the **faces** of the block, creating sharp 90-degree light-cuts.
* **[PLUS] Spectral Dispersion:** Light splits into a "rainbow fringe" (chromatic aberration) on high-contrast edges.
* **[PLUS] Mathematical Sharp Shadows:** Forced `0.0` radius light sources for razor-sharp, cinematic shadows.
* **[PLUS] Inverse Square Law Falloff:** Physically accurate $1/d^2$ dimming for every light source.
* **Spatio-Temporal Denoising:** High-end cleaning of "noisy" pixels to keep the image smooth during movement.
* **[PLUS] Particle-to-Volumetric Haze:** Particles (like campfire smoke or torch steam) physically blend into the volumetric haze (Participating Medium).
* **[PLUS] 3D Ray-Marched Volumetric Clouds:** Clouds with actual "volume" that cast shadows on the ground and themselves.
* **[PLUS] Insane Water Interaction:** 
    * **Refractive Caustics:** Light passing through water surface creates dancing patterns based on PTX rays.
    * **Physical Displacement:** High-quality waves that change the water geometry.
* **[PLUS] Dynamic Puddles & Ripples:** Puddles that accumulate over time. sharp reflections of light sources.
* **[NEW] oe Data Bridge Integration**: Real-time SSBO attribute fetching for data-driven materials.
* **[NEW] Spectral Transparency**: Light blending through tinted glass (Red + Blue = Purple).
* **[NEW] Selective Texel Emission**: Lights emit color based on individual block texture pixels.
* **[NEW] Fail-Safe Stability**: Automatic defaults for undefined block data or sliders.

---

### **Bonus "Expansion" Features (The "Insane" Detail)**
* **[ADD] Spectral Water Refraction:** Light through water bends RGB at different angles for an underwater rainbow.
* **[ADD] Subsurface Scattering:** Makes leaves and skin look "warm" when light shines through from behind.
* **[ADD] Micro-Detail Shadows:** Shadows cast by tiny bumps in a texture (high-res PBR).
* **[ADD] The "Backrooms" Flashlight:** Handheld point-light with the spectral beam.
* **[ADD] Spectral Rainbow Puddles:** Puddle reflections showing spectral dispersion math.
* **[ADD] Localized Haze:** Fog that gathers in low-lying areas (valleys/caves).
* **[ADD] Dimension Customization:** Advanced variables for sky colors, d_gravity_visual, and solar irradiance.
* **[ADD] Atmospheric/Cloud Detail**: Ozone density and Mie/Rayleigh scattering strength controls.

---

# Variable Documentation
$\color{gray}{\text{(For the full list of shader uniforms and GUI options, refer to Settings.glsl and shaders.properties)}}$    


echo "# OSMIUM" >> README.md
git init
git add README.md
git commit -m "LICENSE and README"
git branch -M main
git remote add origin https://github.com/nowyback/OSMIUM.git
git push -u origin main
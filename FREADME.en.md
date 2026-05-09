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
* **[NEW] AVE Data Bridge Integration**: Real-time SSBO attribute fetching for data-driven materials.
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

### **VARIABLE DEFINITIONS**

**1. HAZE (World, Biome, Custom, and Particles)**
* **h_baseworld (bool):** Enables global world haze.
* **hbw_density (0-255):** Particle count per unit.
* **hbw_densityvariation (0-255):** Range of density fluctuation.
* **hbw_densityvariationrange (0-255):** Speed of density change per minute.
* **hbw_color (hex):** Hexcode or comma-separated list for color probability.
* **hbw_type (0-9):** Type selection (Fog, Steam, Smoke, Dust, Vapor, Mist, Ash, Haze, Custom).
* **hbw_lightabsorbtion (0-15):** Light quantity absorbed by medium.
* **hbw_lightscattering (0-15):** Light quantity scattered by medium.
* **hbw_heightfalloff (0-15):** Rate of descent (0.1 blocks/sec).
* **hbw_windspeed (0-255):** Wind influence speed (0.05 blocks/sec).
* **hbw_winddirection (0-360):** Wind heading in degrees.
* **hbw_anisotropy (-1 to 1):** Scattering direction (-1: back, 1: forward).
* **hbw_noisescale / hbw_noisedetail:** Noise frequency and octave count.
* **hbw_groundfog (bool):** Toggle for altitude confinement.
* **hbw_groundheight (0-255):** Max altitude for ground fog layer.
* **h_particlestohaze (bool):** Toggle for auto-rendering particles as volumetric haze.

**2. LIGHT LOGIC**
* **l_color (hex):** Primary light color.
* **lc_variation (hex):** Secondary/variation color.
* **lc_variationamount (0-255):** Speed of color shift per minute.
* **l_flicker (bool):** Enables light frequency oscillation.
* **lf_rate / lf_intensity:** Frequency and strength of flickering.
* **l_absorbtion (0-15):** Blocks light transmission (0: transparent, 15: opaque).
* **l_reflection (0-15):** Ratio of reflected vs. transmitted light.
* **l_reflectionblur (0-15):** Roughness/blur of the reflected light.
* **l_scattering (bool):** Enables light dispersion angle.
* **l_chromaticabberation (bool):** Enables spectral splitting.
* **lc_strength (0-7):** Strength of aberration (3 is base).
* **lc_index (0-15):** Refractive index offset for dispersion.
* **l_godrays (bool):** Enables volumetric light shafts.
* **l_falloff_global / l_falloff_world (0-63):** Inverse Square Falloff intensity.

**3. PUDDLES**
* **p_isdirt (bool):** Applies muddy/dirty texture filter.
* **p_depth (0-15):** Determines ripple intensity and splash scale.

**4. WATER & FLUIDS**
* **w_visibility (0-255):** Biome-based underwater sight distance.
* **w_murkiness (0-255):** Density of particles in liquid.
* **w_refractionindex (0-15):** View-bending strength underwater.
* **w_wave_height / w_wave_speed:** Physical displacement of the water surface.
* **w_viscosity (0-15):** Affects ripple speed and physics interaction.
* **w_dispersion (0-15):** Spectral dispersion of underwater light.
* **w_caustics_intensity (0-255):** Bottom-surface light focusing strength.

**5. ENVIRONMENT & ATMOSPHERE**
* **d_sky_color / d_horizon_color (hex):** Skybox gradients.
* **d_ambient_light (0-255):** Minimum "darkness" floor.
* **d_solar_irradiance (0-255):** Bounce-power of sunlight.
* **a_ozone_density (0-255):** UV/Blue light absorption.
* **a_rayleigh_strength (0-255):** Sky blue intensity (small molecule scattering).
* **a_mie_phase (-1 to 1):** Scattering phase for dust/haze.


## NEW TO IMPLEMENT AND SORT:
* **r_radioactive:** If a block should emmit radiation
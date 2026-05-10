# Variables

-----------------------------------------------------------------------------------------------------
## Haze

- `HAZE_BASEWORLD`=**bool** [$\color{lightblue}{\text{--world}}$]
    - --> $\color{gray}{\text{Enables base haze in a world}}$
    - `HAZE_BASEWORLD_DENSITY`=**0 to 255** [$\color{lightblue}{\text{--world}}$]
        - --> $\color{gray}{\text{Ammount of particles per unit}}$
        - `HAZE_BASEWORLD_DENSITY_VARIATION`=**0 to 255** [$\color{lightblue}{\text{--world}}$]
            - --> $\color{gray}{\text{Range of how much the density can change from the original ammount}}$
            - `HAZE_BASEWORLD_DENSITY_VARIATION_RANGE`=**0 to 255** [$\color{lightblue}{\text{--world}}$]
                - -> $\color{gray}{\text{How much the density can change in a single minute}}$
    - `HAZE_BASEWORLD_COLOR`=**hexcode** [$\color{lightblue}{\text{--world}}$]
        - $\color{gray}{\text{Color of the haze. If you want multiple colors, seperate them by a comma like this: dbc1c1ff,f0f0f0,000000. To increase the chance of a color, type it multiple times.}}$
    - `HAZE_BASEWORLD_TYPE`=**0 to 255**
        ```- 0 = none
        - 1 = fog
        - 2 = steam
        - 3 = smoke
        - 4 = dust
        - 5 = vapor
        - 6 = mist
        - 7 = ash
        - 8 = haze
        - 9+ = custom
    - `HAZE_BASEWORLD_LIGHT_ABsorption`=**0 to 15** (The ammount of light that gets absorbed by the haze) [$\color{lightblue}{\text{--world}}$]
    - `HAZE_BASEWORLD_LIGHT_SCATTERING`=**0 to 15** (The ammount of light that gets scattered by the haze) [$\color{lightblue}{\text{--world}}$]
    - `HAZE_BASEWORLD_HEIGHT_FALLOFF`=**0 to 15** [$\color{lightblue}{\text{--world}}$]
        - $\color{gray}{\text{How fast the haze falls, in 0.1 blocks per second}}$
    - `HAZE_BASEWORLD_WIND_SPEED`=**0 to 255** [$\color{lightblue}{\text{--world}}$]
        - $\color{gray}{\text{How fast the wind affects the haze, in 0.05 blocks per second, 0 disables this}}$
    - `HAZE_BASEWORLD_WIND_DIRECTION`=**0 to 360** [$\color{lightblue}{\text{--world}}$]
        - $\color{gray}{\text{The direction of the wind in degrees}}$
    - `HAZE_BASEWORLD_ANISOTROPY`=**-1 to 1** [$\color{lightblue}{\text{--world}}$]
        - $\color{gray}{\text{Where the light scatters, -1 = back, 1 = forward, suggested 0}}$
    - `HAZE_BASEWORLD_NOISE_SCALE`=**0 to 255** [$\color{lightblue}{\text{--world}}$]
    - `HAZE_BASEWORLD_DISTANCE_FALLOFF`=**0 to 255** [$\color{lightblue}{\text{--world}}$]
    - `HAZE_BASEWORLD_LAYER_PRIORITY`=**0-255** [$\color{lightblue}{\text{--world}}$]
        - $\color{gray}{\text{Z-order when multiple custom haze layers overlap. Higher = rendered on top}}$
---
<br>

- `HAZE_BASEBIOME`=**bool** [$\color{lightblue}{\text{--biome}}$]
    - $\color{gray}{\text{Enables base haze in a biome}}$
    - `HAZE_BASEBIOME_DENSITY`=**0 to 255** [$\color{lightblue}{\text{--biome}}$]
        - $\color{gray}{\text{Particles per Qubic messurement}}$
        - `HAZE_BASEBIOME_DENSITYVARIATION`=**0 to 255** [$\color{lightblue}{\text{--biome}}$]
            - $\color{gray}{\text{+- how many particles more or less}}$
        - `HAZE_BASEBIOME_DENSITYVARIATIONRANGE`=**0 to 255** [$\color{lightblue}{\text{--biome}}$]
            - $\color{gray}{\text{By how much it can change in a single minute}}$
    - `HAZE_BASEBIOME_COLOR`=**hexcode** [$\color{lightblue}{\text{--biome}}$]
        - $\color{gray}{\text{Color of the haze. If you want multiple colors, seperate them by a comma like this: dbc1c1ff,f0f0f0,000000. To increase the chance of a color, type it multiple times.}}$
    - `HAZE_BASEBIOME_TYPE`=**0 to 255**
        ```- 0 = none
        - 1 = fog
        - 2 = steam
        - 3 = smoke
        - 4 = dust
        - 5 = vapor
        - 6 = mist
        - 7 = ash
        - 8 = haze
        - 9+ = custom```
    - `HAZE_BASEBIOME_LIGHT_ABORPTION`=**0 to 15** (The ammount of light that gets absorbed by the haze) [$\color{lightblue}{\text{--block}}$]
    - `HAZE_BASEBIOME_LIGHT_SCATTERING`=**0 to 15** (The ammount of light that gets scattered by the haze) [$\color{lightblue}{\text{--block}}$]
    - `HAZE_BASEBIOME_HEIGHT_FALLOFF`=**0 to 15** [$\color{lightblue}{\text{--biome}}$]
        - $\color{gray}{\text{How fast the haze falls, in 0.1 blocks per second}}$
    - `HAZE_BASEBIOME_WIND_SPEED`=**0 to 255** [$\color{lightblue}{\text{--biome}}$]
        - $\color{gray}{\text{How fast the wind affects the haze, in 0.05 blocks per second, 0 disables this}}$
    - `HAZE_BASEBIOME_WIND_DIRECTION`=**0 to 360** [$\color{lightblue}{\text{--biome}}$]
        - $\color{gray}{\text{The direction of the wind in degrees}}$
    - `HAZE_BASEBIOME_ANISOTROPY`=**-1 to 1** [$\color{lightblue}{\text{--biome}}$]
        - $\color{gray}{\text{Where the light scatters, -1 = back, 1 = forward, suggested 0}}$
    - `HAZE_BASEBIOME_NOISE_SCALE`=**0 to 255** [$\color{lightblue}{\text{--biome}}$]
    - `HAZE_BASEBIOME_DISTANCE_FALLOFF`=**0 to 255** [$\color{lightblue}{\text{--biome}}$]
    - `HAZE_BIOME_BLEND_MODE`=**0-63** [$\color{lightblue}{\text{--biome}}$]
        - $\color{gray}{\text{Radius in blocks over which haze blends at biome borders}}$
    - `HAZE_BIOME_BLEND_MODE`=**0-3** [$\color{lightblue}{\text{--biome}}$]
        - 0=linear 1=cubic 2=nearest 3=custom
    - `HAZE_BIOME_LAYER_PRIORITY`=**0-255** [$\color{lightblue}{\text{--biome}}$]
        - $\color{gray}{\text{Z-order when multiple custom haze layers overlap. Higher = rendered on top}}$
---
<br>

- `HAZE_CUSTOM`=**bool [$\color{lightblue}{\text{--block}}$]
    - $\color{gray}{\text{Enables custom haze in a biome}}$
    - `HAZE_CUSTOM_DENSITY`=**0 to 255** [$\color{lightblue}{\text{--block}}$]
        - $\color{gray}{\text{Particles per Qubic messurement}}$
        - `HAZE_CUSTOM_DENSITY_VARIATION`=**0 to 255** [$\color{lightblue}{\text{--block}}$]
            - $\color{gray}{\text{+- how many particles more or less}}$
        - `HAZE_CUSTOM_DENSITY_VARIATION_RANGE`=**0 to 255** [$\color{lightblue}{\text{--block}}$]
            - $\color{gray}{\text{By how much it can change in a single minute}}$
    - `HAZE_CUSTOM_COLOR`=**hexcode** [$\color{lightblue}{\text{--block}}$]
        - $\color{gray}{\text{Color of the haze. If you want multiple colors, seperate them by a comma like this: dbc1c1ff,f0f0f0,000000. To increase the chance of a color, type it multiple times.}}$
    - `HAZE_CUSTOM_TYPE`=**0 to 255**
        - 0 = none
        - 1 = fog
        - 2 = steam
        - 3 = smoke
        - 4 = dust
        - 5 = vapor
        - 6 = mist
        - 7 = ash
        - 8 = haze
        - 9+ = custom
    - `HAZE_CUSTOM_LIGHT_ABSORPTION` = **0 to 15** (The ammount of light that gets absorbed by the haze) [$\color{lightblue}{\text{--block}}$]
    - `HAZE_CUSTOM_LIGHT_SCATTERING` = **0 to 15** (The ammount of light that gets scattered by the haze) [$\color{lightblue}{\text{--block}}$]
    - `HAZE_CUSTOM_HEIGHT_FALLOFF` = **0 to 15** [$\color{lightblue}{\text{--block}}$]
        - $\color{gray}{\text{How fast the haze falls, in 0.1 blocks per second}}$
    - `HAZE_CUSTOM_WIND_SPEED`=**0 to 255** [$\color{lightblue}{\text{--block}}$]
        - $\color{gray}{\text{How fast the wind affects the haze, in 0.05 blocks per second, 0 disables this}}$
    - `HAZE_CUSTOM_WIND_DIRECTION`=**0 to 360** [$\color{lightblue}{\text{--block}}$]
        - $\color{gray}{\text{The direction of the wind in degrees}}$
    - `HAZE_CUSTOM_ANISOTROPY`=**-1 to 1** [$\color{lightblue}{\text{--block}}$]
        - $\color{gray}{\text{Where the light scatters, -1 = back, 1 = forward, suggested 0}}$
    - `HAZE_CUSTOM_NOISE_SCALE`=**0 to 255** [$\color{lightblue}{\text{--block}}$]
    - `HAZE_CUSTOM_DISTANCE_FALLOFF`=**0 to 255** [$\color{lightblue}{\text{--block}}$]
    - `HAZE_CUSTOM_BLEND_MODE`=**0-3** [$\color{lightblue}{\text{--block}}$]
        - $\color{gray}{\text{0=linear 1=cubic 2=nearest 3=custom}}$
    - `HAZE_CUSTOM_LAYER_PRIORITY`=**0-255** [$\color{lightblue}{\text{--block}}$]
        - $\color{gray}{\text{Z-order when multiple custom haze layers overlap. Higher = rendered on top}}$
---
<br>

- `HAZE_PARTICLES_TO_HAZE`=**bool** [$\color{lightblue}{\text{--block}}$]
    - --> $\color{gray}{\text{Automatically renders particles as a haze}}$
    - `HAZE_PARTICLE_TYPE`=**0 to 255**
    - `HAZE_VARIATION_AMOUNT`**0 to 255  (by how much it can change in a single minute) [$\color{lightblue}{\text{--block}}$]
---
<br>

## Light Handeling
- `LIGHT_ABSORBION`=**0 to 15** (reduces the lightlevel by the value given in this var) [$\color{lightblue}{\text{--block}}$]
    - $\color{gray}{\text{0 = all light passes through, 15 = absorbs all light}}$
- `LIGHT_REFLECTION`=**0 to 15** (how much light of the lightlevel should reflect, the rest will be passed through the block) [$\color{lightblue}{\text{--block}}$]
    - $\color{gray}{\text{0 = all light passes through, 15 = max reflection}}$
- `LIGHT_REFLECTIONBLUR`=**0 to 15** (how much the light blurrs)
- `LIGHT_SCATTERING`=**bool** [$\color{lightblue}{\text{--block}}$]
    - `LIGHT_SCATTERING_VARIATION`=**0 to 255** (how much the light scatters)
        - $\color{gray}{\text{in 0.1 degrees}}$
- `LIGHT_CHROMATICABBERATION`=**bool**    [$\color{lightblue}{\text{--block}}$]
    - `LIGHT_CHROMATICABBERATION_STRENGTH`=**0 to 7**   (how much the light abberates)
        - $\color{gray}{\text{0 = none, 7 = changes to the total color of a pixel, base value = 3 }}$
- `LIGHT_FALLOFF_GLOBAL`=**0 to 63** (slow light falloff with the Inverse Square Falloff) [$\color{lightblue}{\text{--block}}$]
- `LIGHT_FALLOFF_WORLD`=**0 to 63**  (slow light falloff with the Inverse Square Falloff) [$\color{lightblue}{\text{--world}}$]
    - $I(d) = \frac{1}{1 + d + d^2}$ -> $\color{gray}{\text{Smooth light falloff with the Inverse Square Falloff}}$
- `LIGHT_FLICKER`=**bool**    [$\color{lightblue}{\text{--block}}$]
    - `LIGHT_FLICKER_RATE`=**0 to 63** [$\color{lightblue}{\text{--block}}$]
        - $\color{gray}{\text{the frequency of the flicker in 10ms}}$
    - `LIGHT_FLICKER_RATE_VARIATION`=**0 to 63** [$\color{lightblue}{\text{--block}}$]
        - $\color{gray}{\text{how much the frequenzy changes in 10ms}}$
    - `LIGHT_FLICKER_INTENSITY`=**0 to 15** [$\color{lightblue}{\text{--block}}$]
        - $\color{gray}{\text{the intensity of the flicker, in lightlevels}}$
    - `LIGHT_FLICKER_INTENSITY_VARIATION`=**0 to 63** [$\color{lightblue}{\text{--block}}$]
        - $\color{gray}{\text{how much the intensity can vary in 10ms}}$
- `LIGHT_EMMISSION`=**bool** [$\color{lightblue}{\text{--block}}$]
    - `LIGHT_EMMISION_COLOR`=**hexcode** [$\color{lightblue}{\text{--block}}$]
    - `LIGHT_EMISSION_RANGE_OVERRIDE`=**0 to 63** [$\color{lightblue}{\text{--block}}$]
        - $\color{gray}{\text{If set to a value above 0, the light will override the range of the light}}$
    - `LIGHT_EMMISION_TYPE`=**0-3**
        - $\color{gray}{\text{0 = Point Light / Laser, 1 = Flashlight [CONE], 2 = Surround Illumination, 3 = Custom}}$
        - `LIGHT_EMMISION_ANGLE=`***0-360,0-360,0-360**
            - $\color{gray}{\text{The angle of the light in degrees, first value is the X-Axis angle, second is the Y-Axis angle, third is the Z-Axis angle}}$
        - `LIGHT_EMMISION_SOFTNESS`=**0-63**
            - $\color{gray}{\text{The softness of the light, 0 = hard edge, 63 = very soft edge}}$
    - `LIGHT_TEXEL_MODE`=**bool**
        - $\color{gray}{\text{If true, the light will be rendered as a texel, if false, it will be rendered as a central point}}$
        - `LIGHT_TEXEL_BLENDING`=**0 to 15**
            - $\color{gray}{\text{How much the texels blend with each other}}$
- `LIGHT_EMISSION_COLOR`=**hex** [$\color{lightblue}{\text{--block}}$] - Tints the emitted light of a block
- `LIGHT_EMISSION_SPECTRUM`=**0–7** [$\color{lightblue}{\text{--block}}$] - 0=white 1=warm 2=cool 3=fire 4=neon 5=magic 6=moon 7=custom
- `LIGHT_EMISSION_RANGE`=**0–63** [$\color{lightblue}{\text{--block}}$] - Override emission range in blocks
- `LIGHT_CONE_ANGLE`=**0–180** [$\color{lightblue}{\text{--block}}$] - Spotlight cone angle in degrees (0=point light, 180=sphere)
- `LIGHT_CONE_SOFTNESS`=**0–15** [$\color{lightblue}{\text{--block}}$] - Edge softness of spotlight cone
- `LIGHT_SUBSURFACE_SCATTERING`=**bool** [$\color{lightblue}{\text{--block}}$] - Enables SSS for semi-translucent blocks (leaves, ice)
- `LIGHT_SUBSURFACE_RADIUS`=**0–15** [$\color{lightblue}{\text{--block}}$] - SSS scatter radius in 0.1 block steps
- `LIGHT_SUBSURFACE_COLOR`=**hex** [$\color{lightblue}{\text{--block}}$] - Colour tint of subsurface scattered light

<details>
<summary></b>Light Falloff Table</b></summary>

    | Float | Distance | Falloff per Block |
    |-------|----------|-------------------|
    | 0     | 0        | inf               |
    | 1     | 1.5      | 10b               |
    | 5     | 7.5      | 2b                |
    | 10    | 15       | 1b                |
    | 15    | 22.5     | 0.5b              |
    | 20    | 30       | 0.25b             |
    | 25    | 37.5     | 0.125b            |
    | 30    | 45       | 0.0625b           |
    | 35    | 52.5     | 0.03125b          |
    | 40    | 60       | 0.015625b         |
    | 45    | 67.5     | 0.0078125b        |
    | 50    | 75       | 0.00390625b       |
    | 55    | 82.5     | 0.001953125b      |
    | 60    | 90       | 0.0009765625b     |
    | 63    | 97.5     | 0.00048828125b    |

</details>

</details>

-----------------------------------------------------------------------------------------------------

## Surface & Material

- `SURF_ROUGHNESS`=**0–15** [$\color{lightblue}{\text{--block}}$] - PBR roughness. 0=mirror 15=fully diffuse 
- `SURF_METALLIC`=**0–15** [$\color{lightblue}{\text{--block}}$] - PBR metallic factor. 0=dielectric 15=conductor 
- `SURF_REFLECTANCE`=**0–15** [$\color{lightblue}{\text{--block}}$] - Base reflectance at normal incidence (F0) 
- `SURF_EMISSIVE`=**0–15** [$\color{lightblue}{\text{--block}}$] - Emissive intensity. Stacks with block light level 
- `SURF_EMISSIVE_COLOR`=**hex** [$\color{lightblue}{\text{--block}}$] - Emissive colour override 
- `SURF_NORMAL_STRENGTH`=**0–15** [$\color{lightblue}{\text{--block}}$] - Intensity of normal/bump map. 0=flat 15=full depth 
- `SURF_PARALLAX`=**bool** [$\color{lightblue}{\text{--block}}$] - Enables parallax occlusion mapping 
- `SURF_PARALLAX_DEPTH`=**0–15** [$\color{lightblue}{\text{--block}}$] - Depth of parallax displacement in 0.05 block steps 
- `SURF_PARALLAX_STEPS`=**1–64** [$\color{lightblue}{\text{--block}}$] - Ray march steps — higher = more accurate but slower 
- `SURF_DISPLACEMENT`=**bool** [$\color{lightblue}{\text{--block}}$] - Enables geometric vertex displacement 
- `SURF_DISPLACEMENT_SCALE`=**0–15** [$\color{lightblue}{\text{--block}}$] - Displacement height in 0.05 block steps 
- `SURF_AO_STRENGTH`=**0–15** [$\color{lightblue}{\text{--block}}$] - Per-block ambient occlusion intensity override 
- `SURF_TRANSLUCENCY`=**0–15** [$\color{lightblue}{\text{--block}}$] - Amount of light transmitted through thin geometry 
- `SURF_WAVING`=**bool** [$\color{lightblue}{\text{--block}}$] - Enables vertex waving (leaves, grass, banners) 
- `SURF_WAVING_AMPLITUDE`=**0–15** [$\color{lightblue}{\text{--block}}$] - Wave height in 0.05 block steps 
- `SURF_WAVING_SPEED`=**0–15** [$\color{lightblue}{\text{--block}}$] - Wave frequency multiplier 
- `SURF_WAVING_WIND_INFLUENCE`=**0–15** [$\color{lightblue}{\text{--block}}$] - How much HAZE_*_WIND_* values affect waving direction 
- `SURF_CUSTOM_SHADER`=**string** [$\color{lightblue}{\text{--block}}$] - Path to a GLSL snippet injected into surface shader for this block type 

-----------------------------------------------------------------------------------------------------

## Puddles
- `PUDDLE_ISDIRTY`=**bool** (applies a dirtier look) [$\color{lightblue}{\text{--block}}$]
- `PUDDLE_DEPTH`=**0 to 15**  (how deep the puddle is, changes the ammount of ripples / splashes) [$\color{lightblue}{\text{--block}}$]
- `p_ripple_rate`=**0–15** [$\color{lightblue}{\text{--local}}$] - Ripple frequency in rain. 0=calm, 15=heavy 
- `p_ripple_strength`=**0–15** [$\color{lightblue}{\text{--local}}$] - Ripple distortion amplitude 
- `p_reflection_strength`=**0–15** [$\color{lightblue}{\text{--local}}$] - Mirror reflectivity of puddle surface 
- `p_evaporation_speed`=**0–15** [$\color{lightblue}{\text{--local}}$] - How fast puddles shrink after rain stops 

-----------------------------------------------------------------------------------------------------

## Fluids
- `FLUID_VISIBILITY`=**0 to 255    (how far you can see through water) [$\color{lightblue}{\text{-biome}}$]
- `FLUID_FALLOFF`=**0 to 63    (slow light falloff with the Inverse Square Falloff, see l_falloff_table) [$\color{lightblue}{\text{--biome}}$]
- `FLUID_MURKINESS`=**0 to 255 (ammount of particles in the water in cubic messurements) [$\color{lightblue}{\text{--biome}}$]
    - `FLUID_MURKINESS_LIGHTSCATTERING`=**0 to 255  (how much the light scatters in the water, in 0.1 degrees) [$\color{lightblue}{\text{--biome}}$]
    - `FLUID_MURKINESS_LIGHTABSORPTION`=**0 to 15   (how much light is absorbed by the murkiness) [$\color{lightblue}{\text{--biome}}$]
    - `FLUID_MURKINESS_COLOR`=**hexcode  (changes the color of the water, use null if default) [$\color{lightblue}{\text{--biome}}$]
- `FLUID_REFRACTIONINDEX`=**0 to 15    (how much the view "bends" when looking underwater) [$\color{lightblue}{\text{--biome}}$]
- `FLUID_WAVE_HEIGHT`=**0 to 15   (how high the waves are, in 0.05 blocks) [$\color{lightblue}{\text{--biome}}$]
- `FLUID_WAVE_SPEED`=**0 to 15   (how fast the waves move in 0.25 blocks per second) [$\color{lightblue}{\text{--biome}}$]
- `FLUID_VISCOSITY`=**0 to 15    (how viscous the water is, changes how you interact with it (waves included)) [$\color{lightblue}{\text{--biome}}$]
- `f_foam_threshold`=**0–15** [$\color{lightblue}{\text{--biome}}$] - Wave height at which foam/whitecap appears ✦ new
- `f_foam_color`=**hex** [$\color{lightblue}{\text{--biome}}$] - Foam colour ✦ new
- `f_caustics_strength`=**0–15** [$\color{lightblue}{\text{--biome}}$] - Intensity of caustic light patterns on underwater surfaces ✦ new
- `f_caustics_scale`=**0–15** [$\color{lightblue}{\text{--biome}}$] - Scale of caustic pattern in 0.1 block steps ✦ new
- `f_depth_color`=**hex** [$\color{lightblue}{\text{--biome}}$] - Colour at maximum depth (for depth-based tinting) ✦ new
- `f_depth_falloff`=**0–15** [$\color{lightblue}{\text{--biome}}$] - Depth over which colour blends to f_depth_color ✦ new
- `f_bioluminescence`=**bool** [$\color{lightblue}{\text{--biome}}$] - Enables glowing particles in fluid ✦ new
- `f_bioluminescence_color`=**hex** [$\color{lightblue}{\text{--biome}}$] - Particle glow colour ✦ new
- `f_bioluminescence_density`=**0–255** [$\color{lightblue}{\text{--biome}}$] - Glowing particle count ✦ new
- `f_custom_shader`=**string** [$\color{lightblue}{\text{--biome}}$] - Path to GLSL snippet injected into fluid surface shader ✦ new

-----------------------------------------------------------------------------------------------------

## Global Illumination

- `g_world`=**0 to 15    (how much global illumination affects the world) [$\color{lightblue}{\text{--global}}$]
    - $\color{gray}{\text{0 = no global illumination, 15 = max global illumination}}$
- `g_biome`=**0 to 15    (how much global illumination affects the biome) [$\color{lightblue}{\text{--global}}$]
    - $\color{gray}{\text{0 = no global illumination, 15 = max global illumination}}$
- `g_color`=**0 to 15    (which color is used for global illumination(leave blank for default overworld)) [$\color{lightblue}{\text{--global}}$]
    - $\color{gray}{\text{0 = default, 1-15 = custom color}}$
- `g_bounce_count`=**1–8** [$\color{lightblue}{\text{--global}}$] - Number of indirect light bounces. Higher = softer, slower 
- `g_sky_contribution`=**0–15** [$\color{lightblue}{\text{--global}}$] - How strongly sky colour bleeds into shadowed areas 
- `g_emissive_contribution`=**0–15** [$\color{lightblue}{\text{--global}}$] - How much emissive blocks contribute to GI 
- `g_resolution`=**0–3** [$\color{lightblue}{\text{--global}}$] - 0=low (fast) 1=medium 2=high 3=per-texel (expensive) 
- `g_temporal_blend`=**0–15** [$\color{lightblue}{\text{--global}}$] - Temporal accumulation frames — reduces noise, increases ghosting 

-----------------------------------------------------------------------------------------------------

## Weather

- `w_weather`=**bool    (enable weather) [$\color{lightblue}{\text{--world}}$]
    - `w_rain`=**bool    (enable rain) [$\color{lightblue}{\text{--world}}$]
        - `w_rain_density`=**0 to 255  (rain density) [$\color{lightblue}{\text{--world}}$]
        - `w_rain_speed`=**0 to 15   (rain speed) [$\color{lightblue}{\text{--world}}$]
    - `w_thunder`=**bool    (enable thunder) [$\color{lightblue}{\text{--world}}$]
        - `w_thunder_frequency`=**0 to 255  (thunder frequency) [$\color{lightblue}{\text{--world}}$]

---
<br>

## Sky Texture
- `STAR_TYPE`=**integer** (type of stars rendered) [$\color{lightblue}{\text{--global}}$]
- `SKY_TEXTURE_BRIGHTNESS`=**float** (brightness of sky textures) [$\color{lightblue}{\text{--global}}$]

-----------------------------------------------------------------------------------------------------

## Shadows
- `SHADOW_MAP_BIAS`=**float** (bias value for shadow mapping) [$\color{lightblue}{\text{--global}}$]
- `SHADOW_BASIC_BLUR`=**float** (basic blur amount for shadows) [$\color{lightblue}{\text{--global}}$]

-----------------------------------------------------------------------------------------------------

## Performance
Modular Performance: Since this is modular, make sure to wrap these features in #ifdef tags. That way, if a modder doesn't use "Haze," your 9070 XT doesn't waste cycles even looking for the variable.
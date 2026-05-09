# User Settings

## Quality Settings

### Rendering Quality
- `GLOBAL_ILLUMINATION_QUALITY`=**integer** (quality level for global illumination) [$\color{lightblue}{\text{--global}}$]
- `GTAO_QUALITY`=**integer** (quality level for GTAO) [$\color{lightblue}{\text{--global}}$]
- `GTAO_SLICE_QUALITY`=**integer** (slice quality for GTAO) [$\color{lightblue}{\text{--global}}$]
- `GTAO_RADIUS_MODE`=**integer** (radius calculation mode) [$\color{lightblue}{\text{--global}}$]
- `SHADOW_MAP_BIAS`=**float** (bias value for shadow mapping) [$\color{lightblue}{\text{--global}}$]
- `VPS_QUALITY`=**integer** (quality of variable penumbra shadows) [$\color{lightblue}{\text{--global}}$]
- `MOTION_BLUR_QUALITY`=**integer** (quality of motion blur) [$\color{lightblue}{\text{--global}}$]

### Texture Quality
- `CAUSTICS_TEX_RESOLUTION`=**integer** (resolution of caustics texture) [$\color{lightblue}{\text{--global}}$]
- `DH_TEXTURE_NOISE_STEPS`=**float** (noise steps for DH textures) [$\color{lightblue}{\text{--global}}$]
- `DH_TEXTURE_NOISE_STRENGTH`=**float** (noise strength for DH textures) [$\color{lightblue}{\text{--global}}$]

### Post-Processing Quality
- `VIGNETTE_FALLOFF`=**float** (falloff of vignette effect) [$\color{lightblue}{\text{--global}}$]
- `CHROMATIC_ABERRATION_STRENGTH`=**float** (strength of chromatic aberration) [$\color{lightblue}{\text{--global}}$]

-----------------------------------------------------------------------------------------------------

## Distance Settings

### Render Distances
- `GI_RADIUS`=**float** (radius of GI effect) [$\color{lightblue}{\text{--global}}$]
- `GI_FALLOFF`=**float** (falloff distance for GI) [$\color{lightblue}{\text{--global}}$]
- `GTAO_WORLD_RADIUS`=**float** (world space radius for GTAO) [$\color{lightblue}{\text{--global}}$]
- `GTAO_SCREEN_RADIUS`=**float** (screen space radius for GTAO) [$\color{lightblue}{\text{--global}}$]
- `GTAO_MAX_RADIUS`=**float** (maximum radius for GTAO) [$\color{lightblue}{\text{--global}}$]
- `GTAO_FALLOFF_START`=**float** (falloff start distance) [$\color{lightblue}{\text{--global}}$]

### View Distances
- `f_visibility`=**0 to 255** (how far you can see through water) [$\color{lightblue}{\text{--biome}}$]
- `f_falloff`=**0 to 63** (light falloff distance in water) [$\color{lightblue}{\text{--biome}}$]

-----------------------------------------------------------------------------------------------------

## Complexity Settings

### Feature Toggles
- `w_weather`=**bool** (enable weather system) [$\color{lightblue}{\text{--world}}$]
- `w_rain`=**bool** (enable rain effects) [$\color{lightblue}{\text{--world}}$]
- `w_thunder`=**bool** (enable thunder effects) [$\color{lightblue}{\text{--world}}$]

### Effect Intensity
- `GI_BRIGHTNESS`=**float** (brightness multiplier for GI) [$\color{lightblue}{\text{--global}}$]
- `GTAO_STRENGTH`=**float** (strength of ambient occlusion) [$\color{lightblue}{\text{--global}}$]
- `w_rain_density`=**0 to 255** (rain density) [$\color{lightblue}{\text{--world}}$]
- `w_rain_speed`=**0 to 15** (rain speed) [$\color{lightblue}{\text{--world}}$]
- `w_thunder_frequency`=**0 to 255** (thunder frequency) [$\color{lightblue}{\text{--world}}$]
- `w_thunder_intensity`=**0 to 15** (thunder intensity) [$\color{lightblue}{\text{--world}}$]

### Performance vs Quality
- `GI_RENDER_RESOLUTION`=**float** (resolution scale for GI rendering) [$\color{lightblue}{\text{--global}}$]
- `SHADOW_BASIC_BLUR`=**float** (shadow blur performance vs quality) [$\color{lightblue}{\text{--global}}$]
- `VPS_SPREAD`=**float** (shadow penumbra spread) [$\color{lightblue}{\text{--global}}$]
- `MOTION_BLUR_SUTTER_ANGLE`=**float** (motion blur intensity) [$\color{lightblue}{\text{--global}}$]

-----------------------------------------------------------------------------------------------------

## Visual Preferences

### Color & Tone
- `AGX_EV`=**float** (exposure value for AgX tonemapper) [$\color{lightblue}{\text{--global}}$]
- `GAMMA`=**float** (gamma correction value) [$\color{lightblue}{\text{--global}}$]
- `LUMA_GAMMA`=**float** (luma gamma correction) [$\color{lightblue}{\text{--global}}$]
- `SATURATION`=**float** (color saturation) [$\color{lightblue}{\text{--global}}$]
- `WHITE_CLIP`=**float** (white point clipping) [$\color{lightblue}{\text{--global}}$]

### Sharpness & Clarity
- `CAS_SHARPNESS`=**integer** (sharpness level for CAS) [$\color{lightblue}{\text{--global}}$]
- `FSR_SHARPNESS`=**integer** (sharpness level for FSR) [$\color{lightblue}{\text{--global}}$]

### Bloom Effects
- `BLOOM_AMOUNT`=**float** (intensity of bloom effect) [$\color{lightblue}{\text{--global}}$]
- `NETHER_END_BLOOM_BOOST`=**float** (bloom boost for Nether and End) [$\color{lightblue}{\text{--global}}$]
- `GLARE_BRIGHTNESS`=**float** (brightness of lens glare) [$\color{lightblue}{\text{--global}}$]
- `FLARE_BRIGHTNESS`=**float** (brightness of lens flare) [$\color{lightblue}{\text{--global}}$]

### Camera Settings
- `EV_VALUE`=**float** (exposure value in EV) [$\color{lightblue}{\text{--global}}$]
- `AE_OFFSET`=**float** (auto exposure offset) [$\color{lightblue}{\text{--global}}$]
- `EXPOSURE_TIME`=**float** (exposure adaptation time) [$\color{lightblue}{\text{--global}}$]

-----------------------------------------------------------------------------------------------------

## Performance Notes

Modular Performance: Since this is modular, make sure to wrap these features in #ifdef tags. That way, if a modder doesn't use a feature, your GPU doesn't waste cycles even looking for the variable.
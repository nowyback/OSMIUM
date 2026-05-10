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
PARALAX
smooth snow accumilation
  {n:"SHADOW_MAP_BIAS",                       r:"float",      s:[W],    d:"Depth bias to prevent shadow acne"},
  {n:"SHADOW_BASIC_BLUR",                     r:"float",      s:[W],    d:"PCF blur radius for soft shadows"},

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











/* ─── TEMPORAL & AA ─── */
{ id:"temporal", title:"Temporal & Anti-Aliasing", isNew:true, vars:[
  {n:"TAA_ENABLED",                           r:"bool",       s:[G],    d:"Enable temporal anti-aliasing", isNew:true},
  {n:"TAA_FEEDBACK",                          r:"float",      s:[G],    d:"History blend factor. Higher=more stable but more ghosting", isNew:true, p:1},
  {n:"TAA_JITTER_SCALE",                      r:"float",      s:[G],    d:"Sub-pixel jitter spread", isNew:true, p:1},
  {n:"TAA_SHARPEN",                           r:"0–15",       s:[G],    d:"Temporal sharpening to counteract TAA blur", isNew:true, p:1},
  {n:"TAA_GHOST_REJECTION",                   r:"0–15",       s:[G],    d:"Aggressiveness of history rejection on disocclusions", isNew:true, p:1},
  {n:"AA_MODE",                               r:"0–4",        s:[G],    d:"0=none 1=FXAA 2=SMAA 3=TAA 4=DLSS/XeSS (if supported)", isNew:true},
]},




/* ─── POST-PROCESSING ─── */
{ id:"post", title:"Post-Processing", isNew:true, vars:[
  {n:"PP_BLOOM",                              r:"bool",       s:[G],    d:"Enable bloom / glow on bright pixels", isNew:true},
  {n:"PP_BLOOM_THRESHOLD",                    r:"float",      s:[G],    d:"Luminance threshold above which bloom kicks in", isNew:true, p:1},
  {n:"PP_BLOOM_INTENSITY",                    r:"0–15",       s:[G],    d:"Bloom brightness", isNew:true, p:1},
  {n:"PP_BLOOM_RADIUS",                       r:"0–15",       s:[G],    d:"Bloom spread in pixels", isNew:true, p:1},
  {n:"PP_DOF",                                r:"bool",       s:[G],    d:"Enable depth of field", isNew:true},
  {n:"PP_DOF_FOCAL_DISTANCE",                 r:"float",      s:[G],    d:"Focal plane distance in blocks", isNew:true, p:1},
  {n:"PP_DOF_FOCAL_RANGE",                    r:"float",      s:[G],    d:"Sharp zone depth in blocks", isNew:true, p:1},
  {n:"PP_DOF_BLUR_RADIUS",                    r:"0–15",       s:[G],    d:"Max circle of confusion radius in pixels", isNew:true, p:1},
  {n:"PP_DOF_BOKEH_SHAPE",                    r:"0–5",        s:[G],    d:"0=circle 1=hex 2=octagon 3=anamorphic 4=star 5=custom", isNew:true, p:1},
  {n:"PP_MOTIONBLUR",                         r:"bool",       s:[G],    d:"Enable camera motion blur", isNew:true},
  {n:"PP_MOTIONBLUR_STRENGTH",                r:"0–15",       s:[G],    d:"Shutter angle equivalent", isNew:true, p:1},
  {n:"PP_VIGNETTE",                           r:"bool",       s:[G],    d:"Enable vignette darkening at screen edges", isNew:true},
  {n:"PP_VIGNETTE_STRENGTH",                  r:"0–15",       s:[G],    d:"Vignette intensity", isNew:true, p:1},
  {n:"PP_VIGNETTE_RADIUS",                    r:"float",      s:[G],    d:"Radial extent. 1.0=touches corners", isNew:true, p:1},
  {n:"PP_FILM_GRAIN",                         r:"bool",       s:[G],    d:"Add analogue film grain noise", isNew:true},
  {n:"PP_FILM_GRAIN_STRENGTH",                r:"0–15",       s:[G],    d:"Grain intensity", isNew:true, p:1},
  {n:"PP_LENS_FLARE",                         r:"bool",       s:[G],    d:"Enable lens flare from bright light sources", isNew:true},
  {n:"PP_LENS_FLARE_INTENSITY",               r:"0–15",       s:[G],    d:"Flare brightness", isNew:true, p:1},
  {n:"PP_LENS_DISTORTION",                    r:"-15–15",     s:[G],    d:"Barrel (positive) or pincushion (negative) lens distortion", isNew:true},
  {n:"PP_SHARPEN",                            r:"0–15",       s:[G],    d:"Post-AA sharpening (CAS-style). 0=off", isNew:true},
  {n:"PP_CUSTOM_PASS",                        r:"string",     s:[G],    d:"Path to a GLSL file for a full custom post-processing pass", isNew:true},
]},




/* ─── COLOUR GRADING ─── */
{ id:"color", title:"Colour Grading", isNew:true, vars:[
  {n:"CC_EXPOSURE",                           r:"float",      s:[G],    d:"EV exposure offset. 0=neutral", isNew:true},
  {n:"CC_CONTRAST",                           r:"float",      s:[G],    d:"Contrast multiplier. 1.0=neutral", isNew:true},
  {n:"CC_SATURATION",                         r:"float",      s:[G],    d:"Colour saturation. 1.0=neutral, 0=greyscale", isNew:true},
  {n:"CC_TEMPERATURE",                        r:"-15–15",     s:[G],    d:"Colour temperature shift. Negative=cool, positive=warm", isNew:true},
  {n:"CC_TINT",                               r:"-15–15",     s:[G],    d:"Green–magenta tint shift", isNew:true},
  {n:"CC_SHADOWS_COLOR",                      r:"hex",        s:[G],    d:"Colour cast applied to shadow tones", isNew:true},
  {n:"CC_MIDTONES_COLOR",                     r:"hex",        s:[G],    d:"Colour cast applied to midtones", isNew:true},
  {n:"CC_HIGHLIGHTS_COLOR",                   r:"hex",        s:[G],    d:"Colour cast applied to highlights", isNew:true},
  {n:"CC_SHADOWS_LIFT",                       r:"float",      s:[G],    d:"Shadow lift (raises blacks). 0=neutral", isNew:true},
  {n:"CC_HIGHLIGHTS_GAIN",                    r:"float",      s:[G],    d:"Highlight roll-off. 1.0=neutral", isNew:true},
  {n:"CC_TONEMAP",                            r:"0–5",        s:[G],    d:"0=linear 1=Reinhard 2=ACES 3=Filmic 4=AgX 5=custom", isNew:true},
  {n:"CC_LUT",                                r:"string",     s:[G],    d:"Path to a 3D LUT texture applied as final colour grade", isNew:true},
  {n:"CC_BIOME_EXPOSURE",                     r:"float",      s:[L],    d:"Per-biome exposure offset, stacks with CC_EXPOSURE", isNew:true},
  {n:"CC_BIOME_SATURATION",                   r:"float",      s:[L],    d:"Per-biome saturation override", isNew:true},
  {n:"CC_BIOME_TEMPERATURE",                  r:"-15–15",     s:[L],    d:"Per-biome colour temperature", isNew:true},
]},
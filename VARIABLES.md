Here is the provided configuration data formatted into a clean, scannable Markdown document with organized tables for each section.

---

## 1. Haze (`haze`)

*Enables and configures volumetric haze, fog, and particle transitions across worlds and biomes.*

| Variable Name | Range / Type | Scope | Description |
| --- | --- | --- | --- |
| `HAZE_BASEWORLD` | `bool` | `[W]` | Enables base haze in a world. |
| `HAZE_BASEWORLD_DENSITY` | `0–255` | `[W]` | Amount of particles per unit. |
| `HAZE_BASEWORLD_DENSITY_VARIATION` | `0–255` | `[W]` | Range the density can deviate from base. |
| `HAZE_BASEWORLD_DENSITY_VARIATION_RANGE` | `0–255` | `[W]` | Max change per minute. |
| `HAZE_BASEWORLD_COLOR` | `hex[,hex…]` | `[W]` | Haze colour(s). Repeat a hex to increase its probability. |
| `HAZE_BASEWORLD_TYPE` | `0–255` | `[W]` | `0`=none, `1`=fog, `2`=steam, `3`=smoke, `4`=dust, `5`=vapor, `6`=mist, `7`=ash, `8`=haze, `9+`=custom. |
| `HAZE_BASEWORLD_LIGHT_ABSORPTION` | `0–15` | `[W]` | Light absorbed by haze (`0`=none, `15`=all). |
| `HAZE_BASEWORLD_LIGHT_SCATTERING` | `0–15` | `[W]` | Light scattered by haze. |
| `HAZE_BASEWORLD_HEIGHT_FALLOFF` | `0–15` | `[W]` | Haze fall rate in 0.1 blocks/sec. |
| `HAZE_BASEWORLD_WIND_SPEED` | `0–255` | `[W]` | Wind influence speed in 0.05 blocks/sec (`0`=off). |
| `HAZE_BASEWORLD_WIND_DIRECTION` | `0–360` | `[W]` | Wind direction in degrees. |
| `HAZE_BASEWORLD_ANISOTROPY` | `-1–1` | `[W]` | Light scatter direction: `-1`=back, `1`=forward, `0`=neutral. |
| `HAZE_BASEWORLD_NOISE_SCALE` | `0–255` | `[W]` | Scale of density noise pattern. |
| `HAZE_BASEWORLD_DISTANCE_FALLOFF` | `0–255` | `[W]` | Density falloff with view distance. |
| `HAZE_BASEWORLD_LAYER_PRIORITY` New | `0-255` | `[W]` | Z-order when multiple custom haze layers overlap. Defines which layer the base haze renders on. |
| `HAZE_BASEBIOME` | `bool` | `[B]` | Enables base haze in a biome. |
| `HAZE_BASEBIOME_DENSITY` | `0–255` | `[B]` | Particles per cubic unit. |
| `HAZE_BASEBIOME_DENSITY_VARIATION` | `0–255` | `[B]` | $\pm$ particle deviation. |
| `HAZE_BASEBIOME_DENSITY_VARIATION_RANGE` | `0–255` | `[B]` | Max change per minute. |
| `HAZE_BASEBIOME_COLOR` | `hex[,hex…]` | `[B]` | Haze colour(s). |
| `HAZE_BASEBIOME_TYPE` | `0–255` | `[B]` | `0`=none, `1`=fog, `2`=steam, `3`=smoke, `4`=dust, `5`=vapor, `6`=mist, `7`=ash, `8`=haze, `9+`=custom. |
| `HAZE_BASEBIOME_LIGHT_ABSORPTION` | `0–15` | `[B]` | Light absorbed by haze. |
| `HAZE_BASEBIOME_LIGHT_SCATTERING` | `0–15` | `[B]` | Light scattered. |
| `HAZE_BASEBIOME_HEIGHT_FALLOFF` | `0–15` | `[B]` | Fall rate in 0.1 blocks/sec. |
| `HAZE_BASEBIOME_WIND_SPEED` | `0–255` | `[B]` | Wind influence in 0.05 blocks/sec. |
| `HAZE_BASEBIOME_WIND_DIRECTION` | `0–360` | `[B]` | Wind direction in degrees. |
| `HAZE_BASEBIOME_ANISOTROPY` | `-1–1` | `[B]` | Scatter direction. |
| `HAZE_BASEBIOME_NOISE_SCALE` | `0–255` | `[B]` | Noise pattern scale. |
| `HAZE_BASEBIOME_DISTANCE_FALLOFF` | `0–255` | `[B]` | Distance density falloff. |
| `HAZE_BIOME_BLEND` | `bool` | `[B]` | Enables biome blending. |
| `HAZE_BIOME_BLEND_RADIUS` New | `0-63` | `[B]` | Radius in blocks over which haze blends at biome borders. |
| `HAZE_BIOME_BLEND_MODE` New | `0-3` | `[B]` | `0`=linear, `1`=cubic, `2`=nearest, `3`=custom. |
| `HAZE_BIOME_LAYER_PRIORITY` New | `0-255` | `[B]` | Z-order when multiple custom haze layers overlap. |
| `HAZE_BIOME_REMOVE_WORLD_HAZE` New | `bool` | `[B]` | Removes world haze in the area where biome haze is enabled. |
| `HAZE_CUSTOM` | `bool` | `[C]` | Enables a custom haze layer on top of base biome haze. |
| `HAZE_CUSTOM_DENSITY` | `0–255` | `[C]` | Particles per cubic unit. |
| `HAZE_CUSTOM_DENSITY_VARIATION` | `0–255` | `[C]` | $\pm$ deviation. |
| `HAZE_CUSTOM_DENSITY_VARIATION_RANGE` | `0–255` | `[C]` | Max change per minute. |
| `HAZE_CUSTOM_COLOR` | `hex[,hex…]` | `[C]` | Colour(s) of custom haze. |
| `HAZE_CUSTOM_TYPE` | `0–255` | `[C]` | Type index (same table as base). |
| `HAZE_CUSTOM_LIGHT_ABSORPTION` | `0–15` | `[C]` | Light absorption. |
| `HAZE_CUSTOM_LIGHT_SCATTERING` | `0–15` | `[C]` | Light scattering. |
| `HAZE_CUSTOM_HEIGHT_FALLOFF` | `0–15` | `[C]` | Fall rate in 0.1 blocks/sec. |
| `HAZE_CUSTOM_WIND_SPEED` | `0–255` | `[C]` | Wind in 0.05 blocks/sec. |
| `HAZE_CUSTOM_WIND_DIRECTION` | `0–360` | `[C]` | Wind direction. |
| `HAZE_CUSTOM_ANISOTROPY` | `-1–1` | `[C]` | Scatter direction. |
| `HAZE_CUSTOM_NOISE_SCALE` | `0–255` | `[C]` | Noise scale. |
| `HAZE_CUSTOM_DISTANCE_FALLOFF` | `0–255` | `[C]` | Distance falloff. |
| `HAZE_CUSTOM_BLEND` | `bool` | `[C]` | Enables custom haze blending. |
| `HAZE_CUSTOM_BLEND_RADIUS` New | `0-63` | `[C]` | Radius in blocks over which custom haze blends at biome borders. |
| `HAZE_CUSTOM_BLEND_MODE` New | `0-3` | `[C]` | `0`=linear, `1`=cubic, `2`=nearest, `3`=custom. |
| `HAZE_CUSTOM_LAYER_PRIORITY` New | `0-255` | `[C]` | Z-order when multiple custom haze layers overlap. |
| `HAZE_CUSTOM_REMOVE_WORLD_HAZE` New | `bool` | `[C]` | Removes world haze in the area where custom haze is enabled. |
| `HAZE_CUSTOM_REMOVE_BIOME_HAZE` New | `bool` | `[C]` | Removes biome haze in the area where custom haze is enabled. |
| `HAZE_PARTICLES_TO_HAZE` | `bool` | `[C]` | Auto-renders existing particle systems as volumetric haze. |
| `HAZE_VARIATION_AMOUNT` | `0–255` | `[C]` | Max change per minute from particle haze. |
| `HAZE_TYPE` | `0–255` | `[C]` | Type index (same table as base). |
| `HAZE_PARTICLE_TYPE` | `W,B,C` | `[C]` | Which particle type ID to convert. |

---

## 2. Light Emission (`light_emission`) New Section

*Handles dynamically emitted light sources from blocks, including directions, shapes, and structural scattering.*

| Variable Name | Range / Type | Scope | Description |
| --- | --- | --- | --- |
| `LIGHT_EMISSION` | `bool` | `[BL]` | Enables light emission. |
| `LIGHT_EMISSION_COLOR` | `hex` | `[BL]` | Colour of emitted light. |
| `LIGHT_EMISSION_RANGE_OVERRIDE` | `0 to 63` | `[BL]` | If > 0, overrides the standard light source range. |
| `LIGHT_EMMISION_TYPE` | `0-3` | `[BL]` | `0` = Point Light / Laser, `1` = Flashlight [CONE], `2` = Surround Illumination, `3` = Custom. |
| `LIGHT_EMMISION_ANGLE_X_AXIS` | `0-360` | `[BL]` | Direction of the lighting on the X Axis. |
| `LIGHT_EMMISION_ANGLE_Y_AXIS` | `0-360` | `[BL]` | Direction of the lighting on the Y Axis. |
| `LIGHT_EMMISION_ANGLE_Z_AXIS` | `0-360` | `[BL]` | Direction of the lighting on the Z Axis. |
| `LIGHT_EMMISION_SOFTNESS` | `0-63` | `[BL]` | The softness of the light (`0` = hard edge, `63` = very soft edge). |
| `LIGHT_TEXEL_MODE` | `bool` | `[BL]` | If true, texel rendering is active; if false, it renders from the center of the block. |
| `LIGHT_TEXEL_BLENDING` | `0-15` | `[BL]` | How much adjacent texels blend with each other. |
| `LIGHT_SUBSURFACE_SCATTERING` | `bool` | `[BL]` | Enables Subsurface Scattering (SSS) for semi-translucent blocks (leaves, ice). |
| `LIGHT_ADVANCED_SUBSURFACE_SCATTERING` | `bool` | `[BL]` | Enables pixel-based SSS for semi-translucent blocks. |

---

## 3. Light Handling (`light`)

*Controls global properties of light transmission, reflections, falloffs, and aesthetic artifacts.*

| Variable Name | Range / Type | Scope | Description |
| --- | --- | --- | --- |
| `LIGHT_ABSORPTION` | `0–15` | `[BL]` | Reduces light level per reflection. `0` = all light absorbed, `15` = all light reflects. |
| `LIGHT_REFLECTIONBLUR` | `0–15` | `[BL]` | Blurriness of reflected light. |
| `LIGHT_SCATTERING` | `bool` | `[BL]` | Enables directional light scattering. |
| `LIGHT_SCATTERING_VARIATION` | `0–255` | `[BL]` | Scatter spread in 0.1-degree steps. |
| `LIGHT_CHROMATICABBERATION` | `bool` | `[BL]` | Enables chromatic aberration on transmitted light. |
| `LIGHT_CHROMATICABBERATION_STRENGTH` | `0–7` | `[BL]` | `0` = none, `3` = default, `7` = full-pixel shift. |
| `LIGHT_FALLOFF_GLOBAL` | `0–63` | `[G]` | Per-block light falloff via Inverse Square law. (See falloff table). |
| `LIGHT_FALLOFF_WORLD` | `0–63` | `[W]` | World-wide light falloff override. |
| `LIGHT_FLICKER` | `bool` | `[BL]` | Enables light flickering. |
| `LIGHT_FLICKER_RATE` | `0–63` | `[BL]` | Flicker frequency in 10ms steps. |
| `LIGHT_FLICKER_RATE_VARIATION` | `0–63` | `[BL]` | Frequency jitter in 10ms steps. |
| `LIGHT_FLICKER_INTENSITY` | `0–15` | `[BL]` | Flicker amplitude measured in light levels. |
| `LIGHT_FLICKER_INTENSITY_VARIATION` | `0–63` | `[BL]` | Intensity jitter in 10ms steps. |

---

## 4. Puddles (`puddle`)

*Configures environmental surface water collection attributes.*

| Variable Name | Range / Type | Scope | Description |
| --- | --- | --- | --- |
| `PUDDLE_COLOR` | `hex` | `[B]` | Color of the puddle. |
| `PUDDLE_DEPTH` | `0–15` | `[B]` | Puddle depth. Generically affects ripple count, evaporation duration, and splash scale. |
| `PUDDLE_VISCOSITY` New | `0–15` | `[B]` | Ripple distortion amplitude. |
| `PUDDLE_REFLECTION_STRENGHT` New | `0–15` | `[B]` | Mirror reflectivity behavior of the puddle surface. |
| `PUDDLE_EVAPORATION_SPEED` New | `0–15` | `[B]` | How fast puddles shrink after precipitation ceases. |

---

## 5. Fluids (`fluid`)

*Manages visibility, wave behaviors, physics, and rendering overrides within custom volumetric liquids.*

| Variable Name | Range / Type | Scope | Description |
| --- | --- | --- | --- |
| `FLUID_VISIBILITY` | `0–255` | `[C]` | Visibility distance through fluid measured in blocks. |
| `FLUID_LIGHT_FALLOFF` | `0–63` | `[C]` | Light falloff inside the fluid medium (see falloff table). |
| `FLUID_MURKINESS` | `0–255` | `[C]` | Suspended particle density in cubic units. |
| `FLUID_LIGHT_SCATTERING` | `0–255` | `[C]` | Light scatter inside fluid in 0.1-degree steps. |
| `FLUID_LIGHT_ABSORPTION` | `0–15` | `[C]` | Light absorbed specifically by fluid murkiness. |
| `FLUID_COLOR` | `hex / null` | `[C]` | Fluid colour override. `null` = fallback to default. |
| `FLUID_WAVE_HEIGHT` | `0–15` | `[C]` | Wave height scaling in 0.05-block steps. |
| `FLUID_WAVE_SPEED` | `0–15` | `[C]` | Wave propagation speed in 0.25 blocks/sec. |
| `FLUID_VISCOSITY` | `0–15` | `[C]` | Fluid thickness — dampens waves and restricts entity physics. |
| `FLUID_FOAM` New | `bool` | `[C]` | Enables dynamic foam generation. |
| `FLUID_FOAM_SHORE` New | `bool` | `[C]` | Enable surface foam generations at shallow block borders. |
| `FLUID_FOAM_THRESHOLD` New | `0–15` | `[C]` | Minimal required wave height at which whitecaps generate. |
| `FLUID_FOAM_COLOR` New | `hex` | `[C]` | Surface foam colour. |
| `FLUID_CAUSTICS` New | `bool` | `[C]` | Enables caustic light refraction maps onto underwater surfaces. |
| `FLUID_CAUSTICS_STRENGTH` New | `0–15` | `[C]` | Intensity scale of caustic patterns on sub-surface geometry. |
| `FLUID_CAUSTICS_SCALE <mark>New</mark>` | `0–15` | `[C]` | Scale adjustments of caustic tiling patterns in 0.1-block intervals. |
| `FLUID_DEPTH_COLOR` New | `hex` | `[C]` | Deepest target colour utilized for depth-based color grading gradients. |
| `FLUID_DEPTH_FALLOFF` New | `0–15` | `[C]` | Relative depth required before colour maps completely blend into `f_depth_color`. |
| `FLUID_BIOLUMINESCENCE` New | `bool` | `[C]` | Enables glowing particulate matter within fluid volume grids. |
| `FLUID_BIOLUMINESCENCE_COLOR` New | `hex` | `[C]` | Fluid particle emission color glow. |
| `FLUID_BIOLUMINESCENCE_DENSITY` New | `0–255` | `[C]` | Internal count of bioluminescent particles generated. |

---

## 6. Global Illumination (`gi`)

*Controls indirect sky bleeding and reflective source properties.*

| Variable Name | Range / Type | Scope | Description |
| --- | --- | --- | --- |
| `GLOBAL_ILLUMINATION_WORLD` | `0–15` | `[W]` | GI weight on a global scale. `0`=off, `15`=max. |
| `GLOBAL_ILLUMINATION_BIOME` | `0–15` | `[B]` | Localized GI weight adjustments per biome profile. |
| `GLOBAL_ILLUMINATION_COLOR` | `0–15` | `[C]` | `0`=default world colors, `1–15`=assigned index overrides. |
| `GLOBAL_ILLUMINATION_SKY_CONTRIBUTION` New | `0–15` | `[C]` | Scale of sky-dome color bleeding across shadowed geometries. |
| `GLOBAL_ILLUMINATION_EMISSIVE_CONTRIBUTION` New | `0–15` | `[C]` | Determines how intensely emissive block surfaces contribute to GI pipelines. |

---

## 7. Block Properties (`block`) New Section

*Defines physical permeability, absorption rates, responses to liquids, and vertex animations.*

| Variable Name | Range / Type | Scope | Description |
| --- | --- | --- | --- |
| `BLOCK_PERMABLE` | `bool` | `[BL]` | Allows fluid volumes to drop through solid blocks. |
| `BLOCK_PERMABLE_TIME` | `0-255` | `[BL]` | Traversal calculation time for fluid to transition through, throttled by `WATER_VISCOSITY`. |
| `BLOCK_PERMABLE_REDUCTION` | `0-255` | `[BL]` | Absorption deduction factor applied to passing fluids. |
| `BLOCK_PERMABLE_REDICTION_MAX` | `0-255` | `[BL]` | Maximum absorption tolerance threshold before solid block saturates completely. |
| `BLOCK_PERMABLE_DRY_TIME` | `0-255` | `[BL]` | Absolute timeframe mapping block evaporative moisture properties back to default. |
| `BLOCK_PERMABLE_ADAPTATION` | `0-63` | `[BL]` | Determines how a fluid alters properties upon block penetration. |
| `BLOCK_ADAPTATION` | `0-63` | `[BL]` | General trigger condition modifier for contextual environment events. |
| `BLOCK_ADAPTATION_WATER` | `0-63` | `[BL]` | Target adaptability metric specifically when contacting water. |
| `BLOCK_ADAPTATION_LAVA` | `0-63` | `[BL]` | Target adaptability metric specifically when contacting lava. |
| `BLOCK_ADAPTATION_CUSTOM` | `0-63` | `[BL]` | Target adaptability metric specifically when contacting custom user fluids. |
| `BLOCK_ADAPTATION_RAIN` | `0-63` | `[BL]` | Target adaptability metric specifically when interacting with downpour states. |
| `BLOCK_PARTICLE_EMISSION` | `bool` | `[BL]` | Allows standalone block identities to generate native particles. |
| `BLOCK_PARTICLE_EMSION_AMOUNT` | `0-255` | `[BL]` | Numeric volume scale of native emissions. |
| `BLOCK_PARTICLE_EMSION_RADIUS` | `0-63` | `[BL]` | Positional bounds for particle flight pathways. |
| `BLOCK_WAVING` | `bool` | `[BL]` | Enables custom vertex displacement mapping (leaves, tallgrass, banners). |
| `BLOCK_WAVING_AMPLITUDE` | `0–15` | `[BL]` | Wave structural displacement depth in increments of 0.05 blocks. |
| `BLOCK_WAVING_SPEED` | `0–15` | `[BL]` | Frequency calculations multiplier tracking vertex motions. |
| `BLOCK_WAVING_WIND_INFLUENCE` | `0–15` | `[BL]` | Influence coefficient shifting dynamic alignments according to global `HAZE_*` data targets. |

---

## 8. Sky & Atmosphere (`sky`)

*Calculates mathematical horizon sky models, scattering strengths, and celestial assets properties.*

| Variable Name | Range / Type | Scope | Description |
| --- | --- | --- | --- |
| `STAR_TYPE` | `integer` | `[W]` | Star rendering structural formatting index. |
| `SKY_TEXTURE_BRIGHTNESS` | `float` | `[W]` | Linear texture brightness factor for sky objects. |
| `SKY_MODEL` New | `0–3` | `[W]` | `0`=simple gradient, `1`=Rayleigh, `2`=Mie, `3`=Preetham. |
| `SKY_RAYLEIGH_STRENGTH` New | `0–15` | `[W]` | Rayleigh structural scattering adjustment; scales overall atmospheric blueness. |
| `SKY_MIE_STRENGTH` New | `0–15` | `[W]` | Mie scattering; configures light-glow halos wrapped around daylight stars. |
| `SKY_OZONE_STRENGTH` New | `0–15` | `[W]` | Ozone structural calculation factors; accentuates sunset warming profiles. |
| `SUN_ANGULAR_SIZE` New | `float` | `[W]` | Sun structural disc perspective width in degrees (`0.5` = accurate earthly profile). |
| `SUN_COLOR` New | `hex` | `[W]` | Target color values overriding default stellar disc colors. |
| `SUN_CORONA_RADIUS` New | `0–15` | `[W]` | Outer radiant corona glare boundaries recorded in degree intervals. |
| `MOON_ANGULAR_SIZE` New | `float` | `[W]` | Moon geometric size profiles mapped in target degrees. |
| `MOON_PHASE_AFFECTS_LIGHT` New | `bool` | `[W]` | Determines if moonlight luminance correlates directly with phase states. |
| `SKY_CUSTOM_LUT` New | `string` | `[W]` | Asset location address targeting a 3D Color Grading LUT for sky frames. |

---

## 9. Weather (`weather`)

*Sets precipitation densities, atmospheric variations, wind gusts, and surface moisture behaviors.*

| Variable Name | Range / Type | Scope | Description |
| --- | --- | --- | --- |
| `WEATHER_RAIN_DENSITY` | `0–255` | `[B]` | Active downpour droplet concentration targets. |
| `WEATHER_RAIN_SPEED` | `0–15` | `[B]` | Falling speed of raindrops. |
| `WEATHER_SNOW_DENSITY` New | `0–255` | `[B]` | Active snowflake generation concentrations. |
| `WEATHER_SNOW_SIZE` New | `0–15` | `[B]` | Snowflake scaling configurations mapped to pixel sizes. |
| `WEATHER_SNOW_ACCUMULATION` New | `bool` | `[B]` | Allows snowy precipitation vectors to create layers across level blocks. |
| `WEATHER_WIND` New | `bool` | `[B]` | Toggles logical level integrations interacting with atmospheric winds. |
| `WEATHER_WIND_DIRECTION` New | `0-360` | `[B]` | Rotational wind source origin headings in degrees. |
| `WEATHER_WIND_SPEED` New | `0-255` | `[B]` | Baseline wind speed. |
| `WEATHER_WIND_GUSTS` New | `bool` | `[B]` | Determines if periodic random wind gusts emerge over execution cycles. |
| `WEATHER_WIND_GUSTS_INTENSITY` New | `0–255` | `[B]` | Velocity additions multiplier detailing performance spikes during gusts. |
| `WEATHER_WIND_GUSTS_INTENSITY_VARIATION` New | `0–255` | `[B]` | Total potential noise deviations calculated across custom gust profiles. |
| `WEATHER_WIND_GUSTS_CHANCE` New | `0–255` | `[B]` | Frequency distribution markers detailing gust intervals in minute steps. |
| `WEATHER_WIND_GUSTS_DURATION` New | `0–255` | `[B]` | Individual gust execution timelines recorded in 10-second intervals. |
| `WEATHER_FOG OVERRIDE` New | `bool` | `[B]` | Mandates structural storm fog render behaviors regardless of global `HAZE` flags. |
| `WEATHER_FOG_DENSITY` New | `0–255` | `[B]` | Absolute fog density factor deployed entirely within severe storms. |
| `WEATHER_LIGHTNING_COLOR` New | `hex` | `[B]` | Target color values tracking lightning bolts and associated screen flashing. |
| `WEATHER_LIGHTNING_BRIGHTNESS` | `0-15` | `[B]` | Structural flash intensity scale; `15` targets values mapping out up to 45 blocks away. |
| `WEATHER_WETNESS_RAMPUP` New | `0–255` | `[B]` | Operational seconds clock mapping full surface hydration values during rain storms. |
| `WEATHER_WETNESS_RAMPDOWN` New | `0–255` | `[B]` | Operational seconds clock tracking surface moisture dissipation targets after rain stops. |

---

## 10. Shadows (`shadow`)

*Sets depth map details, colored transparency filtration, and cascade configurations.*

| Variable Name | Range / Type | Scope | Description |
| --- | --- | --- | --- |
| `SHADOW_CASCADES` New | `1–4` | `[W]` | Total configuration layers allocated for CSM shadow lookups. (Higher balances distant view fidelity). |
| `SHADOW_PENUMBRA` New | `bool` | `[W]` | Toggles PCSS variable-width filter calculations (Scales from global astronomical dimensions). |
| `SHADOW_PENUMBRA_SAMPLES` New | `4–64` | `[W]` | Lookup counts feeding penumbra maps. (Higher values yield smoother bounds, impacting overhead). |
| `SHADOW_COLORED_TRANSMISSION` New | `bool` | `[W]` | Permits transparent level block objects to pass custom colored light maps onto shadows. |
| `SHADOW_BIOME_TINT` New | `hex` | `[B]` | Contextual color tint vectors shifting baseline shadow regions within targeted environments. |

---

## 11. Biome Transitions (`biome_transition`) New Section

*Determines horizontal zone blends, layering orders, and interpolation modes.*

| Variable Name | Range / Type | Scope | Description |
| --- | --- | --- | --- |
| `BIOME_BLEND_RADIUS` | `0–255` | `[B]` | Total block radius boundaries deployed for blending atmospheric behaviors into adjacent regions. |
| `BIOME_BLEND_PRIORITY` | `0–15` | `[B]` | Arbitrary structural tier markers setting context priorities when contrasting boundary regions merge. |
| `BIOME_BLEND_PRIORITY_VALUE` | `0-255` | `[B]` | Z-ordering layout specifications tracking overlapping biome patterns. (Higher equals dominance). |
| `BIOME_BLEND_CURVE` | `0–3` | `[B]` | Interpolation parameters mapping boundary gradients: `0`=linear, `1`=smooth, `2`=step, `3`=custom curve. |

---

## 12. Custom / Developer Extensions (`custom`) New Section

*Provides developer tool hooks for feeding variables directly into internal system shader pipelines.*

| Variable Name | Range / Type | Scope | Description |
| --- | --- | --- | --- |
| `CUSTOM_UNIFORM_INT` | `string:int` | `[G,L,W,BL]` | Registers a developer uniform configuration format tracking numerical integers (`name=value`). |
| `CUSTOM_UNIFORM_FLOAT` | `string:float` | `[G,L,W,BL]` | Registers a developer uniform configuration format tracking floating point metrics. |
| `CUSTOM_UNIFORM_VEC3` | `string:r,g,b` | `[G,L,W,BL]` | Registers a developer uniform configuration format tracking `vec3` attributes. |
| `CUSTOM_UNIFORM_VEC4` | `string:r,g,b,a` | `[G,L,W,BL]` | Registers a developer uniform configuration format tracking `vec4` attributes. |
| `CUSTOM_DEFINE` | `string` | `[G]` | Forces injection of a text `#define` target directive into all engine pass stages (`KEY=value`). |
| `CUSTOM_VERTEX_SNIPPET` | `string` | `[BL]` | Identifies path targets for custom GLSL scripts bound directly onto structural vertex pass calls. |
| `CUSTOM_FRAGMENT_SNIPPET` | `string` | `[BL]` | Identifies path targets for custom GLSL scripts bound directly onto structural fragment pass calls. |
| `CUSTOM_COMPUTE_SNIPPET` | `string` | `[G]` | Core path pointing to GLSL compute shader execution frameworks hosting global graphic properties. |
| `CUSTOM_TEXTURE_SLOT` | `0–7` | `[BL]` | Sets target layout slots for rendering developer custom map data maps within blocks. |
| `CUSTOM_TEXTURE_PATH` | `string` | `[BL]` | Target location address defining data bound immediately into context definitions from `CUSTOM_TEXTURE_SLOT`. |
| `CUSTOM_PASS_ORDER` | `0–15` | `[G]` | Pipeline execution order designations handling compute passes; lower priority runs earlier. |

---

> **Key for Scope Values:** > `[G]` = Global | `[W]` = World | `[B]` = Biome | `[C]` = Custom | `[L]` = Local / Layer | `[BL]` = Block
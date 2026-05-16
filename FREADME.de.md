Hier ist die deutsche Ãœbersetzung deiner Feature-Liste und Variablen-Definitionen fÃ¼r dein Trello oder die Dokumentation. Ich habe die technischen Fachbegriffe (wie SSAO oder PBR) beibehalten, da sie auch im Deutschen Standard sind, aber die ErklÃ¤rungen Ã¼bersetzt.

---

### **Tier 1: NORMAL (Rasterisierte Grafik)**
*Fokus: Geschwindigkeit und "vorgetÃ¤uschter" Realismus. Gut fÃ¼r allgemeines Gameplay.*
* **Shadow Maps:** Vorberechnete Schatten, die bei niedrigen AuflÃ¶sungen "blockig" oder "zackig" aussehen kÃ¶nnen.
* **SSAO (Screen Space Ambient Occlusion):** Erzeugt kÃ¼nstliche Kontaktschatten nur fÃ¼r Objekte, die aktuell auf dem Bildschirm sichtbar sind.
* **Dynamische Beleuchtung (Vanilla-Stil):** Licht aktualisiert sich in "BlÃ¶cken" oder Stufen, keine weichen ÃœbergÃ¤nge.
* **Einfaches Wasser:** Simple Reflexionen (SSR) und eine scrollende Textur.
* **Standard Tone Mapping:** Grundlegende Anpassungen von Helligkeit und Kontrast.
* **[PLUS] Volumetrischer Nebel:** Einfache Lichtstrahlen ("God Rays"), die auf den Sonnenstand reagieren.
* **[PLUS] Flache PfÃ¼tzen:** Eine einfache "NÃ¤sse"-Ebene, die die Reflexion auf BlÃ¶cken erhÃ¶ht.
* **[PLUS] Sprite-Wolken:** 2D-Wolkenschichten, die sich mit dem Himmel drehen.
* **[PLUS] Partikel-Rauch:** Standard Minecraft-Partikel, die keine Schatten werfen oder auf Licht reagieren.

---

### **Tier 2: RAYTRACING (Hybrid-Engine)**
*Fokus: Physikalische Genauigkeit fÃ¼r Schatten und Reflexionen. Der "Pro"-Look.*
* **Ray-Traced Shadows:** Pixelgenaue Schatten ohne "Shadow Acne" oder schwebende Schatten ("Peter Panning").
* **SSR (Screen Space Reflections):** Fortgeschrittene Reflexionen, die Spiegel und glÃ¤nzende BlÃ¶cke korrekt darstellen.
* **Punktlicht-Berechnung:** Einzelne Lichtquellen (wie Fackeln) agieren als echte Lichtpunkte im Raum.
* **Kaustik:** Grundlegende Lichtmuster durch Wasser.
* **[PLUS] Variable Penumbra:** Schatten, die nah am Objekt scharf sind und mit zunehmender Entfernung weicher werden.
* **[PLUS] PBR-UnterstÃ¼tzung:** Volles "Physical Based Rendering" (Materialien wirken wie echtes Metall, Stein oder Plastik).
* **[PLUS] Echtzeit-PfÃ¼tzen:** Nutzt eine "Noise-Map" fÃ¼r variierende NÃ¤sse (trockene/nasse Stellen) mit Raytracing-Reflexionen.
* **[PLUS] Volumetrischer Dunst (Basis):** Ein gleichmÃ¤ÃŸiger Nebel, der in der Ferne dichter wird und leuchtet, wenn die Sonne hineinscheint.
* **[PLUS] Screen-Space Wasser-Interaktion:** Wasser bildet leichte Wellen, wenn sich Spieler oder Wesen hindurchbewegen (vorgetÃ¤uschte Physik).
* **[PLUS] 2D Volumetrische Wolken:** Wolken mit "Dicke", die jedoch auf einer flachen Ebene gerendert werden.

---

### **Tier 3: PATHTRACING (Die PTX Hyperrealist-Engine)**
*Fokus: Unendliche Lichtabpraller und spektrale Physik. Deine "Huge"-Vision.*
* **PTGI (Path Traced Global Illumination):** Licht prallt von WÃ¤nden ab, um dunkle RÃ¤ume indirekt zu beleuchten.
* **Voxel-Basierter Tracer:** Die Engine "sieht" jeden Block als physikalisches Objekt fÃ¼r 100% korrekte Lichtblockierung.
* **[PLUS] OberflÃ¤chen-Emission:** Licht wird von den **SeitenflÃ¤chen** der BlÃ¶cke emittiert, was scharfe 90-Grad-Lichtkanten erzeugt.
* **[PLUS] Spektrale Dispersion:** Licht bricht sich in "Regenbogen-Kanten" (chromatische Aberration) an kontrastreichen RÃ¤ndern.
* **[PLUS] Mathematisch scharfe Schatten:** Erzwungene Lichtquellen mit Radius `0.0` fÃ¼r messerscharfe, cineastische Schatten.
* **[PLUS] Quadratisches Abfallsgesetz (Inverse Square Law):** Physikalisch korrekte Lichtabnahme ($1/d^2$) fÃ¼r jede Lichtquelle.
* **Spatio-Temporales Denoising:** Hochwertiges Filtern von "verrauschten" Pixeln fÃ¼r ein flÃ¼ssiges Bild bei Bewegung.
* **[PLUS] Partikel-zu-Volumen Dunst:** Partikel (wie Lagerfeuer-Rauch) verschmelzen physikalisch mit dem volumetrischen Dunst.
* **[PLUS] 3D Ray-Marched Volumengrafik-Wolken:** Wolken mit echtem Volumen, die Schatten auf sich selbst und den Boden werfen.
* **[PLUS] Extreme Wasser-Interaktion:** * **Lichtbrechende Kaustik:** Licht durch die WasseroberflÃ¤che erzeugt tanzende Muster basierend auf PTX-Strahlen.
    * **Physikalische Verschiebung:** Hochwertige Wellen, die die Geometrie des Wassers verÃ¤ndern.
* **[PLUS] Dynamische PfÃ¼tzen & Wellen:** PfÃ¼tzen, die sich Ã¼ber Zeit ansammeln; scharfe Reflexionen von Lichtquellen.
* **[NEW] oe Data Bridge Integration:** Echtzeit-Abfrage von Attributen via SSBO fÃ¼r datengesteuerte Materialien.
* **[NEW] Spektrale Transparenz:** Lichtmischung durch gefÃ¤rbtes Glas (Rot + Blau = Lila).
* **[NEW] Selektive Texel-Emission:** Lichter emittieren Farben basierend auf einzelnen Pixeln der Blocktextur.
* **[NEW] Fail-Safe StabilitÃ¤t:** Automatische Standardwerte fÃ¼r undefinierte Blockdaten oder Regler.

---

### **Bonus "Erweiterungs"-Features (Die "Insane"-Details)**
* **[ADD] Spektrale Wasserbrechung:** Licht biegt sich unter Wasser in verschiedenen Winkeln fÃ¼r Unterwasser-RegenbÃ¶gen.
* **[ADD] Subsurface Scattering:** LÃ¤sst BlÃ¤tter und Haut "warm" leuchten, wenn Licht von hinten hindurchscheint.
* **[ADD] Mikro-Detail Schatten:** Schatten, die von winzigen Unebenheiten in einer Textur geworfen werden (High-Res PBR).
* **[ADD] Die "Backrooms"-Taschenlampe:** Tragbares Punktlicht mit spektralem Lichtstrahl.
* **[ADD] Spektrale Regenbogen-PfÃ¼tzen:** PfÃ¼tzenreflexionen, die spektrale Dispersion zeigen.
* **[ADD] Lokalisierter Dunst:** Nebel, der sich in Senken (TÃ¤lern/HÃ¶hlen) sammelt.
* **[ADD] Dimensions-Anpassung:** Variablen fÃ¼r Himmelsfarben, Schwerkraft-Visualisierung und Sonnenstrahlung.
* **[ADD] AtmosphÃ¤re/Wolken-Details:** Ozon-Dichte und Mie/Rayleigh-StreustÃ¤rke-Regler.

---

### **VARIABLEN-DEFINITIONEN**

**1. DUNST (Welt, Biom, Custom und Partikel)**
* **h_baseworld (bool):** Aktiviert globalen Weltdunst.
* **hbw_density (0-255):** Partikelanzahl pro Einheit.
* **hbw_densityvariation (0-255):** Bereich der Dichteschwankung.
* **hbw_densityvariationrange (0-255):** Geschwindigkeit der DichteÃ¤nderung pro Minute.
* **hbw_color (hex):** Hexcode oder Liste fÃ¼r Farbwahrscheinlichkeiten.
* **hbw_type (0-9):** Typ-Auswahl (Nebel, Dampf, Rauch, Staub, Dunst, etc.).
* **hbw_lightabsorbtion (0-15):** Lichtmenge, die vom Medium absorbiert wird.
* **hbw_lightscattering (0-15):** Lichtmenge, die vom Medium gestreut wird.
* **hbw_heightfalloff (0-15):** Sinkrate (0.1 BlÃ¶cke/Sek).
* **hbw_windspeed (0-255):** Windgeschwindigkeit (0.05 BlÃ¶cke/Sek).
* **hbw_winddirection (0-360):** Windrichtung in Grad.
* **hbw_anisotropy (-1 bis 1):** Streurichtung (-1: zurÃ¼ck, 1: vorwÃ¤rts).
* **hbw_noisescale / hbw_noisedetail:** Frequenz und Detailtiefe des Noise-Algorithmus.
* **hbw_groundfog (bool):** BeschrÃ¤nkt Dunst auf niedrige HÃ¶hen.
* **hbw_groundheight (0-255):** Maximale HÃ¶he fÃ¼r Bodennebel.
* **h_particlestohaze (bool):** Partikel automatisch als Volumen-Dunst rendern.

**2. LICHT-LOGIK**
* **l_color (hex):** Hauptfarbe des Lichts.
* **lc_variation (hex):** Variationsfarbe.
* **lc_variationamount (0-255):** Geschwindigkeit des Farbwechsels pro Minute.
* **l_flicker (bool):** Aktiviert Flackern der Lichtquelle.
* **lf_rate / lf_intensity:** Frequenz und StÃ¤rke des Flackerns.
* **l_absorbtion (0-15):** Blockiert Lichtdurchlass (0: transparent, 15: opak).
* **l_reflection (0-15):** VerhÃ¤ltnis von reflektiertem zu durchgelassenem Licht.
* **l_reflectionblur (0-15):** Rauheit/UnschÃ¤rfe der Reflexion.
* **l_scattering (bool):** Aktiviert den Streuwinkel des Lichts.
* **l_chromaticabberation (bool):** Aktiviert spektrale Aufspaltung.
* **lc_strength (0-7):** StÃ¤rke der Aberration (Basiswert 3).
* **lc_index (0-15):** Brechungsindex-Offset fÃ¼r Dispersion.
* **l_godrays (bool):** Aktiviert volumetrische LichtschÃ¤chte.
* **l_falloff_global / l_falloff_world (0-63):** IntensitÃ¤t des quadratischen Lichtabfalls.

**3. PFÃœTZEN**
* **p_isdirt (bool):** Aktiviert schlammigen/dreckigen Texturfilter.
* **p_depth (0-15):** Bestimmt WellenintensitÃ¤t und Spritzer-GrÃ¶ÃŸe.

**4. WASSER & FLÃœSSIGKEITEN**
* **w_visibility (0-255):** Unterwasser-Sichtweite je nach Biom.
* **w_murkiness (0-255):** Partikeldichte in der FlÃ¼ssigkeit (TrÃ¼bung).
* **w_refractionindex (0-15):** StÃ¤rke der Lichtbrechung unter Wasser.
* **w_wave_height / w_wave_speed:** Physikalische Verschiebung der WasseroberflÃ¤che.
* **w_viscosity (0-15):** Beeinflusst Wellengeschwindigkeit und Physik-Interaktion.
* **w_dispersion (0-15):** Spektrale Aufspaltung von Unterwasserlicht.
* **w_caustics_intensity (0-255):** StÃ¤rke der LichtbÃ¼ndelung am Boden.

**5. UMGEBUNG & ATMOSPHÃ„RE**
* **d_sky_color / d_horizon_color (hex):** FarbverlÃ¤ufe des Himmels.
* **d_ambient_light (0-255):** Minimale Helligkeit in totaler Dunkelheit.
* **d_solar_irradiance (0-255):** RÃ¼ckstrahlkraft des Sonnenlichts.
* **at_ozone_density (0-255):** Absorption von UV/Blauem Licht in der oberen AtmosphÃ¤re.
* **at_rayleigh_strength (0-255):** IntensitÃ¤t des Himmelsblaus (Rayleigh-Streuung).
* **at_mie_phase (-1 bis 1):** Phasenfunktion fÃ¼r grÃ¶ÃŸere Partikel (Staub/Dunst).
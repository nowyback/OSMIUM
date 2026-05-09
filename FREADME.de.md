Hier ist die deutsche Übersetzung deiner Feature-Liste und Variablen-Definitionen für dein Trello oder die Dokumentation. Ich habe die technischen Fachbegriffe (wie SSAO oder PBR) beibehalten, da sie auch im Deutschen Standard sind, aber die Erklärungen übersetzt.

---

### **Tier 1: NORMAL (Rasterisierte Grafik)**
*Fokus: Geschwindigkeit und "vorgetäuschter" Realismus. Gut für allgemeines Gameplay.*
* **Shadow Maps:** Vorberechnete Schatten, die bei niedrigen Auflösungen "blockig" oder "zackig" aussehen können.
* **SSAO (Screen Space Ambient Occlusion):** Erzeugt künstliche Kontaktschatten nur für Objekte, die aktuell auf dem Bildschirm sichtbar sind.
* **Dynamische Beleuchtung (Vanilla-Stil):** Licht aktualisiert sich in "Blöcken" oder Stufen, keine weichen Übergänge.
* **Einfaches Wasser:** Simple Reflexionen (SSR) und eine scrollende Textur.
* **Standard Tone Mapping:** Grundlegende Anpassungen von Helligkeit und Kontrast.
* **[PLUS] Volumetrischer Nebel:** Einfache Lichtstrahlen ("God Rays"), die auf den Sonnenstand reagieren.
* **[PLUS] Flache Pfützen:** Eine einfache "Nässe"-Ebene, die die Reflexion auf Blöcken erhöht.
* **[PLUS] Sprite-Wolken:** 2D-Wolkenschichten, die sich mit dem Himmel drehen.
* **[PLUS] Partikel-Rauch:** Standard Minecraft-Partikel, die keine Schatten werfen oder auf Licht reagieren.

---

### **Tier 2: RAYTRACING (Hybrid-Engine)**
*Fokus: Physikalische Genauigkeit für Schatten und Reflexionen. Der "Pro"-Look.*
* **Ray-Traced Shadows:** Pixelgenaue Schatten ohne "Shadow Acne" oder schwebende Schatten ("Peter Panning").
* **SSR (Screen Space Reflections):** Fortgeschrittene Reflexionen, die Spiegel und glänzende Blöcke korrekt darstellen.
* **Punktlicht-Berechnung:** Einzelne Lichtquellen (wie Fackeln) agieren als echte Lichtpunkte im Raum.
* **Kaustik:** Grundlegende Lichtmuster durch Wasser.
* **[PLUS] Variable Penumbra:** Schatten, die nah am Objekt scharf sind und mit zunehmender Entfernung weicher werden.
* **[PLUS] PBR-Unterstützung:** Volles "Physical Based Rendering" (Materialien wirken wie echtes Metall, Stein oder Plastik).
* **[PLUS] Echtzeit-Pfützen:** Nutzt eine "Noise-Map" für variierende Nässe (trockene/nasse Stellen) mit Raytracing-Reflexionen.
* **[PLUS] Volumetrischer Dunst (Basis):** Ein gleichmäßiger Nebel, der in der Ferne dichter wird und leuchtet, wenn die Sonne hineinscheint.
* **[PLUS] Screen-Space Wasser-Interaktion:** Wasser bildet leichte Wellen, wenn sich Spieler oder Wesen hindurchbewegen (vorgetäuschte Physik).
* **[PLUS] 2D Volumetrische Wolken:** Wolken mit "Dicke", die jedoch auf einer flachen Ebene gerendert werden.

---

### **Tier 3: PATHTRACING (Die PTX Hyperrealist-Engine)**
*Fokus: Unendliche Lichtabpraller und spektrale Physik. Deine "Huge"-Vision.*
* **PTGI (Path Traced Global Illumination):** Licht prallt von Wänden ab, um dunkle Räume indirekt zu beleuchten.
* **Voxel-Basierter Tracer:** Die Engine "sieht" jeden Block als physikalisches Objekt für 100% korrekte Lichtblockierung.
* **[PLUS] Oberflächen-Emission:** Licht wird von den **Seitenflächen** der Blöcke emittiert, was scharfe 90-Grad-Lichtkanten erzeugt.
* **[PLUS] Spektrale Dispersion:** Licht bricht sich in "Regenbogen-Kanten" (chromatische Aberration) an kontrastreichen Rändern.
* **[PLUS] Mathematisch scharfe Schatten:** Erzwungene Lichtquellen mit Radius `0.0` für messerscharfe, cineastische Schatten.
* **[PLUS] Quadratisches Abfallsgesetz (Inverse Square Law):** Physikalisch korrekte Lichtabnahme ($1/d^2$) für jede Lichtquelle.
* **Spatio-Temporales Denoising:** Hochwertiges Filtern von "verrauschten" Pixeln für ein flüssiges Bild bei Bewegung.
* **[PLUS] Partikel-zu-Volumen Dunst:** Partikel (wie Lagerfeuer-Rauch) verschmelzen physikalisch mit dem volumetrischen Dunst.
* **[PLUS] 3D Ray-Marched Volumengrafik-Wolken:** Wolken mit echtem Volumen, die Schatten auf sich selbst und den Boden werfen.
* **[PLUS] Extreme Wasser-Interaktion:** * **Lichtbrechende Kaustik:** Licht durch die Wasseroberfläche erzeugt tanzende Muster basierend auf PTX-Strahlen.
    * **Physikalische Verschiebung:** Hochwertige Wellen, die die Geometrie des Wassers verändern.
* **[PLUS] Dynamische Pfützen & Wellen:** Pfützen, die sich über Zeit ansammeln; scharfe Reflexionen von Lichtquellen.
* **[NEW] AVE Data Bridge Integration:** Echtzeit-Abfrage von Attributen via SSBO für datengesteuerte Materialien.
* **[NEW] Spektrale Transparenz:** Lichtmischung durch gefärbtes Glas (Rot + Blau = Lila).
* **[NEW] Selektive Texel-Emission:** Lichter emittieren Farben basierend auf einzelnen Pixeln der Blocktextur.
* **[NEW] Fail-Safe Stabilität:** Automatische Standardwerte für undefinierte Blockdaten oder Regler.

---

### **Bonus "Erweiterungs"-Features (Die "Insane"-Details)**
* **[ADD] Spektrale Wasserbrechung:** Licht biegt sich unter Wasser in verschiedenen Winkeln für Unterwasser-Regenbögen.
* **[ADD] Subsurface Scattering:** Lässt Blätter und Haut "warm" leuchten, wenn Licht von hinten hindurchscheint.
* **[ADD] Mikro-Detail Schatten:** Schatten, die von winzigen Unebenheiten in einer Textur geworfen werden (High-Res PBR).
* **[ADD] Die "Backrooms"-Taschenlampe:** Tragbares Punktlicht mit spektralem Lichtstrahl.
* **[ADD] Spektrale Regenbogen-Pfützen:** Pfützenreflexionen, die spektrale Dispersion zeigen.
* **[ADD] Lokalisierter Dunst:** Nebel, der sich in Senken (Tälern/Höhlen) sammelt.
* **[ADD] Dimensions-Anpassung:** Variablen für Himmelsfarben, Schwerkraft-Visualisierung und Sonnenstrahlung.
* **[ADD] Atmosphäre/Wolken-Details:** Ozon-Dichte und Mie/Rayleigh-Streustärke-Regler.

---

### **VARIABLEN-DEFINITIONEN**

**1. DUNST (Welt, Biom, Custom und Partikel)**
* **h_baseworld (bool):** Aktiviert globalen Weltdunst.
* **hbw_density (0-255):** Partikelanzahl pro Einheit.
* **hbw_densityvariation (0-255):** Bereich der Dichteschwankung.
* **hbw_densityvariationrange (0-255):** Geschwindigkeit der Dichteänderung pro Minute.
* **hbw_color (hex):** Hexcode oder Liste für Farbwahrscheinlichkeiten.
* **hbw_type (0-9):** Typ-Auswahl (Nebel, Dampf, Rauch, Staub, Dunst, etc.).
* **hbw_lightabsorbtion (0-15):** Lichtmenge, die vom Medium absorbiert wird.
* **hbw_lightscattering (0-15):** Lichtmenge, die vom Medium gestreut wird.
* **hbw_heightfalloff (0-15):** Sinkrate (0.1 Blöcke/Sek).
* **hbw_windspeed (0-255):** Windgeschwindigkeit (0.05 Blöcke/Sek).
* **hbw_winddirection (0-360):** Windrichtung in Grad.
* **hbw_anisotropy (-1 bis 1):** Streurichtung (-1: zurück, 1: vorwärts).
* **hbw_noisescale / hbw_noisedetail:** Frequenz und Detailtiefe des Noise-Algorithmus.
* **hbw_groundfog (bool):** Beschränkt Dunst auf niedrige Höhen.
* **hbw_groundheight (0-255):** Maximale Höhe für Bodennebel.
* **h_particlestohaze (bool):** Partikel automatisch als Volumen-Dunst rendern.

**2. LICHT-LOGIK**
* **l_color (hex):** Hauptfarbe des Lichts.
* **lc_variation (hex):** Variationsfarbe.
* **lc_variationamount (0-255):** Geschwindigkeit des Farbwechsels pro Minute.
* **l_flicker (bool):** Aktiviert Flackern der Lichtquelle.
* **lf_rate / lf_intensity:** Frequenz und Stärke des Flackerns.
* **l_absorbtion (0-15):** Blockiert Lichtdurchlass (0: transparent, 15: opak).
* **l_reflection (0-15):** Verhältnis von reflektiertem zu durchgelassenem Licht.
* **l_reflectionblur (0-15):** Rauheit/Unschärfe der Reflexion.
* **l_scattering (bool):** Aktiviert den Streuwinkel des Lichts.
* **l_chromaticabberation (bool):** Aktiviert spektrale Aufspaltung.
* **lc_strength (0-7):** Stärke der Aberration (Basiswert 3).
* **lc_index (0-15):** Brechungsindex-Offset für Dispersion.
* **l_godrays (bool):** Aktiviert volumetrische Lichtschächte.
* **l_falloff_global / l_falloff_world (0-63):** Intensität des quadratischen Lichtabfalls.

**3. PFÜTZEN**
* **p_isdirt (bool):** Aktiviert schlammigen/dreckigen Texturfilter.
* **p_depth (0-15):** Bestimmt Wellenintensität und Spritzer-Größe.

**4. WASSER & FLÜSSIGKEITEN**
* **w_visibility (0-255):** Unterwasser-Sichtweite je nach Biom.
* **w_murkiness (0-255):** Partikeldichte in der Flüssigkeit (Trübung).
* **w_refractionindex (0-15):** Stärke der Lichtbrechung unter Wasser.
* **w_wave_height / w_wave_speed:** Physikalische Verschiebung der Wasseroberfläche.
* **w_viscosity (0-15):** Beeinflusst Wellengeschwindigkeit und Physik-Interaktion.
* **w_dispersion (0-15):** Spektrale Aufspaltung von Unterwasserlicht.
* **w_caustics_intensity (0-255):** Stärke der Lichtbündelung am Boden.

**5. UMGEBUNG & ATMOSPHÄRE**
* **d_sky_color / d_horizon_color (hex):** Farbverläufe des Himmels.
* **d_ambient_light (0-255):** Minimale Helligkeit in totaler Dunkelheit.
* **d_solar_irradiance (0-255):** Rückstrahlkraft des Sonnenlichts.
* **at_ozone_density (0-255):** Absorption von UV/Blauem Licht in der oberen Atmosphäre.
* **at_rayleigh_strength (0-255):** Intensität des Himmelsblaus (Rayleigh-Streuung).
* **at_mie_phase (-1 bis 1):** Phasenfunktion für größere Partikel (Staub/Dunst).
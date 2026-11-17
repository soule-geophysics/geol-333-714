# Glossary

GEOL 333/714 Geophysical Exploration Methods, Fall 2026. The course's
terms, in the course's words; new terms join as each week teaches them.
This file is generated from the course glossary; the Brightspace copy
carries the same content.

### 68-95-99.7 rule

For the normal distribution: about 68% of values land within one standard deviation of the mean, 95% within two, 99.7% within three. The quick test for whether a value's distance from the mean is ordinary scatter. Course text: OpenIntro Statistics Section 4.1. Video: [Normal distribution](https://www.openintro.org/go?id=video_stat_normal_distribution).

### accuracy

How close a result lands to the true value. Limited by systematic error; taking more readings does not improve it.

### air wave

The sound of the source, traveling through the air to the geophones. It is recorded with the ground motion, so it shows up on a seismic record. Sound in air is slow, about 0.33 km/s (the figure GPG gives on the page linked below). Even so, sound in air can be faster than a seismic wave in some surface materials. Burger says to look for the air wave on every record. In Burger's worked example, Table 2.4, the air wave reaches a geophone 60 m from the source at 179.10 ms, well after the direct wave at 40.00 ms. Course text: Burger Sections 2.1.4 and 2.2.8 (Fig. 2.20, Table 2.4). Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/wave_basics.html#wave-velocity-and-particle-velocity" target="_blank" rel="noopener">Wave Velocity and Particle Velocity</a> (CC BY 4.0).

### anomaly

The difference between what we observe and what we can explain. The whole aim of a gravity survey is to explain as much as possible, so that what remains points at the buried body we are looking for. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_data.html#data-presentation-options" target="_blank" rel="noopener">Data presentation options</a> (CC BY 4.0).

### attenuation

The loss of a seismic wave's amplitude as it travels away from the source. Burger gives two main causes. The first is spherical spreading: the wave's energy spreads over a growing sphere, so energy falls off as 1/r² (one over r squared) and amplitude as 1/r (one over r), where r is the distance from the source. The second is absorption: the rock takes up some of the wave's energy along the way. Burger writes absorption as `I = I₀e^(−qr)` (I equals I sub zero times e to the minus q r), where I is the energy intensity at distance r, I₀ is the intensity at the start and q is the absorption coefficient. Energy is also split at every boundary the wave meets. Course text: Burger Sections 2.3.1, 2.3.2 and 2.3.3, Eq. 2.28. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/wave_basics.html#attenuation" target="_blank" rel="noopener">Attenuation</a> (CC BY 4.0).

### base station

A measurement point the survey returns to. Returning to it ties the relative readings to a known value and records how far the instrument drifted while you worked. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_data.html#field-procedures" target="_blank" rel="noopener">Field procedures</a> (CC BY 4.0).

In magnetics, the base station is a magnetometer left at one spot, logging the field all day while the rover reads the line. The change in its record since the first base reading is the diurnal variation. That change is subtracted from each rover reading taken at the same time. A modern magnetometer does not drift the way a gravimeter does, so the magnetic base station tracks the field's change through the day. Course text: Burger Sections 7.4.2 and 7.4.4. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/magnetics/magnetics_survey.html#base-station" target="_blank" rel="noopener">Base Station</a> (CC BY 4.0).

### bob

The weight on the end of a pendulum's string. Ours is a one-inch metal ball.

### body wave

A seismic wave that travels through the inside of Earth rather than along its surface. There are two kinds: P waves and S waves. Body waves travel faster than surface waves, so they reach a seismometer first. Course text: Burger Section 2.1.3. Further reading: Earle, <em>Physical Geology</em>, <a href="https://geo.libretexts.org/Bookshelves/Geology/Physical_Geology_(Earle)/11%3A_Earthquakes/11.03%3A_Measuring_Earthquakes" target="_blank" rel="noopener">11.3 Measuring Earthquakes</a> (CC BY 4.0); UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/wave_basics.html#body-waves" target="_blank" rel="noopener">Body Waves</a> (CC BY 4.0).

### Bouguer anomaly

What remains of the difference between two gravity readings once the instrument and the stations' elevations have been accounted for: in our surveys, the drift removed, the field days tied to a common reference, the free-air correction added back and the slab correction subtracted. It is the quantity a survey interprets. It still contains everything the corrections did not remove, including whatever broad structure runs under the whole line, which is why a regional is usually separated from it before anything local is claimed. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_data.html#data-presentation-options" target="_blank" rel="noopener">Data presentation options</a> (CC BY 4.0).

### Bouguer correction

The correction that removes the pull of the rock lying between a station and the datum. The free-air correction treats that space as empty; this one models it as a flat slab of thickness h and density ρ whose attraction is 2πGρh, and subtracts it. We wrote it at the board as 0.04193 ρ h mGal, with ρ in g/cm³ and h in meters. It needs a density nobody measured, so the value used is a choice that has to be stated and defended. UBC-GIF, linked below, writes the same coefficient as 0.04191 rather than the 0.04193 we used at the board. The difference is the value of the gravitational constant G each was computed from, and it lands in the fourth significant figure, well below anything a survey of this size can resolve. Use the board form; the point is that a constant quoted to four figures still depends on a measurement somebody made. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_data.html#corrections" target="_blank" rel="noopener">Corrections</a> (CC BY 4.0).

### bulk modulus, K

How strongly a material resists being squeezed into a smaller volume. Burger defines it as the change in pressure divided by the fractional change in volume it causes, `K = ΔP/Δ` (K equals delta P over delta), where Δ is the change in volume divided by the starting volume. A large K means a material is hard to compress. K appears in the P-wave velocity and not in the S-wave velocity, so it is one reason P waves are faster. Course text: Burger Section 2.1.2, Eq. 2.7, and Section 2.1.4, Eq. 2.11. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/wave_basics.html#body-waves" target="_blank" rel="noopener">Body Waves</a> (CC BY 4.0).

### correlation

A number between −1 and +1 for how tightly two quantities follow a straight line together, and
in which direction. Course text: OpenIntro Statistics Section 8.1. Video: [Line fitting, residuals, and correlation](https://www.openintro.org/go?id=video_stat_linear_regression_line_fitting_residuals_correlation).

### covariance matrix

The table of uncertainties a least-squares fit returns. The square roots of its diagonal
entries are the standard errors of the slope and the intercept, which is where every fitted
slope's error bar in this course comes from.

### critical angle, θic

The angle of incidence at which the refracted ray bends to 90° and travels along the boundary. It comes from Snell's law with the refracted angle set to 90°: `θic = sin⁻¹(V1/V2)` (theta i c equals the inverse sine of V1 over V2). A critical angle exists only when the lower layer is faster, V2 greater than V1. Burger's example in Table 2.3 uses 1500 m/s over 4000 m/s: the critical angle is 22°, and at 23° there is no refracted angle at all. At incidence beyond the critical angle, all of the energy is reflected. At the critical angle, the ray traveling along the boundary sets up the head wave. Course text: Burger Section 2.2.6, Eq. 2.27, Fig. 2.16 and 2.17. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/waves_at_interfaces.html#critical-angle" target="_blank" rel="noopener">Critical angle</a> (CC BY 4.0). It writes the critical angle as θ_c.

### critical distance

The distance from the source to the nearest point where the head wave reaches the surface. Head-wave energy leaves the boundary at the critical angle, starting from the point where a ray from the source first meets the boundary at that angle. Closer to the source than the critical distance, no head wave arrives at all. Burger writes it `x_crit` (x crit): `x_crit = 2 h1 / √((V2/V1)² − 1)` (x crit equals two h1 over the square root of the quantity V2 over V1 squared, minus one), where h1 is the thickness of the top layer. In Burger's Table 3.1 (1400 m/s over 4500 m/s), a top layer 10 m thick gives a critical distance of 6.55 m. Between the critical distance and the crossover distance, the head wave arrives after the direct wave. The first breaks there are still the direct wave. Course text: Burger Section 3.2.5 (Fig. 3.5, Eq. 3.25, Table 3.1).

### crossover distance

The distance from the source at which the direct wave and the head wave arrive at the same time. On a time-distance plot it is where the two lines cross. Closer to the source, the direct wave arrives first. Beyond the crossover distance, the head wave arrives first. Its path is longer, but it covers most of that path along the boundary at the faster velocity V2. In Burger's Table 3.1 (1400 m/s over 4500 m/s, a layer 10 m thick) the two lines cross between 27 m and 30 m. Course text: Burger Section 3.2.4, and Table 3.1 in Section 3.2.2. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/traveltimes.html" target="_blank" rel="noopener">Travel times</a> (CC BY 4.0).

### datum

The surface every corrected reading is referred back to. The corrections do not produce absolute gravity; they produce gravity as it would have been read at the datum. In our surveys the datum is the base station's elevation, so a corrected station value answers one question: how much does this place differ from the base, once the instrument and the elevation have been accounted for.

### declination

The angle between magnetic north and geographic north, measured in the horizontal plane. A compass needle points along the horizontal part of the Earth's field, so it is off true north by the declination. Burger writes it d: the northward part of the horizontal field is `X_E = H_E cos d` (X sub E equals H sub E times cosine d) and the eastward part is `Y_E = H_E sin d` (Y sub E equals H sub E times sine d). Course text: Burger Section 7.2.1, Eq. 7.9. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/magnetics/magnetics_basic_principles.html#earth-s-magnetic-field-source" target="_blank" rel="noopener">Earth's magnetic field (Source)</a> (CC BY 4.0). It writes the declination as D.

### determinant

A single number computed from a square matrix; for a 2x2 it is `ad - bc` (a d minus b c). It tells you whether a system of equations has one answer: when the determinant is zero the two lines are parallel or identical, so there is no unique solution, and the solver calls the system singular.

### dial constant

The number that converts a gravimeter's dial reading into milligals. The instrument does not read gravity directly. It reads a position on a dial, and the dial constant is the calibration that turns dial divisions into mGal. It belongs to the individual meter and comes from its calibration, so using the wrong one scales every reading in a survey by the same wrong factor, which is a systematic error rather than a random one. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_data.html#field-procedures" target="_blank" rel="noopener">Field procedures</a> (CC BY 4.0).

### dipole

Two nearby poles of equal strength and opposite sign. A magnetized body whose size is small compared with its distance from the sensor behaves as a dipole. So does the Earth's main field, to a first approximation. On the dipole's axis the field is `H_r = 2M/r³` (H sub r equals two M over r cubed; Burger Eq. 7.12), where M is the dipole's moment and r the distance from its center. Here H is Burger's symbol for field strength. It is a different quantity from the horizontal component, H. Doubling the distance cuts the field to one eighth. A gravity anomaly falls off as 1/r², so a magnetic anomaly from a compact body is narrower and dies away faster with depth. Course text: Burger Section 7.2.4. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/magnetics/magnetics_basic_principles.html#fields-due-to-a-magnetic-dipole" target="_blank" rel="noopener">Fields due to a magnetic dipole</a> (CC BY 4.0).

### direct wave

The wave that travels straight through the top layer from the source to a geophone, at the top layer's velocity V1. Its travel time is `t = x/V1` (t equals x over V1), where x is the distance from the source. On a time-distance plot it is a straight line through the origin with slope 1/V1 (one over V1). Near the source it is the first wave to arrive. Course text: Burger Section 2.2.8 (Fig. 2.20) and Section 3.1, Eq. 3.2. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/traveltimes.html" target="_blank" rel="noopener">Travel times</a> (CC BY 4.0).

### diurnal variation and the diurnal correction

The diurnal variation is the change in the measured field through the day at one spot, several to a few tens of nT. Its source is outside the Earth: currents in the upper atmosphere driven by the Sun. It is corrected the way gravimeter drift is: a base station logs the field all day, and each rover reading has the base station's change since the start subtracted from it, `corrected = rover − (base − first base reading)` (corrected equals the rover reading minus the quantity base reading minus first base reading). This works because the outside source changes the field by the same amount at the base station and on the survey line at the same moment. When the field rises during a survey, the correction lowers the rover readings. During a magnetic storm the variation is too large to correct, and the survey stops. Course text: Burger Section 7.4.2. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/magnetics/magnetics_processing.html#removal-of-time-variations" target="_blank" rel="noopener">Removal of time variations</a> (CC BY 4.0). British Geological Survey, <a href="https://geomag.bgs.ac.uk/education/earthmag.html" target="_blank" rel="noopener">The Earth's Magnetic Field: An Overview</a>, section 3.6.

### drift

The slow change in a gravimeter's reading while the meter sits still. Two things cause it: the spring creeps under its load, and temperature changes its stiffness; the tidal effect rides on top. A survey tracks the combined change by re-occupying the base station, two readings at the least and a fitted line when there are more, and corrects each reading by how much had accumulated when it was taken. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_data.html#corrections" target="_blank" rel="noopener">Corrections</a> (CC BY 4.0).

### elasticity

The property of a material that deforms under an applied force and returns to its original shape when the force is removed. For small deformations the strain is proportional to the stress, which is Hooke's law: double the load and the stretch doubles, remove the load and the stretch goes to zero. The constants of proportionality are the elastic moduli: Young's modulus for stretching, the bulk modulus for squeezing, the shear modulus for twisting. Rock is elastic at the strains a seismic wave carries, and those moduli with density set the wave's speed.

### equivalence principle

The mass gravity pulls on is the same as the mass that resists a push, so when gravity is the only force acting, everything falls with the same g. It is the reason the bob's mass drops out of the pendulum's period. Course text: Burger Section 6.1.1, Eqs. 6.2-6.4, where `F = ma` (F equals m a) set against `F = GmM/R²` (F equals G m M over R squared) lets the m cancel.

### error bar (uncertainty)

The ± reported with a value: the range a repeat of the same experiment could reasonably land in. A result in this course is a value with its error bar. The course's error bars are one sigma; see sigma.

### excess mass

The difference between the mass of a buried body and the mass of host rock that would fill the same volume: the volume times the density contrast, `V Δρ` (V times delta rho). Gravity responds to the excess mass alone. A void or a low-density fill has a negative excess mass, a mass deficit, and produces a gravity low. The excess mass differs from the body's total mass, `V ρ_body` (V times the density of the body), which is what a mine would haul out. For a sphere, `M_e = (4/3)πR³Δρ` (M sub e equals four thirds pi R cubed delta rho), and the anomaly directly above the center is `G M_e / z²` (G M sub e over z squared). A small dense sphere and a larger, less dense sphere at the same depth with the same excess mass produce the same anomaly. Course text: Burger Section 6.5.2. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_basics.html#what-is-actually-measured" target="_blank" rel="noopener">What is actually measured?</a> (CC BY 4.0). It writes the density contrast the other way round, host rock minus body.

### Fermat's principle

A wave travels between two points along the path that takes the least time. Burger uses the principle to show that the angle of reflection equals the angle of incidence, and again to derive Snell's law. Course text: Burger Sections 2.2.2, 2.2.3 (Eq. 2.18) and 2.2.4 (Eq. 2.25).

### first break

The moment the ground first moves at a geophone: the earliest arrival on its trace. Picking the first break on each trace gives one arrival time per geophone. Plotted against distance from the source, those times make the time-distance plot used in a refraction survey. Near the source the first break is the direct wave; beyond the crossover distance it is the head wave. Course text: Burger Section 3.2.6 (Fig. 3.6, Table 3.3). Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/seismic_data.html#signals-that-get-recorded" target="_blank" rel="noopener">Signals that get recorded</a> (CC BY 4.0). It also calls first breaks first arrivals.

### free-air correction

The correction that accounts for a station sitting above or below the datum, treating everything in between as empty air. Gravity falls with distance from Earth's center at about 0.3086 mGal per meter, so the correction adds back what a station above the datum lost and subtracts from one below it. It is the free-air gradient applied to a real station's elevation. Applied on its own it leaves the rock between the station and the datum unaccounted for, which is what the Bouguer correction handles. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_data.html#corrections" target="_blank" rel="noopener">Corrections</a> (CC BY 4.0).

### free-air gradient

The rate gravity decreases with elevation: about 0.3086 mGal per meter (milligals per meter). Climbing one floor of a building lowers g by about one milligal. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_data.html#corrections" target="_blank" rel="noopener">Corrections</a> (CC BY 4.0).

### G and g

`G` is the universal gravitational constant, `6.674 × 10⁻¹¹ m³ kg⁻¹ s⁻²`, the same everywhere in the universe. `g` is the strength of gravity where you stand, about `9.81 m/s²`, and it changes with latitude, elevation, and what sits underneath you. The course measures g; nature fixes G. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_basics.html#fundamentals" target="_blank" rel="noopener">Fundamentals</a> (CC BY 4.0).

### geophone

The sensor of a land seismic survey. It is a small case with a spike that is pushed into the ground. Inside, a coil of wire sits on springs in the field of a magnet. When the ground moves, the coil and the magnet move relative to each other, and that motion produces a voltage. The recorder stores the voltage against time. A survey lays out a line of geophones at measured distances from the source. Course text: Burger Section 2.5.1. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/seismic_receivers.html" target="_blank" rel="noopener">Receivers</a> (CC BY 4.0).

### gravimeter

The field instrument for gravity: a mass on a very soft spring in a rigid case. To take a reading, you turn a screw a known amount to bring the mass back to a fixed resting mark, and the screw's counter is the reading. It reads changes in g, in milligals. The What a Gravimeter Is page carries the full story. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_basics.html#measuring-gravity" target="_blank" rel="noopener">Measuring gravity</a> and <a href="https://gpg.geosci.xyz/content/gravity/gravity_data.html#instrumentation-part-i" target="_blank" rel="noopener">Instrumentation part I</a> (CC BY 4.0).

### ground roll

A surface wave from the source that travels along the ground. It is slower than the body waves, so it arrives late. In Burger's worked example, Table 2.4, ground roll reaches a geophone 60 m from the source at 88.89 ms, after the direct wave at 40.00 ms. Course text: Burger Section 2.2.8 (Fig. 2.20, Table 2.4). Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/wave_basics.html#surface-waves" target="_blank" rel="noopener">Surface Waves</a> (CC BY 4.0).

### the set of gravity corrections

The sequence applied to raw gravimeter readings before anything is interpreted. Each one repairs a different hidden assumption in `g = GM/R²` (g equals G M over R squared): drift for the instrument moving while you work, tidal for the Sun and Moon, latitude for Earth being an ellipsoid rather than a sphere, free-air for the observer standing above the datum, Bouguer for the rock in between, terrain for the ground not being flat, isostatic for the crust floating on the mantle. What survives all of them is the anomaly, and what a survey can claim depends on which corrections were applied and how well. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_data.html#corrections" target="_blank" rel="noopener">Corrections</a> (CC BY 4.0).

### half-maximum technique (depth rule)

A depth estimate read from an anomaly's width. The deeper a body, the broader and lower its anomaly, so once a shape is assumed the half-width fixes the depth. For a sphere, `z = 1.305 x½` (z equals one point three zero five times the half-width; Burger Eq. 6.54); for a horizontal cylinder, `z = x½` (z equals the half-width; Eq. 6.55). Both give the depth to the body's center or axis. An infinite slab has no depth rule, because its attraction, `2πGΔρh` (two pi G delta rho h), with h the slab's thickness, does not depend on depth. The result depends on the shape assumed: the same half-width places a sphere's center deeper than a cylinder's axis. It also depends on how cleanly the regional was removed. Course text: Burger Section 6.7.1. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_basics.html#what-is-actually-measured" target="_blank" rel="noopener">What is actually measured?</a> (CC BY 4.0).

### half-width (x½)

The horizontal distance from the peak (or trough, for a low) of an anomaly to the point where it has fallen to half its peak amplitude. The amplitude is measured from the background level, so the half level is the background plus half the amplitude. When the two sides of a profile differ, this course takes the half-width as the average of the two distances. That equals half the full width at half maximum. Burger writes it x½max (x sub one-half max). It is the input to the half-maximum technique. Course text: Burger Section 6.7.1. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_basics.html#what-is-actually-measured" target="_blank" rel="noopener">What is actually measured?</a> (CC BY 4.0).

### head wave

The refracted arrival used in a refraction survey. A ray from the source strikes a boundary at the critical angle, and the refracted ray then travels along the boundary at the lower layer's velocity V2. As it travels, it sends energy back up into the top layer at the critical angle. That returning energy is the head wave. On a time-distance plot it is a straight line with slope 1/V2 (one over V2), and it meets the time axis above the origin. Beyond the crossover distance it is the first wave to arrive. A head wave forms only when the lower layer is faster. Burger also calls it the critically refracted wave. Course text: Burger Section 2.2.6 (Fig. 2.16) and Section 3.2.1, Eq. 3.15. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/traveltimes.html#refracted-ray-in-a-two-layered-earth" target="_blank" rel="noopener">Refracted ray in a two layered-earth</a> (CC BY 4.0).

### histogram

A bar chart of a set of repeated measurements: each bar counts how many values landed in its slice of the number line. Course text: OpenIntro Statistics Section 2.1. Video: [Examining numerical data](https://www.openintro.org/go?id=video_stat_numerical_data).

### Hooke's law

The rule that a spring's restoring force is proportional to how far it has been stretched, `F = −kx` (F equals minus k x), where k is the spring constant and the minus sign says the force opposes the stretch. It holds for small deformations, which is the elastic regime. A gravimeter is built on it: a mass hangs on a spring, a change in gravity changes the force on that mass, and the spring's length changes in proportion, so measuring a length becomes measuring gravity. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_basics.html#measuring-gravity" target="_blank" rel="noopener">Measuring gravity</a> (CC BY 4.0).

For rock, Burger writes Hooke's law as stress and strain: `σ = Eε` (sigma equals E times epsilon), where σ is the force per unit area, ε is the fractional change in length and E is Young's modulus. Seismic waves strain rock by tiny amounts, so rock follows this law as a wave passes. Course text: Burger Section 2.1.2, Eq. 2.4.

### horizontal component, H

The horizontal part of the Earth's field, pointing toward magnetic north: `H = F cos i` (H equals F times cosine i), where F is the total field and i the inclination. It is largest at the magnetic equator and zero at the magnetic poles. The horizontal part of a buried body's own field, measured toward magnetic north, is written H_A. Course text: Burger Section 7.2.1, Eq. 7.9. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/magnetics/magnetics_basic_principles.html#earth-s-magnetic-field-source" target="_blank" rel="noopener">Earth's magnetic field (Source)</a> (CC BY 4.0).

### horizontal cylinder (simple-shape model)

The model for a buried body much longer than it is wide, such as a tunnel, a buried channel or a pipe, with the profile crossing it at right angles. R is the cylinder's radius, z the depth to its axis, and Δρ (delta rho) the density contrast. Its anomaly is `Δg(x) = 2πGΔρR²z / (x² + z²)` (delta g of x equals two pi G delta rho R squared z, over x squared plus z squared), largest directly above the axis, where it equals `2πGΔρR² / z` (two pi G delta rho R squared over z). With distance from the axis it falls off more slowly than a sphere's anomaly. Depth rule: `z = x½` (z equals the half-width). Course text: Burger Section 6.5.3. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_basics.html#what-is-actually-measured" target="_blank" rel="noopener">What is actually measured?</a> (CC BY 4.0). It writes the density contrast the other way round, host rock minus body.

### Huygens' principle

Every point on a wave front acts as a small source that sends out its own spherical wavelet. A short time later, the new wave front is the surface that touches all of those wavelets. Each wavelet's radius is the velocity times the time step, so a wavelet in faster rock grows larger. Burger uses this construction to show how a wave front reflects at a boundary and how it bends when it crosses into rock of a different velocity. Course text: Burger Section 2.2.1 (Fig. 2.10), with its use in Sections 2.2.3 and 2.2.4.

### IGRF

The International Geomagnetic Reference Field: the global model of the Earth's main field, updated every five years. It gives the field's strength and direction at any place and date. Subtracting the IGRF value for the survey area from the corrected readings removes the Earth's main field, `anomaly = corrected − IGRF` (anomaly equals the corrected reading minus the IGRF value). The result still contains any broad regional trend. That trend is separated as in gravity. Course text: Burger Section 7.4.4. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/magnetics/magnetics_basic_principles.html#the-igrf" target="_blank" rel="noopener">The IGRF</a> (CC BY 4.0).

### impedance contrast

The jump in a material property across a boundary that makes the boundary reflect. No jump, no echo, and the boundary is invisible even though it is right there. Each method has its own impedance: seismic impedance is density times wave speed; radar impedance is set by the electrical properties, and water dominates those. Both are mostly set by how much pore space is down there and what is sitting in it, which is why the two often light up the same boundary. Module 3 works the seismic case. Course resource: [Seismic Reflection](https://www.iris.edu/hq/inclass/lesson/seismic_reflection) (EarthScope/IRIS, CC BY 4.0).

### inclination

The angle the Earth's field plunges below the horizontal, written i. In the southern hemisphere the field points upward, and i is negative, down to −90° at the south magnetic pole. It is 0° at the magnetic equator, 90° at the north magnetic pole, and about 65° at Queens. It fixes how the field splits into its parts, `tan i = Z/H` (tangent i equals Z over H), and it sets the shape of a magnetic anomaly: at most inclinations the anomaly over a buried body is lopsided, and at the pole it is symmetric. Course text: Burger Section 7.2.1, Eq. 7.9. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/magnetics/magnetics_basic_principles.html#earth-s-magnetic-field-source" target="_blank" rel="noopener">Earth's magnetic field (Source)</a> (CC BY 4.0). It writes the inclination as I. Burger and this course write i, because Burger's I is the magnetization.

### induced magnetization

Magnetization a rock acquires from the field it sits in today. It points along the Earth's field, and its strength is the susceptibility times the field, `I = kF_E` (I equals k times F sub E). Burger writes Eq. 7.7 as `I = kH` (I equals k times H), with H the whole field acting on the rock. Remove the field and induced magnetization goes away. The anomaly formulas in this course assume all magnetization is induced. Course text: Burger Section 7.1.5, Eq. 7.7. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/magnetics/magnetics_basic_principles.html#magnetization" target="_blank" rel="noopener">Magnetization</a> (CC BY 4.0). It writes the magnetization as M and the susceptibility as κ (kappa). In Burger, M is the dipole moment. Burger's symbol for the magnetization is I.

### intercept time, ti

The time where the head-wave line on a time-distance plot, extended back to zero distance, meets the time axis. Burger writes it `ti` (t i). No head wave arrives at zero distance. The line is drawn back to the time axis because the thickness of the top layer is calculated from that time. For one flat layer over a faster one, `h1 = (ti/2) V2 V1 / √(V2² − V1²)` (h1 equals ti over two, times V2 times V1, over the square root of V2 squared minus V1 squared). Put ti in seconds and both velocities in meters per second. Then h1 comes out in meters. A thicker top layer gives a larger intercept time. In Burger's Table 3.1 (1400 m/s over 4500 m/s, a layer 10 m thick) the head-wave line meets the time axis at 13.58 ms. The intercept time usually gives a better thickness than the crossover distance. It comes from one fitted line, and the crossover distance comes from two. With three flat layers, each head-wave line has its own intercept time (Burger Section 3.3). Course text: Burger Section 3.2.3, Eq. 3.17, Table 3.1 in Section 3.2.2, and Section 3.2.4 on the comparison with the crossover distance.

### inverse problem

Working backward from observed data to the properties of the body that produced them, as in estimating a depth from an anomaly's width. The forward problem runs the other way: given a body, compute its anomaly. The simple-shape formulas are forward models, and the depth rules invert them. A gravity inverse problem has more than one answer, so an assumed shape or density is part of every result. Course text: Burger Section 6.7. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/foundations/foundations_inversion.html" target="_blank" rel="noopener">Inversion outline</a> (CC BY 4.0).

### latitude correction

The correction for Earth being an ellipsoid rather than a sphere, and rotating. Normal gravity rises from the equator toward the pole, so two stations at different latitudes read differently before any geology is involved. The northward gradient is `0.811 sin 2φ` (zero point eight one one times sine of two phi) mGal per kilometer, where φ is the latitude. It is largest near 45 degrees and goes to zero at the equator and at the poles. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_data.html#corrections" target="_blank" rel="noopener">Corrections</a> (CC BY 4.0).

### least squares

The fitting recipe that picks the line with the smallest total of squared vertical distances between the data points and the line. Week 2 works it on the board; the homework uses it wherever a slope carries physics. Course text: OpenIntro Statistics Section 8.2. Video: [Fitting a Line with Least Squares Regression](https://www.openintro.org/go?id=video_stat_linear_regression_fitting_least_squares_line).

### Love wave

A surface wave in which the ground moves horizontally, at right angles to the direction the wave travels. Its motion gets smaller with depth. Love waves are usually not generated in exploration work. Surface waves usually have larger amplitudes than body waves, and they do more damage. Course text: Burger Sections 2.1.3 and 2.1.4. Further reading: Earle, <em>Physical Geology, 2nd Edition</em>, <a href="https://opentextbc.ca/physicalgeology2ed/chapter/11-3-measuring-earthquakes/" target="_blank" rel="noopener">11.3 Measuring Earthquakes</a> (CC BY 4.0); UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/wave_basics.html#surface-waves" target="_blank" rel="noopener">Surface Waves</a> (CC BY 4.0).

### matrix

A rectangular grid of numbers. In this course a matrix carries a whole system of equations at once: Week 2 solves a 2x2 system by hand, then writes the least-squares fit as the normal equations `(AtA)m = Atd` (A transpose A m equals A transpose d) and solves that same 2x2 shape built from 25 data points. The Matrix Methods card in the Math Reference Cards works the 2x2 case by hand.

### mean

The best single value a set of repeated measurements gives: the sum divided by the count. Course text: OpenIntro Statistics Section 2.1. Video: [Examining numerical data](https://www.openintro.org/go?id=video_stat_numerical_data).

### median

The middle value once the data are sorted: half the measurements sit below it, half above.
`describe()` prints it as the 50% row. Course text: OpenIntro Statistics Section 2.1. Video: [Examining numerical data](https://www.openintro.org/go?id=video_stat_numerical_data).

### milligal (mGal)

The working unit of field gravity: `1 mGal = 10⁻⁵ m/s²` (ten to the minus five meters per second squared), about one part per million of g. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_basics.html#units" target="_blank" rel="noopener">Units</a> (CC BY 4.0).

### model

A mathematical claim about how the world behaves, written so data can test it. The word also names a proposed body underground, such as a buried sphere, whose computed anomaly is compared with the survey; the simple-shape entries are models in this sense.
`T = 2π√(l/g)` (T equals two pi root l over g) is HW0's model; an anomaly is always measured
against one. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/foundations/foundations_model_types.html" target="_blank" rel="noopener">Mathematical representations of the Earth</a> (CC BY 4.0).

### nanotesla (nT)

The working unit of field magnetics: `1 nT = 10⁻⁹ T` (one nanotesla equals ten to the minus nine tesla). The Earth's field is about 51,000 nT at Queens. Anomalies from buried bodies range from under 1 nT to thousands of nT. Burger's Chapter 7 examples run from about 3 nT to over 1,000 nT. A proton-precession magnetometer reads to about 1 nT. The gamma of older texts is the same size as the nanotesla. Course text: Burger Section 7.1.2. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/magnetics/magnetics_basic_principles.html#the-igrf" target="_blank" rel="noopener">The IGRF</a> (CC BY 4.0).

### Nettleton's method (density sweep)

A way to choose the reduction density from the survey itself. Reduce the profile at a range of densities and keep the one at which the anomaly is least correlated with station elevation. The reasoning is that the density of buried rock is independent of the shape of the ground surface, so a remaining match between the anomaly and elevation points to a slab correction made at the wrong density. Source: Nettleton, L. L. (1939), Determination of density for reduction of gravimeter observations, <em>Geophysics</em> 4(3), 176–183, doi:10.1190/1.1437088.

### Newton's law of universal gravitation

Every mass pulls every other, along the line between them, with force `F = GMm/r²` (F equals G M m over r squared). Its surface form, `g = GM/R²` (g equals G M over R squared), gives the gravity at a planet's surface. It rests on assumptions the course tests one by one. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_basics.html#fundamentals" target="_blank" rel="noopener">Fundamentals</a> (CC BY 4.0).

### noise floor (detectability)

The size of the measurement scatter a survey cannot see below: the repeatability of readings taken at one place, quoted as one standard deviation. In HW2b it is the standard deviation of the corrected base-station reads. An anomaly is judged against it: the ratio of the anomaly's amplitude to the noise floor, read with the 68-95-99.7 rule, says how plausibly measurement scatter alone could have produced it.

### normal distribution

The bell-shaped curve that stacks of repeated measurements approach. Its width is the standard deviation, and it obeys the 68-95-99.7 rule. Course text: OpenIntro Statistics Section 4.1. Video: [Normal distribution](https://www.openintro.org/go?id=video_stat_normal_distribution).

### outlier

A measurement that sits far from the rest of its stack. One is never deleted silently: the
analysis states it, then shows the result with and without it. Course text: OpenIntro Statistics Section 2.1.5. Video: [Examining numerical data](https://www.openintro.org/go?id=video_stat_numerical_data).

### P wave

A seismic wave in which the ground moves back and forth in the same direction the wave travels, alternately squeezing and stretching the material. P stands for primary: it is the fastest seismic wave, so it arrives first at a seismograph. It travels through solids and liquids. It is also called a compressional wave. Course text: Burger Section 2.1.3. Further reading: Earle, <em>Physical Geology, 2nd Edition</em>, <a href="https://opentextbc.ca/physicalgeology2ed/chapter/9-1-understanding-earth-through-seismology/" target="_blank" rel="noopener">9.1 Understanding Earth Through Seismology</a> (CC BY 4.0); UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/wave_basics.html#body-waves" target="_blank" rel="noopener">Body Waves</a> (CC BY 4.0).

### pendulum length (l)

The distance from the pivot to the **center** of the bob. A mark at the top of the bob sits half the bob's height above its center. Measuring to the mark and calling it `l` makes `g` come out low when you compute `g` from a single length, by more than the stopwatch scatter. In the multi-length fit of `T²` against `l` (T squared against l), the same constant offset moves the intercept and leaves the slope, so the `g` taken from the slope is unchanged.

### period (T)

The time for one complete swing. Our protocol times ten complete swings and divides by ten, which shares one stopwatch error across ten periods.

For a wave, the period is the time between two crests passing one point. Its inverse is the frequency, `f = 1/T` (f equals one over T). Course text: Burger Section 2.1.1, Eq. 2.1.

### Poisson's ratio, μ

How much a material narrows sideways when it is stretched lengthwise, or bulges sideways when it is squeezed. It is the sideways strain divided by the lengthwise strain, with the sign set so the ratio is positive. Burger gives 0.5 as its upper limit. In Burger's Table 2.1 it runs from 0.040 to 0.271 for the rocks listed. With Young's modulus and density it gives both seismic velocities. On its own it fixes their ratio, V_P/V_S. Course text: Burger Section 2.1.2, Eq. 2.6, and Section 2.1.4, Eq. 2.13. Burger writes Poisson's ratio as μ (mu). GPG uses μ for the shear modulus.

### potential field

A field, like gravity or magnetism, where a reading is the summed pull of every source at once, near or far. There is no way to send in a signal and listen for an echo. Gravity and magnetics are the course's two potential-field methods.

### precision

How tightly repeated measurements agree with each other. Limited by random error. Averaging N readings does not tighten the readings themselves; it steadies their mean by a factor of the square root of N.

### probability density function (PDF)

The smooth curve the histogram of a stack of repeated measurements approaches as the stack grows, once the histogram is scaled so its total area is one. The normal distribution is the one our measurements follow. Course text: OpenIntro Statistics Section 3.5.

### property contrast

A difference in a physical property (density, how strongly the rock is magnetized, or how fast seismic waves travel through it) between a buried body and its surroundings. In gravity the property is density, and the difference is the density contrast, Δρ (delta rho), which Burger writes ρ_c. A body with no contrast in the property a method senses is invisible to that method. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_basics.html#the-physical-property-density" target="_blank" rel="noopener">The physical property: density</a> (CC BY 4.0).

### proton-precession magnetometer (PPM)

A magnetometer that reads the strength of the total field, F, and nothing about its direction. It is routinely precise to about ±1 nT and does not need to be leveled or pointed. A steep field gradient, near a steel object for instance, spoils the reading. Course text: Burger Section 7.3.2. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/magnetics/magnetics_survey.html#proton-precession-magnetometer" target="_blank" rel="noopener">Proton Precession Magnetometer</a> (CC BY 4.0).

### quartile (percentile)

The 25% and 75% rows of `describe()`: one quarter of the data sits below the first quartile,
three quarters below the third. A percentile generalizes this: the value below which that
percent of the data sits. Course text: OpenIntro Statistics Section 2.1.

### random error

Scatter that changes size and sign from trial to trial, like the small timing errors from pressing a stopwatch. Averaging N trials shrinks the uncertainty of the average by the square root of N.

### ray (ray path)

A line drawn at right angles to the wave fronts, pointing the way the wave's energy travels. A ray path is the route a ray takes from the source to a geophone, including where it bends or reflects at a boundary. Rays are a drawing tool: they make reflection and refraction easy to sketch and to compute with Snell's law. They stop giving correct answers when an object is not much larger than the wavelength. Course text: Burger Sections 2.1 and 2.2 (the ray limit is in Section 2.2.7). Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/wave_basics.html#waves-and-rays" target="_blank" rel="noopener">Waves and Rays</a> (CC BY 4.0).

### Rayleigh wave

A surface wave in which the ground moves in ellipses in the vertical plane, along the direction the wave travels, like a wave on water. The motion gets smaller with depth. Rayleigh waves are about 10 percent slower than S waves. Course text: Burger Section 2.1.3. Further reading: Earle, <em>Physical Geology, 2nd Edition</em>, <a href="https://opentextbc.ca/physicalgeology2ed/chapter/11-3-measuring-earthquakes/" target="_blank" rel="noopener">11.3 Measuring Earthquakes</a> (CC BY 4.0); UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/wave_basics.html#surface-waves" target="_blank" rel="noopener">Surface Waves</a> (CC BY 4.0).

### reduction density

The density assumed for the rock between a station and the datum when the Bouguer correction is computed. Texts quote 2.67 g/cm³ for average continental crust, but the material under a particular survey may be nothing like that, and the anomaly that comes out depends on the number chosen.

### reduction to the pole

A processing step. From the anomaly measured at the survey's inclination, it computes the anomaly that would have been measured if the Earth's field were vertical, as at the magnetic pole. At the pole the H_A term of the total-field anomaly drops out, so the anomaly over a compact body is symmetric, with its peak over the body. The calculation assumes the magnetization is all induced. A body with strong remanent magnetization is not moved to the right place. Magnetic maps are often shown reduced to the pole so that each high sits over its source. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/magnetics/magnetics_processing.html#reduction-to-pole" target="_blank" rel="noopener">Reduction to Pole</a> (CC BY 4.0).

### reflected wave

The part of a wave that bounces back up from a boundary between two layers. The angle of reflection equals the angle of incidence, both measured from the line at right angles to the boundary. The reflected wave travels at the top layer's velocity V1, like the direct wave, but its path down and back up is longer. So it arrives after the direct wave at every distance and is never a first break. In Burger's Table 2.4 the reflected wave reaches 60 m at 44.72 ms and the direct wave at 40.00 ms. Course text: Burger Section 2.2.3, Eq. 2.18, and Section 2.2.8 (Fig. 2.20, Table 2.4). Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/traveltimes.html#reflected-rays-single-layer" target="_blank" rel="noopener">Reflected rays - single layer</a> (CC BY 4.0).

### refraction (refracted wave)

The bending of a wave as it crosses a boundary into rock of a different velocity. The wave that continues into the lower layer is the refracted wave. Going into faster rock, the ray bends away from the line at right angles to the boundary. Going into slower rock, it bends toward that line. Snell's law gives the new angle. In Burger's Table 2.3 (1500 m/s over 4000 m/s), a ray arriving at 10° leaves at 28°. Course text: Burger Sections 2.2.4 and 2.2.5, Table 2.3. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/waves_at_interfaces.html#angles-of-reflection-and-refraction" target="_blank" rel="noopener">Angles of reflection and refraction</a> (CC BY 4.0).

### regional

The broad, slowly varying part of a gravity profile or map, produced by structure deeper or wider than the target: a thickening sediment cover, a dipping contact, relief on the basement, or the change in normal gravity with latitude. It is removed to leave the residual anomaly. Whether a feature counts as regional depends on what the survey is looking for; the same curve can be the regional in one survey and the target in another. In HW2a the regional is a straight line fitted by least squares; Burger calls a fitted polynomial of this kind a trend surface. Course text: Burger Sections 6.6.1 and 6.6.2. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_data.html#data-presentation-options" target="_blank" rel="noopener">Data presentation options</a> and <a href="https://gpg.geosci.xyz/content/gravity/gravity_example.html" target="_blank" rel="noopener">Gravity example</a> (CC BY 4.0).

### relative and absolute measurement

A spring gravimeter reads differences between stations; an absolute gravimeter drops a mirror in a vacuum chamber and times its fall with a laser to read g itself. Surveys read differences and tie them to a base station whose absolute value is known. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_data.html#field-procedures" target="_blank" rel="noopener">Field procedures</a> (CC BY 4.0).

### remanent magnetization

Magnetization a rock keeps with no field applied. An igneous rock acquires it as it cools through the Curie temperature, the temperature below which its magnetic minerals can hold a magnetization. It records the field of that time, so it can point in a direction unrelated to today's field. Burger sets it aside for anomaly work and assumes all magnetization is induced. Where a body carries strong remanence, an anomaly computed from induced magnetization alone can place the body in the wrong spot. Course text: Burger Section 7.1.5. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/magnetics/magnetics_basic_principles.html#remanent-magnetization" target="_blank" rel="noopener">Remanent Magnetization</a> (CC BY 4.0).

### residual

A data point's vertical miss from the fitted line: the data value minus the fitted value, so it carries a sign. Least squares is the recipe that makes the summed squared residuals as small as possible. Course text: OpenIntro Statistics Section 8.1. Video: [Line fitting, residuals, and correlation](https://www.openintro.org/go?id=video_stat_linear_regression_line_fitting_residuals_correlation).

### residual anomaly

What remains of the Bouguer anomaly once the regional is removed: the Bouguer anomaly minus the regional, station by station. It is the local signal an interpretation works from, and the input to the half-width and the depth rules. Its shape depends on the regional chosen and on the reduction density, so both are reported with it. The statistics sense of residual, a data point's miss from a fitted line, applies here too: the residual anomaly is the miss from the fitted regional. Course text: Burger Section 6.6.1. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_data.html#data-presentation-options" target="_blank" rel="noopener">Data presentation options</a> (CC BY 4.0).

### rover

The magnetometer carried along the survey line, reading at each station. A second magnetometer stays at the base station. Each rover reading carries the time it was taken, so the base station's record at that time can correct it for the diurnal variation. Course text: Burger Section 7.4.2. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/magnetics/magnetics_processing.html#removal-of-time-variations" target="_blank" rel="noopener">Removal of time variations</a> (CC BY 4.0). It calls it the roving sensor.

### S wave

A seismic wave in which the ground moves at right angles to the direction the wave travels, shearing the material sideways. S stands for secondary: it is slower than the P wave, so it arrives second at a seismograph. It travels only through solids. It is also called a shear wave. Course text: Burger Section 2.1.3. Further reading: Earle, <em>Physical Geology, 2nd Edition</em>, <a href="https://opentextbc.ca/physicalgeology2ed/chapter/9-1-understanding-earth-through-seismology/" target="_blank" rel="noopener">9.1 Understanding Earth Through Seismology</a> (CC BY 4.0); UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/wave_basics.html#body-waves" target="_blank" rel="noopener">Body Waves</a> (CC BY 4.0).

### seismic velocity

The speed at which a seismic wave front moves through a material, in m/s. It is set by the material's elastic moduli and its density: `V_P = √((K + 4G/3)/ρ)` (V sub P equals the square root of K plus four thirds G, all over rho) and `V_S = √(G/ρ)` (V sub S equals the square root of G over rho). K is always positive, and G is positive in a solid. Both velocities divide by the same density, and `K + 4G/3` is always larger than `G`, so `V_P` is always greater than `V_S`. In Burger's Table 2.1, P-wave velocities run from 996 m/s in tuff to 6569 m/s in diabase. A refraction survey measures velocity, and velocity is the physical property contrast it senses. Course text: Burger Section 2.1.4, Eq. 2.11 and 2.12, and Table 2.1 in Section 2.1.2. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/wave_basics.html#body-waves" target="_blank" rel="noopener">Body Waves</a> (CC BY 4.0). It writes the shear modulus as μ (mu).

### shear modulus, G

How strongly a material resists shear, the change of shape that slides one face of a block past the opposite face. Burger defines it as the shear stress divided by the angle of shear it causes, and also calls it the rigidity modulus. G appears in both seismic velocities. A liquid has a shear modulus of zero, so an S wave cannot travel through it. Course text: Burger Section 2.1.2, Eq. 2.8 (Fig. 2.6), and Section 2.1.4, Eq. 2.11 and 2.12. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/wave_basics.html#body-waves" target="_blank" rel="noopener">Body Waves</a> (CC BY 4.0). It writes the shear modulus as μ (mu). Burger uses μ for Poisson's ratio.

### shell theorem

A round body whose density depends on how deep you are but not on which way you face pulls on anything outside it as if all its mass sat at its center. Layers are fine and the Earth is layered; a lump on one side is not. It is why the R in `g = GM/R²` (g equals G M over R squared) is the distance to the planet's center. Run the other way, the same result makes a buried sphere the simplest anomaly model: from outside, a sphere of radius R and density contrast Δρ pulls exactly like a point mass `M = (4/3)πR³Δρ` (M equals four thirds pi R cubed delta rho) sitting at its center. Newton proved it in the *Principia* (1687), Book I, Section XII, "Of the attractive forces of spherical bodies": nothing pulls a body placed inside a shell (Prop. LXX), and from outside, a shell pulls as though its mass sat at the center (Prop. LXXI). A layered planet is a stack of shells, which is why the layers do not matter. Further reading: [Newton's *Principia*, Book I, Section XII](https://en.wikisource.org/wiki/The_Mathematical_Principles_of_Natural_Philosophy_(1729)/Book_1/Section_12) in Motte's 1729 translation, public domain; Turcotte & Schubert, *Geodynamics* (2nd ed.), Section 5-6, Eq. 5.99 for the buried-sphere case.

### sigma

Sigma is the symbol papers and instruments use for the quantity you met as the **standard deviation** and the **standard error**. Which one it means depends on what it is attached to. A sigma on a set of readings is their spread. A sigma on a number that came out of a fit, such as a slope, is how far that number would move if you ran the survey again, which is a standard error. Quoting a value as `−0.287 ± 0.008` is quoting a 1-sigma uncertainty: one sigma either side. What that buys you is the **68-95-99.7 rule**: a fitted value lands within 1 sigma of the truth about 68 percent of the time and within 2 sigma about 95 percent. So a gap of more than about 2 sigma is one the scatter is unlikely to have produced by chance.

### slope and intercept

The two numbers a line fit returns. In this course the slope carries the physics (g from the pendulum, a drift rate, the free-air gradient), and the intercept picks up apparatus effects: a constant error in the length moves the line up or down without changing its slope. Course text: OpenIntro Statistics Section 8.2.

### small-angle approximation

`sin θ ≈ θ` (sine theta is about theta, with theta in radians) for swings under about 15 degrees. It is what makes `T = 2π√(l/g)` (T equals two pi root l over g) true, and it is why the lab procedure keeps the swing angle small.

### Snell's law

The rule for how much a ray bends when it crosses a boundary between two velocities: `sin θ1 / sin θ2 = V1 / V2` (the sine of the angle of incidence over the sine of the angle of refraction equals V1 over V2). Both angles are measured from the line at right angles to the boundary. V1 is the velocity on the incoming side and V2 the velocity on the far side. Burger derives it two ways, from Huygens' principle and from Fermat's principle. It also holds when an incoming P wave produces a refracted S wave, with the P velocity on one side and the S velocity on the other. Course text: Burger Section 2.2.4, Eq. 2.21 and 2.25, and Section 2.2.5. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/waves_at_interfaces.html#angles-of-reflection-and-refraction" target="_blank" rel="noopener">Angles of reflection and refraction</a> (CC BY 4.0).

### sphere (simple-shape model)

The model for a compact buried body, roughly equal in extent in every direction, such as an ore body. Outside itself a sphere attracts as if its whole excess mass sat at its center, by the shell theorem. Its anomaly is `Δg(x) = G M_e z / (x² + z²)^(3/2)` (delta g of x equals G M sub e z, over x squared plus z squared to the three halves), with `M_e` the excess mass, largest directly above the center, where it equals `G M_e / z²` (G M sub e over z squared). Depth rule: `z = 1.305 x½` (z equals one point three zero five times the half-width). Course text: Burger Section 6.5.2. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_basics.html#what-is-actually-measured" target="_blank" rel="noopener">What is actually measured?</a> (CC BY 4.0). It writes the density contrast the other way round, host rock minus body.

### stack

A set of repeated measurements of the same thing, treated together. Five timings of one pendulum length are a stack; the stack's mean, standard deviation, and standard error describe it. The word comes from seismic processing, where stacking repeated traces cancels random
noise by the same square-root-of-N mathematics; Module 3 meets it again.

### standard deviation (s)

The typical distance of one measurement from the mean of its stack. It reports the scatter of a single trial. Course text: OpenIntro Statistics Section 2.1. Video: [Examining numerical data](https://www.openintro.org/go?id=video_stat_numerical_data).

### standard error (SE)

`SE = s/√N` (s over root N): the uncertainty of the **mean** of N trials. Taking more trials does not shrink the scatter of a single trial. It does make the mean more certain. Course text: OpenIntro Statistics Section 7.1, where `SE = s/√n` is worked; Section 5.1 gives the same idea for a proportion. Video: [Inference for one mean](https://www.openintro.org/go?id=video_stat_inference_for_a_mean).

### station

A place where a reading is taken. A survey is a planned set of stations. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_data.html#field-procedures" target="_blank" rel="noopener">Field procedures</a> (CC BY 4.0).

### surface wave

A seismic wave that travels along Earth's surface. Surface waves form when body waves reach the surface. Love waves and Rayleigh waves are the two kinds. They travel more slowly than body waves, so they arrive last. They usually shake the ground hardest and do the most damage. Course text: Burger Section 2.1.3. Further reading: Earle, <em>Physical Geology</em>, <a href="https://geo.libretexts.org/Bookshelves/Geology/Physical_Geology_(Earle)/11%3A_Earthquakes/11.03%3A_Measuring_Earthquakes" target="_blank" rel="noopener">11.3 Measuring Earthquakes</a> (CC BY 4.0); UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/wave_basics.html#surface-waves" target="_blank" rel="noopener">Surface Waves</a> (CC BY 4.0).

### survey loop

Read the base station, read the survey stations, then read the base station again. The gap between the two base readings is the drift, and each station gets a correction sized by when it was read. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_data.html#field-procedures" target="_blank" rel="noopener">Field procedures</a> (CC BY 4.0).

### susceptibility, k

How strongly a rock magnetizes in a field. In the Earth's field a rock acquires magnetization `I = kF_E` (I equals k times F sub E). For the small k of rocks, twice the k gives twice the magnetization and twice the anomaly. Burger quotes k in emu (electromagnetic units, the cgs system Burger uses): about 0.00005 for sedimentary rocks, about 0.0005 for granites, about 0.012 for ultrabasic rocks, and 1 to 10 for many iron and steel objects. Susceptibility is the physical property contrast a magnetic survey senses. Course text: Burger Sections 7.1.5 (Eq. 7.7) and 7.5.1. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/magnetics/magnetics_physical_property.html" target="_blank" rel="noopener">Susceptibility</a> and <a href="https://gpg.geosci.xyz/content/physical_properties/magnetics_susceptibility_duplicate.html" target="_blank" rel="noopener">Magnetic susceptibility</a> (CC BY 4.0). It writes the susceptibility as κ (kappa) and uses SI units. To convert, multiply an emu value by 4π to get the SI value.

### systematic error

An error that pushes every reading in the same direction, so averaging never removes it. Calling a mark at the top of the bob the pendulum length is one: it makes a single-length `g` come out low, and in the multi-length fit it moves the intercept while leaving the slope. Found by checking assumptions against the apparatus; taking more readings does not reveal it.

### terrain correction

The correction for the ground not being flat. The Bouguer correction models everything between the station and the datum as a slab of uniform thickness. A hill standing above the station pulls upward on the meter, and a valley beside it removes mass the slab assumed was there; both make the reading too low, so the terrain correction is always positive. Whether it is needed at all depends on how rough the ground is near the station. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_data.html#corrections" target="_blank" rel="noopener">Corrections</a> (CC BY 4.0).

### tidal effect

The sun and moon pull on the gravimeter and on the Earth. The effect is a few tenths of a milligal over a day. It can be predicted in advance, so a survey that needs to can separate it from the instrument's own drift; a short survey's base loop corrects the two together. Course text: Burger Section 6.4.1. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/gravity/gravity_data.html#corrections" target="_blank" rel="noopener">Corrections</a> (CC BY 4.0).

### time-distance plot (travel-time curve)

A graph of arrival time against distance from the source, one point per geophone. Time is on the vertical axis, usually in ms. Distance is on the horizontal axis, in m. Each kind of wave plots as its own line or curve. For a straight line, the slope is one over the velocity, so `V = 1/slope` (V equals one over the slope). With time in milliseconds and distance in meters, Burger's working rule is `V = 1000/slope` (V in m/s equals 1000 divided by the slope). The direct wave plots as a line through the origin, and the head wave as a line with a smaller slope. Burger calls this graph a travel-time curve. Course text: Burger Section 2.2.8 (Fig. 2.21) and Section 3.1, Eq. 3.2 to 3.5. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/traveltimes.html" target="_blank" rel="noopener">Travel times</a> (CC BY 4.0).

### total field, F

The strength of the magnetic field at the sensor, in nT. Away from any buried body it is the Earth's field, written F_E, about 51,000 nT at Queens. It is the long side of the triangle whose legs are H and Z: `F = √(H² + Z²)` (F equals the square root of H squared plus Z squared). A total-field magnetometer reads F and nothing about its direction. Course text: Burger Section 7.2.1, Eq. 7.9. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/magnetics/magnetics_basic_principles.html#earth-s-magnetic-field-source" target="_blank" rel="noopener">Earth's magnetic field (Source)</a> (CC BY 4.0). It writes the field strength as |B|.

### total-field anomaly, F_AT

The part of a buried body's field that lies along the Earth's field. It is what a total-field survey measures once the diurnal variation and the IGRF are removed: `F_AT = Z_A sin i + H_A cos i` (F sub A T equals Z sub A times sine i, plus H sub A times cosine i), where Z_A is the vertical part of the body's field and H_A is its horizontal part toward magnetic north. In the northern hemisphere, between the magnetic equator and the north magnetic pole, sin i and cos i are both positive, so each term takes the sign of Z_A or H_A. There, south of the body the two terms add. North of the center they oppose, and farther north both are negative, giving the low. That is why the anomaly is lopsided. In the southern hemisphere the pattern is reversed. Course text: Burger Section 7.3.3, Eq. 7.18. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/magnetics/magnetics_data.html#magnetic-field-data" target="_blank" rel="noopener">Magnetic field data</a> (CC BY 4.0). It writes the total-field anomaly as B_T.

### trial

One complete measurement in a stack. In HW0, one 10-swing timing at one pendulum length.

### variance

The square of the standard deviation. The fit's covariance matrix is built from variances,
which is why the square roots of its diagonal entries are standard errors. Course text: OpenIntro Statistics Section 2.1.

### vertical component, Z

The vertical part of the Earth's field, positive downward: `Z = F sin i` (Z equals F times sine i). It is zero at the magnetic equator. At the north magnetic pole it equals F, about 70,000 nT. At the south magnetic pole the field points up, so Z equals −F. The vertical part of a buried body's own field is written Z_A. Course text: Burger Section 7.2.1, Eq. 7.9. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/magnetics/magnetics_basic_principles.html#earth-s-magnetic-field-source" target="_blank" rel="noopener">Earth's magnetic field (Source)</a> (CC BY 4.0). It takes z positive up in its applets.

### volume, V, and the product k times V

In the sphere's anomaly (Burger Eqs. 7.36 and 7.37), the radius and the susceptibility enter only through the front factor `(4/3)πR³ kF_E` (four thirds pi R cubed, times k, times F sub E). The `(4/3)πR³` part is the sphere's volume, V. At one depth and one site, two spheres with the same k times V give the same anomaly at every station. The width of the anomaly gives the depth. The amplitude gives only k times V: a small, strongly magnetic body and a large, weakly magnetic one cannot be told apart from the profile alone. A drill hole, a measured susceptibility or the geology decides between them. Gravity has the same limit with the excess mass. Course text: Burger Section 7.5.4. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/magnetics/magnetics_basic_principles.html#magnetization" target="_blank" rel="noopener">Magnetization</a> (CC BY 4.0).

### wave front

The surface that joins every point a seismic wave has reached at one moment. From a small source in uniform rock it is a sphere that grows outward. Rays are drawn at right angles to the wave fronts. Course text: Burger Section 2.1 and Section 2.2.1. Further reading: UBC-GIF, <em>Geophysics for Practicing Geoscientists</em>, <a href="https://gpg.geosci.xyz/content/seismic/wave_basics.html#waves-and-rays" target="_blank" rel="noopener">Waves and Rays</a> (CC BY 4.0). It spells it "wavefront".

### wavelength, λ

The distance between two neighboring points of a wave at the same stage of its cycle, for instance from one crest to the next. Wavelength, frequency and velocity are tied by `V = fλ` (V equals f times lambda). The frequency f is the number of cycles per second, in hertz (Hz), and is one over the period: `f = 1/T` (f equals one over T). Burger's example: in saturated sediment at 1500 m/s, a 10 Hz wave has a wavelength of 150 m. Course text: Burger Section 2.1.1, Eq. 2.1 and 2.3, and the example at the end of Section 2.1.4.

### Young's modulus, E

How strongly a material resists being stretched or squeezed along one direction. It is the stress divided by the strain it causes, `σ = Eε` (sigma equals E times epsilon), where σ is the stress and ε the strain. This is Hooke's law in the form Burger uses for rock. Burger's Table 2.1 lists E for each rock in units of 10¹¹ N/m² (ten to the eleven newtons per square meter). With density and Poisson's ratio, E gives both seismic velocities. Course text: Burger Section 2.1.2, Eq. 2.4, Table 2.1, and Section 2.1.4, Eq. 2.11 and 2.12.

### z-score

A measurement rewritten as its distance from the mean of its own stack, in units of standard deviation: `z = (value − mean) / s` (z equals value minus mean, over s). It puts every stack on one axis so the 68-95-99.7 rule can be checked across all of them. Course text: OpenIntro Statistics Section 4.1. Video: [Normal distribution](https://www.openintro.org/go?id=video_stat_normal_distribution).

### comment

A note after `#` that Python ignores. It is written for the person reading the code.

### CSV

A plain text file of comma-separated values, the simplest way to store a table.

### DataFrame

A Pandas table with named columns. Every dataset in this course loads into one. The full
reference: [pandas.DataFrame](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.html).

### f-string

A print pattern: an `f` before the opening quote makes any `{name}` inside the text fill in
with that variable's value.

### for loop

A statement that repeats a computation once for each value in a list.

### GitHub

The website where the course's [repository](#repository) is kept. You do not need an account
to read it, and the course never asks you to make one.

### library

A collection of ready-made Python tools, loaded with `import`. NumPy, Pandas, and Plotly are
the course's three.

### list

A Python value that holds several values in order, written in square brackets. Python's own
tutorial covers them in depth: [docs.python.org, Data Structures](https://docs.python.org/3/tutorial/datastructures.html).

### notebook and cell

A Colab notebook is a page of cells. Text cells hold instructions and questions; code cells
hold Python you run.

### repository

A folder of files kept online together with its history. The course's is
<a href="https://github.com/soule-geophysics/geol-333-714">`soule-geophysics/geol-333-714`</a>,
and it holds every notebook and dataset you use. It is public, which is why the links that
fetch from it work without a login: `colab.research.google.com/github/...` opens a notebook
from it, and `raw.githubusercontent.com/...` is a data file inside it.

### variable

A name that holds a value, so later lines can use the value by its name.


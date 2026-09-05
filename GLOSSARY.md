# Glossary

GEOL 333/714 Geophysical Exploration Methods, Fall 2026. The course's
terms, in the course's words; new terms join as each week teaches them.
This file is generated from the course glossary; the Brightspace copy
carries the same content.

### 68-95-99.7 rule

For the normal distribution: about 68% of values land within one standard deviation of the mean, 95% within two, 99.7% within three. The quick test for whether a value's distance from the mean is ordinary scatter. Course text: OpenIntro Statistics §4.1. Video: [Normal distribution](https://www.openintro.org/go?id=video_stat_normal_distribution).

### accuracy

How close a result lands to the true value. Limited by systematic error; taking more readings does not improve it.

### anomaly

The difference between what we observe and what we can explain. The whole aim of a gravity survey is to explain as much as possible, so that what remains points at the buried body we are looking for.

### base station

A measurement point the survey returns to. Returning to it ties the relative readings to a known value and records how far the instrument drifted while you worked.

### bob

The weight on the end of a pendulum's string. Ours is a one-inch metal ball.

### correlation

A number between −1 and +1 for how tightly two quantities follow a straight line together, and
in which direction. Course text: OpenIntro Statistics §8.1. Video: [Line fitting, residuals, and correlation](https://www.openintro.org/go?id=video_stat_linear_regression_line_fitting_residuals_correlation).

### covariance matrix

The table of uncertainties a least-squares fit returns. The square roots of its diagonal
entries are the standard errors of the slope and the intercept, which is where every fitted
slope's error bar in this course comes from.

### determinant

A single number computed from a square matrix; for a 2x2 it is `ad - bc` (a d minus b c). It tells you whether a system of equations has one answer: when the determinant is zero the two lines are parallel or identical, so there is no unique solution, and the solver calls the system singular.

### drift

The slow change in a gravimeter's reading while the meter sits still. Two things cause it: the spring slowly stretches, and the tidal effect rides on top. A survey tracks the combined change by re-occupying the base station and corrects each reading by how much had accumulated when it was taken. Our stairwell dataset does exactly this with its two base readings.

### equivalence principle

The mass gravity pulls on is the same as the mass that resists a push, so when gravity is the only force acting, everything falls with the same g. It is the reason the bob's mass drops out of the pendulum's period. Course text: Burger §6.1.1, Eqs. 6.3-6.4, where `F = ma` (F equals m a) set against `F = GmM/R²` (F equals G m M over R squared) lets the m cancel.

### error bar (uncertainty)

The ± reported with a value: the range a repeat of the same experiment could reasonably land in. A result in this course is a value with its error bar.

### free-air gradient

The rate gravity decreases with elevation: about 0.3086 mGal per meter (milligals per meter). Climbing one floor of a building lowers g by about one milligal.

### G and g

`G` is the universal gravitational constant, `6.674 × 10⁻¹¹ m³ kg⁻¹ s⁻²`, the same everywhere in the universe. `g` is the strength of gravity where you stand, about `9.81 m/s²`, and it changes with latitude, elevation, and what sits underneath you. The course measures g; nature fixes G.

### gravimeter

The field instrument for gravity: a mass on a very soft spring in a rigid case. To take a reading, you turn a screw a known amount to bring the mass back to a fixed resting mark, and the screw's counter is the reading. It reads changes in g, in milligals. The What a Gravimeter Is page carries the full story.

### histogram

A bar chart of a set of repeated measurements: each bar counts how many values landed in its slice of the number line. Course text: OpenIntro Statistics §2.1. Video: [Examining numerical data](https://www.openintro.org/go?id=video_stat_numerical_data).

### impedance contrast

The jump in a material property across a boundary that makes the boundary reflect. No jump, no echo, and the boundary is invisible even though it is right there. Each method has its own impedance: sound cares about density and how fast it travels, radar cares about the electrical properties, and water dominates those. Both are mostly set by how much pore space is down there and what is sitting in it, which is why the two often light up the same boundary. Module 3 works the seismic case. Course resource: [Seismic Reflection](https://www.iris.edu/hq/inclass/lesson/seismic_reflection) (EarthScope/IRIS, CC BY 4.0).

### least squares

The fitting recipe that picks the line with the smallest total of squared vertical distances between the data points and the line. Week 2 works it on the board; the homework uses it wherever a slope carries physics. Course text: OpenIntro Statistics §8.2. Video: [Fitting a Line with Least Squares Regression](https://www.youtube.com/watch?v=z8DmwG2G4Qc&list=PLkIselvEzpM63ikRfN41DNIhSgzboELOM).

### matrix

A rectangular grid of numbers. In this course a matrix carries a whole system of equations at once: Week 2 solves a 2x2 system by hand, then writes the least-squares fit as the normal equations `(AtA)m = Atd` (A transpose A m equals A transpose d) and solves that same 2x2 shape built from 25 data points. The Matrix Methods card in the Math Reference Cards works the 2x2 case by hand.

### mean

The best single value a set of repeated measurements gives: the sum divided by the count. Course text: OpenIntro Statistics §2.1. Video: [Examining numerical data](https://www.openintro.org/go?id=video_stat_numerical_data).

### median

The middle value once the data are sorted: half the measurements sit below it, half above.
`describe()` prints it as the 50% row. Course text: OpenIntro Statistics §2.1. Video: [Examining numerical data](https://www.openintro.org/go?id=video_stat_numerical_data).

### milligal (mGal)

The working unit of field gravity: `1 mGal = 10⁻⁵ m/s²` (ten to the minus five meters per second squared), about one part per million of g.

### model

A mathematical claim about how the world behaves, written so data can test it.
`T = 2π√(l/g)` (T equals two pi root l over g) is HW0's model; an anomaly is always measured
against one.

### Newton's law of universal gravitation

Every mass pulls every other, along the line between them, with force `F = GMm/r²` (F equals G M m over r squared). Its surface form, `g = GM/R²` (g equals G M over R squared), gives the gravity at a planet's surface. It rests on assumptions the course tests one by one.

### normal distribution

The bell-shaped curve that stacks of repeated measurements approach. Its width is the standard deviation, and it obeys the 68-95-99.7 rule. Course text: OpenIntro Statistics §4.1. Video: [Normal distribution](https://www.openintro.org/go?id=video_stat_normal_distribution).

### outlier

A measurement that sits far from the rest of its stack. One is never deleted silently: the
analysis states it, then shows the result with and without it. Course text: OpenIntro Statistics §2.1. Video: [Outliers in regression](https://www.openintro.org/go?id=video_stat_linear_regression_outliers).

### pendulum length (l)

The distance from the pivot to the **center** of the bob. A mark at the top of the bob sits half the bob's height above its center. Measuring to the mark and calling it `l` makes `g` come out low when you compute `g` from a single length, by more than the stopwatch scatter. In the multi-length fit of `T²` against `l` (T squared against l), the same constant offset moves the intercept and leaves the slope, so the `g` taken from the slope is unchanged.

### period (T)

The time for one complete swing. Our protocol times ten complete swings and divides by ten, which shares one stopwatch error across ten periods.

### potential field

A field, like gravity or magnetism, where a reading is the summed pull of every source at once, near or far. There is no way to send in a signal and listen for an echo. Gravity and magnetics are the course's two potential-field methods.

### precision

How tightly repeated measurements agree with each other. Limited by random error. Averaging N readings does not tighten the readings themselves; it steadies their mean by a factor of the square root of N.

### probability density function (PDF)

The smooth curve the histogram of a stack of repeated measurements approaches as the stack grows, once the histogram is scaled so its total area is one. The normal distribution is the one our measurements follow. Course text: OpenIntro Statistics §3.5.

### property contrast

A difference in a physical property (density, how strongly the rock is magnetized, or how fast seismic waves travel through it) between a buried body and its surroundings. A body with no contrast in the property a method senses is invisible to that method.

### quartile (percentile)

The 25% and 75% rows of `describe()`: one quarter of the data sits below the first quartile,
three quarters below the third. A percentile generalizes this: the value below which that
percent of the data sits. Course text: OpenIntro Statistics §2.1.

### random error

Scatter that changes size and sign from trial to trial, like the small timing errors from pressing a stopwatch. Averaging N trials shrinks it by the square root of N.

### relative and absolute measurement

A spring gravimeter reads differences between stations; an absolute gravimeter drops a mirror in a vacuum chamber and times its fall with a laser to read g itself. Surveys read differences and tie them to a base station whose absolute value is known.

### residual

A data point's vertical miss from the fitted line: the data value minus the fitted value, so it carries a sign. Least squares is the recipe that makes the summed squared residuals as small as possible. Course text: OpenIntro Statistics §8.1. Video: [Line fitting, residuals, and correlation](https://www.openintro.org/go?id=video_stat_linear_regression_line_fitting_residuals_correlation).

### shell theorem

A round body whose density depends on how deep you are but not on which way you face pulls on anything outside it as if all its mass sat at its center. Layers are fine and the Earth is layered; a lump on one side is not. It is why the R in `g = GM/R²` (g equals G M over R squared) is the distance to the planet's center. Run the other way, the same result makes a buried sphere the simplest anomaly model: from outside, a sphere of radius R and density contrast Dr pulls exactly like a point mass `M = (4/3)piR³Dr` (M equals four thirds pi R cubed delta rho) sitting at its center. Newton proved it in the *Principia* (1687), Book I, Section XII, "Of the attractive forces of spherical bodies": nothing pulls a body placed inside a shell (Prop. LXX), and from outside, a shell pulls as though its mass sat at the center (Prop. LXXI). A layered planet is a stack of shells, which is why the layers do not matter. Further reading: [Newton's *Principia*, Book I, Section XII](https://en.wikisource.org/wiki/The_Mathematical_Principles_of_Natural_Philosophy_(1729)/Book_1/Section_12) in Motte's 1729 translation, public domain; Turcotte & Schubert, *Geodynamics* (2nd ed.), §5-6, Eq. 5.99 for the buried-sphere case.

### slope and intercept

The two numbers a line fit returns. In this course the slope carries the physics (g from the pendulum, a drift rate, the free-air gradient), and the intercept picks up apparatus effects: a constant error in the length moves the line up or down without changing its slope. Course text: OpenIntro Statistics §8.2.

### small-angle approximation

`sin θ ≈ θ` (sine theta is about theta, with theta in radians) for swings under about 15 degrees. It is what makes `T = 2π√(l/g)` (T equals two pi root l over g) true, and it is why the lab procedure keeps the swing angle small.

### stack

A set of repeated measurements of the same thing, treated together. Five timings of one pendulum length are a stack; the stack's mean, standard deviation, and standard error describe it. The word comes from seismic processing, where stacking repeated traces cancels random
noise by the same square-root-of-N mathematics; Module 3 meets it again.

### standard deviation (s)

The typical distance of one measurement from the mean of its stack. It reports the scatter of a single trial. Course text: OpenIntro Statistics §2.1. Video: [Examining numerical data](https://www.openintro.org/go?id=video_stat_numerical_data).

### standard error (SE)

`SE = s/√N` (s over root N): the uncertainty of the **mean** of N trials. Taking more trials does not shrink the scatter of a single trial. It does make the mean more certain. Course text: OpenIntro Statistics §7.1, where `SE = s/√n` is worked; §5.1 gives the same idea for a proportion. Video: [Variability in estimates](https://www.openintro.org/go?id=video_stat_variability_in_estimates_prop).

### station

A place where a reading is taken. A survey is a planned set of stations.

### survey loop

Read the base station, read the survey stations, then read the base station again. The gap between the two base readings is the drift, and each station gets a correction sized by when it was read.

### systematic error

An error that pushes every reading in the same direction, so averaging never removes it. Calling a mark at the top of the bob the pendulum length is one: it makes a single-length `g` come out low, and in the multi-length fit it moves the intercept while leaving the slope. Found by checking assumptions against the apparatus; taking more readings does not reveal it.

### tidal effect

The sun and moon pull on the gravimeter and on the Earth. The effect is a few tenths of a milligal over a day. It can be predicted in advance, so a survey that needs to can separate it from the instrument's own drift; a short survey's base loop corrects the two together.

### trial

One complete measurement in a stack. In HW0, one 10-swing timing at one pendulum length.

### variance

The square of the standard deviation. The fit's covariance matrix is built from variances,
which is why the square roots of its diagonal entries are standard errors. Course text: OpenIntro Statistics §2.1.

### z-score

A measurement rewritten as its distance from the mean of its own stack, in units of standard deviation: `z = (value − mean) / s` (z equals value minus mean, over s). It puts every stack on one axis so the 68-95-99.7 rule can be checked across all of them. Course text: OpenIntro Statistics §4.1. Video: [Normal distribution](https://www.openintro.org/go?id=video_stat_normal_distribution).

## Python and Colab terms

The computing words the course teaches deliberately.

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

### library

A collection of ready-made Python tools, loaded with `import`. NumPy, Pandas, and Plotly are
the course's three.

### list

A Python value that holds several values in order, written in square brackets. Python's own
tutorial covers them in depth: [docs.python.org, Data Structures](https://docs.python.org/3/tutorial/datastructures.html).

### notebook and cell

A Colab notebook is a page of cells. Text cells hold instructions and questions; code cells
hold Python you run.

### variable

A name that holds a value, so later lines can use the value by its name.


# ME2102 — Chapters 2–9 Summary

> [!summary]
> This revision note consolidates **ME2102 Chapters 2–9**: Multiview Projection, Dimensioning & Sectioning, Fasteners, Limit Tolerance & Fits, Geometric Tolerance, Sketching & Couplers, Conventions & Symmetry, and Welding.

---

# Chapter 2 — Multiview Projection

## Projection Types

- **Orthographic projection** — views along principal axial directions.
- **Isometric projection** — gives an even three-dimensional view of the principal directions.
- **Oblique projection** — keeps one face orthographic while showing depth at a chosen angle.
  - **Cavalier:** depth uses **1:1 scale**.
  - **Cabinet:** depth uses **half scale**.
  - The distinction is determined by **scale**, not projection angle.
- **Perspective projection** — parallel lines may converge toward vanishing points; useful visually but unsuitable as the main engineering projection because distances are distorted.

## Choosing Orthographic Views

A component has six possible principal views, but normally only the views needed to communicate its geometry should be shown.

- Usually use **at most three principal views**.
- Often only **one or two views** are required.
- Prefer views that expose important geometry directly.
- Avoid unnecessary views containing mainly hidden lines.
- More views are **not automatically better**.

### One-view parts

A rotationally symmetric component can sometimes be completely described using a single side view and a centre line.

### Two-view parts

The lecturer uses **structurally monotonic** as a rule of thumb: if one direction exposes the geometry without hidden lines and another supplies the required depth information, two views may be sufficient.

## Drawing Lines

- **Hidden lines** → geometry not directly visible.
- **Centre mark** → rotational feature viewed along its axis.
- **Centre line** → axis of a rotational feature viewed from the side.

## 3rd Angle Projection

Views are placed on the **same side** as the viewing direction:

| Physical view | Position |
|---|---|
| Right | Right |
| Left | Left |
| Top | Above |
| Bottom | Below |

> [!tip]
> **3rd Angle:** right on right, top on top.

## 1st Angle Projection

Views are placed on the **opposite side**:

| Physical view | Position |
|---|---|
| Right | Left |
| Left | Right |
| Top | Below |
| Bottom | Above |

> [!warning]
> When identifying the projection method, check **both horizontal and vertical relationships**, as well as the orientation produced by rotation.

## Auxiliary Projection

Used when an **inclined surface** needs to be viewed directly.

1. Identify the inclined surface.
2. Indicate viewing direction.
3. Project the view in that direction.
4. Place the auxiliary view according to the projection convention.

---

# Chapter 3 — Dimensioning & Sectioning

## Dimensioning

A drawing is fully dimensioned when it is:

- **Complete** — sufficient information is given to define the component.
- **Minimal** — dimensions already determined by other information are omitted.

Unless otherwise stated, dimensions in this course are interpreted in **millimetres**.

> [!warning]
> Decimal places communicate precision. Do not add decimal places merely for appearance.

## Dimension and Projection Lines

### Dimension line
Carries the numerical dimension and normally terminates in arrowheads.

### Projection line
Connects the dimension line to the measured feature.

Good practice:

- leave a small gap from the component where possible;
- extend slightly beyond the dimension line;
- space dimensions clearly;
- avoid unnecessary crossings;
- prefer horizontal and vertical dimensions where practical.

## Datum vs Chain Dimensioning

### Datum dimensioning
Multiple dimensions are measured from a common reference.

Advantages:

- systematic;
- easier to interpret;
- reduces accumulation of tolerance error.

### Chain dimensioning
Dimensions are specified consecutively.

> [!warning]
> Individual dimensional deviations can **accumulate** through the chain.

## Leaders

- Arrowhead → edge/surface viewed from the side.
- Dot → face viewed head-on.
- Can specify notes, radii and diameters.

## PCD

**Pitch Circle Diameter (PCD)** describes the circle on which repeated circular features such as holes are positioned.

## Auxiliary Dimensions

A dimension in **parentheses** is auxiliary.

- Provided for convenience.
- Does not drive the tolerance requirements.

## Diameter and Radius

- `Ø` → diameter of circular/cylindrical features.
- `R` → radius.
- Leaders for radii/diameters should align with the centre of curvature.
- `Sphere Ø` distinguishes spherical diameter where needed.

---

## Sectioning

Section views expose internal geometry and can replace views containing excessive hidden lines.

### Full Section

A cutting plane passes completely through the component.

1. Define cutting plane.
2. Show viewing direction with arrows.
3. Remove material on the viewing side mentally.
4. Draw visible geometry behind the plane.
5. Hatch surfaces actually cut.

### Hatching

Typical lecture convention:

- thin lines;
- approximately **0.3 mm**;
- spacing approximately **4–6 mm**;
- normally **45°**.

Same component → same slope/spacing.  
Adjacent components → change slope and/or spacing.

### Features Normally Not Hatched

- ribs
- spokes
- gear teeth
- shafts
- rods
- bolts
- nuts
- rivets
- keys
- pins

### Half Section

Combines:

- half external view;
- half section view.

Used mainly for **symmetric components**. The halves are separated by a **centre line**.

### Offset Section

The cutting plane uses parallel portions joined by **90° offsets** to pass through features in different parallel planes.

### Aligned Section

The cutting plane **rotates about an axis** so separated radial features are represented as though they lie in one plane.

### Part / Broken-out Section

Only a local region is sectioned. A freeform boundary separates sectioned and unsectioned portions.

### Revolved Section

A local cross-section is rotated **90°** and drawn directly on the external view.

---

# Chapter 4 — Fasteners

## Main Fasteners

- **Screw**
- **Bolt**
- **Stud**
- **Nut**
- **Washer**

### Washer

Not threaded. Used to:

- protect the workpiece surface;
- distribute clamping force;
- reduce local pressure.

### Bolt vs Screw

- **Bolt:** normally passes through clearance holes and works with a nut.
- **Screw / set bolt:** threads directly into one component.
- **Stud:** threaded rod without a head.

## Thread Geometry

- **Major diameter** → outer diameter of an external thread.
- **Minor diameter** → inner extent of thread profile.
- **Crest** → top of thread tooth.
- **Root** → bottom of thread groove.
- **Flank** → side of thread tooth.
- **Pitch** → distance between equivalent points on adjacent threads.

## Pitch and Lead

**Lead** = axial travel during one complete revolution.

For the lecture examples:

- Single start: `Lead = Pitch`
- Double start: `Lead = 2 × Pitch`
- Four start: `Lead = 4 × Pitch`

Therefore:

**Lead = Pitch × number of starts**

## Taps and Dies

- **Die** → creates an external thread.
- **Tap** → creates an internal thread.

External thread:
1. Start from material at the **major diameter**.
2. Remove material inward.

Internal thread:
1. Drill near the required **minor diameter**.
2. Tap outward toward the major diameter.

## Clearance Hole

A hole slightly larger than the thread major diameter so the fastener passes through without threading into the component.

## ISO Metric Thread Designation

Example:

`M16 × 1.5 - 6H`

- `M` → metric thread
- `16` → nominal/major diameter
- `1.5` → pitch
- `6H` → internal-thread tolerance designation

Capital letter → **internal thread**.  
Lowercase letter → **external thread**.

## Right- and Left-Hand Threads

Normal threads are **right-handed**:

- clockwise → tighten/move inward;
- counterclockwise → loosen/move outward.

A left-hand thread is identified using **LH**.

## Conventional Thread Representation

Engineering drawings do not normally show the full helix.

End view:

- **External thread:** inner/minor-diameter circle is broken.
- **Internal thread:** outer/major-diameter circle is broken.

---

# Chapter 5 — Limit Tolerance & Hole/Shaft Fits

## Tolerance

**Tolerance** = permissible deviation from a specified dimension.

Tolerance is necessary because manufacturing cannot achieve arbitrary precision.

> [!tip]
> Use looser tolerance when function allows. Tighter tolerance increases manufacturing and inspection cost.

## Limits and Offsets

Example:

`41 ± 0.2`

means:

- minimum = `40.8 mm`
- maximum = `41.2 mm`

Offset notation preserves the **basic size**, unlike a pair of limits alone.

## Unilateral Tolerance

Variation occurs in only one direction.

Example:

`60 +0.05/-0`

→ `60.00–60.05 mm`

## Bilateral Tolerance

Variation occurs in both directions.

Symmetric:

`57.2 ± 1.5`

→ `55.7–58.7 mm`

Asymmetric:

`57.2 +0.8/-1.5`

→ `55.7–58.0 mm`

## Cumulative Tolerance

Chained tolerances can accumulate.

> [!tip]
> Prefer **ordinate/datum dimensioning** where possible.

## ISO 2768

Tolerance classes:

- Fine `(f)`
- Medium `(m)`
- Coarse `(c)`
- Very coarse `(v)`

When reading ranges:

- **Above** = exclusive
- **Up to** = inclusive

Thus, a basic size exactly on a boundary belongs to the row ending at that value.

## IT Grade

The **International Tolerance (IT) grade** specifies the **width of the allowable dimensional range**.

Higher IT grade number → wider tolerance.

It does **not** specify the location of the range relative to the basic size.

## Fundamental Deviation

Determines where the tolerance range lies relative to the basic size.

- Number → **IT grade**
- Letter → **fundamental deviation**

`h/H` has fundamental deviation zero.

## Hole Basis

The course uses **hole basis**.

For an `H` hole:

- Minimum hole = Basic size
- Maximum hole = Basic size + IT grade

## Standard Fits

### Clearance Fit

Shaft always smaller than hole.

- Maximum clearance = Maximum hole − Minimum shaft
- Minimum clearance = Minimum hole − Maximum shaft

### Interference Fit

Shaft always larger than hole.

- Maximum interference = Maximum shaft − Minimum hole
- Minimum interference = Minimum shaft − Maximum hole

### Transition Fit

Depending on manufactured dimensions, the result may be either clearance or interference.

## Hole-Basis Fit Designations

| Fit | Hole | Shaft |
|---|---:|---:|
| Running Loose | H11 | c11 |
| Running Free | H9 | d9 |
| Running Close | H8 | f7 |
| Precision Sliding | H7 | g6 |
| Precision Location | H7 | h6 |
| Transition Light | H7 | k6 |
| Transition Heavy | H7 | n6 |
| Interference Location | H7 | p6 |
| Interference Drive | H7 | s6 |
| Interference Force | H7 | u6 |

---

# Chapter 6 — Geometric Tolerance

## Why Limit Tolerance Is Insufficient

Limit tolerance constrains **dimension values**, but a component can still have unacceptable:

- form;
- shape;
- orientation;
- location.

Geometric tolerance constrains these geometric properties.

## Geometric-Tolerance Frame

Typically contains:

1. geometric characteristic symbol;
2. permitted deviation;
3. datum reference(s), where required.

## Main Groups

| Group | Characteristics |
|---|---|
| Form | Straightness, Flatness, Circularity, Cylindricity |
| Profile | Profile of any line, Profile of any surface |
| Orientation | Parallelism, Perpendicularity, Angularity |
| Location | Position, Concentricity, Symmetry |
| Run-out | Circular Run-out, Total Run-out |

## Intrinsic vs Extrinsic

### Intrinsic
Feature is constrained relative to its own geometry.

Examples:

- straightness
- flatness
- circularity
- cylindricity

### Extrinsic
Feature is constrained relative to another feature or **datum**.

Examples:

- parallelism
- perpendicularity
- angularity
- position
- concentricity
- symmetry
- run-out

Profile tolerances may be intrinsic or extrinsic.

## Form Tolerances

### Straightness
Constrains lines on a feature.

### Flatness
Entire surface lies between two parallel planes separated by the tolerance.

### Circularity
Each required cross-section lies between two concentric circles.

Circularity does **not** require:

- identical radius at every section;
- identical centre at every section;
- the overall feature to be cylindrical.

### Cylindricity
Constrains the **entire cylindrical surface** between two cylinders.

> [!important]
> Circularity → individual slices.  
> Cylindricity → entire surface.

## Datum

An idealized reference:

- plane, usually from a planar surface;
- line/axis, usually from a cylindrical feature.

> [!warning]
> A datum attached to a cylindrical feature represents its **idealized axis**, not its outer cylindrical surface.

## Orientation Tolerances

### Parallelism
Tolerance-zone planes are parallel to a specified datum.

### Perpendicularity
Tolerance-zone planes are perpendicular to a datum.

### Angularity
Tolerance-zone planes are at a specified arbitrary angle relative to a datum.

## Location Tolerances

### Position
Constrains the axis of a feature relative to its ideal position.

### Symmetry
Constrains a centre plane relative to a datum centre plane.

### Concentricity
Constrains cylindrical **axes**, not outer surfaces.

## Run-out

### Circular Run-out
Constrains individual circular slices relative to a datum axis.

### Total Run-out
Constrains the complete rotational surface relative to a datum axis.

### Key Comparison

- Circularity → slices, intrinsic.
- Cylindricity → full surface, intrinsic.
- Circular run-out → slices relative to datum.
- Total run-out → full surface relative to datum.

---

# Chapter 7 — Sketching & Couplers

## Orthographic and Isometric Sketching

- Orthographic sketch sheet → **square grid**.
- Isometric sketch sheet → **isometric triangular grid**.

Orthographic views must be interpreted **together**, not independently.

Dashed lines indicate hidden features.

## Orthographic → Isometric Workflow

1. Read all orthographic views.
2. Establish overall three-dimensional size and shape.
3. Transfer important edges and changes in geometry.
4. Construct inclined surfaces using endpoints.
5. Retain actual object edges.
6. Remove unnecessary construction lines.

> [!important]
> The lecture repeatedly builds **construction geometry first**, then identifies the final visible edges.

## Isometric Circles

A circle on an isometric plane appears as an **elliptical-looking profile**.

Procedure:

1. Establish centre lines and construction box.
2. Transfer the box to the relevant isometric plane.
3. Locate construction points.
4. Draw a smooth curve through the points.

## Couplers — Core Purpose

Couplers connect mechanical components and prevent unwanted relative motion.

Main items covered include:

- keys;
- splines;
- serrations;
- shaft couplings;
- locking devices.

### Keys
Transmit torque between a shaft and a mounted component by engaging corresponding keyways.

### Splines and Serrations
Use multiple engaging features around the shaft rather than a single key.

---

# Chapter 8 — Conventions & Symmetry

## Mirror Symmetry

A symmetry line uses:

- centre line along the symmetry axis;
- two short parallel marks at each end;
- part outlines extending slightly beyond the centre line.

A half view is valid only when the omitted half is symmetric.

Asymmetric features must be explicitly identified, e.g. **“This side only.”**

## Special Views

### Aligned View
Rotates/aligns features into the viewing plane to communicate circularly arranged features clearly.

### Enlarged Part View

Used when a feature is too small to dimension clearly.

1. Circle the region.
2. Draw a leader.
3. Show an enlarged view.

### Interrupted View

Shortens the drawing of a long, constant-cross-section component.

Used for:

- circular sections;
- tubes;
- rectangular sections.

> [!warning]
> The break is a drawing convention; the physical component is not actually broken.

## Repetitive Information

For repeated identical features:

- draw one representative feature;
- show remaining positions using centre lines.

## Knurling

- Parallel straight lines → **straight knurling**
- Crossed diagonal lines → **diamond knurling**

## Square-ended Shaft

Represented using **diagonals on the flat face**.

## Bearings

Conventional representation uses **crossed boxes**.

## Compression Springs

- Do not project true helices.
- Draw helices using straight lines.
- Exact pitch is unnecessary.
- Show **2 or 3 coils at each end**.
- Schematic representation may use a single zig-zag line.

## Gears

Circular gear view:

- individual teeth may be omitted;
- **thick circle** → tooth tips;
- **thin chain circle** → pitch circle.

Rack:

- one or two teeth shown;
- thick line → tooth tips;
- thin line → roots;
- pitch line omitted.

## Important Abbreviations

| Abbreviation | Meaning |
|---|---|
| A/F | Across Flat |
| A/C | Across Corner |
| Assy | Assembly |
| CRS | Centre |
| CL | Centre line |
| CSK | Countersunk |
| C'BORE | Counterbore |
| Ø | Diameter |
| DRG | Drawing |
| HEX | Hexagon |
| MAT'L | Material |
| PCD | Pitch circle diameter |
| R | Radius |
| REQD | Required |
| SPEC | Specification |
| □ | Square |
| STD | Standard |

> [!warning]
> `CBE - Counter Bore` is **not** the abbreviation used in the lecture. Use `C'BORE`.

---

# Chapter 9 — Welding

## Welding Fundamentals

Welding uses sufficiently high heat to melt materials locally and create a **permanent joint**.

Unlike low-temperature soldering, the materials being joined also melt locally.

## Welding Processes

Classification includes:

- chemical energy → gas welding;
- electrical energy → arc welding;
- consumable / non-consumable;
- shielded / unshielded.

### MIG

**Metal Inert Gas welding**

- inert shielding gas;
- metal electrode normally consumed;
- electrode and filler functions combined in the illustrated process.

### TIG

**Tungsten Inert Gas welding**

- tungsten electrode;
- electrode does not melt away in the described process;
- separate filler rod may be used.

> [!important]
> The main ME2102 objective is **recognising and representing welds on engineering drawings**, rather than fabrication technique.

## Main Weld Types

### Fillet Weld
Commonly joins surfaces meeting approximately at a right angle.

Basic symbol → **triangle**.

### Butt Weld
Joins pieces that abut one another.

Common forms shown include:

- single V;
- single bevel;
- broad-root-face variants;
- single U;
- single J;
- square butt.

### Other Welds

- **Plug weld**
- **Spot weld** → circle symbol.
- **Seam weld** → repeated overlapping spot welds forming a seam.

## Weld Shape

Finished contour can be:

- flat/flush;
- convex;
- concave.

Shape symbols are combined with the basic weld symbol.

## Drawing Representation

A weld callout contains:

- **arrow line** → points to joint;
- **reference line**;
- **weld symbol**;
- **joint**.

## Arrow Side vs Other Side

- Symbol **below** reference line → **arrow side**
- Symbol **above** reference line → **other side**
- Symbols above and below → **both sides**

> [!warning]
> “Other side” means the opposite side of the **same joint**, not simply the upper or lower part of the drawing.

## Weld All Around

A **circle at the arrow/reference-line intersection** means:

**weld all around**

This applies to the complete perimeter even if it is not circular.

## Fillet-Weld Dimensioning

In the notation shown:

- number beside the short side → **weld size**;
- number associated with the long side → **weld length**.

If length is omitted, the weld may continue along the whole applicable side.

## Intermittent Weld

Example notation:

`100(150)`

- first number → length of each welded portion;
- number in brackets → distance before welding begins again.

## Site Weld

A **flag at the arrow/reference-line intersection** means the weld is made **on site**.

> [!important]
> Circle at intersection → weld all around.  
> Flag at intersection → weld on site.

## Interpreting Weld Symbols

1. Identify the joint.
2. Recognise the basic weld symbol.
3. Check whether the symbol is above or below the reference line.
4. Apply **below = arrow side**, **above = other side**.
5. If symbols occur above and below, weld both sides.
6. Check supplementary information:
   - weld-all-around circle;
   - site-weld flag;
   - weld shape;
   - size;
   - length;
   - intermittent spacing.

---

# High-Yield ME2102 Recognition Table

| Feature | Recognition |
|---|---|
| 3rd Angle Projection | Right view on right; top view above |
| 1st Angle Projection | Right view on left; top view below |
| Auxiliary view | Inclined surface projected head-on |
| Fully dimensioned | Minimal + complete |
| Auxiliary dimension | Dimension in parentheses |
| PCD | Pitch Circle Diameter |
| Full section | Cutting plane completely through part |
| Half section | Half external + half section |
| Offset section | Cutting plane with 90° offsets |
| Aligned section | Cutting plane rotated about axis |
| Broken-out section | Local section with irregular boundary |
| Revolved section | Cross-section rotated 90° onto view |
| External thread end view | Inner circle broken |
| Internal thread end view | Outer circle broken |
| Capital thread letter | Internal thread |
| Lowercase thread letter | External thread |
| Lead | Pitch × number of starts |
| Hole basis | Hole uses H; minimum hole = basic size |
| Clearance fit | Shaft always smaller |
| Interference fit | Shaft always larger |
| Transition fit | May give clearance or interference |
| Circularity | Individual cross-sectional slices |
| Cylindricity | Entire cylindrical surface |
| Circular run-out | Slices relative to datum axis |
| Total run-out | Entire surface relative to datum axis |
| Straight knurl | Parallel lines |
| Diamond knurl | Crossed diagonal lines |
| Bearing convention | Crossed boxes |
| Fillet weld | Triangle |
| Spot weld | Circle |
| Weld symbol below line | Arrow side |
| Weld symbol above line | Other side |
| Circle at weld intersection | Weld all around |
| Flag at weld intersection | Site weld |

---

# Final Revision Priorities

> [!tip]
> For visual questions, work from **geometry and drawing conventions**, rather than memorising the appearance of one example.

1. Be able to distinguish **1st vs 3rd Angle Projection** quickly.
2. Recognise every major **section type** from the cutting plane.
3. Know conventional **internal/external thread representation**.
4. Be comfortable calculating **limits, fits, clearance and interference**.
5. Distinguish geometric tolerances by **what is constrained** and whether a **datum** is required.
6. Practise reconstructing objects between **orthographic and isometric** views.
7. Memorise high-frequency **drawing conventions and abbreviations**.
8. Practise reading weld symbols systematically: **joint → symbol → side → supplementary notation → dimensions**.

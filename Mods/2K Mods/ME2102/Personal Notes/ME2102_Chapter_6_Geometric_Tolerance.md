# ME2102 — Chapter L06: Geometric Tolerance

> [!summary] Chapter overview
> Limit tolerances specify allowable ranges for individual linear or angular dimensions, but they do not fully constrain the **form, shape, orientation, or location** of every point on a manufactured part. This lecture introduces **geometric tolerance** as additional drawing notation for constraining these properties. It covers intrinsic and extrinsic geometric tolerances, datum references, common tolerance symbols and tolerance zones, and concludes with **surface texture / roughness** and its engineering-drawing notation.

---

## Why Limit Tolerance Is Insufficient

Limit tolerances provide an allowable range for a single dimension, but a part can still satisfy those limits while having an undesirable overall form or shape.

The lecturer highlights assumptions that are often made when reading an engineering drawing:

- a drawn straight line is assumed to represent a straight feature;
- a planar surface is assumed to be flat;
- surfaces that appear perpendicular are assumed to be perpendicular;
- a cylindrical surface is assumed to behave like a cylinder.

These assumptions are not necessarily communicated by ordinary limit tolerances.

![[Attachments/Limit_Tolerance_Insufficient.png]]

For example, a shaft may remain within its permitted diameter limits while becoming tapered or bent. Similarly, the axes of different cylindrical features may be misaligned even though every individual diameter remains within its stated limits.

> [!important]
> **Limit tolerance and geometric tolerance constrain different things.** Limit tolerance constrains the values of dimensions; geometric tolerance constrains the shape, form, orientation, or location of features.

Geometric tolerance therefore adds notation to communicate which geometric deviations are acceptable to manufacturing.

---

## Geometric Tolerance Notation

A geometric tolerance is communicated using a sequence of boxes. The lecturer describes the information in these boxes as:

1. a **symbol** identifying the type of geometric tolerance;
2. a **number** specifying how much deviation is allowed;
3. where required, later boxes identifying **datum references** to which the tolerance is related.

Geometric tolerance does **not** replace limit tolerance. Both can appear on the same engineering drawing because they constrain different properties.

### Geometric tolerance characteristics

The lecture groups the common characteristics as follows:

| Feature | Tolerance group | Characteristics |
|---|---|---|
| Individual features | Form | Straightness, Flatness, Circularity (Roundness), Cylindricity |
| Individual or related features | Profile | Profile of any line, Profile of any surface |
| Related features | Orientation | Parallelism, Perpendicularity, Angularity |
| Related features | Location | Position, Concentricity, Symmetry |
| Related features | Run-out | Circular Run-out, Total Run-out |

![[Attachments/Geometric_Tolerance_Symbols.png]]

The lecturer emphasizes that you should be able to **identify the common symbols** and have an idea of what each one constrains.

---

## Intrinsic and Extrinsic Tolerances

### Intrinsic tolerances

An **intrinsic** tolerance describes a feature relative to its own geometry rather than relative to another feature.

Examples introduced as intrinsic include:

- Straightness
- Flatness
- Circularity
- Cylindricity
- Profile when used intrinsically

For example, flatness asks whether the points on a surface can lie between two sufficiently close parallel planes. It does not require those planes to be aligned to another surface.

### Extrinsic tolerances

An **extrinsic** tolerance describes a feature in relation to another feature or datum.

Examples include:

- Parallelism
- Perpendicularity
- Angularity
- Position
- Concentricity
- Symmetry
- Circular Run-out
- Total Run-out
- Profile when used extrinsically

> [!important]
> **Profile of any line** and **profile of any surface** can be used in either an intrinsic or an extrinsic capacity.

---

## Form Tolerances

### Straightness

Straightness constrains lines running in a specified direction on a feature.

For a straightness tolerance of `0.01`, the measured line must remain within a tolerance band whose separation is `0.01 mm`. The lecturer explains that this does **not** require the entire surface to be flat: lines in the specified direction may be straight while the surface can still vary in another direction.

![[Attachments/Straightness_Tolerance_Zone.png]]

A **dial gauge** can be moved along the feature to sample its variation. If the maximum and minimum readings differ by more than the allowed tolerance, the required straightness has not been achieved.

For a cylindrical feature, straightness can similarly constrain lines running along the axis without requiring the cross-section itself to be circular.

### Flatness

Flatness extends the idea of straightness from lines to an entire surface.

For a flatness tolerance of `0.05`, the complete surface must be able to lie between **two parallel planes separated by 0.05 mm**.

![[Attachments/Flatness_Tolerance_Zone.png]]

Flatness is intrinsic: the orientation of those two planes is not defined relative to another datum.

### Circularity

Circularity constrains individual cross-sectional slices of a cylindrical, conical, or other rotational feature.

At any given section, the surface must lie between **two concentric circles** whose separation is the specified tolerance.

![[Attachments/Circularity_Tolerance_Zone.png]]

The lecturer stresses that circularity does not require:

- every cross-section to have the same radius;
- every cross-section to have the same centre;
- the overall feature to be cylindrical.

A conical or varying profile can still satisfy circularity as long as each required cross-section is sufficiently circular.

### Cylindricity

Cylindricity constrains the entire surface rather than separate one-dimensional cross-sectional slices.

The surface must lie between **two cylinders** whose radii are separated by the specified tolerance.

![[Attachments/Cylindricity_Tolerance_Zone.png]]

> [!important]
> The lecture compares **circularity** with a one-dimensional slice constraint and **cylindricity** with a constraint on all points of the cylindrical surface.

---

## Profile Tolerances

Profile tolerances generalize the earlier form tolerances to arbitrary shapes.

### Profile of any line

A line-profile tolerance constrains a **one-dimensional arbitrary curve**. The manufactured curve must remain close to an ideal profile specified by the drawing or model.

The lecturer uses the idea of an arbitrary aeroplane-wing curve: the produced profile should fit within a tolerance region around the ideal curve.

### Profile of any surface

A surface-profile tolerance similarly constrains an **arbitrary two-dimensional surface**.

The lecture illustrates that profile can be used:

- **intrinsically**, to match an idealized line or surface; or
- **extrinsically**, to make one surface follow another referenced surface even if that reference surface itself varies within its allowed tolerance.

---

## Datum References

Extrinsic tolerances require a reference. A **datum** is an idealized plane or axis used as that reference.

Datum references are shown using lettered tags that look like small flags.

![[Attachments/Datum_References.png]]

In this lecture, datum references are treated as:

- **planes**, usually associated with planar surfaces; or
- **lines / axes**, usually associated with the axes of cylindrical features.

> [!warning]
> When a datum is attached to a cylindrical feature, the lecturer emphasizes that the datum is **not the outer cylindrical surface**. It represents the idealized axis associated with that feature.

A datum tag may be placed directly against a feature or on an extension/projection line associated with that feature.

---

## Orientation Tolerances

### Parallelism

Parallelism is described as similar to flatness, but with an additional requirement: the two planes defining the tolerance zone must be **parallel to a specified datum**.

A surface can therefore be very flat but still fail a parallelism requirement if its overall angle relative to the datum is incorrect.

![[Attachments/Parallelism.png]]

> [!important]
> Parallelism is stronger than flatness in the sense described in the lecture: it constrains the surface within two planes **and** fixes the orientation of those planes relative to a datum.

### Perpendicularity

Perpendicularity similarly constrains a surface between two planes, but those planes must be **perpendicular to a specified datum**.

The actual surface does not have to be perfectly perpendicular at every point; it must remain within the permitted tolerance zone defined by the two perpendicular planes.

![[Attachments/Perpendicularity.png]]

### Angularity

Angularity generalizes parallelism and perpendicularity to an arbitrary specified angle.

For the example in the lecture, the surface must remain between two planes oriented at `30°` relative to datum face A, with a tolerance-zone separation of `0.2`.

![[Attachments/Angularity.png]]

---

## Location Tolerances

### Position

Position tolerance constrains the location of the **axis** of a feature such as a drilled hole relative to its ideal position.

The lecture example locates a hole centre `45 mm` from one reference and `15 mm` from another. Rather than giving independent limit tolerances in two perpendicular directions, position tolerance creates a **circular/cylindrical tolerance zone** around the ideal position.

The lecturer's key distinction is that ordinary coordinate limit tolerances would create a rectangular allowable region, while position tolerance allows a symmetric region around the desired centre.

![[Attachments/Position.png]]

### Symmetry

Symmetry constrains the idealized centre plane of a feature relative to a datum centre plane.

The lecture explains that a datum can represent the average or idealized plane between two opposite surfaces. The corresponding centre plane of another feature must then remain within the specified tolerance zone around that datum plane.

![[Attachments/Symmetry.png]]

### Concentricity

Concentricity constrains the **axes of cylindrical features**, not their outer surfaces.

The axis of one cylindrical feature must remain within a cylindrical tolerance zone relative to the datum axis.

![[Attachments/Concentricity.png]]

> [!warning]
> Concentricity is about the alignment of **centres / axes**. The lecturer notes that these idealized centres are difficult to measure directly, which is one reason run-out is a more practical way to measure related cylindrical behaviour.

---

## Run-out

Run-out is used for cylindrical or rotational features relative to a datum axis.

### Circular Run-out

Circular run-out is the one-dimensional version. Individual circular slices are constrained relative to the referenced datum axis.

### Total Run-out

Total run-out constrains all points over the outside of the cylindrical surface relative to the datum axis.

![[Attachments/Circular_Total_Runout.png]]

The lecturer compares:

- **Circularity** → circular slices constrained intrinsically;
- **Cylindricity** → the full cylindrical surface constrained intrinsically;
- **Circular Run-out** → circular slices constrained relative to a datum axis;
- **Total Run-out** → the full cylindrical surface constrained relative to a datum axis.

A practical measurement can be made by rotating the part about the datum axis and using a dial gauge to observe how much the surface reading varies.

---

## Reading a Geometric-Tolerance Example

The lecture returns to the rotationally symmetric example to show how geometric tolerances add information that limit tolerances alone cannot communicate.

![[Attachments/Geometric_Tolerance_Example.png]]

In the example:

- the left reference surface has a **flatness** tolerance;
- that surface is identified as **datum A**;
- another cylindrical feature is constrained by **perpendicularity** relative to A;
- position tolerances constrain cylindrical axes relative to datum references.

The lecturer notes that the course does **not** require students to design and apply a complete geometric-tolerance scheme to their own drawings. The expected focus is recognizing the symbols and understanding what they are trying to constrain.

---

## Surface Texture / Roughness

Geometric tolerance primarily addresses the permitted geometric extent of a feature. The lecture then introduces **surface texture / roughness** to describe smaller-scale variation over a surface.

A surface can contain different scales of variation:

- fine-grained roughness;
- broader waviness;
- flaws or scratches;
- tool-mark direction.

### Surface roughness measurement

The surface profile is measured over a specified **cut-off length** $L$. The lecture gives typical cut-off lengths of:

- `0.25 mm`
- `0.8 mm`
- `2.5 mm`

The profile is referenced to its mean line. The roughness value is shown as:

$$
R_a=\frac{A_1+A_2+A_3+A_4+\ldots+A_n}{L}
$$

![[Attachments/Surface_Roughness_Measurement.png]]

The lecturer explains this as adding the areas of the profile above and below the mean line and dividing by the cut-off length. $R_a$ therefore has units of length.

For a purely triangular profile, the slide notes:

$$
R_a=R_t/4
$$

The instrument identified in the slide is the **Taylar-Hobson Talysurf**.

### Roughness grades

The lecture provides roughness grades from **N1 to N12**, corresponding to increasing $R_a$ values. The chart does not need to be memorized; the lecturer states that a chart would be provided if required.

The manufacturing-process chart shows that different processes achieve different typical surface roughness ranges. The lecturer contrasts rougher processes such as sand casting and forging with processes such as grinding, honing, polishing, lapping, tumbling, and super-finishing, which can produce much smaller surface variation.

---

## Surface Texture Symbols

The surface-texture symbol can carry several annotations.

![[Attachments/Surface_Texture_Symbol.png]]

The lecture identifies:

- **roughness value $R_a$**;
- **cut-off length**;
- **production process**, such as `MILL`;
- **tool marks or lay direction**;
- **machining allowance**, representing material intentionally left for later machining.

The lecturer gives the example that a cast part may be made larger so that a later machining process has material available to remove.

### Symbol interpretation

![[Attachments/Surface_Texture_Symbol_Interpretation.png]]

The slide distinguishes symbols that indicate:

- machining is necessary to obtain the desired surface texture;
- material removal is **not permitted**;
- a particular machining process and roughness value;
- maximum and minimum limits of surface roughness obtained by a machining process;
- maximum and minimum limits of surface roughness obtained without machining.

> [!important]
> A **circle** on the surface-texture symbol indicates that material removal is **not permitted**.

The lecturer also notes the drawing convention that the leader/flag projects to the **right**.

---

## Lecture Practice Questions

### Identifying total run-out

The lecture asks which symbol denotes **total run-out**. The correct choice is **B**, the double-arrow run-out symbol. The lecturer contrasts it with circular run-out and the line/surface profile symbols.

![[Attachments/Practice_Total_Runout.png]]

### Geometric tolerance that does not require a datum

Among **concentricity, cylindricity, circular run-out, and perpendicularity**, the correct choice is **cylindricity**. The lecturer explains that cylindricity is intrinsic, whereas the other three require a datum reference.

![[Attachments/Practice_Datum.png]]

### Symbol for no material removal

The correct choice is **D**. The circle on the surface-texture symbol means that material should **not** be removed from the surface. The lecturer also notes that the leader projects to the right by convention.

![[Attachments/Practice_Material_Removal.png]]

---

## Chapter Summary / Key Connections

- **Limit tolerance** constrains allowable dimensional ranges but does not fully constrain form, shape, orientation, or location.
- **Geometric tolerance** adds symbols and tolerance values to communicate those additional requirements.
- **Intrinsic tolerances** describe a feature relative to itself.
- **Extrinsic tolerances** require a datum or another reference feature.
- **Straightness, flatness, circularity, and cylindricity** constrain form.
- **Profile** generalizes these ideas to arbitrary curves and surfaces and can be intrinsic or extrinsic.
- **Datum references** provide idealized planes or axes for extrinsic tolerances.
- **Parallelism, perpendicularity, and angularity** constrain orientation relative to a datum.
- **Position, symmetry, and concentricity** constrain feature location or alignment.
- **Circular and total run-out** constrain rotational features relative to a datum axis and can be checked using rotation and a dial gauge.
- **Surface texture / roughness** describes smaller-scale surface variation over a specified cut-off length.

---

## Exam / Revision Checklist

- [ ] Can I explain why limit tolerances alone may be insufficient?
- [ ] Can I distinguish limit tolerance from geometric tolerance?
- [ ] Can I identify the common geometric-tolerance symbols shown in the lecture?
- [ ] Can I distinguish intrinsic from extrinsic tolerances?
- [ ] Can I explain straightness, flatness, circularity, and cylindricity using their tolerance zones?
- [ ] Can I distinguish circularity from cylindricity?
- [ ] Can I explain the difference between profile of a line and profile of a surface?
- [ ] Can I explain what a datum represents in this lecture?
- [ ] Can I explain parallelism, perpendicularity, and angularity relative to a datum?
- [ ] Can I explain why position tolerance differs from two independent coordinate limit tolerances?
- [ ] Can I explain what symmetry and concentricity constrain?
- [ ] Can I distinguish circular run-out from total run-out?
- [ ] Can I distinguish circularity/cylindricity from circular/total run-out?
- [ ] Can I explain how a dial gauge is used conceptually to inspect geometric variation?
- [ ] Can I identify the meaning of $R_a$ and the cut-off length $L$?
- [ ] Can I interpret the surface-texture symbols introduced in the lecture?
- [ ] Can I identify the symbol indicating that material removal is not permitted?

---

## Key Equations / Relationships

> [!summary] Core relationships
> Surface roughness value:
>
> $$
> R_a=\frac{A_1+A_2+A_3+A_4+\ldots+A_n}{L}
> $$
>
> For a purely triangular profile:
>
> $$
> R_a=R_t/4
> $$
>
> Typical cut-off lengths shown in the lecture: `0.25 mm`, `0.8 mm`, `2.5 mm`.

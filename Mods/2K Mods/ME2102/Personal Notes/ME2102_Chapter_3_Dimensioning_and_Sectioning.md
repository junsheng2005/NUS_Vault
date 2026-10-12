# ME2102 — Lecture 03: Dimensioning & Sectioning

> [!summary] Chapter overview
> This lecture introduces **dimensioning** as the method for communicating lengths, angles, sizes, and design intent on engineering drawings, followed by **sectioning** as a method for revealing internal geometry. The lecture emphasizes clear communication: drawings should be **minimal and complete**, dimensions should be placed and styled clearly, and section views should expose internal features without unnecessary clutter.

---

## 1. Dimensioning

### Purpose of dimensions

A dimension is a **specification of a length or angle** on an engineering drawing. A drawing is **fully dimensioned** when it is both:

- **Complete** — enough information is present to identify the part unambiguously under the drawing conventions being used.
- **Minimal** — redundant information that can be computed from other dimensions is omitted.

Dimensions should also be placed on an **appropriate view**.

![[Attachments/dimensioning_overview.png]]

The lecturer explains that some geometry is inferred using normal drawing assumptions. For example, straight-looking lines are taken as straight, perpendicular-looking lines as perpendicular, circular-looking curves as parts of circles, and regular-looking polygons as regular unless dimensions indicate otherwise. Symmetry can likewise allow repeated dimensions to be omitted.

> [!important]
> Minimal does **not** mean leaving necessary information out. It means communicating everything needed without adding dimensions that are already determined by other information.

### Units and default interpretation

For this class, numbers without explicitly stated units are taken to be in **millimetres** unless stated otherwise. Engineering drawings normally specify a sheet unit so the unit does not need to be repeated after every dimension.

The lecturer also warns that SolidWorks installations may use a different default unit, so the model units must be checked when completing assignments.

### Dimension precision and tolerance

The number of displayed digits communicates precision and can imply tolerance. The lecturer's default interpretation is to measure one additional decimal place beyond the displayed dimension and check whether it rounds to the displayed value.

Thus, writing `50` is not equivalent in meaning to writing `50.0000`. Unnecessarily high precision can imply that much tighter manufacturing control and inspection are required, increasing fabrication cost.

> [!warning]
> Do not add decimal places merely for appearance. Precision on an engineering drawing communicates manufacturing requirements.

---

## 2. Dimension and Projection Lines

### Dimension lines

A **dimension line** carries the numerical length or angle and normally terminates in arrowheads. Depending on available space, the arrowheads may be:

- inside the measured extent and pointing outward; or
- outside the measured extent and pointing inward.

The second arrangement is useful for very thin features where there is insufficient space for arrowheads inside the feature.

### Projection lines

Projection lines connect the dimension line to the points or features being measured.

The lecture recommends:

- a small gap between the projection line and the part where possible;
- a short extension beyond the dimension line;
- dimension lines spaced sufficiently apart for clarity; and
- dimensions arranged mainly horizontally or vertically unless a particular design reason requires otherwise.

The lecturer connects this preference for orthogonal dimensions to machining: machine tools commonly work in a three-axis reference frame, so horizontal and vertical dimensions are more directly useful than diagonal distances.

### Dimensioning points

Projection lines may pass through or touch a point of interest, including a point that is not itself a vertex of the final part. Intersections may be emphasized with dots.

This can communicate **design intent** or how a part is made. A dimension may deliberately identify the size at a particular location because that location is functionally important, rather than merely dimensioning the geometric endpoints of a sloping feature.

### Positioning for clarity

Dimensioning conventions are guides for communication. Prefer arrangements that:

- keep dimension lines well spaced;
- avoid unnecessary overlap with centre lines or centre marks;
- avoid placing dimension lines directly over the part when possible; and
- avoid unnecessary crossings.

> [!important]
> The lecturer repeatedly emphasizes that engineering drawings are **communication documents**. A convention may be broken when doing so genuinely improves communication.

---

## 3. Datum and Chain Dimensioning

### Common datum / datum dimensioning

A useful approach is to choose a common reference or **datum** and measure multiple positions from it.

![[Attachments/common_datum.png]]

Benefits discussed in the lecture include:

- a clean and systematic way to choose dimensions;
- easier interpretation by the machinist; and
- reduced accumulation of tolerance error between distant features.

### Chain dimensioning

In **chain dimensioning**, consecutive distances are specified one after another. The slide states that it should only be used where possible accumulation of tolerances does not endanger the functional requirements of the part.

The lecturer explains that if each chained distance is allowed some deviation, the deviations can accumulate across the chain. Chain dimensioning can also become visually ambiguous when many arrowheads are crowded together.

> [!tip]
> The lecturer recommends using datum dimensioning when possible. If chain dimensioning is necessary, offset the dimension lines so the corresponding arrowheads remain clear.

---

## 4. Leaders and Repeated Features

### Leader lines

A **leader** indicates where a dimension or note applies.

- An **arrowhead** can point to an edge or surface viewed from the side.
- A **dot** can terminate on a face viewed head-on.

Leaders can be used for notes such as surface instructions and also for dimensions such as radii and diameters.

Leader lines should not run so close to an edge that they visually merge with the part, and they should avoid touching unrelated lines.

### Avoiding long or intersecting leaders

Repeated dimensions may be shown separately rather than connecting many long leaders to one note. When repeated features are visually too similar to infer safely, letter symbols can identify groups of features sharing the same dimension.

![[Attachments/leaders_pitch_circle.png]]

The lecture also shows a circular arrangement of holes. A sketch-style circle can be used to communicate the common circle on which their centres lie. This is called the **pitch circle diameter (PCD)**.

---

## 5. Units, Dual Dimensioning, and Text Positioning

### Sheet units and other units

If all dimensions use the same unit, the unit can be specified for the whole sheet. Any dimension using a different unit must state that unit explicitly.

### Dual dimensioning

When a dimension must be given in a unit different from the sheet unit, an approximate equivalent may be added in parentheses as auxiliary information, for example:

`100 mm (3.94 in.)`

The value in parentheses is auxiliary rather than the driving value.

Use dual dimensioning only when it is actually needed.

### Angles

Angles may be given in radians or in degrees. The slides also show degrees/minutes/seconds notation such as:

`22°30'30"`

### Position of dimension text

Dimension text is generally placed:

- above or to the left of its dimension line; and
- near the middle of the line.

The lecture shows two text-orientation conventions, while noting that keeping text oriented to the sheet is commonly seen.

---

## 6. Redundant and Auxiliary Dimensions

### Redundant dimensions

A cycle of dimensions should not be created when one dimension can be calculated from the others. For example, if an overall dimension and all but one intermediate distance are given, the final intermediate distance is determined and should normally be omitted.

![[Attachments/redundant_dimensions.png]]

An overall dimension can still be useful because it tells the manufacturer the total stock length required.

### Auxiliary dimensions

Sometimes a useful overall or converted dimension is intentionally included even though it is determined by other dimensions. This is an **auxiliary dimension** and is placed in parentheses.

Auxiliary dimensions are provided for convenience and are not intended to drive tolerance requirements.

> [!example]
> In the lecture practice question, the parenthesized overall dimension is best identified as an **auxiliary dimension**. It is also overall and redundant in a descriptive sense, but the parentheses specifically mark its auxiliary status.

---

## 7. Dimensioning Diameters and Radii

### Diameters

The diameter symbol `Ø` is used only for circular or cylindrical features. A dimension crossing an axis of symmetry is not automatically a diameter if the measured feature is not cylindrical.

Diameters may be shown:

- across the feature in a suitable orthographic or section view; or
- with a leader pointing to the circular/cylindrical surface.

When a leader specifies a diameter or radius, it should be aligned with the centre of curvature.

![[Attachments/diameter_leaders.png]]

For doubly curved spherical surfaces, the drawing may explicitly state **Sphere** to distinguish the surface from the more common cylindrical surfaces.

### Radii

The abbreviation `R` precedes a radius value. Leaders point to the curved surface and align with the centre of curvature.

If a straight and curved surface appear tangent, tangency may be inferred. This can make an additional radius or diameter dimension unnecessary when the geometry is already determined.

### Large-radius curves

For very large radii whose centres would lie far outside the practical drawing area, the radius dimension line may be broken or kinked. The centre can then be represented at a convenient location while dimensions locate the true centre relative to the part.

---

## 8. Sectioning

### Purpose of section views

Sectioning provides a way to see **inside** a part when ordinary external orthographic views would hide important internal features. It can replace a view that would otherwise require many hidden lines.

The lecture covers:

- Full Section
- Half Section
- Offset Section
- Aligned Section
- Part / Broken-out Section
- Revolved Section

---

## 9. Full Section

A **full section** uses a cutting plane that passes completely through the object.

Procedure shown in the lecture:

1. Define the cutting plane in another view.
2. Use arrows to indicate the direction from which the section is viewed.
3. Imagine removing the material on the viewing side of the cutting plane.
4. Draw the visible edges behind the cutting plane.
5. Cross-hatch the surfaces actually cut by the plane.

![[Attachments/full_section.png]]

The cutting-plane line commonly uses a centre-line style even though it is serving a different purpose. Different arrow-placement conventions may be seen; the important information is the **direction the arrows point**.

A section view can replace the corresponding ordinary orthographic view instead of being added as another redundant view.

### Hidden lines in section views

Because a section view is intended to reveal the interior, hidden lines are commonly omitted unless they help communicate something important. This is a rule of thumb rather than an absolute prohibition.

---

## 10. Hatching

Cut surfaces are identified by **section lines / hatching**.

Typical hatching style shown in the lecture:

- thin lines, approximately `0.3 mm`;
- equally spaced, approximately `4–6 mm`;
- normally at `45°`;
- changed to another angle when `45°` would align with the outline or axes and cause confusion.

![[Attachments/hatching_rules.png]]

Good hatching should have even spacing, should not be excessively dense or thick, and should remain inside the outline.

### Same and adjacent components

For separated cut areas belonging to the **same component**, use the same hatching slope and spacing.

For **adjacent different components**, change the hatching slope and/or spacing so the components remain distinguishable. Spacing can also be adjusted for very thin details.

---

## 11. Sectioning Exceptions

Some elements are **not typically cross-hatched** when sectioned by convention:

- ribs;
- spokes;
- gear teeth;
- shafts;
- rods;
- bolts;
- nuts;
- rivets;
- keys;
- pins.

![[Attachments/section_exceptions.png]]

### Why these exceptions are used

The lecturer explains several motivations:

- **Ribs** are support/web features; hatching them longitudinally can obscure the intended form of the supported structure.
- **Spokes and gear teeth** can produce awkward or misleading sections depending on rotational alignment.
- **Shafts and rods** are usually on-axis components whose interiors add little useful information.
- **Bolts, nuts, rivets, keys, and pins** are commonly off-the-shelf functional components, so their internal section is usually not what the drawing needs to communicate.

These are conventions rather than absolute rules. A feature can be sectioned when there is a specific reason to show its internal geometry.

> [!example]
> In the lecture practice question, **pulleys** are the item that is normally cross-hatched; shafts, ribs, and nuts are on the exception list.

---

## 12. Half Section

A **half section** combines half of an external orthographic view with half of a section view.

![[Attachments/half_section.png]]

It is mainly used to exploit symmetry and show the **inside and outside simultaneously** in a minimum number of views.

The lecturer's useful mental model is:

1. Make a full external orthographic view.
2. Make a full section view.
3. Take half of each.
4. Join them along the centre line.

The two halves are separated by a **centre line**, not an outline. Hidden lines are normally shown only on the outside half.

---

## 13. Offset Section

An **offset section** changes the position of the cutting plane so features lying in different parallel planes can be shown together in one section view.

![[Attachments/offset_section.png]]

The lecture describes the cutting plane as having parallel portions connected by `90°` offsets. This allows several holes or internal features that are not coplanar to appear simultaneously in one section view.

> [!important]
> To recognize an offset section, inspect the view that defines the cutting plane. The resulting section itself may look similar to an ordinary full section.

---

## 14. Aligned Section

An **aligned section** rotates the cutting plane about an axis without offset and presents the cut features as though they lie in one plane.

![[Attachments/aligned_section.png]]

The lecturer suggests thinking of it as **two half section views joined around a rotation centre**. Unlike an offset section, the cutting plane bends around the centre rather than using two `90°` offsets separated by an unseen transition.

---

## 15. Part / Broken-out Section

A **part section** or **broken-out section** exposes only a local subset of the part.

![[Attachments/broken_out_section.png]]

It is useful when:

- only a small internal region needs to be shown; or
- a full section would conceal external features that must remain visible.

A freeform/squiggly boundary commonly marks the transition between the sectioned and unsectioned regions. A separate cutting-plane view is often unnecessary when the local cut location is obvious.

---

## 16. Revolved Section

A **revolved section** shows a local cross-section directly on the outside view.

![[Attachments/revolved_section.png]]

The method is:

1. take a thin cross-sectional slice through an arm, rib, or similar feature;
2. revolve the cutting plane by `90°`; and
3. draw the resulting cross-section directly on the part.

Unlike the other section views discussed, the purpose is to show the local cross-sectional shape without drawing all geometry behind the cutting plane.

---

## Chapter Summary / Key Connections

Dimensioning and sectioning both serve the same overall purpose: **clear and unambiguous engineering communication**.

- Dimensioning communicates the **size, position, and functional importance** of features.
- A fully dimensioned drawing is **minimal and complete**.
- Datum dimensioning helps avoid tolerance accumulation compared with long chains of dimensions.
- Leaders, auxiliary dimensions, diameter/radius notation, and text positioning improve clarity without unnecessary clutter.
- Section views reveal **internal geometry** that external views may not communicate clearly.
- Full sections establish the basic sectioning method; half, offset, aligned, broken-out, and revolved sections adapt that method for different geometric situations.
- Hatching identifies cut material and can distinguish adjacent components.
- Certain elements are conventionally left unhatched when sectioned.

## Exam / Revision Checklist

- [ ] Can I explain why a fully dimensioned drawing must be both **minimal** and **complete**?
- [ ] Can I distinguish a **dimension line**, **projection line**, and **leader line**?
- [ ] Can I recognize good dimension placement and spacing?
- [ ] Can I explain the difference between **datum dimensioning** and **chain dimensioning**?
- [ ] Can I explain why chain dimensioning can accumulate tolerance error?
- [ ] Can I identify an **auxiliary dimension** from parentheses?
- [ ] Can I distinguish diameter `Ø` notation from radius `R` notation?
- [ ] Can I recognize a **pitch circle diameter (PCD)** arrangement?
- [ ] Can I explain what a **full section** shows and how the viewing arrows work?
- [ ] Can I identify correct hatching style and distinguish hatching of adjacent components?
- [ ] Can I recall the common sectioning exceptions: ribs, spokes, gear teeth, shafts, rods, bolts, nuts, rivets, keys, and pins?
- [ ] Can I distinguish **full**, **half**, **offset**, **aligned**, **broken-out**, and **revolved** section views from unfamiliar drawings?
- [ ] Can I recognize an offset section from the `90°` bends in its cutting plane?
- [ ] Can I explain why a half section uses a centre line between the two halves?

## Key Concepts / Relationships

> [!summary] Core reference
> - **Fully dimensioned** = minimal + complete
> - Sheet dimensions in this class default to **millimetres** unless stated otherwise
> - **Datum dimensioning**: dimensions measured from a common datum
> - **Chain dimensioning**: consecutive dimensions; tolerance accumulation must be considered
> - **Auxiliary dimension**: extra/reference information shown in parentheses
> - `Ø` = diameter of circular/cylindrical feature
> - `R` = radius
> - **Full section**: cutting plane passes completely through object
> - **Half section**: half external view + half section view
> - **Offset section**: cutting plane shifts through parallel planes using `90°` offsets
> - **Aligned section**: cutting plane rotates about an axis and is shown in one plane
> - **Broken-out section**: local section of only part of a view
> - **Revolved section**: local cross-section revolved `90°` and drawn directly on the outside view

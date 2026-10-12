# ME2102 --- Chapter 2: Multiview Projection

> [!summary] Chapter overview This lecture completes the discussion of
> projection and then develops **multi-view drawings**: how to choose
> useful orthographic views, how to arrange them using **1st Angle
> Projection** and **3rd Angle Projection**, and how **auxiliary
> projections** can show inclined surfaces head-on. The lecturer
> emphasizes communicating a part with enough information to understand
> it, while avoiding unnecessary or redundant views.

------------------------------------------------------------------------

## Projection Recap

The lecture begins by finishing the previous topic on projecting
three-dimensional objects onto two-dimensional planes.

The lecturer distinguishes the projection types covered across the
projection topic:

-   **Single-view drawings**
    -   Orthographic
    -   Axonometric
    -   Oblique
    -   Perspective
-   **Multi-view drawings**
    -   3rd Angle Projection
    -   1st Angle Projection
    -   Auxiliary Views

### Orthographic and isometric views

Orthographic views correspond to views along the principal axial
directions. They are convenient to draw on square grid paper because two
principal directions appear at right angles while the third direction
goes into and out of the page.

Isometric views look from a corner direction of an axis-aligned cube and
provide an even view of the principal directions. The corresponding
equal spacing gives rise to isometric grid paper.

------------------------------------------------------------------------

## Oblique Projection

An **oblique projection** keeps one face as an orthographic view while
showing the third direction at a chosen skew angle and scale.

The lecturer describes two parameters:

-   the **angle** used for the oblique direction;
-   the **scale** used for the third direction.

Common projection angles mentioned are **45 degrees** and **30
degrees**, although other angles may be used.

### Cavalier projection

For a **cavalier projection**, the oblique direction uses a **1 to 1
scaling**.

-   A length in the third direction is drawn at the same scale as the
    corresponding lengths in the orthographic directions.
-   This makes measurement in that direction possible.
-   However, the object can appear much longer or deeper than expected
    to the eye.

### Cabinet projection

For a **cabinet projection**, the oblique direction is drawn at **half
scale**.

The lecturer notes that this often looks better visually than a 1 to 1
depth scale.

> [!important] The distinction between **cavalier** and **cabinet**
> projection is determined by the **scale**, not by the projection
> angle.

Oblique projections can appear in building or assembly instructions
where one face needs to remain clear and dimensionally faithful while
some depth information is still communicated.

The lecturer does not use oblique projection as a main drawing method
for the rest of the course.

------------------------------------------------------------------------

## Perspective Projection

Perspective projection resembles how objects are seen visually: lines
that are parallel on the object can appear to converge toward a
**vanishing point**.

The lecture distinguishes:

-   **one point projection** --- perspective is applied in one principal
    direction;
-   **two point projection** --- perspective is applied in two principal
    directions;
-   **three point projection** --- perspective is applied in all three
    principal directions.

The lecturer notes that two point projection is common, while adding
perspective in the vertical direction can emphasize the apparent height
of a building.

> [!warning] Perspective projection is useful for realistic rendering,
> but it **distorts distances**. Because engineering drawings are
> intended to communicate dimensions and geometry clearly, perspective
> projection is not the main projection method used in this course.

------------------------------------------------------------------------

## Multi-view Drawings

A part has six standard orthographic directions: front/back, top/bottom,
and left/right. However, engineering drawings usually do **not** need
all six.

The lecture emphasizes:

-   usually using at most **3 principal views**;
-   often using only **1 or 2 views**;
-   choosing views according to how clearly they communicate the part.

![[Attachments/Choosing_Views.png]]

### Choosing useful views

When deciding which views to keep, prefer views that expose important
geometry directly rather than compressing information into many hidden
lines.

In the first lecture example:

-   the **plan view** is valuable because it directly shows the circular
    hole;
-   the **front view** communicates the overall shape well;
-   the **right view** contains more overlapping visible and hidden
    information.

The lecturer therefore presents the plan + front combination as a good
choice.

In the tuning-fork-shaped example:

-   the **front view** clearly shows the circular features;
-   the **plan view** best communicates the fork-like shape;
-   the **right view** compresses information and contains many hidden
    lines.

Again, the lecturer prefers the two views that communicate the
distinctive geometry most directly.

> [!important] More views are not automatically better. An unnecessary view can make a reader search for a difference that does not actually exist. The drawing should communicate the design with the useful  information, not simply the maximum amount of information.

### Hidden lines, centre marks and centre lines

The lecture uses:

-   **hidden lines** to indicate geometry that is not directly visible
    from a view;
-   a **centre mark** when a rotationally symmetric feature such as a
    cylinder is viewed along its axis and appears as a circle;
-   a **centre line** when the axis of a rotationally symmetric feature
    is viewed from the side.

These marks help communicate cylindrical or rotationally symmetric
geometry even when some of it is hidden.

------------------------------------------------------------------------

## Choosing the Number of Projection Views

![[Attachments/Number_of_Views.png]]

### One-view parts

A part can sometimes be communicated using only **one view**.

The lecture's example is a rotationally symmetric part whose shape is fully described by its side profile together with its centre line. Because the profile is rotated about the axis, another principal view does not add necessary shape information.

The lecturer notes that additional features, such as a bore or features on an end face, could make another view necessary.

### Two-view parts and "structurally monotonic" geometry

The lecturer introduces the informal term **structurally monotonic** as a rule of thumb for parts that may be communicated using two views.

A structurally monotonic part has an orthographic direction from which its geometry can be seen without hidden lines. When imagined as successive slices, each cross-section is contained within the cross-sections below it, so there is no undercut hidden from that direction.

If one view exposes all of the geometry clearly, a second view can then provide the required depth information.

> [!tip] A useful lecturer-supported rule of thumb is to look for a
> view with **no hidden lines**. If the geometry is clearly visible from
> that direction and another view communicates the depth, two views may  be sufficient.

------------------------------------------------------------------------

## Angle of Projection

Multi-view drawings need a standard layout so that engineers can
understand how the views relate to each other without relying on labels
such as "front", "top", or "right".

The lecture presents two standards:

-   **3rd Angle Projection**
-   **1st Angle Projection**

![[Attachments/First_vs_Third_Angle.png]]

### 3rd Angle Projection

![[Attachments/Third_Angle_Layout.png]]

In 3rd Angle Projection:

-   the **right view is placed on the right**;
-   the **left view is placed on the left**;
-   the **top view is placed on top**;
-   the **bottom view is placed on the bottom**.

The lecturer describes this as unwrapping the object from the front, or
rotating the object so that the face in a direction appears on that same
side.

### 1st Angle Projection

![[Attachments/First_Angle_Layout.png]]

In 1st Angle Projection, the arrangement is opposite:

-   the **right view is placed on the left**;
-   the **left view is placed on the right**;
-   the **top view is placed below**;
-   the **bottom view is placed above**.

The lecturer visualizes this by rotating the front face in the direction
where the new view will be placed; the opposite side then becomes
visible.

### Comparison

  -----------------------------------------------------------------------
  Relationship to the     3rd Angle Projection    1st Angle Projection
  front view                                      
  ----------------------- ----------------------- -----------------------
  Right-side view         Right                   Left

  Left-side view          Left                    Right

  Top view                Above                   Below

  Bottom view             Below                   Above
  -----------------------------------------------------------------------

> [!important] The lecturer recommends remembering either the rotation
> visualization or the simpler rule: **right is on the right and top is
> on the top for 3rd Angle Projection; the arrangement is opposite for
> 1st Angle Projection.**

### Projection symbols

The symbols used to identify the projection standard are themselves
multi-view drawings of a truncated cone.

The relative positions of:

-   the side view of the truncated cone; and
-   the view showing two concentric circles

indicate whether the engineering drawing uses 1st Angle or 3rd Angle
Projection.

### Why "1st" and "3rd" angle?

The lecture briefly shows the plane/quadrant construction from which the
names originate, but the lecturer explicitly recommends **not using that
construction as the main way to remember the standards** because it is
more complicated than necessary.

There is no corresponding 2nd Angle or 4th Angle Projection standard in
this treatment.

### Software defaults mentioned in the lecture

The lecturer states that:

-   **Fusion / AutoCAD** defaults to **1st Angle Projection**;
-   **SolidWorks** defaults to **3rd Angle Projection**;

and that the projection style can be changed in the software settings.

For course assignments, students need to select the projection standard
specified by the assignment.

------------------------------------------------------------------------

## Identifying 1st vs 3rd Angle Projection

![[Attachments/Third_Angle_Example.png]]

The lecture repeatedly practices identifying projection layouts from
sets of views.

### Procedure

1.  Choose one view as the reference.
2.  Determine which physical side of the object another view represents.
3.  Check where that view is placed relative to the reference.
4.  Apply the standard:
    -   same-side placement → 3rd Angle Projection;
    -   opposite-side placement → 1st Angle Projection.
5.  Check both the **horizontal** and **vertical** relationships.
6.  Ensure the view orientation corresponds to the required rotation
    rather than merely placing the correct face in the correct general
    location.

\\![[Attachments/Projection_Practice.png]]

> [!warning] A layout can be correct vertically but wrong
> horizontally, or vice versa. Such a layout is not a valid 1st or 3rd
> Angle Projection. Check both directions.

> [!warning] Correct projection is not only about which face appears
> in a position. The **rotation correspondence and orientation of the
> view** must also be correct.

### Symmetric objects

For a perfectly symmetric object, opposite views can be identical. In
the lecture example:

-   left and right views are the same;
-   top and bottom views are the same;
-   front and back views are the same.

Therefore the displayed views alone may be compatible with either 1st or
3rd Angle Projection.

------------------------------------------------------------------------

## Auxiliary Projection

Most orthographic views are taken along the principal directions.
Sometimes an inclined surface needs to be seen **head-on** even though
its normal direction is not one of those principal directions.

An **auxiliary projection** provides this additional view.

![[Attachments/Auxiliary_Projection.png]]

The slide describes an **auxiliary plane parallel with the inclined
surface**. The view is then projected so that the inclined surface can
be seen directly.

### Constructing / interpreting an auxiliary view

1.  Identify the inclined surface that needs to be viewed directly.
2.  Indicate the viewing direction with an arrow.
3.  Project the corresponding view in that direction.
4.  Lay out the auxiliary view according to the applicable projection
    convention.

The lecture examples use 3rd Angle Projection when placing the auxiliary
view.

![[Attachments/Auxiliary_Bracket.png]]

Auxiliary views are useful when a feature such as a hole, bolt pattern,
decal, connection, or mating surface lies on an inclined face and needs
to be communicated clearly.

### Centre marks on auxiliary features

The lecturer points out some inconsistency in the example drawings about
centre marks on features that are not aligned with the principal axes.

Either choice can be used in the examples shown, but the lecturer
recommends being **consistent** across the engineering drawing: either
include the relevant centre marks consistently or omit them
consistently.

------------------------------------------------------------------------

## Chapter Summary / Key Connections

-   Projection converts three-dimensional geometry into two-dimensional
    views.
-   Oblique projection preserves an orthographic face while adding depth
    at a chosen angle and scale.
-   Perspective projection uses vanishing points and is useful visually,
    but its distance distortion makes it less suitable for engineering
    communication.
-   Multi-view drawings combine orthographic views to communicate a
    part.
-   The number and choice of views should be based on how much useful
    geometry each view communicates.
-   Rotationally symmetric parts may sometimes require only one view.
-   Parts that the lecturer calls structurally monotonic may often be
    communicated with two views.
-   1st and 3rd Angle Projection are standardized ways to arrange
    related orthographic views.
-   In 3rd Angle Projection, views are placed on the corresponding side;
    in 1st Angle Projection, they are placed on the opposite side.
-   Auxiliary projections provide head-on views of inclined surfaces
    that are not aligned with the principal directions.

------------------------------------------------------------------------

## Exam / Revision Checklist

-   [ ] Can I distinguish orthographic, oblique and perspective
    projection as explained in the lecture?
-   [ ] Can I distinguish cavalier and cabinet projection by their
    scaling?
-   [ ] Can I explain why perspective projection is not preferred for
    engineering dimension communication?
-   [ ] Can I identify useful views and recognize when a view contains
    unnecessarily compressed or hidden information?
-   [ ] Can I recognize hidden lines, centre marks and centre lines?
-   [ ] Can I explain when a part may need 1, 2 or 3 principal views?
-   [ ] Can I apply the lecturer's "structurally monotonic" rule of
    thumb?
-   [ ] Can I identify 1st Angle Projection from a set of views?
-   [ ] Can I identify 3rd Angle Projection from a set of views?
-   [ ] Can I check both horizontal and vertical view relationships?
-   [ ] Can I recognize the projection-standard symbols?
-   [ ] Can I mentally rotate / unwrap a part to determine where each
    view belongs?
-   [ ] Can I explain why a symmetric object may not reveal which
    projection standard was used?
-   [ ] Can I explain why an auxiliary view is needed?
-   [ ] Can I identify the viewing direction for an inclined surface and
    interpret its auxiliary view?

------------------------------------------------------------------------

## Key Concepts / Relationships

> [!summary] Projection reference **Cavalier projection:** oblique
> direction uses 1 to 1 scaling.
>
> **Cabinet projection:** oblique direction uses half scale.
>
> **3rd Angle Projection:** right on right, left on left, top on top,
> bottom on bottom.
>
> **1st Angle Projection:** right on left, left on right, top below,
> bottom above.
>
> **Centre mark:** used when looking along the axis of a rotationally
> symmetric feature.
>
> **Centre line:** indicates the axis of rotation when the feature is
> viewed from the side.
>
> **Auxiliary projection:** provides a direct view of a surface not
> aligned with the principal orthographic directions.

# ME2102 - Chapter 4: Fasteners

> [!summary] Chapter overview
> This lecture introduces **threaded fasteners** and how they are represented on engineering drawings. It covers screws, bolts, studs, nuts and washers; thread geometry such as **major diameter, minor diameter, pitch and lead**; taps and dies; tap and clearance drill sizes; ISO thread tolerances; right- and left-hand threads; and the conventional representation and dimensioning of internal and external threads.

---

## Screws and Nuts

A screw is a **simple machine** that provides mechanical advantage through its geometry. The lecturer relates it to a ramp: instead of a straight inclined surface, the ramp is effectively wrapped around a cylinder as a **helix**.

This geometry allows:

- a large amount of rotation to produce a small amount of axial travel;
- precise axial positioning, such as in 3D printers or milling machines;
- a high clamping force from a relatively small applied torque.

Threaded components are formed by a **helical groove cut on a cylinder**:

- on the outside of a cylinder -> **external thread**;
- on the inside of a cylindrical hole -> **internal thread**.

The lecture emphasizes that threaded fasteners exist in a very large variety of forms and scales. The exact catalogue of fastener types is not required; the important idea is the common helical-thread principle.

---

## Types of Fasteners

The main terminology introduced is:

- **Screw**
- **Bolt**
- **Stud**
- **Nut**
- **Washer**

![[Attachments/Fastener Types.png]]

### Washer

A washer is the item in this list that is **not threaded**. It is a flat annulus placed between a fastener head or nut and the workpiece.

Its purposes described in the lecture are to:

- prevent the rotating bolt head or nut from scratching the workpiece;
- spread the clamping load over a larger area;
- reduce the pressure applied directly to the workpiece surface.

### Nut

A nut is an **internally threaded component**. Internal threads can also be built directly into a component of an assembly rather than provided by a separate nut.

### Stud

A stud is essentially a **threaded rod without a head**.

- It may be threaded over its full length or only over selected regions, commonly near its ends.
- A portion may have a square or hexagonal interface so that torque can be applied.
- Threading only the necessary regions avoids unnecessary machining and avoids removing material where threads are not required.

### Bolt assembly

In the terminology used in the lecture, a **bolt** is typically used with a **nut** to clamp components together.

The basic arrangement contains:

1. the bolt;
2. the nut;
3. one component being clamped;
4. the other component being clamped.

The components being clamped do not need internal threads. Instead, the bolt passes through **clearance holes** and the clamping action is produced between the bolt head and nut.

### Screw / set bolt assembly

A **screw**, also referred to in the lecture as a **machine screw** or, in this configuration, a **set bolt**, threads directly into one of the components being assembled.

This arrangement normally involves:

1. the screw;
2. the outer component being clamped;
3. the component containing the internal thread.

A separate nut is therefore not required.

> [!important] Bolt vs screw terminology
> The lecture emphasizes that the distinction is often more about **how the externally threaded component is used** than about its visible geometry. A bolt is typically clamped with a nut, whereas a screw/set bolt threads into the component itself.

A screw with sharp threads may also form its own internal threads in a material such as wood as it is driven in. Such a screw is not necessarily designed to mate with a nut.

---

## Fastener Length and Variety

Fasteners can have many different:

- thread profiles;
- head styles;
- drive types;
- washer types;
- nut types.

The lecture states that the names of all the illustrated varieties do **not** need to be memorized.

The important dimensional idea is **how screw length is measured**.

- If the head is intended to project above the workpiece surface, length is measured from the **underside of the head** to the end of the fastener.
- If the head is intended to be recessed into the workpiece, the length is measured from the location corresponding to the **top surface of the workpiece** to the end of the fastener.

In other words, the fastener length represents the depth of the fastener that extends into or through the workpiece from its intended surface.

---

## Thread Geometry

A thread profile has several geometric features. For this part of the course, the lecturer emphasizes three quantities in particular:

- **major diameter**;
- **minor diameter**;
- **pitch**.

![[Attachments/Thread Pitch Geometry.png]]

### Major diameter

The **major diameter** is the outer diameter of an external thread profile.

### Minor diameter

The **minor diameter** is the inner extent of the thread profile. The thread geometry lies between the major and minor diameters.

### Crest, root and flank

The slide also identifies:

- **crest** - the outer extent/top of the thread tooth;
- **root** - the bottom of the thread groove;
- **flank** - the side of the thread tooth;
- **thread angle** - the angle between the thread flanks.

### Pitch

> [!definition] Pitch
> The **pitch** is the distance between equivalent points on adjacent repeated thread profiles, such as crest-to-crest distance.

The thread profile repeats periodically along the axis, and the pitch measures this repeat distance.

---

## Thread Profiles

The lecture shows several possible thread profiles, including Metric, Whitworth and British Association threads as well as Acme, Square, Modified Square, Buttress, Trapezoidal Metric and U.S. 60° forms.

These examples demonstrate that there are many standards and geometries for threads.

> [!important]
> For this part of the course, the lecturer states that you do **not** need to identify or memorize the names of the different thread profiles shown. The important point is that mating threaded components must have compatible thread profiles.

For a nut and bolt to mate correctly, their relevant thread geometry must match, particularly the **major diameter and pitch** for the standard being used.

---

## Pitch and Lead

> [!definition] Lead
> **Lead** is the amount of axial travel produced by one complete revolution of a threaded component.

For a **single-start thread**, one revolution follows the same helix to the next equivalent thread position, so:

**Lead = Pitch**

A thread can also contain multiple distinct helices wrapped around the same cylinder. These are called **multi-start threads**.

![[Attachments/Pitch and Lead Multi Start Threads.png]]

The slide gives:

- Single start: **Lead = Pitch**
- Double start: **Lead = 2 x Pitch**
- Four start: **Lead = 4 x Pitch**

The lecturer summarizes the general relationship as:

**Lead = Pitch x number of starts**

### Why use multiple starts?

Multiple starts increase the axial distance travelled per revolution. The lecture gives a **water-bottle cap** as a common example:

- there are multiple positions at which the cap can catch the thread;
- the cap begins engaging with less rotation;
- it travels axially faster for each turn.

The lecture describes the design consideration as a balance between **strength and speed**. Multi-start threads provide another independent parameter for controlling thread density and axial travel.

---

## Taps and Dies

**Taps and dies** are tools used to create threaded components from blank cylinders or cylindrical holes.

![[Attachments/Taps and Dies.png]]

### Die - creating an external thread

A **die** is used to cut external threads on a cylinder.

Procedure described in the lecture:

1. Start with a blank cylinder at the **major diameter**.
2. Place the die over the end of the cylinder.
3. Rotate the die so its cutting edges remove material and form the helical thread profile.
4. The openings in the die provide space for the removed chips to escape.

The lecturer notes that cutting creates substantial friction, so chip removal and cutting oil are important during the process.

### Tap - creating an internal thread

A **tap** is used to cut internal threads inside a hole.

1. First drill a hole smaller than the major diameter, corresponding to the required **tap drill / minor diameter**.
2. Insert the tap into the hole.
3. Rotate the tap so its cutting edges remove material and form the internal thread out toward the major diameter.
4. Flutes in the tap provide space for chips to leave the workpiece.

> [!important]
> An external thread begins from material at the **major diameter** and removes material inward. An internal thread begins from a drilled hole near the **minor diameter** and removes material outward to form the thread.

---

## Tap and Clearance Drills

The lecture provides a standard metric chart containing:

- screw size;
- pitch;
- tap drill sizes for aluminium and steel;
- close and standard clearance-hole sizes.

![[Attachments/Tap and Clearance Drill Table.png]]

The lecturer states that this table does **not** need to be memorized. If a question requires information from such a chart, it will be provided.

### Metric screw size and pitch

A metric designation such as **M5** identifies a standard thread with a **5 mm major diameter**.

The same major diameter can be available with different standard pitches. Therefore, mating components need both the same relevant diameter and the same pitch.

### Tap drill size

The tap drill size is the diameter drilled before an internal thread is cut.

The chart gives different values for aluminium and steel because the material affects how much material is intended to be removed during tapping.

According to the lecturer:

- aluminium is softer, so a smaller tap drill can be used and more material can be cut to form the thread;
- steel is stronger and harder to cut, so a larger tap drill can be used, requiring less material to be removed during tapping.

### Clearance hole

A **clearance hole** allows an externally threaded fastener to pass through without threading into that component.

The hole is made slightly larger than the thread's major diameter so that:

- manufacturing tolerance does not prevent assembly;
- the thread does not rub heavily against or damage the hole during insertion and removal.

The table distinguishes **close** and **standard** clearance sizes.

---

## Cosmetic Threads in CAD

The lecturer specifically states that in this class, threaded helical geometry should generally **not** be modelled as a full physical helical cut in SolidWorks.

Reasons given include:

- the exact thread geometry is often unnecessary for communicating the part's function;
- detailed helical geometry can greatly increase model complexity and file size;
- the important information is usually that a threaded feature exists at a specified diameter and depth and will mate with another threaded component.

Instead, SolidWorks can use **cosmetic threads** to visually indicate the threaded feature without modelling the full helical tooth geometry.

> [!important]
> For the engineering drawing, the objective is often to communicate the **function and specification of the threaded feature**, rather than explicitly model every helical tooth.

---

## ISO Thread Tolerance

The lecture introduces three qualitative classes of threaded fit:

- **Close Fit (5H/4h)**
- **Medium Fit (6H/6g)**
- **Free Fit (7H/8g)**

![[Attachments/ISO Thread Tolerance.png]]

These describe how much space or play exists between mating threaded components.

Examples shown are:

- **M16 x 1.5 - 6H** - internal thread
- **M6 x 0.75 - 8g** - external thread

For threaded components, the tolerance designation is written with the **number first, then the letter**.

The case of the letter distinguishes the thread type:

- **capital letter** -> internal thread;
- **lowercase letter** -> external thread.

The lecture indicates that the detailed meaning of the number and letter is continued in the following lecture; here, the focus is on recognizing the designation and its role in specifying fit.

---

## ISO Metric Thread Designation

The slide gives the following interpretation:

**M16 x 1.5 - 6H** (internal thread)

**M6 x 0.75 - 6g** (external thread)

The components of the designation are:

| Part | Meaning |
|---|---|
| **M** | Metric thread |
| **16 / 6** | Nominal diameter in mm |
| **1.5 / 0.75** | Pitch in mm |
| **6H** | Internal-thread tolerance designation |
| **6g** | External-thread tolerance designation |

The slide notes **6H above nominal value** and **6g below nominal value**.

---

## Right-Hand vs Left-Hand Threads

Most screw threads are **right-handed**.

![[Attachments/Right Hand and Left Hand Threads.png]]

For a right-hand thread, when looking at the head of the fastener:

- turning **clockwise** moves/tightens the screw inward;
- turning **counterclockwise** moves/loosens the screw outward.

The lecturer relates this to the right-hand rule and also gives the mnemonic **"lefty loosey, righty tighty."**

Left-hand threads also exist but are much less common and can be significantly more expensive because they are produced in lower quantities.

> [!important]
> A right-hand thread is the normal convention and does not require an additional designation. If the thread is left-handed, the abbreviation **LH** should be used on the engineering drawing.

### Left-hand thread application: gas welding

The lecture gives gas-welding cylinders as an example of why opposite thread directions may be useful:

- oxygen uses a right-hand thread;
- acetylene uses a left-hand thread.

The different thread directions act as a **mechanical safety measure** so that the connections cannot be accidentally swapped.

---

## Internal vs External Thread Representation

Engineering drawings do not show the complete physical helix of a thread. Instead, conventional lines indicate the **major and minor diameters** and therefore the region occupied by the thread.

![[Attachments/Internal and External Thread Representation.png]]

In a section view of an internally threaded hole, hatching extends through the threaded region because material is present there for part of the repeating thread profile.

When viewing the thread end-on, two concentric circles indicate the major and minor diameters. One is shown as a complete circle and the other as a broken/partial circle.

The lecturer explains the convention in terms of which side the thread teeth connect to:

- for an **external thread**, the inner circle is broken;
- for an **internal thread**, the outer circle is broken.

---

## Thread Representation Example

![[Attachments/Thread Representation Example.png]]

The slide illustrates an internal threaded hole represented without drawing the full helical profile. The example is identified as **M5 x 15**, with the thread size and depth communicated by the drawing rather than explicit helical geometry.

---

## Nut and Bolt Assembly

![[Attachments/Nut and Bolt Assembly.png]]

The bolt assembly drawing shows the bolt passing through clearance holes in the components and being secured by a nut.

The slide notes:

- a **clearance hole in each component**;
- thread on each side of the nut;
- use of a plain washer in the assembly.

This reinforces the earlier distinction that the parts clamped by a bolt do not themselves need to contain mating threads.

---

## Screw Assembly

![[Attachments/Screw Assembly.png]]

The screw assembly drawing shows a fastener passing through a clearance hole in the outer component and threading directly into the inner component.

The slide notes:

- **120° drill point**;
- **unthreaded bottom of tapping hole**;
- **thread in tapping hole below bolt**;
- **bolt thread above joint line**;
- **clearance hole in outer detail**.

This is the drawing representation of the screw/set-bolt arrangement introduced earlier in the lecture.

---

## Screw Thread Dimensioning

Threaded holes and external threads are specified by notes that communicate the thread size, tolerance and required threaded length/depth.

![[Attachments/Screw Thread Dimensioning 1.png]]

Examples shown on the slide include:

- **M16 x 1.5 - 6H THROUGH**
- **M8 - 6H, 32 MIN LENGTH FULL THREAD**
- **M12 x 1 - 7H, 18 MIN LENGTH FULL THREAD, 25 MAX INCLUDING RUNOUT**

For tapping drill sizes, the slide refers to the relevant standard table rather than requiring the drill diameter to be derived directly from the thread designation.

![[Attachments/Screw Thread Dimensioning 2.png]]

Further examples distinguish the dimensions of:

- internal threaded holes;
- minimum full-thread length;
- maximum hole/depth limits;
- external full-thread length;
- thread run-out.

The slide explicitly labels the external-thread examples as **dimensioning to end of full thread and limit of thread run-out**.

---

## Practice Questions from the Lecture

### Meaning of `M`

For **M16 x 1.5 - 6H**, the `M` means:

**Metric Thread**.

### Meaning of `1.5`

For **M16 x 1.5 - 6H**, `1.5` refers to the **pitch in mm**. In the multiple-choice wording on the slide, this corresponds to **Pitch Length**.

### Minor diameter of an M16 x 1.5 internal thread

The major/nominal diameter is 16 mm, while the minor diameter lies inside the thread profile. Therefore the correct relationship in the lecture practice question is:

**minor diameter < 16 mm**.

---

## Chapter Summary / Key Connections

- A screw is a helical simple machine that converts rotation into axial movement and can provide mechanical advantage.
- **External threads** are formed on cylinders; **internal threads** are formed inside cylindrical holes.
- A **bolt** normally clamps components using a nut, while a **screw/set bolt** threads directly into a component.
- A **washer** is unthreaded and protects the workpiece while spreading clamping load.
- Thread geometry is described using the **major diameter, minor diameter and pitch**.
- **Lead** is axial travel per revolution; for multi-start threads, lead increases with the number of starts.
- **Dies** cut external threads; **taps** cut internal threads.
- **Tap drill sizes** prepare a hole for internal threading; **clearance holes** allow threaded fasteners to pass through without engaging.
- Thread specifications identify the metric size, pitch and tolerance class.
- Right-hand threads are standard; left-hand threads must be identified using **LH**.
- Engineering drawings use **conventional/cosmetic thread representations** instead of drawing the complete helix.
- Thread dimensioning communicates the required thread size, tolerance, depth/full-thread length and run-out limits.

---

## Exam / Revision Checklist

- [ ] Can I explain why a screw provides mechanical advantage?
- [ ] Can I distinguish a screw, bolt, stud, nut and washer?
- [ ] Can I explain the difference between a bolt assembly and a screw/set-bolt assembly?
- [ ] Can I explain the purpose of a washer?
- [ ] Can I identify the major diameter, minor diameter, crest, root, flank and pitch?
- [ ] Can I distinguish pitch from lead?
- [ ] Can I relate lead to the number of starts in a multi-start thread?
- [ ] Can I explain how a die creates an external thread?
- [ ] Can I explain how a tap creates an internal thread?
- [ ] Can I distinguish a tap drill hole from a clearance hole?
- [ ] Can I interpret a designation such as `M16 x 1.5 - 6H`?
- [ ] Can I distinguish internal and external thread tolerance notation by letter case?
- [ ] Can I distinguish right-hand and left-hand threads and identify when `LH` is required?
- [ ] Can I recognize the conventional drawing representation of internal and external threads?
- [ ] Can I interpret the thread length/depth information used in screw-thread dimensioning?

---

## Key Relationships

> [!summary] Core relationships and conventions
> **Pitch** = distance between equivalent points on adjacent thread profiles
>
> **Lead** = axial travel for one revolution
>
> **Single start:** Lead = Pitch
>
> **Double start:** Lead = 2 x Pitch
>
> **Four start:** Lead = 4 x Pitch
>
> **General relationship stated in the lecture:** Lead = Pitch x number of starts
>
> **M** = metric thread
>
> Number after `M` = nominal / major diameter in mm
>
> Number after `x` = pitch in mm
>
> Capital tolerance letter = internal thread
>
> Lowercase tolerance letter = external thread
>
> **LH** = left-hand thread; right-hand is the standard convention

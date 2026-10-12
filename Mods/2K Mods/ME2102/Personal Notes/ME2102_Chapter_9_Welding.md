# ME2102 — Chapter 09: Welding

> [!summary] Chapter overview
> This lecture introduces **welding as a permanent joining process**, the main welding-process classifications, and—most importantly for ME2102—how welds are **recognised and represented on engineering drawings**. Revision should focus on weld symbols, arrow-side/other-side conventions, weld shape, supplementary symbols, and dimensioning.

---

## 9.1 Welding Fundamentals

### Welding

Welding uses **high heat to melt materials together**, creating a permanent joint.

- Commonly used for **metals**, but also applicable to **thermoplastics**.
- Different from low-temperature soldering.
- Can join assemblies directly.
- Can create affordable custom metal parts from available material.

In soldering, a low-melting-point filler material melts and adheres to the parts. In welding, the heat is high enough that the **parts being joined also melt locally**. Filler material may be used, but is not always required.

The lecturer noted that welded joints are very strong. For later weld-strength analysis, the filler material is generally assumed to be stronger than the two metals being joined, so the limiting material is the lower-strength material being joined.

---

## 9.2 Welding Processes

Welding processes may be classified by:

- **Energy source**
  - Chemical — **Gas Welding**
  - Electrical — **Arc Welding**
- **Consumable / Non-consumable**
- **Shielded / Unshielded**

### Gas welding

Gas welding uses a chemical energy source. The lecture example combines **acetylene** and **oxygen** in a torch.

- Gas-flow valves control the flame.
- The torch heats the seam.
- A separate filler rod can be melted into the joint.
- Consistent flame strength, distance, and movement speed require skill.

![[Attachments/Gas Welding Setup.png]]

### Arc welding

Arc welding uses electrical energy. One lead of the power supply is connected to the workpiece and the other to an electrode/filler material. Bringing the electrode near the workpiece produces an electrical **arc**, concentrating energy at the weld location and melting the metals.

![[Attachments/Arc Welding Setup.png]]

### Consumable / non-consumable

In this lecture, **consumable / non-consumable** mainly describes whether filler material—a third metal—is consumed and deposited during welding. In some arc-welding processes the electrode is itself consumed; in others the electrode and filler material are separate.

### Shielded / unshielded

Molten metal can mix with gases in the surrounding environment, such as oxygen or nitrogen, and this can weaken the weld locally. A shielding gas can therefore be supplied around the weld region to protect it while molten.

### MIG and TIG

**MIG — Metal Inert Gas welding**

- Uses an inert shielding gas.
- The metal electrode is normally consumed during welding.
- The electrode and filler-material functions are combined in the illustrated setup.

**TIG — Tungsten Inert Gas welding**

- Uses a **tungsten electrode**.
- Tungsten conducts electricity but has a very high melting point, so the electrode does not melt away in the process described.
- A separate filler rod can still be used.
- Separating filler feed from the electrode provides more flexibility in controlling power delivery and filler addition.

![[Attachments/MIG and TIG Welding.png]]

> [!important]
> The lecturer emphasized that this is **not a manufacturing/fabrication class**. The main objective is to **represent and recognise welds on engineering drawings**.

---

## 9.3 Main Types of Weld

### Fillet weld

A **fillet weld** commonly joins two surfaces meeting at approximately a right angle, with weld material placed along the corner.

- The lecturer described it as probably the most common weld type.
- Its outer contour can be flat, concave, or convex.
- Its basic symbol is a **right triangle**.

### Butt weld

A **butt weld** joins pieces that abut one another. The parts may be melted directly, or their edges may be ground away to create space for filler material.

![[Attachments/Butt and Fillet Welds.png]]

> [!warning]
> At intermediate joint angles, the distinction between fillet and butt welds can become less clear. The lecturer stated that assessment questions would use the **obvious cases**.

---

## 9.4 Weld Symbols

The important skill is to **match weld illustrations to their symbols**. The lecturer explicitly stated that memorising every detailed descriptive name is not required.

### Butt-weld forms

Examples shown include:

- Single V-butt weld
- Single bevel butt weld
- Single V-butt weld with broad root face
- Single bevel butt weld with broad root face
- Single U butt weld
- Single J butt weld

The symbols closely resemble the cross-section of the prepared joint.

![[Attachments/Weld Symbols V Bevel Broad Root.png]]

![[Attachments/Weld Symbols Bevel U J.png]]

### Flanged, square, and fillet welds

- **Butt weld between flanged plates** — edges are bent and melted together.
- **Square butt weld** — a gap is left between the pieces and filled; symbol is two parallel lines.
- **Fillet weld** — triangular symbol.

![[Attachments/Weld Symbols Flange Square Fillet.png]]

### Plug, spot, and seam welds

**Plug weld:** one part contains a hole or shaped opening that is filled to join it to the other part.

**Spot weld:** two pieces are clamped between electrodes and locally welded using electrical current and pressure, without filler material in the process described. Its symbol is a **circle**.

**Seam weld:** produced by repeated overlapping spot welds to create a continuous seam.

![[Attachments/Weld Symbols Plug Spot Seam.png]]

---

## 9.5 Shape of Weld

The finished outer shape can be specified as:

- **Flat (casual finished flush)**
- **Convex**
- **Concave**

![[Attachments/Weld Shape Symbols.png]]

The shape symbol is combined with the basic weld symbol. Examples shown are a flat single V-butt weld, convex double V-butt weld, and concave fillet weld.

![[Attachments/Weld Shape Examples.png]]

The lecturer noted that producing the requested finish directly depends on welding skill; finishing such as grinding may otherwise be needed.

---

## 9.6 Drawing Representation

A weld is represented using:

- **Arrow line** — points to the joint.
- **Reference line** — horizontal line connected to the arrow line.
- **Symbol** — identifies the weld.
- **Joint** — the location between the parts being joined.

![[Attachments/Weld Drawing Representation.png]]

### Arrow side and other side

The position of the weld symbol relative to the reference line determines the side of the joint:

- **Below reference line → arrow side**
- **Above reference line → other side**
- **Above and below → both sides**

![[Attachments/Weld Arrow Side Other Side.png]]

![[Attachments/Weld Both Sides and Bevel Side.png]]

> [!important] Arrow-side rule
> **Below = arrow side.**  
> **Above = other side.**

For butt welds, the same convention determines the side toward which the prepared weld opening faces.

> [!warning]
> The **other side** is the opposite side of the same joint. Trace the actual joint between the two parts; it does not simply mean “up” or “down” on the drawing.

---

## 9.7 Weld All Around

A **circle at the intersection of the arrow line and reference line** means **weld all around**.

![[Attachments/Weld All Around.png]]

The symbol applies around the entire perimeter, even when that perimeter is not circular. For a hollow pipe, arrow-side versus other-side placement can distinguish the outside seam from the inside seam.

---

## 9.8 Dimensioning

For the fillet-weld notation shown in the lecture:

- the number beside the short side specifies the **size of the weld**;
- the number associated with the longer side specifies the **length of the weld**.

![[Attachments/Weld Dimensioning Size Length.png]]

The illustrated example specifies weld size **5** and weld length **10**. The length may be omitted when the weld is intended to continue along the whole applicable side.

### Intermittent weld

A seam does not always need to be welded continuously. Welding may be performed intermittently in a repeating pattern to reduce work while obtaining the desired strength.

- First number → **length of each welded portion**.
- Number in brackets → **distance before starting the weld again**.

![[Attachments/Intermittent Weld Dimensioning.png]]

The slide illustrates the notation `100(150)` together with the corresponding repeating weld pattern.

---

## 9.9 Site Welds

A **flag at the intersection of the arrow line and reference line** means the weld is to be made **on site** rather than in the shop beforehand.

![[Attachments/Site Weld Flag.png]]

The lecturer used examples such as handrails: components can be transported separately and welded at the installation location. This can also allow the final fit to be adjusted on site.

> [!important]
> **Circle at the intersection → weld all around.**  
> **Flag at the intersection → weld on site.**

---

## 9.10 Illustration, Graphic and Symbolic Representation

The lecture connects three ways of representing the same weld:

1. **Illustration** — physical appearance of the welded assembly.
2. **Graphic representation** — appearance in orthographic views.
3. **Symbolic representation** — arrow/reference line with weld symbols.

![[Attachments/Weld Representation Examples 1.png]]

![[Attachments/Weld Representation Examples 2.png]]

### Procedure for interpreting a weld symbol

1. Identify the **joint** indicated by the arrow.
2. Recognise the **basic weld symbol**.
3. Check whether the symbol is above or below the reference line.
4. Apply **below = arrow side** and **above = other side**.
5. If symbols appear above and below, apply the indicated weld on both sides.
6. Check for supplementary information: weld-all-around circle, site-weld flag, weld shape, size, length, or intermittent spacing.

---

## 9.11 Lecture Practice

The lecture ends with recognition questions:

- A **circle weld symbol** corresponds to a **spot weld**.
- The **triangle** is the **fillet-weld symbol**.
- A **flag** at the arrow/reference-line intersection means **weld on-site**.
- In the final arrow-side/other-side question, the correct answer is **C**: the upper fillet is on the other side and therefore has its symbol above the reference line; the lower fillet is on the arrow side and therefore has its symbol below the reference line.

---

## Chapter 09 — Key Connections

**Welding process → weld type → weld symbol → arrow/reference-line placement → supplementary symbols and dimensions → engineering-drawing interpretation**

The process discussion provides context, but the central ME2102 skill is moving correctly between the **physical weld**, its **graphic representation**, and its **symbolic representation**.

## Exam / Revision Checklist

- [ ] Can I distinguish welding from low-temperature soldering?
- [ ] Can I distinguish **gas welding** from **arc welding**?
- [ ] Do I understand **consumable / non-consumable** and **shielded / unshielded** at the level taught?
- [ ] Can I distinguish **MIG** from **TIG**?
- [ ] Can I recognise **fillet** and **butt** welds?
- [ ] Can I match the weld illustrations and symbols shown in the lecture?
- [ ] Can I recognise **plug, spot, and seam** weld symbols?
- [ ] Can I recognise flat, convex, and concave weld shapes?
- [ ] Can I identify the arrow line, reference line, symbol, and joint?
- [ ] Do I remember **below = arrow side; above = other side**?
- [ ] Can I interpret a weld specified on both sides?
- [ ] Can I recognise the **weld-all-around circle**?
- [ ] Can I recognise the **site-weld flag**?
- [ ] Can I interpret weld **size, length, and intermittent-weld notation**?
- [ ] Can I move between illustration, graphic representation, and symbolic representation?

## Key Concepts / Frameworks

> [!summary] Core welding-drawing conventions
> - **Fillet weld:** triangular symbol.
> - **Spot weld:** circle symbol.
> - **Below reference line:** arrow-side weld.
> - **Above reference line:** other-side weld.
> - **Above and below:** weld both sides.
> - **Circle at arrow/reference-line intersection:** weld all around.
> - **Flag at arrow/reference-line intersection:** site weld.
> - Weld symbols can specify **flat, convex, or concave** finished shape.
> - Weld notation can specify **size, length, and intermittent welding**.

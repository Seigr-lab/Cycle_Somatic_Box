# Step 14: Fabricate Electrode Quarters

## Objective

Create the physical electrode structures that will contain biochar blend, provide electrical contact, and fit together to form functional circular electrodes for a high-output 2m³ system.

**Scale for high-output system:** This step fabricates electrodes for one 2m³ unit with 24 electrodes (4 cathodes + 4 anodes in each of 3 layers). This is a MAJOR increase from small 6-electrode systems.

## Why This Matters

**Electrodes are the heart of the MFC:**
- **Physical structure** - Holds biochar in place while allowing water/gas circulation
- **Electrical contact** - Collects electrons from distributed biochar particles
- **Modular design** - Quarter sections enable assembly, disassembly, replacement
- **Scalability** - Same quarter design scales from small (150mm) to large (300mm) electrodes
- **High density** - 24 electrodes (vs 6 in small system) = 4× more active surface area for power generation

**Poor electrode design causes:**
- Biochar spillage or compaction (lost surface area)
- Poor electrical collection (electrons can't reach wires)
- Difficult assembly (frustration, time waste)
- Premature failure (cracks, corrosion)
- **For high-output system:** Even small design flaws multiply across 24 electrodes = major performance loss

**Our modular quarter design:**
- 4 quarters + 1 hub = complete circular electrode
- Enables transport before assembly (lighter, easier)
- Allows targeted replacement if one section fails
- Compatible with 3D printing OR handcrafting
- **Manufacturing efficiency:** One design template makes all 24 electrodes

## Electrode Designs

### **For 2m³ High-Output System (from Step 04):**

**System architecture: 3 layers × 8 electrodes/layer = 24 total electrodes**

**Layer 1 (Bottom - 50cm depth):**
- 4 cathodes: 300mm diameter (oxygen-rich from water flow)
- 4 anodes: 300mm diameter (organic-rich from drainage)
- Spacing: 400mm center-to-center in square pattern

**Layer 2 (Middle - 90cm depth):**
- 4 cathodes: 300mm diameter
- 4 anodes: 300mm diameter  
- Spacing: 400mm center-to-center, offset 200mm from Layer 1

**Layer 3 (Top - 120cm depth):**
- 4 cathodes: 300mm diameter (oxygen-rich from surface air)
- 4 anodes: 300mm diameter
- Spacing: 400mm center-to-center, aligned with Layer 1

**Grand total fabrication needs:**
- **24 electrodes × 4 quarters each = 96 quarters**
- **24 electrodes × 1 hub each = 24 hubs**
- All use 300mm diameter design (standardization simplifies manufacturing)

**Realistic fabrication strategy:**
- **DO NOT attempt to make all 96 quarters in one session**
- Fabricate in batches of 8-12 quarters (2-3 electrodes worth)
- Test first batch in prototype unit before mass production
- Expect 2-3 weeks of work for complete set (part-time)

## Fabrication Methods

**You have three options:**

### **Method 1: 3D Printing (Recommended if Printer Available)**

**Advantages:**
- Precise geometry (perfect fit every time)
- Integrated features (wire channels, mounting points)
- Repeatable (print identical spares)
- Material options (PLA+, wood-filled PLA, PETG)

**Disadvantages:**
- Requires 3D printer access (or service bureau)
- Filament cost: €25-50 for full set
- Print time: 40-60 hours total for all parts
- Layer adhesion can fail (quality control needed)

**Best for:** Tech-savvy builders, access to printer, desire for precision

### **Method 2: Laser-Cut Plywood + Wire Mesh (DIY Accessible)**

**Advantages:**
- Low-tech, widely accessible materials
- Strong and durable (plywood lasts 7-10 years)
- Easy to modify/repair (cut new pieces)
- Low cost: €10-20 for materials

**Disadvantages:**
- Less precise (manual assembly tolerance)
- Requires tools (saw, drill, stapler)
- More assembly steps

**Best for:** Practical builders, no printer access, prefer traditional materials

### **Method 3: Handcrafted from Reclaimed Materials**

**Advantages:**
- Zero cost (use what you have)
- Ultimate Seigr philosophy (reuse, adapt)
- Creative freedom

**Disadvantages:**
- Variable quality (depends on materials)
- Time-intensive (fitting, testing, revising)
- May need replacement sooner (3-5 years vs 7-10)

**Best for:** Experimenters, very limited budget, enjoy hands-on problem-solving

**Seigr Hub recommendation:**
- **Method 1** if you have printer access (precision and ease)
- **Method 2** if not (reliable fallback, proven to work)

## Method 1: 3D Printing Process

### **Design Files (Available from Seigr Repository or Create Your Own):**

**Large quarter (for 360mm electrode):**
- Outer arc: 360mm diameter × 90° sector
- Inner arc: 80mm diameter (center hub opening)
- Height: 40mm
- Wall thickness: 3mm
- Bottom: Perforated mesh (2mm holes, 5mm spacing)
- Top: Open or mesh (allows biochar loading)
- Wire channel: 5mm groove along inner edge

**Large hub (for 360mm electrode):**
- Disc: 80mm diameter × 15mm thick
- Four slots: 90° apart, accept quarter tabs
- Center hole: 10mm (wire passage)
- Top: Flat with wire terminal mounting points
- Bottom: Perforated (water/gas flow)

**Medium quarter (for 150mm electrode):**
- Outer arc: 150mm diameter × 90° sector
- Inner arc: 40mm diameter
- Height: 30mm
- Otherwise similar features to large quarter

**Medium hub (for 150mm electrode):**
- Disc: 40mm diameter × 12mm thick
- Four slots or simplified single-piece design

**Alternative: Medium single-piece disc (simpler):**
- Solid disc: 150mm diameter × 30mm height
- Center hole: 10mm (wire passage)
- Perforated bottom: 2mm holes throughout
- Top: Open rim (biochar loading)

### **Printing Parameters:**

**Filament selection:**
- **PLA+** (recommended): Strong, easy to print, low cost (€15-20/kg)
- **Wood-filled PLA**: Natural appearance, biodegradable, same cost
- **PETG**: More heat-resistant (if MFC gets >60°C), €20-25/kg
- **Avoid ABS**: Requires heated enclosure, toxic fumes

**Settings:**
- **Layer height:** 0.2-0.3mm (balance speed vs strength)
- **Infill:** 20-30% (provides structure without excessive weight)
- **Wall thickness:** 3-4 perimeters (strong outer shell)
- **Supports:** Required for overhangs, especially wire channels
- **Bed adhesion:** Use brim or raft (prevents warping on large parts)

**Print time estimates (per part):**
- Large quarter: 4-6 hours
- Large hub: 1-2 hours
- Medium quarter: 1.5-2.5 hours
- Medium hub: 30-60 minutes
- **Total for full system:** 40-60 hours

### **Printing Sequence:**

**1. Test print one large quarter first:**
- Verify dimensions fit together (hub slot, quarter tab)
- Check perforations aren't clogged (post-process with drill if needed)
- Adjust design or printer settings if issues found

**2. Print all large quarters (8 total):**
- Can print 1-2 per batch (depends on printer bed size)
- Monitor first layers (adhesion critical for large parts)
- Allow to cool fully before removing (prevents warping)

**3. Print large hubs (2 total):**
- Smaller, faster prints
- Ensure center hole is clear (use 10mm drill bit to clean if needed)

**4. Print medium quarters (8 total) or medium discs (2 total):**
- Faster prints (less material)
- Can batch several at once

**5. Print medium hubs (2 total) if using quarter design:**
- Skip if using single-piece disc design

**6. Post-processing:**
- Remove supports (pliers, knife)
- Clean wire channels (small file or sandpaper)
- Test fit all parts (quarters should slide into hub slots easily but snugly)
- Drill out any clogged holes in perforated areas

### **Quality Control:**

**Check each printed part:**
- **Dimensional accuracy:** Quarter tabs fit hub slots (not too tight, not loose)
- **Layer adhesion:** No cracks or delamination (flex gently to test)
- **Perforations open:** Holes clear for water/gas flow
- **Wire channels clear:** Can route wire without forcing

**Reject criteria:**
- Cracked or warped (structural failure risk)
- Slots don't align (assembly impossible)
- Perforations fully clogged (rework or re-print)

## Method 2: Laser-Cut Plywood Process

### **Materials:**

**For full electrode set:**
- **Plywood sheets:** 3-5mm thick, ~1m² total area
  - Marine or exterior grade (moisture resistant)
  - €10-20 from hardware store
- **Wire mesh:** Hardware cloth, 5mm grid, ~0.5m²
  - Galvanized or stainless steel (corrosion resistant)
  - €5-10
- **Fasteners:** Small screws or wire ties for assembly
- **Wood glue:** Waterproof (PVA or epoxy)

### **Cutting Templates:**

**Create cardboard templates first:**

**Large quarter template:**
- Draw 360mm diameter circle on cardboard
- Divide into quarters (90° sectors)
- Cut out one quarter (this is your template)
- Trace onto plywood, cut 8 copies

**Large hub template:**
- Draw 80mm diameter circle
- Cut out, trace onto plywood, cut 2 copies

**Medium quarter or disc template:**
- Draw 150mm diameter circle
- Divide into quarters OR leave as full disc
- Cut templates, trace, cut final pieces

### **Cutting:**

**By hand (if no laser cutter access):**
- Use jigsaw or coping saw for curves
- Drill pilot holes for interior cuts
- Sand edges smooth (rough edges tear mesh)

**Laser cutting service:**
- Upload templates to service (e.g., Ponoko, local makerspace)
- Plywood cuts clean and precise
- Cost: €20-40 for full set

**Quality cuts are important:**
- Smooth edges prevent biochar leakage
- Accurate shapes enable good assembly fit

### **Assembly:**

**1. Create bottom mesh layer:**
- Cut wire mesh to match plywood quarter shape (slightly smaller, ~2mm inset)
- Attach mesh to plywood bottom with staples or small screws
- Mesh provides drainage while containing biochar

**2. Create side walls:**
- Cut plywood strips: 40mm (large) or 30mm (medium) height × length of arc
- Glue/screw strips to perimeter of bottom layer
- Forms biochar container

**3. Create hubs:**
- Plywood disc as base
- Drill four radial slots (for quarter tabs if using)
- Or simplify: Solid disc with center wire hole only

**4. Waterproofing (optional but recommended):**
- Coat all plywood with linseed oil or biochar tar
- 2-3 coats (prevents swelling, rot)
- Let dry fully between coats

### **Testing:**

**Dry fit all quarters around hub:**
- Should form ~360mm circle (large) or 150mm circle (medium)
- Small gaps (<5mm) are okay (will fill with biochar)
- Large gaps (>10mm) indicate cutting error (trim pieces to fit)

## Method 3: Handcrafted Alternatives

**Creative solutions using reclaimed materials:**

### **Option A: Plastic Container Modification:**
- Find round containers (food buckets, plant pots)
- Cut to height (40mm or 30mm)
- Drill drainage holes in bottom (2mm, dense pattern)
- Cut into quarters if needed (or leave whole for medium electrodes)
- Cost: Free (reclaimed)

### **Option B: Woven Wire Basket:**
- Form wire mesh into cylindrical baskets (open top)
- Line bottom/sides with landscape fabric (contains biochar)
- No rigid structure (adapts to compost settling)
- Cost: ~€5-10 for mesh

### **Option C: Layered Cardboard:**
- Cut cardboard to shape
- Laminate 5-8 layers with biochar-tar paste (creates composite)
- Functional for 2-3 years (degrades slowly, releases carbon to system)
- Cost: Free
- Aligns with Seigr philosophy (biodegradable, low-impact)

## Wire Integration

**All electrode designs must include wire attachment:**

### **For 3D printed electrodes:**
- Wire channel molded into quarter (5mm groove)
- Wire exits at hub (center hole)
- Secure with wire clip or terminal screw in hub

### **For plywood/handcrafted electrodes:**
- Drill wire channel along edge (3-5mm hole)
- Thread bare copper wire through
- Twist multiple quarters' wires together at hub
- Secure with wire nut or solder

**Wire specifications:**
- 14-16 AWG copper (solid or stranded)
- Insulated if routing through wet zones (strip ends only)
- Corrosion-resistant coating optional (tin-plated copper)

## Quality Checks

After fabricating all electrodes, you should have:

✅ **All quarters fabricated:** 8 large + 8 medium (or 8 large + 2 medium discs)  
✅ **All hubs fabricated:** 2 large + 2 medium (or 2 large only)  
✅ **Test fit successful:** Quarters assemble around hubs without forcing  
✅ **Perforations/mesh clear:** Water/gas can flow through bottom  
✅ **Wire channels functional:** Can route wire easily  
✅ **Materials are durable:** Plywood oiled, 3D prints solid, no cracks  

## Timeline

**3D printing:** 2-3 days (actual print time: 40-60 hours, but can run overnight)
**Laser-cut plywood:** 1 day (cutting: 2-4 hours, assembly: 4-6 hours)
**Handcrafted:** 1-2 days (depends on material sourcing and complexity)

## Troubleshooting

**"3D printed parts warp during printing"**
- Increase bed temperature (PLA: 60°C, PETG: 80°C)
- Use brim or raft (larger adhesion area)
- Slow first layer speed (improves adhesion)
- Enclose printer (reduces cooling draft)

**"Quarters don't fit hub slots"**
- File or sand tabs (reduce size slightly)
- Or enlarge hub slots (drill/file)
- Test fit early (print one quarter + hub before full batch)

**"Plywood swells when wet"**
- Use marine-grade plywood (better moisture resistance)
- Apply more coats of oil (seals wood fibers)
- Accept some swelling (biochar will fill gaps)

**"Mesh tears or corrodes"**
- Use stainless steel or coated mesh (not plain steel)
- Secure mesh more thoroughly (every 2-3cm around perimeter)
- Or double-layer mesh (redundancy)

**"Biochar falls through perforations during filling"**
- Line bottom with landscape fabric or coconut coir mat (biodegradable)
- Use slightly smaller biochar particles (screen out >10mm)
- Or make perforations smaller (1-2mm instead of 3-5mm)

**"Can't access 3D printer or laser cutter"**
- Check libraries, schools, makerspaces (many offer public access)
- Online services (upload files, receive parts by mail)
- Or use Method 3 (handcrafted, no special tools needed)

## Design Variations

**Simplified single-piece electrodes:**
- Skip quarters, make solid disc with central wire hole
- Easier fabrication, less assembly
- Harder to replace if section fails
- Good for medium electrodes (less biochar volume)

**Hexagonal or square electrodes:**
- Easier to cut (straight lines)
- Less efficient packing (wasted space)
- Can work if circular cutting is difficult

**Adjustable-height electrodes:**
- Make side walls modular (stackable rings)
- Can adjust biochar depth based on performance
- More complex, but very adaptable

## Important Notes

**Function over form:**
- Electrodes don't need to be beautiful (microbes don't care)
- Rough but functional beats perfect but delayed
- First system: Use simpler method, learn, improve for next build

**Material longevity:**
- PLA: 5-7 years in compost (eventually biodegrades, which is okay)
- Plywood: 7-10 years if properly sealed
- Stainless mesh: 10-15+ years (most durable component)

**Modularity is key:**
- Quarter design allows repair without system teardown
- One cracked quarter → replace it, keep other three
- Spares are cheap insurance (print/cut extras now while setup is ready)

**This step connects everything:**
- Electrodes hold biochar (Steps 11-13)
- Electrodes collect electrons (Step 20: Wiring)
- Electrodes fit in system (Steps 08-10: Structure)
- Everything depends on functional electrodes

---

**Electrode quarters fabricated - structure complete!**

With all physical electrode components ready, we now have the containers that will hold our biochar blend and provide the electrical interface between microbes and our power system. Whether 3D printed, laser-cut, or handcrafted, these electrodes are the mechanical translation of electrical engineering into compostable reality.

Next: **Step 15 - Coat Electrodes with Graphite** (enhancing electrical conductivity of electrode surfaces to maximize electron collection efficiency).
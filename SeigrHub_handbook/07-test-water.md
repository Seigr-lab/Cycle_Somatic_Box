# Step 07: Test Water Quality

## Objective

Verify that local water sources are suitable for occasional system moisture addition and understand the mineral contribution they provide to microbial fuel cell performance.

## Why This Matters

**Water serves multiple roles in your system:**

- **Moisture regulation** - Maintains 50-70% moisture for optimal microbial activity
- **Ion transport** - Dissolved minerals carry electrical charges between electrodes
- **pH buffering** - Natural alkalinity prevents acidification
- **Nutrient delivery** - Trace minerals support diverse microbial communities

**At Seigr Hub, groundwater chemistry gives us advantages:**

- Low conductivity (15-45 µS/cm) = clean water, few pollutants
- Neutral pH (6.8-7.2) = perfect for microbes and electrode stability
- Dissolved Ca²⁺, Mg²⁺ = natural buffering against organic acids
- Trace Fe²⁺, Mn²⁺ = supports electron transfer bacteria

**Testing confirms:**

- Water is safe (no heavy metal contamination)
- Mineral content is beneficial (not just pure distilled water)
- pH is compatible with system operation
- No hidden problems (sulfides, excessive hardness, pathogens)

## Understanding NGU Water Data

**From Step 01 (NGU 299300.01 - Groundwater dataset):**

### **Major Ion Chemistry:**

**Cations (positively charged):**

- **Ca²⁺ (Calcium):** 5-15 mg/L
  - Forms from calcite dissolution in moraine
  - Neutralizes organic acids (pH buffering)
  - Supports bacterial cell walls

- **Mg²⁺ (Magnesium):** 2-8 mg/L
  - From dolomite, Mg-silicate minerals
  - Cofactor for enzymes in bacteria
  - Contributes to alkalinity

- **K⁺ (Potassium):** 1-4 mg/L
  - From feldspar weathering
  - Cell membrane function in microbes

- **Na⁺ (Sodium):** 2-6 mg/L
  - Low (good - excess salt inhibits some bacteria)
  - Maintains osmotic balance

**Anions (negatively charged):**

- **HCO₃⁻ (Bicarbonate):** 15-40 mg/L
  - Main pH buffer system
  - Allows pH to resist change from acid production

- **SO₄²⁻ (Sulfate):** 5-15 mg/L
  - From sulfide mineral oxidation
  - Energy source for some bacteria
  - Moderate levels okay, high levels can cause H₂S production

- **Cl⁻ (Chloride):** 2-8 mg/L
  - Low (good - high Cl can corrode electrodes)
  - Natural background levels

**Trace Metals:**

- **Fe²⁺/Fe³⁺ (Iron):** 0.5-2.0 mg/L
  - Key electron shuttle for MFC bacteria
  - Will precipitate as oxides (the nodules we collected)

- **Mn²⁺ (Manganese):** 0.1-0.5 mg/L
  - Cathode catalyst when oxidized
  - Beneficial even at trace levels

**Physical Properties:**

- **pH:** 6.8-7.2 (neutral, ideal range)
- **Conductivity:** 15-45 µS/cm (low, but adequate for ion transport)
- **Temperature:** 6-10°C (groundwater stable year-round)
- **Dissolved Oxygen:** 5-9 mg/L (good for aerobic zones, cathode)

**What this means:**

- Water is naturally optimized for MFC operation
- No treatment needed for system use
- Safe for handling and incidental contact
- Mineral content enhances performance vs distilled water

## Testing Methods

**You have two options:**

### **Option A: Field Testing (Basic, Immediate)**

**Advantages:**

- Done on-site during collection
- Inexpensive (<€50 for test kit)
- Immediate feedback
- Learn water characteristics hands-on

**Disadvantages:**

- Less precise than lab analysis
- Requires some interpretation
- Limited parameters tested

**Suitable for:** Confirming NGU data applies to your specific site, catching obvious problems

### **Option B: Laboratory Analysis (Comprehensive, Precise)**

**Advantages:**

- Highly accurate measurements
- Full trace metal panel
- Professional interpretation
- Documentation for records

**Disadvantages:**

- €80-200 per sample
- 1-2 week turnaround
- Requires proper sampling technique

**Suitable for:** Thorough baseline documentation, if contamination suspected, if data for publication/sharing

**Recommendation for Seigr Hub first build:**

- **Option A** (field testing) is sufficient given NGU data confidence
- Can upgrade to Option B if field tests show unexpected results

## Field Testing Protocol

### **Equipment Needed:**

**Water test kit (€30-50, available online/hardware stores):**

- pH test strips or meter (range 4.0-9.0)
- Total hardness test (measures Ca + Mg)
- Iron test (measures Fe²⁺/Fe³⁺)
- Nitrate/Nitrite test (pollution indicator)
- Optional: TDS/conductivity meter (€15-30)

**Sampling equipment:**

- Clean glass or plastic bottles (500ml-1L)
- Labels and permanent marker
- Gloves (nitrile or latex)
- Cooler with ice (if delaying testing >4 hours)

### **Sampling Locations:**

**Collect samples from 3 sites:**

1. **Primary water source (stream/spring near system location):**
   - This is water you'll most likely use for moisture addition
   - Sample from flowing section (not stagnant pool)
   - Mid-depth (not surface scum, not bottom sediment)

2. **Groundwater (if well or spring accessible):**
   - Most stable chemistry year-round
   - Best represents NGU data (groundwater monitoring)
   - May be cleaner than surface water

3. **Alternative source (backup if primary is inaccessible):**
   - Rain catchment (if available)
   - Secondary stream
   - Or skip if only one source available

### **Sampling Procedure:**

**At each site:**

1. **Rinse container 3 times with source water:**
   - Removes any residue from storage
   - Pre-conditions bottle to water chemistry

2. **Collect sample from mid-depth, mid-current:**
   - Avoid surface (floating debris, pollen, oil films)
   - Avoid bottom (suspended sediment)
   - In flowing water, face bottle opening upstream

3. **Fill completely, cap immediately:**
   - Minimize air headspace (prevents oxygen absorption)
   - Tighten cap firmly

4. **Label clearly:**
   - Site name (e.g., "Stream 200m N of cabin")
   - Date and time
   - Weather conditions (affects surface water quality)

5. **Store cool and dark if not testing immediately:**
   - <10°C if possible
   - Test within 24 hours for best accuracy
   - Some parameters (pH, dissolved O₂) change rapidly

### **Testing Procedure:**

**Perform tests in this order (freshest sample):**

#### **1. Temperature:**

- Measure immediately upon sampling
- Use clean thermometer or temperature probe
- **Expected:** 6-12°C for groundwater, varies for surface water
- **Acceptable range:** Any (just for reference)

#### **2. pH:**

- Dip pH strip or rinse pH probe in sample
- Read immediately (color change on strip, digital on probe)
- **Expected:** 6.8-7.2 (from NGU data)
- **Acceptable range:** 6.0-8.0 for MFC operation
- **Red flags:** <5.5 (acidic, may indicate pollution) or >8.5 (alkaline, unusual for natural water)

#### **3. Conductivity / TDS (Total Dissolved Solids):**

- Insert probe in sample, wait for reading to stabilize
- **Expected:** 15-45 µS/cm conductivity, ~10-30 mg/L TDS
- **Acceptable range:** 10-200 µS/cm
- **What it means:**
  - Low (<10): Nearly pure water (like distilled) - lacks minerals
  - Moderate (10-100): Good for MFC, sufficient ions
  - High (>200): Hard water, may cause mineral buildup

#### **4. Total Hardness (Ca + Mg):**

- Follow kit instructions (usually add drops until color change)
- Count drops to determine hardness level
- **Expected:** 25-75 mg/L as CaCO₃ (from NGU Ca + Mg data)
- **Acceptable range:** 20-200 mg/L
- **Classification:**
  - <60 mg/L: Soft water
  - 60-120 mg/L: Moderately hard (ideal for MFC)
  - 120-180 mg/L: Hard
  - >180 mg/L: Very hard (may clog fine pores)

#### **5. Iron (Fe):**

- Add reagent tablets/drops, wait for color development
- Compare to color chart
- **Expected:** 0.5-2.0 mg/L (NGU data)
- **Acceptable range:** 0.1-5.0 mg/L
- **What it means:**
  - Present (>0.1): Good! Iron supports electron transfer
  - High (>5): Water may stain fixtures, but not harmful to MFC

#### **6. Nitrate/Nitrite (NO₃⁻/NO₂⁻):**

- Add reagent, compare color
- **Expected:** <1 mg/L (pristine natural water)
- **Acceptable range:** <10 mg/L
- **Red flags:**
  - >10 mg/L: Agricultural runoff or sewage contamination
  - >50 mg/L: Serious pollution - do not use water

**Optional Tests (if kit includes):**

- **Ammonia (NH₃):** Should be <0.5 mg/L (higher indicates pollution)
- **Phosphate (PO₄³⁻):** Should be <0.5 mg/L (higher indicates fertilizer runoff)
- **Chlorine (Cl₂):** Should be 0 (municipal water treatment chemical)

### **Recording Results:**

**Create data table:**

| Parameter | Site 1 (Stream) | Site 2 (Groundwater) | Site 3 (Backup) | NGU Expected | Acceptable Range |
|-----------|----------------|---------------------|----------------|-------------|------------------|
| pH | ___ | ___ | ___ | 6.8-7.2 | 6.0-8.0 |
| Conductivity (µS/cm) | ___ | ___ | ___ | 15-45 | 10-200 |
| Total Hardness (mg/L) | ___ | ___ | ___ | 25-75 | 20-200 |
| Iron (mg/L) | ___ | ___ | ___ | 0.5-2.0 | 0.1-5.0 |
| Nitrate (mg/L) | ___ | ___ | ___ | <1 | <10 |

**Interpretation:**

- All values in acceptable range → Water is safe and suitable
- One value outside range → Investigate (retest, check for contamination source)
- Multiple values outside range → Consider alternative source or water treatment

## Laboratory Analysis Option

**If you choose professional testing:**

### **Selecting a Lab:**

**Options in Norway:**

- **Eurofins** (eurofins.no) - National lab network, comprehensive packages
- **ALS Scandinavia** - Environmental testing specialist
- **Local kommune water lab** - May offer testing for residents
- **University labs** - Research quality, may be slower or require contact

**Cost:** €80-200 depending on parameter package

**Recommended package for MFC application:**

- Standard water chemistry panel (pH, conductivity, major ions)
- Trace metals (Fe, Mn, Pb, Cd, Hg, Cu, Zn)
- Nutrients (nitrate, phosphate, ammonia)

### **Sampling for Lab Analysis:**

**Lab will provide specific instructions, but generally:**

1. **Use lab-supplied bottles:**
   - Pre-cleaned to avoid contamination
   - May contain preservatives for certain analyses

2. **Fill completely, no headspace:**
   - Prevents oxidation changes during transport

3. **Keep cool during transport:**
   - Ship same day or next-day delivery
   - Include ice pack in shipping box

4. **Fill out chain-of-custody form:**
   - Documents sample origin and handling
   - Required for quality assurance

**Turnaround:** 1-2 weeks typically

## Interpreting Results

### **Ideal Water Profile for MFC:**

**pH:** 6.5-7.5

- Neutral pH supports broadest microbial diversity
- Prevents electrode corrosion
- Maintains biochar stability

**Conductivity:** 30-150 µS/cm

- Enough ions for electrical transport
- Not so high that it shorts electrodes

**Hardness:** 50-150 mg/L as CaCO₃

- Provides buffering capacity
- Supports bacterial cell function
- Prevents rapid pH swings

**Iron:** 0.5-3.0 mg/L

- Supports Fe-cycling bacteria
- Enhances electron transfer
- Natural occurrence in groundwater

**Manganese:** 0.1-1.0 mg/L

- Beneficial for cathode when oxidizes
- Natural in reducing groundwater

**Heavy Metals:** All <0.01 mg/L

- Pb, Cd, Hg, As should be minimal
- High levels toxic to bacteria

**Nitrate:** <10 mg/L

- Low indicates clean water
- High indicates agricultural/sewage contamination

### **Problem Indicators:**

**pH <5.5 or >8.5:**

- Investigate source (acid rain, mine drainage, cement contamination)
- May need neutralization before use

**Conductivity >500 µS/cm:**

- Hard water, mineral buildup risk
- Consider diluting with rainwater

**Nitrate >10 mg/L:**

- Pollution from fertilizer or sewage
- Find cleaner source

**Heavy metals detected (>0.01 mg/L):**

- Can inhibit bacteria, may bioaccumulate
- Do not use - find alternative source

**Sulfate >100 mg/L:**

- Risk of hydrogen sulfide (H₂S) production
- Can poison cathode catalysts
- Add aeration or find different source

## Using Water in Your System

**How much water will you need?**

**Initial system filling:**

- 1m³ system = ~400-600L total material volume (biochar + compost + bulking agents)
- Target moisture: 60% by weight
- Water needed: ~240-360L for initial moisture
- Sources: Rain, stream, groundwater (mixed as available)

**Ongoing moisture addition:**

- Evaporation loss: 2-5L per week (depends on temperature, ventilation)
- Leachate drainage: 1-3L per week (from fresh food waste moisture)
- Net need: 0-3L per week added (self-balancing in rainy climate)

**Water addition method:**

- Watering can with diffuser (gentle addition, prevents channeling)
- Or natural rainfall (if system is open/vented)
- Monitor moisture by feel (squeeze test - should be damp like wrung sponge)

**Water quality priority ranking:**

1. **Rainwater** (cleanest, softest, free)
2. **Groundwater/spring** (stable chemistry, consistent quality)
3. **Stream water** (variable, but generally good)
4. **Tap water** (if no better option - let chlorine off-gas 24 hours first)

**Treatment if needed:**

- **High chlorine (tap water):** Let sit open 24 hours or add vitamin C tablet (neutralizes)
- **High hardness:** Mix 50:50 with rainwater
- **Low pH:** Add pinch of baking soda (raises pH)
- **Contamination:** Boil for 10 minutes, cool before use

## Quality Checks

After completing this step, you should have:

✅ **Water tested from at least one source** (field kit or lab)  
✅ **Results documented** in table or report  
✅ **Water quality confirmed suitable** (pH 6-8, conductivity <200 µS/cm, no heavy metals)  
✅ **Water sources identified** for construction and operation  
✅ **Treatment plan** if water needs adjustment (or alternative source selected)  

## Timeline

**Field testing:** 2-4 hours total

- Sample collection: 1-2 hours
- Testing: 1 hour
- Documentation: 30 minutes

**Laboratory testing:** 1-2 weeks

- Sample collection: 1 hour
- Shipping: 1 day
- Lab processing: 5-10 days
- Report review: 1 hour

## Troubleshooting

**"Test kit results don't match NGU data"**

- NGU data is regional average, your site may vary
- Seasonal variation (spring snowmelt vs summer low flow)
- Retest from different location or different time
- If consistently different, trust your test (use actual site data)

**"Water shows contamination (high nitrate, heavy metals)"**

- Identify upstream source (agriculture, old mine, road runoff)
- Find alternative water source farther upstream or different watershed
- Can use rainwater exclusively (more effort, but cleanest)

**"Can't afford test kit or lab analysis"**

- Minimum: Test pH with litmus paper (€5)
- Observe water: Clear, no smell, no oil/scum = probably okay
- NGU data gives confidence if no obvious pollution sources
- System will reveal problems (poor performance, bad smell) if water is unsuitable

**"pH is acidic (5.0-6.0)"**

- Common in peat bog drainage or conifer forest runoff
- Add crushed moraine (calcite) to buffer - we collected this in Step 06
- Or add hydrated lime (Ca(OH)₂) sparingly - 1-2 tablespoons per 10L water

**"Conductivity is very low (<10 µS/cm)"**

- Nearly distilled water (rainwater, snowmelt)
- Can add small amount (5-10%) groundwater or stream water to provide minerals
- Or dissolve tiny pinch of sea salt (NaCl) or wood ash (K₂CO₃)

**"Results are borderline but not clearly bad"**

- Proceed with system construction
- Monitor performance (voltage, current output)
- Compare to expected values
- If underperforming, revisit water quality as possible factor

## Important Notes

**Water testing is a snapshot:**

- Chemistry changes with season, weather, upstream activities
- Spring snowmelt: Lower minerals, more acidic (humic acids)
- Summer low flow: Higher minerals, more stable pH
- After heavy rain: Diluted, more turbid (suspended sediment)

**The system is forgiving:**

- MFC bacteria adapt to wide range of water chemistries
- pH buffering from moraine compensates for acidic water
- Biochar filters some contaminants during operation
- Perfect water is not required - adequate water is sufficient

**Norwegian water is generally excellent:**

- Low population density = less pollution
- Bedrock geology = natural mineral content
- Cold temperatures = slow bacterial growth in source water (stays cleaner)
- NGU monitoring = documented quality assurance

**This test validates NGU data applicability:**

- If your results match NGU expectations, confidence is high
- We can rely on full NGU dataset (all 15 parameters) for system optimization
- Discrepancies indicate site-specific factors to account for

---

**Water quality confirmed - hydration secured!**

Clean, mineralized water is the invisible backbone of MFC performance. With local water chemistry understood, we can now begin physical construction knowing our biological and electrical systems will have the environment they need to thrive.

Next: **Step 08 - Build Foundation** (creating the physical structure that will house this biogeochemical powerhouse).

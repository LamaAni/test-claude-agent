# Airline Rules

## Purpose
This document defines how to handle airline baggage restrictions, ensure compliance, and optimize packing within airline-imposed limits.

## Core Principle
**Pack smart within airline limits to avoid fees, delays, and stress at the airport.**

## How to Lookup Airline Policies

### When User Specifies Airline
1. **Reference airline_limits.yaml** for standard policies
2. **Note route-specific variations** (domestic vs. international)
3. **Check class of service** (economy, premium economy, business, first)
4. **Verify current policies** (note: policies change, recommend user verification)

### When User Doesn't Specify Airline
1. **Identify common airlines** for the route
2. **Use most restrictive limits** as baseline
3. **Provide range** of typical allowances
4. **Recommend user verification** once airline is booked

### Key Information to Gather
- ✅ Carry-on dimensions (length × width × height)
- ✅ Carry-on weight limit
- ✅ Personal item dimensions
- ✅ Personal item allowance (and what qualifies)
- ✅ Checked bag dimensions
- ✅ Checked bag weight limits (per bag and total)
- ✅ Number of free checked bags
- ✅ Fee structure for additional/overweight bags
- ✅ Special item policies (sports equipment, musical instruments, etc.)
- ✅ Prohibited items

## Standard Airline Limits Reference

### Typical Carry-On Limits

**Most Common Standard:**
- **Dimensions:** 55 × 40 × 20 cm (22 × 16 × 8 in)
- **Weight:** 7-10 kg (15-22 lbs)
- **Wheels and handles** included in measurements

**Regional Variations:**
- **US Carriers:** Often 56 × 35 × 23 cm, weight limits vary or not enforced
- **European Carriers:** Stricter, often 55 × 40 × 20 cm, 8-10 kg
- **Asian Carriers:** Often 55 × 40 × 25 cm, 7 kg strictly enforced
- **Budget Airlines:** Can be smaller (e.g., 40 × 30 × 20 cm) and lighter (e.g., 5-7 kg)

### Typical Personal Item Limits

**Standard:**
- **Type:** Purse, laptop bag, small backpack
- **Typical Dimensions:** 40 × 30 × 15 cm (16 × 12 × 6 in)
- **Weight:** Usually must fit under seat, weight not typically specified
- **Combined Weight:** Some airlines enforce combined carry-on + personal item weight

**What Qualifies:**
- ✅ Backpack (small to medium)
- ✅ Laptop bag
- ✅ Purse or handbag
- ✅ Briefcase
- ❌ Rolling bag (too large)
- ❌ Duffel bag (unless very small)

### Typical Checked Bag Limits

**Economy Class Standard:**
- **Dimensions:** 158 cm total (length + width + height) / 62 linear inches
  - Common: 75 × 50 × 30 cm (30 × 20 × 12 in)
- **Weight:** 
  - US/Americas: 23 kg (50 lbs) per bag
  - Europe/Asia: 20-23 kg per bag
- **Number Free:**
  - US Domestic: Often 0-1 (varies by airline)
  - International: Usually 1-2 depending on route and class

**Premium Cabin Standards:**
- **Business Class:** Usually 2 bags at 32 kg each
- **First Class:** Usually 3 bags at 32 kg each
- **Premium Economy:** Usually 2 bags at 23 kg each

## Baggage Fee Structures

### Typical Fee Ranges (Economy Class)

**Checked Bags:**
- **First Checked Bag:** $30-60 USD (domestic), often free (international)
- **Second Checked Bag:** $40-100 USD
- **Third Checked Bag:** $150-200 USD

**Overweight Bags:**
- **23-32 kg (50-70 lbs):** $50-100 per bag
- **Over 32 kg (70 lbs):** $200+ per bag or refused

**Oversized Bags:**
- **Over 158 cm linear:** $200+ or refused

**Regional Variations:**
- **Budget Airlines:** All baggage often costs extra ($30-60 per bag)
- **International Long-Haul:** First bag often free
- **Premium Carriers:** More generous allowances

### Fee Avoidance Strategies

**Strategy 1: Maximize Carry-On**
- Use full carry-on allowance (55 × 40 × 20 cm, up to 7-10 kg)
- Use full personal item allowance (~40 × 30 × 15 cm)
- **Total Capacity:** ~40-50 liters combined
- **Total Weight:** 10-15 kg of gear (7-10 kg + 3-5 kg personal item)
- **Savings:** $60-120 per round trip

**Strategy 2: Checked Bag Optimization**
- Stay within free allowance (if provided)
- Pack to exactly weight limit (bring scale)
- Use every dimension available
- **Avoid:** Overweight fees by distributing weight across bags or travelers

**Strategy 3: Multi-Traveler Distribution**
- Distribute weight across travelers' allowances
- Each traveler maxes their limits
- Share luggage space efficiently

**Strategy 4: Airline Credit Card Benefits**
- Many airline cards offer free checked bag
- **ROI:** Card fee often pays for itself in bag fees

## Compliance Validation Process

### Pre-Packing Assessment

**Step 1: Identify Limits**
```
Airline: [Name]
Class: [Economy/Business/First]

Carry-On: [dimensions] cm, [weight] kg
Personal Item: [dimensions] cm
Checked Bag (free): [number] × [weight] kg
```

**Step 2: Calculate Required Capacity**
```
Total Items Weight: [calculated from packing list]
Total Items Volume: [estimated from item volumes]

Required Bags: [number and type]
```

**Step 3: Validate Compliance**
```
✅ Carry-on: [X] kg / [limit] kg - [OK/Overweight]
✅ Checked: [X] kg / [limit] kg - [OK/Overweight]
✅ Dimensions: [OK/Oversized]
✅ Number of bags: [X] / [allowance] - [OK/Extra bag needed]
```

### In Recommendations Output

Always include compliance check:
```
✈️ AIRLINE COMPLIANCE CHECK

Based on: [Airline Name or "Standard International Limits"]
Class: [Economy/Business/First]

Carry-On Bag:
  Your Packing: 6.8 kg / 42L
  Airline Limit: 10 kg / 55×40×20cm
  Status: ✅ Compliant (3.2 kg buffer)

Personal Item:
  Your Packing: 3.2 kg / 15L
  Airline Limit: Under-seat fit
  Status: ✅ Compliant

Checked Bag:
  Your Packing: 18.5 kg
  Airline Limit: 23 kg (1 free bag)
  Status: ✅ Compliant (4.5 kg buffer)
  Fee: $0 (within free allowance)

Total: ✅ Fully Compliant
```

## Luggage Type Recommendations

### Based on Trip Length and Type

**1-3 Days (Carry-On Only)**
- **Recommended:** Carry-on spinner or backpack (40L)
- **Capacity:** Sufficient for short trips
- **Complies:** Standard 55×40×20 cm limits
- **Weight:** 2-3 kg empty

**4-7 Days (Carry-On or Small Checked)**
- **Option A:** Large carry-on (45-50L) - if disciplined packing
- **Option B:** Carry-on + small checked bag (60L total)
- **Depends:** Laundry access, climate, activities

**8-14 Days (Medium Checked)**
- **Recommended:** Medium checked bag (70-80L)
- **Stays within:** 23 kg limit with careful packing
- **Allow:** Carry-on for valuables and essentials

**15+ Days (Large Checked or Multiple Bags)**
- **Recommended:** Large checked bag (90-100L) or multiple bags
- **Consider:** Laundry to minimize quantity
- **Plan for:** Possible second bag or overweight fees

### Luggage-Airline Fit

**For Strict Asian/Budget Airlines:**
- Choose smaller carry-on (under 7 kg achievable)
- Lightweight luggage critical (under 2.5 kg empty)
- Consider soft-sided for flexibility

**For US Domestic:**
- Can use maximum dimensions
- Weight less often enforced
- Hardside spinner acceptable

**For International Long-Haul:**
- Full-size luggage appropriate
- Use complete allowance
- Focus on durability

## Special Item Handling

### Sports Equipment

**Common Sports Items:**
- Golf clubs: Usually count as checked bag or fee ($30-75)
- Ski/snowboard: Usually fee ($30-150), dimensions critical
- Bicycle: Often fee ($50-150), disassembly required
- Surfboard: Often fee ($50-150), size limits apply
- Diving gear: Check airline policy (sometimes free as checked bag)

**Strategy:**
- Research specific airline policy for specific item
- Consider rental vs. transport
- Pack other items in sports bag to maximize space

### Musical Instruments

**Small Instruments (Fits carry-on):**
- Guitar (acoustic): Personal item or small instrument fee
- Violin/viola: Usually allowed as carry-on

**Large Instruments:**
- Must buy separate seat OR
- Check (risk of damage) OR
- Ship separately

### Medical Equipment

**Usually Allowed Without Counting Against Limits:**
- CPAP machines
- Oxygen concentrators
- Mobility devices (wheelchairs, walkers)
- Medications (in reasonable quantities)

**Requirements:**
- May need documentation
- TSA notification for security screening
- Airline pre-notification recommended

### Infant/Child Equipment

**Often Allowed Free:**
- Stroller (usually gate-checked)
- Car seat
- Diaper bag (as personal item)
- Portable crib

**Verify:** Specific airline family policies

## Prohibited Items

### Never in Carry-On
- Liquids over 100ml (except exceptions)
- Sharp objects (knives, scissors >6cm, razors)
- Sporting goods (bats, clubs, ski poles)
- Tools over certain size
- Self-defense items (pepper spray, tasers)
- Flammable items

### Never in Checked
- Lithium batteries (loose spares)
- Valuables (jewelry, cash, electronics - not prohibited but not recommended)
- Medications (take in carry-on)
- Flammable items (certain types)
- Compressed gases

### Liquid Rules (Carry-On)
- **Container Size:** Max 100ml (3.4 oz) per container
- **Total Allowed:** All must fit in 1 quart (1 liter) clear plastic bag
- **Exceptions:** Medications, baby formula/food, breast milk (reasonable quantities)

**Packing Advice:**
- Buy liquids after security or at destination
- Use solid alternatives (shampoo bars, solid sunscreen)
- Pack full-size liquids in checked baggage

## Weight Distribution Strategies

### Optimizing Weight Across Bags

**Heavy Items in Carry-On:**
- Shoes (heaviest footwear)
- Books, tablets, laptops (already carrying)
- Jacket (wear during boarding if needed)
- **Why:** Carry-on weight limits less enforced on some airlines

**Light/Bulky in Checked:**
- Clothing (relatively light per volume)
- Soft items that compress
- **Why:** Maximize checked bag space

### Traveler Weight Distribution

**Family of 4 Example:**
Each person has:
- Carry-on: 10 kg allowance = 40 kg total
- Checked: 23 kg allowance = 92 kg total
- **Total allowance:** 132 kg for family

**Strategy:**
- Distribute heavy shared items (toiletries, gear) across bags
- Each traveler manages their personal clothing
- Use one person's bag for shared overflow if needed

### Weight Management Tools

**Recommend Users:**
1. Use luggage scale before airport (±200g accuracy is fine)
2. Leave 1-2 kg buffer for measurement variations
3. Wear heaviest items if close to limit
4. Repack at airport if needed (have plan B)

## Fee Calculation and Presentation

### Present Fee Scenarios

**Example Output:**
```
💰 BAGGAGE COST ESTIMATE

Current Packing Plan: 1 Carry-On + 1 Checked Bag

Scenario 1: Your Planned Airline ([Airline Name])
  - Carry-on: Free
  - 1 Checked Bag: $30 each way = $60 total
  - TOTAL FEES: $60

Scenario 2: Budget Airline Alternative
  - Carry-on: $35 each way = $70
  - 1 Checked Bag: $50 each way = $100
  - TOTAL FEES: $170
  - DIFFERENCE: $110 more expensive

Scenario 3: Carry-On Only (Repack)
  - Carry-on: Free
  - No checked bags
  - TOTAL FEES: $0
  - SAVINGS: $60

Recommendation: [Based on budget and packing needs]
```

## Airline-Specific Considerations

### Major US Carriers (AA, Delta, United)
- Free carry-on + personal item
- First checked bag: $30-35 (domestic), often free (international)
- Loyalty status benefits (free bags)

### Budget US Carriers (Spirit, Frontier)
- Carry-on costs extra ($35-65)
- Personal item free (but smaller size)
- All checked bags cost ($30-60 for first)

### European Budget Carriers (Ryanair, EasyJet)
- Very strict size and weight limits
- Small personal item free
- Everything else costs money
- Enforcement: Rigorous

### European Flag Carriers (Lufthansa, British Airways, Air France)
- Standard carry-on free
- 1 checked bag free on international
- Reasonable limits (23 kg)

### Asian Carriers (Singapore, Cathay, JAL, ANA)
- Generous international allowances (2 bags often)
- Strict carry-on weight enforcement (7 kg)
- High service standards

### Middle Eastern Carriers (Emirates, Qatar, Etihad)
- Very generous allowances (often 2×30 kg)
- Premium service
- Relaxed enforcement generally

## Integration with Other Rules

### Climate Rules Integration
Heavy weather gear (winter coats, boots) can push weight limits
- Strategy: Wear heaviest items during travel
- Note: Winter packing often requires checked bag

### Budget Rules Integration
- Low budget: Prioritize carry-on only to save fees
- Calculate: Fees vs. convenience trade-off
- Consider: Buying luggage vs. paying fees long-term

### Traveler Rules Integration
- Families: Distribute weight across all allowances
- Children: May have reduced allowances (check airline)
- Infants: Usually no baggage allowance

## Communication Best Practices

### Always Include:
1. **Airline name** (if known) or "standard limits"
2. **Compliance status** for planned packing
3. **Buffer space/weight** remaining
4. **Fee estimates** (if applicable)
5. **Alternative options** if over limit

### Red Flags to Highlight:
- ⚠️ **Overweight:** "Your packing exceeds limit by X kg"
- ⚠️ **Oversized:** "Bag dimensions exceed airline limits"
- ⚠️ **Extra Bag Needed:** "Requires additional bag ($X fee)"
- ⚠️ **Strict Enforcement:** "This airline strictly enforces limits"

### Verification Reminders:
Always include:
> **⚠️ VERIFY BEFORE TRAVEL:** Airline policies change frequently. Confirm current baggage rules with your specific airline before your trip, especially for:
> - Weight and size limits
> - Number of free bags
> - Current fee structures
> - Special item policies

## Summary Checklist

**When making packing recommendations:**
- [ ] Identify airline or use standard limits
- [ ] Calculate total weight and volume
- [ ] Recommend appropriate luggage types
- [ ] Validate compliance with limits
- [ ] Calculate fee estimates (if applicable)
- [ ] Show weight/space buffers
- [ ] Provide alternative options
- [ ] Highlight special items needing attention
- [ ] Remind user to verify policies
- [ ] Integrate with budget and climate considerations

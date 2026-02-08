# Airline Rules

## Purpose
Define how the Packing Advisor agent should research and apply airline baggage policies to ensure compliance and optimize packing recommendations.

## Core Principle
**"Pack within limits, know the rules, avoid surprise fees"**

The agent must proactively research specific airline policies and validate recommendations against those restrictions.

## How to Lookup Airline Policies

### When Airline is Specified
1. **Look up current policies** from official airline website
2. **Identify route** (domestic vs. international affects allowances)
3. **Check cabin class** (economy, premium economy, business, first)
4. **Note fee structures** for checked bags and overweight/oversized items
5. **Check restricted items** for special gear

### When Airline is Not Specified
1. **Identify common carriers** for the route
2. **Use most restrictive common policy** as baseline
3. **Note**: "Based on typical airlines for this route..."
4. **Recommend**: "Confirm with your specific airline"

### Information to Gather
- Carry-on dimensions (length × width × height) in cm and inches
- Carry-on weight limit (if any)
- Personal item dimensions and restrictions
- Checked bag dimensions
- Checked bag weight limits (typically 23kg/50lbs)
- Number of bags allowed by class
- Fee structure for additional/overweight/oversized bags
- Restricted items relevant to trip (sports equipment, liquids, etc.)

## Carry-On Size and Weight Limits

### Standard Carry-On (Most Airlines)
**Dimensions**: 55cm × 40cm × 20cm (22" × 16" × 8")  
**Weight**: 7-10kg (15-22 lbs), varies by airline and region
**Placement**: Must fit in overhead bin

**Variations by Region:**
- **US Airlines**: Usually no weight limit, size focus
- **European Airlines**: Often 10kg limit
- **Asian Airlines**: Often 7kg limit, strict enforcement
- **Budget Airlines**: Often smaller dimensions and stricter limits

**Agent Behavior:**
- Look up specific airline
- If unknown, use conservative: 55×40×20cm, 7kg
- Note regional variations

### Personal Item (All Airlines)
**Examples**: Purse, laptop bag, small backpack  
**Typical Dimensions**: 45cm × 35cm × 20cm (18" × 14" × 8")  
**Weight**: Usually included in carry-on weight allowance  
**Placement**: Must fit under seat in front of you

**What Counts:**
- Laptop bag
- Purse or handbag
- Small backpack
- Briefcase

**What Doesn't Count (typically):**
- Duty-free shopping
- Reading materials
- Assistive devices
- Infant care items

**Packing Strategy:**
- Maximize personal item for heavy items (laptop, books, layers)
- Keeps carry-on lighter

### Carry-On Optimization Strategies

**Weight Distribution:**
1. **Personal item**: Heavy items (laptop, camera, books, coat)
2. **Carry-on**: Clothing and lighter items
3. **Worn**: Bulkiest clothing and heaviest shoes

**Example:**
```
Total: 12kg of items for carry-on only

Distribution:
- Personal item (backpack): 5kg (laptop 2kg, camera 1kg, coat 1kg, books 1kg)
- Carry-on suitcase: 7kg (clothing, toiletries)
- Worn: Heaviest shoes and jacket

Result: Each bag under typical limits
```

**Liquid Restrictions (Security):**
- 3-1-1 Rule: 3.4oz (100ml) per container
- All containers in 1 quart-size bag
- 1 bag per passenger

**Agent Behavior:**
- Remind of liquid limits for carry-on
- Suggest: Check full-size toiletries or buy on-site
- Note exceptions (medications, baby formula)

## Checked Baggage Allowances

### Standard Checked Bag Limits
**Weight**: 23kg (50 lbs) for economy, 32kg (70 lbs) for premium/business  
**Dimensions**: Linear dimensions (L+W+H) typically 158cm (62 inches)  
**Standard Size**: Large suitcase approximately 75cm × 50cm × 30cm

**By Cabin Class:**

#### Economy
- **Domestic US**: Usually 0-1 free checked bags (airline-dependent)
- **International**: Often 1 free checked bag (23kg)
- **Additional bags**: $50-150 each
- **Overweight** (23-32kg): $50-100 additional
- **Oversized** (>158cm): $100-200 additional

#### Premium Economy
- Usually 1-2 free checked bags
- Weight limit: 23-32kg
- Less restrictive than economy

#### Business/First Class
- Usually 2-3 free checked bags
- Weight limit: 32kg per bag
- More generous dimensions

**Agent Behavior:**
- Look up specific class allowances
- Calculate fees for extra bags
- Warn if approaching weight limits
- Suggest redistribution if overweight

### Number of Bags Allowed

**By Class (Typical International):**
- Economy: 1 free checked bag
- Premium Economy: 2 free checked bags
- Business: 2 free checked bags
- First: 3 free checked bags

**Domestic US Variations:**
- Basic Economy: Often 0 free checked bags
- Standard Economy: 0-1 free bags (airline dependent)
- Premium: 1-2 free bags

**Fee Structure Examples:**
```
United Economy (International):
- First bag: Free (up to 23kg)
- Second bag: $100
- Overweight (23-32kg): $100 additional
- Total for 2 heavy bags: $200

Southwest (US Domestic):
- First bag: Free
- Second bag: Free
- Overweight: $75

Spirit (Budget):
- First bag: $30-65 (higher at airport)
- Second bag: $45-80
- All fees apply
```

**Agent Calculation:**
```
Scenario: 2 people, 10-day trip, economy international

Option A: 2 checked bags (1 each)
- Cost: $0 (included)
- Weight limit: 46kg total
- Packing flexibility: High

Option B: 3 checked bags (add 1)
- Cost: $100
- Weight limit: 69kg total
- Needed if: >46kg or special equipment

Recommendation: Option A unless >23kg per person
```

## Personal Item Specifications

### What Qualifies as Personal Item
**Acceptable:**
- Purse or handbag
- Laptop bag (up to 17" laptop typically)
- Small backpack (under ~40L)
- Briefcase
- Camera bag
- Diaper bag

**Dimensions** (typical): 45×35×20cm (18×14×8")

**Not Acceptable as Personal Item:**
- Large backpacks (hiking backpacks)
- Shopping bags (usually, but duty-free often OK)
- Oversized totes
- Additional suitcases

### Strategic Packing
**Best items for personal item:**
- Laptop and electronics (heavy, valuable)
- Medications and essentials (accessible)
- Entertainment (books, headphones)
- Layers (jacket, sweater)
- Valuables

**Why:**
- Accessible during flight
- Reduces carry-on weight
- Keeps essentials with you

## Compliance Validation

### Agent Validation Checklist

For every packing recommendation, verify:

1. **Weight Compliance**
   - [ ] Total weight within carry-on limit (if carry-on only)
   - [ ] Each checked bag under 23kg (or airline-specific limit)
   - [ ] Warn if within 2kg of limit (safety buffer)

2. **Size Compliance**
   - [ ] Carry-on dimensions meet airline specs
   - [ ] Checked bags under linear dimension limits
   - [ ] Note if oversized items (sports equipment)

3. **Item Restrictions**
   - [ ] No prohibited items (weapons, chemicals)
   - [ ] Liquids meet 3-1-1 rule if carry-on
   - [ ] Batteries in carry-on (not checked)
   - [ ] Sharp items (scissors, razors) noted

4. **Special Equipment**
   - [ ] Sports equipment (surfboard, skis, bike) noted with fees
   - [ ] Musical instruments policy
   - [ ] Medical devices clearance

**Validation Output:**
```
✅ AIRLINE COMPLIANCE CHECK (United Airlines, Economy)

Carry-On: 8.5kg / 10kg limit ✅
Dimensions: 54×38×20cm / 56×36×23cm limit ✅
Personal Item: Small backpack ✅

Compliance: PASSED
No additional fees expected
```

**Warning Example:**
```
⚠️ WEIGHT WARNING (American Airlines, Economy)

Checked Bag 1: 22kg / 23kg limit ⚠️
- Currently under limit but close
- Adding more items risks overweight fee ($100)
- Consider removing 2-3kg for safety buffer

Checked Bag 2: Proposed 25kg / 23kg limit ❌
- OVERWEIGHT: Would incur $100 fee
- Recommendation: Redistribute 2kg to Bag 1 or remove items
```

## Fee Structures

### Common Fee Types

1. **First Checked Bag**: $0-65 (varies by airline and route)
2. **Second Checked Bag**: $50-150
3. **Additional Bags** (3+): $150-300 each
4. **Overweight** (23-32kg): $50-150
5. **Overweight** (32-45kg): $200-400 (if accepted)
6. **Oversized** (>158cm linear): $100-200
7. **Special Equipment**: $50-200 (surfboards, bikes, skis)

### How to Present Fees

**Format:**
```
💰 BAGGAGE FEE ANALYSIS (Delta, Economy, International)

Current Plan: 2 checked bags (1 per person)
- Bag 1 (Person 1): Free (included)
- Bag 2 (Person 2): Free (included)
Total Fees: $0

Alternative: Add 1 bag for shared items
- Bag 3: $150
Total Fees: $150

Recommendation: Stick with 2 bags, redistribute items to stay within limits
```

**Fee Saving Opportunities:**
```
💡 FEE SAVINGS AVAILABLE

Current: 2 checked bags = $100 in fees
Option: Optimize to carry-on only = $0 in fees
Savings: $100

Trade-offs:
- Requires laundry planning (2 sessions, ~$20)
- Less clothing variety
- More effort at destination
Net Savings: $80

Worth it? For budget travel, yes. For convenience, no.
```

### Regional Fee Variations

**US Domestic:**
- Most airlines charge for first bag: $30
- Southwest and some others: 2 free bags
- Basic economy: Often higher fees or no included bags

**International:**
- First bag usually free in economy
- Some budget airlines charge for all bags
- Long-haul typically more generous

**Europe:**
- Many budget airlines (Ryanair, EasyJet): Charge for everything
- Full-service: Similar to US international

**Asia:**
- Generally generous allowances
- Stricter weight enforcement

**Agent Behavior:**
- Look up specific route regulations
- Note regional differences
- Calculate precise fees for user's situation

## Special Item Handling

### Sports Equipment

**Common Items:**
- Surfboards: $50-150, often size-limited
- Bicycles: $50-200, may need box
- Skis/Snowboards: $50-150 first bag, sometimes free in winter
- Golf clubs: Often free as first bag
- Scuba gear: Usually free as checked bag

**Agent Recommendations:**
- **Pack**: If frequent use, own equipment preferred
- **Rent**: If occasional, likely cheaper and easier
- **Check Fees**: Compare baggage fee vs. rental cost
- **Note Requirements**: Boxing, size limits, advance notice

**Example:**
```
Surfboard for Hawaii Trip:

Option A: Pack (United)
- Baggage fee: $150 each way = $300
- Risk of damage
- Have your own board

Option B: Rent on-site
- Rental: $30/day × 7 days = $210
- No baggage hassle
- Try different boards

Recommendation: Rent (saves $90, less hassle)
```

### Musical Instruments

**Small** (violin, small guitar): May qualify as carry-on or personal item  
**Medium** (guitar): May need to buy seat or check  
**Large** (cello): Must buy seat typically

**Agent Behavior:**
- Note instrument size
- Check airline-specific policies (vary widely)
- Recommend case protection
- Suggest advance notice to airline

### Medical Devices and Medications

**Allowed in Carry-On:**
- Liquid medications (exempt from 3-1-1 rule)
- CPAP machines
- Nebulizers
- Assistive devices

**Agent Recommendations:**
- Always in carry-on (never check)
- Bring prescription labels
- Pack more than needed
- Carry doctor's note if controlled substances

### Lithium Batteries

**Rules:**
- Spare batteries: Must be in carry-on
- Installed in devices: Can be in checked
- Power banks: Carry-on only
- Size limits: Typically 100Wh (check for larger)

**Agent Behavior:**
- Remind to pack power banks in carry-on
- Check requirements for large batteries (camera equipment)
- Note restrictions

## Airline-Specific Quirks

### Budget Airlines (Spirit, Frontier, Ryanair, EasyJet)
**Characteristics:**
- Charge for everything
- Smaller carry-on limits
- Strict enforcement
- Fees increase at airport vs. online booking

**Agent Approach:**
- Check ALL fees ahead
- Plan for minimal packing
- Pre-pay bags online (cheaper)
- Warn about strict enforcement

### Premium Airlines (Emirates, Singapore, Qatar)
**Characteristics:**
- Generous allowances even in economy
- 30-35kg often allowed
- Extra bags often included
- Less strict enforcement

**Agent Approach:**
- Take advantage of generous limits
- Can pack more comfortably
- Less need for optimization

### Domestic Budget Carriers (Southwest)
**Southwest Specifics:**
- 2 free checked bags (50 lbs each)
- No change fees
- More generous than most US carriers

**Agent Approach:**
- Recommend checking bags (it's free!)
- Less need for carry-on optimization

## Compliance Communication

### Green Light (Fully Compliant)
```
✅ FULLY COMPLIANT
Your packing plan meets all [Airline] requirements:
• Carry-on: 7.2kg (under 10kg limit)
• Dimensions: Within limits
• No additional fees
Ready to pack!
```

### Yellow Light (Close to Limits)
```
⚠️ APPROACHING LIMITS
Current plan is compliant but close:
• Weight: 21.5kg / 23kg (1.5kg buffer)
• Adding more items risks overweight fee
• Consider removing 2-3 items for safety
Otherwise, you're good!
```

### Red Light (Non-Compliant)
```
❌ EXCEEDS LIMITS
Current plan exceeds [Airline] allowances:
• Checked Bag: 26kg (3kg over 23kg limit)
• Overweight fee: $100 per bag

SOLUTIONS:
1. Remove 3kg of items
2. Add second checked bag ($150) and redistribute
3. Ship heavy items separately

Recommendation: Remove items (save $100)
```

## Cross-Airline Considerations

### Multi-Leg Journeys with Different Airlines
**Challenge**: Different allowances on each leg

**Agent Behavior:**
1. Identify most restrictive airline
2. Pack to meet strictest requirements
3. Note differences: "Your first leg allows more, but your connection is limited"
4. Recommend: Plan for strictest

**Example:**
```
⚠️ MULTI-AIRLINE JOURNEY
Outbound: United (23kg checked bag free)
Return: Air France partner (23kg checked bag free)
Both aligned, no issues.

But if:
Outbound: Southwest (2 bags free)
Return: Budget airline (bags cost extra, 20kg limit)

Recommendation: Pack to return flight limits (20kg, budget for fees)
```

### International Connections
**Factors:**
- Through-check vs. reclaim and recheck
- Customs considerations
- Different regulations by country

**Agent Notes:**
- Mention if bags will be rechecked
- Note customs allowances (liquids, food, etc.)
- Recommend conservative packing

## Summary Rules

### Always Do:
1. ✅ Look up specific airline policies when airline is known
2. ✅ Verify weight and size compliance
3. ✅ Calculate and present total fees
4. ✅ Warn when approaching limits
5. ✅ Consider special equipment separately

### Never Do:
1. ❌ Assume generic airline policies (look it up!)
2. ❌ Ignore weight limits
3. ❌ Forget to account for luggage weight itself
4. ❌ Recommend non-compliant packing
5. ❌ Hide potential fees from user

### Remember:
- **Airlines enforce rules strictly** (especially budget carriers)
- **Fees add up quickly** ($100+ is common)
- **Weight limits are hard stops** (can't board if overweight)
- **Advance planning saves money** (pre-pay bags online)
- **When in doubt, verify** with airline before travel
- **Build in buffer** (2kg under limit is safer than exactly at limit)

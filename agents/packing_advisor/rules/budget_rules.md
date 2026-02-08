# Budget Rules

## Purpose
This document defines how the Packing Advisor agent should interpret budget constraints and optimize packing recommendations for cost-effectiveness while maintaining travel quality.

## Budget Level Definitions

### Low Budget ($)
**Characteristics:**
- Minimize baggage fees at all costs
- Prioritize carry-on only when possible
- Recommend buying basic consumables on-site
- Focus on multi-use, versatile items
- Suggest budget-friendly alternatives

**Target Luggage:**
- One carry-on + one personal item (avoid checked bag fees)
- Total weight: ≤7-10kg combined

**Approach:**
- Every item must justify its weight and space
- Lean toward "buy there" for toiletries, basics
- Emphasize laundry usage to reduce clothing quantity
- Avoid single-use items

### Medium Budget ($$)
**Characteristics:**
- Balance between convenience and cost
- One checked bag acceptable if beneficial
- Pack full-size toiletries if space allows
- Moderate gear investment
- Some convenience items acceptable

**Target Luggage:**
- Carry-on + checked bag OR large carry-on only
- Total weight: ≤15-20kg

**Approach:**
- Pack efficiently but don't sacrifice comfort excessively
- Bring specialty items if they save money long-term
- Consider checked bag if it avoids purchases on-site
- Balance laundry frequency with packing quantity

### High Budget ($$$)
**Characteristics:**
- Convenience and comfort prioritized
- Multiple bags or larger luggage acceptable
- Premium or specialized gear when beneficial
- Bring everything needed for comfort
- Baggage fees not a primary concern

**Target Luggage:**
- Multiple bags as needed
- Total weight: ≤30kg+ (within airline limits)

**Approach:**
- Pack for maximum comfort and convenience
- Bring preferred brands and items
- Include nice-to-have items
- Reduce reliance on on-site purchases
- Quality and convenience over weight/space optimization

## When to Recommend Buying On-Site vs. Packing

### Buy On-Site (All Budget Levels)
1. **Basic toiletries** (shampoo, soap, toothpaste) - UNLESS:
   - Specific brand required for medical/skin reasons
   - Not widely available at destination
   - Extended trip where buying multiple times costs more

2. **Consumables** (sunscreen, insect repellent) - UNLESS:
   - Specific formulation needed
   - Significantly more expensive at destination
   - Availability uncertain

3. **Bulky, low-value items** (beach towels, basic flip-flops)
   - UNLESS: Already owned and space available

### Always Pack (All Budget Levels)
1. **Personal medications and prescriptions**
2. **Essential documents**
3. **Electronics and chargers**
4. **Prescription eyewear/contacts**
5. **Specialized gear** not available on-site
6. **Expensive items** that would cost more to buy than to check

### Budget-Specific Decisions

**Low Budget:**
- Buy: All toiletries, basic beach/sports gear, one-time use items
- Pack: Only absolute essentials and multi-use items
- Calculation: If item costs <$10 locally and weighs >500g, buy there

**Medium Budget:**
- Buy: Basic toiletries, bulky single-use items
- Pack: Preferred brands, frequently-used items, quality gear
- Calculation: Balance convenience vs. cost

**High Budget:**
- Buy: Only if unavailable or more convenient
- Pack: Everything for optimal comfort
- Calculation: Convenience and quality prioritized

## Cost Calculation Framework

### Baggage Fee Considerations

**Low Budget - Fee Avoidance Priority:**
```
Checked Bag Fee: $30-60 (each direction) = $60-120 total
Strategy: Avoid checked bags entirely
Acceptable Trade-offs:
  - Buy toiletries locally: ~$15-25
  - Do laundry: ~$10-20 per trip
  - Buy basic items: ~$20-40
Total Savings: $60-120 minus $45-85 = $15-35 saved
```

**Medium Budget - Balanced Approach:**
```
Checked Bag Fee: $30-60 (each direction) = $60-120 total
Decision Factor: Is checked bag worth the convenience?
  - If saves >$60 in on-site purchases: Yes
  - If enables bringing valuable owned gear: Yes
  - Otherwise: Optimize for carry-on
```

**High Budget - Convenience Focus:**
```
Checked Bag Fees: Not a primary decision factor
Focus: What makes travel most comfortable?
Multiple Bags: Acceptable if beneficial
```

### Luggage Purchase Recommendations

**When to Suggest Buying New Luggage:**

**Low Budget:**
- Only if current luggage exceeds airline limits
- Recommend: Budget spinner ($50-80)
- ROI: If saves even one baggage fee, pays for itself

**Medium Budget:**
- If current luggage is inadequate or broken
- Recommend: Quality mid-range ($100-200)
- Consider: Investment in good luggage for future trips

**High Budget:**
- Suggest premium options for optimal experience
- Recommend: High-quality brands ($200-400+)
- Consider: Specialized luggage for trip type

### On-Site Purchase Cost Estimates

Provide users with estimated costs for items to buy locally:

**Example Communication:**
```
💰 BUY ON-SITE RECOMMENDATIONS
These items are widely available in [destination]:
  
  Basic Toiletries Kit:
    - Shampoo, soap, toothpaste
    - Estimated cost: $10-15
    - Weight saved: ~1.5kg
    
  Beach Towel:
    - Available at local shops
    - Estimated cost: $8-12
    - Weight saved: ~500g
    
  Total savings: ~2kg, Cost: ~$20-30
  
  ✅ Cheaper than $60 checked bag fee!
```

## Budget Optimization Strategies

### Strategy 1: Laundry-Based Reduction
**All Budget Levels:**
- Calculate optimal laundry frequency
- Reduce clothing quantity accordingly
- Cost vs. quantity trade-off

**Example:**
```
7-day trip with laundry:
  - Mid-trip laundry: ~$15
  - Pack 4 outfits instead of 7
  - Weight saved: ~2-3kg
  - Enables carry-on only: Saves $60-120 baggage fees
  - Net savings: $45-105
```

### Strategy 2: Multi-Use Item Maximization
**Emphasize items that serve multiple purposes:**
- Sarong: Beach towel, blanket, scarf, dress
- Buff/neck gaiter: Hat, scarf, mask, headband
- Convertible pants: Shorts and long pants
- Smartphone: Camera, guidebook, entertainment, communication

**Budget Impact:**
- Reduces total items needed
- Reduces weight and space
- Reduces purchase requirements

### Strategy 3: Rental vs. Pack vs. Buy Analysis

**For Specialized Gear (ski equipment, diving gear, camping gear):**

**Low Budget:**
```
Rental Analysis:
  Equipment rental: $30-50/day
  Baggage fees for equipment: $50-150 each way
  
  If trip ≤ 7 days: Rent (saves transport hassle)
  If trip > 7 days: Buy locally if staying long-term
```

**Medium Budget:**
```
Consider:
  - Own the gear: Bring it (accept baggage fees)
  - Don't own it: Rent if trip < 10 days, buy if longer or frequent use
```

**High Budget:**
```
Preference:
  - Own quality gear: Bring it for comfort/familiarity
  - Don't own it: Rent premium options
```

### Strategy 4: Clothing Quantity Optimization

**Formula by Budget:**

**Low Budget:**
```
Base Clothing Formula:
  - Underwear: (Trip days ÷ 2) + 1
  - Shirts: (Trip days ÷ 2) + 1
  - Pants/Shorts: 2-3
  - Sleepwear: 1
  
  Requires: Mid-trip laundry
```

**Medium Budget:**
```
Base Clothing Formula:
  - Underwear: (Trip days ÷ 1.5) rounded up
  - Shirts: (Trip days ÷ 1.5) rounded up
  - Pants/Shorts: 3-4
  - Sleepwear: 1-2
  
  Allows: Optional mid-trip laundry
```

**High Budget:**
```
Base Clothing Formula:
  - Underwear: 1 per day + 2 extra
  - Shirts: 1 per day
  - Pants/Shorts: 1 per 2 days + 1 extra
  - Sleepwear: 2
  
  Laundry: As desired for freshness, not necessity
```

## Cost-Benefit Analysis Framework

### Present to Users
When recommending checked bag vs. carry-on only:

```
📊 BAGGAGE COST ANALYSIS

Option A: Carry-On Only
  Baggage Fees: $0
  Items to buy locally: ~$30-40
  Laundry costs: ~$15
  Total: $45-55
  Pros: No bag check time, no loss risk
  Cons: Less flexibility, some purchases needed

Option B: One Checked Bag
  Baggage Fees: $60-120 (round trip)
  Items to buy locally: $0-10
  Laundry costs: Optional
  Total: $60-130
  Pros: Bring everything, more comfort
  Cons: Higher cost, bag check time

Recommendation: [Based on budget level and trip type]
```

## Budget Communication Best Practices

### Do:
- ✅ Present cost comparisons clearly
- ✅ Show trade-offs explicitly
- ✅ Provide estimated local prices
- ✅ Calculate total trip packing costs
- ✅ Align recommendations with stated budget level
- ✅ Offer alternatives at different price points

### Don't:
- ❌ Assume everyone wants to minimize costs
- ❌ Ignore convenience for extreme budget optimization
- ❌ Recommend excessive purchases for minimalism alone
- ❌ Present baggage fees without context
- ❌ Forget to account for time and hassle costs

## Special Situations

### When Budget Level Not Specified
- Default to **Medium Budget** approach
- Present options for all three levels
- Let user choose based on preferences

### When Budget Conflicts with Trip Type
Example: Low budget but luxury resort destination
- Acknowledge the conflict
- Provide realistic guidance
- Focus on strategic cost-cutting that doesn't compromise experience
- "Strategic packing can help manage costs while maintaining comfort"

### When Budget Allows Multiple Options
- Present 2-3 options with cost implications
- Let user decide based on their priorities
- Example: "You could carry-on only ($45 total) or check a bag ($90 total) for more comfort"

## Return Trip Capacity

### Budget Implications

**Low Budget:**
- Plan for no additional purchases requiring space
- If shopping likely: Start with minimal packing to allow room
- Compression bags for return trip

**Medium Budget:**
- Allow some shopping capacity
- Consider: Leave space or accept second bag fee on return

**High Budget:**
- Plan for shopping
- Second bag or larger luggage acceptable
- Pre-plan for return luggage expansion

## Summary Guidelines by Budget Level

### Low Budget ($)
- **Priority:** Minimize fees and purchases
- **Luggage:** Carry-on only
- **Buy on-site:** Toiletries, basics, consumables
- **Laundry:** Required, mid-trip
- **Trade-off:** Accept some inconvenience for savings

### Medium Budget ($$)
- **Priority:** Balance cost and comfort
- **Luggage:** Efficient packing, one checked if beneficial
- **Buy on-site:** Bulky or single-use items
- **Laundry:** Optional, for convenience
- **Trade-off:** Optimize without sacrificing experience

### High Budget ($$$)
- **Priority:** Comfort and convenience
- **Luggage:** As needed for comfort
- **Buy on-site:** Only if more convenient
- **Laundry:** Optional, for freshness
- **Trade-off:** Efficiency still valued, but not at expense of comfort

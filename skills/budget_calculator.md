# Budget Calculator Skill
## Purpose
Calculate total costs related to packing decisions and optimize for budget constraints.

## When to Use
- All trips (provides cost transparency)
- Budget-conscious travelers
- To compare packing strategies (laundry vs. extra bag)
- Buy-on-site vs. pack decisions

## Input
- **Budget level**: Low, Medium, High (or specific dollar amount)
- **Airline**: For baggage fee calculation
- **Packing strategy**: Carry-on only, checked bags, etc.
- **Destination**: For on-site purchase costs
- **Trip length**: Affects various costs

## Cost Categories to Calculate

### 1. Baggage Fees
**Calculate:**
- Carry-on fees (if budget airline)
- First checked bag fee (if applicable)
- Second checked bag fee (if applicable)
- Overweight fees (if over limits)
- Special item fees (sports equipment)

**Source:** Airline Lookup Skill

**Example:**
```
United Economy Domestic:
- First bag: $35
- Second bag: $45
Total: $80 round-trip for 2 bags
```

### 2. Luggage Purchase (if needed)
**Factors:**
- Does user need to buy new luggage?
- Quality level based on budget
- Expected lifespan / cost per use

**Recommendation:**
```
If current luggage broken/inadequate:
- Low budget: $50-80 basic but functional
- Medium budget: $150-250 quality mid-range
- High budget: $300+ premium brands

If luggage adequate: $0
```

### 3. Laundry Costs
**Calculate:**
- Number of washes needed
- Cost per wash (from Destination Research)
- Total trip laundry cost

**From:** Laundry Optimizer Skill

**Example:**
```
10-day trip, 2 washes:
- Coin laundry: $10 × 2 = $20
- Hotel service: $25 × 2 = $50
```

### 4. Buy On-Site Costs
**Estimate costs for:**
- Toiletries (shampoo, sunscreen, etc.)
- Consumables (bottled water, snacks)
- Forgotten items
- Rental gear (snorkel, camping, etc.)

**Decision Framework:**
```
Pack if:
- Item is expensive at destination
- Hard to find at destination
- Specific brand needed
- Weight/space not significant

Buy on-site if:
- Heavy/bulky
- Cheap and widely available
- Consumable (will use up)
- Uncertain if needed
```

**Example:**
```
Beach trip buy-on-site:
- Sunscreen refill: $10
- Bottled water: $20 for trip
- Beach towel (if needed): $15
Total: $45
```

### 5. Gear Rental Costs
**Calculate:**
- Rental cost × days needed
- Compare to baggage fee for bringing

**Example:**
```
Snorkel gear:
- Pack: Baggage fee $50, or takes carry-on space
- Rent: $10/day × 5 days = $50
Decision: Rent (same cost, less hassle)

Camping gear:
- Pack: Baggage fee $100 + hassle
- Rent: $150 for week
Decision: Pack if own gear, rent if don't
```

### 6. Travel Insurance
**Recommend:**
- Basic: $20-40 for short trips
- Comprehensive: $50-100 for international
- Adventure: $100-200 if high-risk activities

**Factor in:** Medical coverage abroad, trip cancellation, baggage loss

## Calculation Process

### Step 1: Calculate Current Plan Cost
```
Baggage fees: $[X]
Laundry: $[Y]
Buy on-site: $[Z]
Rentals: $[W]
TOTAL: $[X+Y+Z+W]
```

### Step 2: Calculate Alternative Strategies

**Alternative A: Carry-On Only**
```
Baggage fees: $0
Laundry: $30 (more frequent)
Buy on-site: $50 (toiletries)
TOTAL: $80
SAVINGS vs. current: $[difference]
```

**Alternative B: Extra Checked Bag**
```
Baggage fees: $150 (2 bags)
Laundry: $0 (pack full wardrobe)
Buy on-site: $20
TOTAL: $170
ADDITIONAL COST: $[difference]
```

### Step 3: Optimize for Budget

**If Low Budget:**
- Minimize baggage fees (carry-on only if possible)
- Do laundry instead of packing more
- Buy consumables on-site
- Rent bulky gear instead of pack
- Use existing luggage

**If Medium Budget:**
- Balance convenience and cost
- Optimize, but don't sacrifice too much comfort
- One checked bag acceptable
- Pack important items, buy cheap stuff on-site

**If High Budget:**
- Prioritize convenience over cost
- Pack everything needed
- Multiple bags if beneficial
- Premium luggage
- Less concern about fees

## Output Format

```markdown
💰 BUDGET ANALYSIS
Budget Level: [Low / Medium / High]

CURRENT PACKING PLAN COSTS:
• Baggage fees: $[X] ([details])
• Laundry: $[X] ([Y] washes @ $[Z] each)
• Buy on-site: $[X] ([items])
• Gear rental: $[X] ([items])
• Luggage purchase: $[X] (if needed)
• Travel insurance: $[X] (recommended)
━━━━━━━━━━━━━━━━━━━━━
TOTAL PACKING-RELATED COSTS: $[TOTAL]

OPTIMIZATION OPPORTUNITIES:
✅ Option 1: [Strategy]
   - Cost: $[X]
   - Savings: $[Y]
   - Trade-off: [What you give up]

✅ Option 2: [Strategy]
   - Cost: $[X]
   - Savings: $[Y]
   - Trade-off: [Consideration]

RECOMMENDATION FOR [Budget Level]:
[Specific advice]

COST BREAKDOWN BY TRIP PHASE:
• Before trip: $[X] (luggage, prep)
• Outbound flight: $[X] (baggage fees)
• During trip: $[X] (laundry, purchases)
• Return flight: $[X] (baggage fees)
```

## Examples

### Example 1: Budget Beach Trip
```
💰 BUDGET - Low (Minimize Costs)
10-day Bali trip, couple

CURRENT PLAN:
• 2 checked bags: $100
• Laundry: $20
• Buy on-site: $30
TOTAL: $150

OPTIMIZED PLAN:
• Carry-on only: $0
• Laundry (3 washes): $30
• Buy toiletries: $40
TOTAL: $70

SAVINGS: $80 (53% reduction)
Trade-off: Less clothing variety, need laundry time

Recommendation: Carry-on optimization worth it for budget goals.
```

### Example 2: Business Trip, Medium Budget
```
💰 BUDGET - Medium (Balance)
3-day London trip, solo

CURRENT PLAN:
• Carry-on: $0 (included)
• No laundry: $0 (too short)
• UK adapter: $15
TOTAL: $15

Alternative (if checked bag):
• Checked bag: $60
• More clothes comfort
TOTAL: $60

Recommendation: Carry-on saves $60 and time (no bag wait). For 3 days, packing light is practical. Invest in quality carry-on if traveling frequently.
```

### Example 3: Family Adventure, High Budget
```
💰 BUDGET - High (Convenience Priority)
7-day Canadian Rockies, family of 4

CURRENT PLAN:
• 2 checked bags: $100
• Camping gear rental: $200
• Laundry mid-trip: $10
• Groceries: $250
TOTAL: $560

Alternative (pack all gear):
• 2 checked + 2 overweight: $300
• Own camping gear: $0
• Laundry: $10
• Groceries: $250
TOTAL: $560

Recommendation: Renting gear is same cost and much less hassle. High budget allows convenience focus. Packed clothes + rented bulky gear optimal.
```

## Buy vs. Pack Decision Matrix

| Item Type | Pack if... | Buy on-site if... |
|-----------|-----------|-------------------|
| Toiletries | Specific brand needed, small sizes | Bulky, widely available |
| Sunscreen | Already own, small trip | Long trip, buy large bottle there |
| Medications | Prescription, specific needs | OTC and available there |
| Clothing | Fits well, you own it | Cheap destination, uncertain need |
| Activity gear | You own, light, frequently used | Heavy, one-time use, rental available |
| Beach towel | Pack microfiber towel (light) | Buy cheap local towel or rent |

## Best Practices
- ✅ Calculate all costs, not just obvious ones
- ✅ Compare total cost of strategies, not just one factor
- ✅ Factor in time cost (waiting for laundry, shopping)
- ✅ Consider long-term (luggage amortized over many trips)
- ✅ Account for return trip (souvenirs add weight/cost)
- ✅ Include hidden costs (taxi because too much luggage)
- ❌ Don't focus only on baggage fees (laundry, purchases matter too)
- ❌ Don't forget peace of mind value (insurance, being prepared)
- ❌ Don't over-optimize if savings are minimal ($10-20)

## Integration
- Uses: Airline Lookup (baggage fees)
- Uses: Destination Research (local prices)
- Uses: Laundry Optimizer (laundry costs)
- Works with: All skills (provides cost context)
- Informs: Final recommendations (cost-optimized)

## Pro Tips
1. **Book bags online**: Cheaper than at airport (often $10-20 savings)
2. **Credit card perks**: Some cards include free checked bags
3. **Airline status**: Frequent flyers get free bags
4. **Travel insurance**: Compare policies, shop around
5. **Loyalty programs**: Hotel laundry may be discounted for members
6. **Local SIM**: $10 local SIM vs. $100 roaming fees
7. **Airport shopping**: Usually expensive, buy beforehand
8. **Duty-free**: Good for alcohol/perfume, not necessities
9. **Pack vs. buy decision**: If cost difference <$20, optimize for convenience
10. **Long-term thinking**: $200 quality luggage lasts 10 years = $20/trip

## Summary
**Key Takeaways:**
- Total packing costs often $50-300 depending on strategy
- Baggage fees are largest cost (often $50-150)
- Carry-on only saves $100+ on fees
- Laundry costs $10-50 but saves baggage fees
- Buying on-site varies greatly by destination
- Budget level should inform strategy
- Compare total cost, not individual line items
- Sometimes spending $20 more saves significant hassle
- Always calculate both options before deciding

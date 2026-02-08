# Laundry Optimizer Skill
## Purpose
Calculate optimal laundry frequency and determine how it reduces clothing quantities needed for trip.

## When to Use
- Trips longer than 5 days
- When laundry facilities are available
- To minimize luggage weight/volume
- Budget-conscious travelers

## Input
- Trip length (days)
- Laundry availability (type, cost, time)
- Clothing change frequency (active trip vs. casual)
- Climate (humidity affects drying time)

## Calculation Process

### Step 1: Determine Base Clothing Need
Without laundry:
```
Trip Length × Items per day = Total items needed
10 days × 1 shirt/day = 10 shirts
10 days × 1 underwear/day = 10 underwear
```

### Step 2: Calculate Laundry Schedule
Factors:
- **Wash frequency**: Every 3-5 days typical
- **Drying time**: 24 hours in humid climates, 12 hours dry
- **Processing time**: 2-3 hours for coin laundry, overnight for hotel service

Optimal schedule:
```
10-day trip example:
- Day 1-4: Wear first set (4 days clothes)
- Day 4-5: Laundry (wash day 1-4 clothes)
- Day 5-8: Wear second set (4 days clothes)
- Day 8-9: Laundry (wash day 5-8 clothes)
- Day 9-10: Wear first set again (2 days)

Result: Only need 5 days of clothes for 10-day trip
Savings: 50% less clothing
```

### Step 3: Calculate Laundry Costs
```
Number of washes × Cost per wash = Total laundry cost
2 washes × $10 = $20 total

Compare to:
Packing 10 days clothes = Extra checked bag = $100

Savings: $80 by doing laundry
```

### Step 4: Factor in Activity/Climate
Adjustments:
- **Hot/humid climate**: +1 extra set (clothes may not dry completely)
- **Active activities**: +20% (get dirtier faster, may need backup)
- **Business/formal**: Less practical (suits harder to wash)
- **Casual beach/hiking**: Very practical

## Output Format
```
🧺 LAUNDRY OPTIMIZATION ANALYSIS
Trip: [X] days

WITHOUT LAUNDRY:
- Clothing needed: [Y] days of outfits
- Weight: ~[Z] kg
- Space: [W] liters

WITH LAUNDRY STRATEGY:
- Clothing needed: [Y2] days of outfits (reduced by [%])
- Laundry schedule: Day [X] and Day [Y]
- Facility: [Coin laundry / Hotel service]
- Cost: $[X] per wash × [Y] washes = $[Z] total
- Time: [X] hours per wash

WEIGHT SAVINGS:
- Reduced by: [X] kg
- Allows: [Smaller luggage / Room for souvenirs / Lighter travel]

COST COMPARISON:
- Laundry cost: $[X]
- vs. Packing full wardrobe: $[Y] (potential extra bag fee)
- Net savings/cost: $[Z]

RECOMMENDATION:
✅ [Do laundry on Day X and Y] / ❌ [Not practical for this trip]

CONSIDERATIONS:
• [Factor 1: e.g., Hotel has self-service laundry]
• [Factor 2: e.g., Humid climate may extend drying time]
• [Factor 3: e.g., Pack quick-dry fabrics]
```

## Examples

**Example 1: 10-Day Beach Vacation, Budget Conscious**
```
WITHOUT: 10 days clothes = 5kg
WITH: 5 days clothes + 2 washes = 2.5kg + $20 laundry

Laundry Days: 4 and 8
Savings: 2.5kg weight, fits in smaller bag
Cost: $20 laundry vs. $100 extra bag fee
Recommendation: ✅ Definitely do laundry
Pack: Quick-dry fabrics, 5 outfits, laundry detergent packets
```

**Example 2: 3-Day Business Trip**
```
Trip too short: Laundry not practical
Suits difficult to wash/dry quickly
Recommendation: ❌ Pack full wardrobe (3 days only)
```

**Example 3: 14-Day Backpacking, Hostels**
```
WITHOUT: 14 days = 7kg clothes
WITH: 5 days + laundry every 4 days = 2.5kg + $30 laundry

Laundry Days: 4, 8, 12
Savings: 4.5kg (huge for backpacking!)
Recommendation: ✅ Essential for pack weight
Notes: Hostels often have coin laundry, pack clothesline
```

**Example 4: 7-Day Humid Tropics**
```
Base plan: 4 days clothes + laundry day 4
Adjustment: +1 day buffer (slow drying)
= Pack 5 days, wash once on day 4
Result: 5 days clothes for 7-day trip (30% reduction)
Note: Clothes may take 24+ hours to dry in 80% humidity
```

## Decision Matrix

| Trip Length | Laundry Worthwhile? | Recommended Schedule |
|-------------|---------------------|----------------------|
| 1-4 days | ❌ No | Pack full wardrobe |
| 5-7 days | ⚖️ Maybe | Mid-trip (day 3-4) |
| 8-14 days | ✅ Yes | Every 4-5 days |
| 15+ days | ✅ Essential | Every 3-5 days |

Exceptions:
- **Business/formal**: Less practical (suits/dresses)
- **Luxury travel**: Hotel service available but expensive
- **Adventure/backpacking**: Highly recommended (weight critical)
- **Family with kids**: More frequent (kids get dirty)

## Laundry Types Comparison

**Coin Laundry / Laundromat:**
- Cost: $5-10 per load
- Time: 2-3 hours (wash + dry)
- Effort: Medium (need to go there, wait)
- Best for: Budget travel, casual clothes

**Hotel Laundry Service:**
- Cost: $15-30 per load (more expensive)
- Time: 24-48 hours (overnight service)
- Effort: Low (drop off, pick up)
- Best for: Business travel, convenience

**Self-Service in Accommodation:**
- Cost: $0-5 (sometimes free)
- Time: 2-3 hours
- Effort: Low (in building)
- Best for: Apartments, hostels, campgrounds

**Sink Washing:**
- Cost: $0 (free)
- Time: Overnight drying
- Effort: Medium (manual washing)
- Best for: Underwear/socks, emergency, very budget

## Packing Additions for Laundry Strategy
```
Required:
- Laundry detergent packets (5-pack, 100g)
- Plastic bags (for dirty clothes transport)

Recommended:
- Clothesline with clips (80g)
- Travel-size stain remover (50ml, 60g)
- Mesh laundry bag (keeps items together in machines)

For Sink Washing:
- Biodegradable soap bar (100g)
- Microfiber towel (for wringing/rolling to remove water)
```

## Best Practices
- ✅ Plan laundry days in itinerary (downtime days)
- ✅ Pack quick-dry fabrics (dry in 12 hours vs. 24+ for cotton)
- ✅ Bring detergent (cheaper than buying on-site)
- ✅ Do laundry before last 2 days (allow drying time)
- ✅ Wash mid-trip so clean clothes for return flight
- ✅ Check accommodation laundry options when booking
- ❌ Don't assume laundry always available (research first)
- ❌ Don't plan laundry on very humid days (won't dry)
- ❌ Don't wash suits/formal wear in machines (dry clean only)

## Integration
- Works with: Destination Research (laundry availability & cost)
- Works with: Budget Calculator (cost comparison)
- Works with: Weight Calculator (weight savings)
- Informs: Clothing quantities (can pack 50% less)

## Pro Tips
1. **Pack dark colors**: Show less dirt, need washing less often
2. **Merino wool**: Can wear 2-3 times before washing, naturally antimicrobial
3. **Reversible clothing**: Wear inside-out for "clean" look
4. **Wash overnight**: Clothes have all night to dry
5. **Humidity check**: In very humid climates, add extra drying day
6. **Coin supply**: Keep coins/quarters for coin laundry
7. **Clothesline in bathroom**: Hang over shower/tub, use fan
8. **Packing cube strategy**: One cube for clean, one for worn

## Summary
**Key Takeaways:**
- Laundry is practical for trips 7+ days
- Can reduce clothing by 30-50%
- Saves weight and luggage space
- Usually costs $10-30 total
- Much cheaper than extra baggage fees ($100+)
- Best for casual clothes, less practical for formal
- Plan laundry days into itinerary
- Pack quick-dry fabrics and minimal detergent

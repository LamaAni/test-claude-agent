# Weight Calculator Skill
## Purpose
Calculate total packing weight, distribution across bags and travelers, and verify airline compliance.

## When to Use
- After creating packing list
- To verify airline limit compliance
- To identify overweight situations
- For multi-traveler coordination

## Input
- Packing list with item weights (from item database)
- Number of travelers
- Airline weight limits
- Luggage empty weights

## Calculation Process

### Step 1: Sum Item Weights by Category
```
Clothing: Sum all clothing items
Toiletries: Sum all toiletry items
Electronics: Sum electronics
Activity Gear: Sum gear
Miscellaneous: Sum misc
```

### Step 2: Calculate Per Traveler
For multi-traveler trips:
- Adult 1 items + shared items proportion
- Adult 2 items + shared items proportion  
- Child items distributed appropriately

### Step 3: Add Luggage Weight
- Empty carry-on: ~2-3kg
- Empty medium checked: ~4kg
- Empty large checked: ~5-6kg
- Backpack: ~0.5-1kg

### Step 4: Compare to Limits
```
Bag 1 Total: [Items + Luggage] kg
Airline Limit: [23kg typical]
Status: [Under by Xkg / Over by Xkg]
```

### Step 5: Calculate Buffer
Recommend staying 2-3kg under limit for:
- Safety margin
- Souvenirs on return
- Scale variations

## Output Format
```
⚖️ WEIGHT ANALYSIS

TOTAL PACKED ITEMS: [X.X kg]

BY CATEGORY:
• Clothing: [X.X kg] ([Y]%)
• Toiletries: [X.X kg] ([Y]%)
• Electronics: [X.X kg] ([Y]%)
• Activity Gear: [X.X kg] ([Y]%)
• Miscellaneous: [X.X kg] ([Y]%)

BY TRAVELER:
• Person 1: [X.X kg]
• Person 2: [X.X kg]
• Shared: [X.X kg]

LUGGAGE BREAKDOWN:
Checked Bag 1: [X.X kg items] + [Y kg bag] = [Z kg total]
- Airline Limit: 23 kg
- Status: ✅ [Under by X kg] / ⚠️ [At limit] / ❌ [Over by X kg]

Carry-On: [X.X kg items] + [Y kg bag] = [Z kg total]
- Airline Limit: [10 kg or No limit]
- Status: ✅

COMPLIANCE: [✅ All bags compliant / ⚠️ Close to limits / ❌ Over limits]

RECOMMENDATIONS:
• [Remove X kg to stay comfortably under limit]
• [Redistribute Y kg from Bag 1 to Bag 2]
• [Buffer of Z kg available for souvenirs]
```

## Examples
**Single Traveler, Carry-On Only:**
```
Total Items: 7.2 kg
Carry-on bag: 2.5 kg
Total: 9.7 kg

Airline limit (7kg typical): ⚠️ Over by 2.7kg
Solution: Move 3kg to personal item (laptop bag)
Result: 6.7kg carry-on, 3kg personal item ✅
```

**Family of 4, 2 Checked Bags:**
```
Total items: 60 kg
2 checked bags: 2×5kg = 10kg
Total: 70 kg

Bag 1: 32kg + 5kg = 37kg ❌ Over limit by 14kg
Bag 2: 28kg + 5kg = 33kg ❌ Over limit by 10kg

Solution: Redistribute + consider rentals
- Rent camping gear (save 15kg)
- Move kids' items to their backpacks (save 5kg)
Result: 25kg per bag ✅
```

## Best Practices
- ✅ Calculate for all bags, not just checked
- ✅ Include luggage empty weight (often forgotten!)
- ✅ Build in 2-3kg buffer
- ✅ Provide solutions if over limit
- ✅ Consider distribution across multiple bags
- ❌ Don't forget personal item weight
- ❌ Don't pack to exact limit (risky)

## Integration
- Uses: Item Database (weights)
- Works with: Airline Lookup (limits)
- Informs: Luggage Recommender (size needs)
- Connects to: Budget Calculator (fees if overweight)

# Luggage Recommender Skill
## Purpose
Match packing needs to appropriate luggage types based on trip length, activities, weight, and transportation.

## When to Use
- After determining total volume/weight needed
- When user asks for luggage advice
- To optimize luggage choice for trip type

## Input
- Total volume needed (liters)
- Total weight (kg)
- Trip length (days)
- Activities (business, adventure, beach)
- Transportation (car, public transit, flights)
- Airline restrictions
- Budget level

## Recommendation Process

### Step 1: Determine Capacity Needed
```
Short trip (1-3 days): 20-40L
Week trip (4-7 days): 40-70L
Long trip (8-14 days): 70-95L
Extended (15+ days): 95L+
```
Adjust for:
- Winter/bulky clothes: +30%
- Activities gear: +20-40%
- Business attire: +15%
- Laundry access: -30%

### Step 2: Consider Constraints
- Airline carry-on limits
- Weight distribution (multiple bags vs. one large)
- Traveler capability (elderly, children)
- Transport method (stairs, public transit, car)

### Step 3: Match to Luggage Types
From luggage database:
- Size/weight match
- Use case alignment
- Price point for budget
- Features needed

### Step 4: Provide Options
- Primary recommendation
- Alternative option
- Budget option
- Premium upgrade option

## Output Format
```
🧳 LUGGAGE RECOMMENDATIONS
Capacity Needed: ~[X] liters
Weight to Pack: ~[Y] kg

PRIMARY RECOMMENDATION:
[Luggage Type]
- Capacity: [X]L
- Empty weight: [Y]kg
- Dimensions: [measurements]
- Best for: [Use cases]
- Price range: $[X-Y]
- Why: [Rationale]

ALTERNATIVE:
[Another option]
- [Brief specs]
- Why: [When to choose this instead]

BUDGET OPTION:
[Cheaper option]
- [Brief specs]
- Trade-offs: [What you give up]

UPGRADE OPTION:
[Premium option]
- [Brief specs]
- Benefits: [Extra features]

SPECIFIC TO YOUR TRIP:
• [Recommendation 1]
• [Consideration 2]
```

## Examples
**3-Day Business Trip (Carry-On Only):**
```
Recommended: International Carry-On (40L)
- Fits suits with garment sleeve
- 55×40×20cm compliant
- 2.5kg empty weight
- $100-250
Why: Professional appearance, overhead bin compatible, no baggage wait

Alternative: Garment bag with wheels
- Keeps suits wrinkle-free
- May need to check on smaller planes
```

**7-Day Beach Vacation:**
```
Recommended: Medium Checked Suitcase (65L)
- Plenty of room for beach clothes
- 66×45×28cm
- 4kg empty
- $120-300
Why: Comfortable capacity, within 23kg limit, room for souvenirs

Alternative: Travel Backpack (40L) if minimalist
- Laundry mid-trip
- More versatile
```

## Best Practices
- ✅ Match luggage to trip type
- ✅ Consider user's physical capability
- ✅ Account for return trip (souvenirs)
- ✅ Recommend wheels for most travelers
- ✅ Suggest backpack for adventure/backpacking
- ❌ Don't recommend luggage user can't handle
- ❌ Don't suggest oversized for airline limits

## Integration
- Uses: Luggage Specs Database
- Uses: Weight Calculator (total weight)
- Works with: Airline Lookup (size limits)
- Works with: Budget Calculator (luggage cost)

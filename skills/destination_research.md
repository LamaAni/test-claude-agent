# Destination Research Skill

## Purpose
Research destination-specific logistics including power outlets, water potability, laundry availability, shopping options, and transportation to inform practical packing decisions.

## When to Use
Always for international trips, or domestic trips to unfamiliar regions. Provides practical context for packing recommendations.

## Input Parameters
- **Destination**: City/country
- **Accommodation type**: Hotel, hostel, Airbnb, camping (affects laundry access)
- **Trip length**: Affects whether laundry is needed

## Research Areas

### 1. Power & Electronics
**Look up:**
- Outlet type (A, B, C, etc.)
- Voltage (110V vs. 220V)
- Frequency (50Hz vs. 60Hz)
- Multiple outlet types in country (e.g., UK uses G exclusively)

**Packing Impact:**
- Need adapter? Which type?
- Need voltage converter? (most modern electronics are dual-voltage)
- How many adapters needed?

### 2. Water Potability
**Research:**
- Tap water safe to drink?
- Filtered/boiled water recommended?
- Bottled water only?
- Water for brushing teeth?

**Packing Impact:**
- Reusable water bottle appropriate?
- Need water purification tablets/filter?
- Budget for bottled water purchases?

### 3. Laundry Facilities
**Find out:**
- Laundromats / coin laundry available?
- Hotel laundry service typical cost?
- Self-service at accommodation?
- Average cost per load
- Availability in area (widely available vs. limited)

**Packing Impact:**
- Can reduce clothing quantities if easy laundry access
- Need laundry detergent packets?
- Trip length where laundry makes sense
- Budget impact of laundry vs. packing more clothes

### 4. Shopping Availability
**Assess:**
- Good shopping for basics (toiletries, clothes)?
- What stores are common (pharmacies, supermarkets)?
- Pricing (cheap to buy on-site vs. expensive)?
- Product availability (can find familiar brands?)

**Packing Impact:**
- Pack minimal if great shopping, full kit if limited
- What to buy on arrival vs. pack
- Backup plan if forgot something

### 5. Transportation
**Research:**
- Public transit quality (excellent, good, limited, none)
- Walkability of destination
- Car rental necessary?
- Taxi/rideshare availability
- Luggage handling considerations

**Packing Impact:**
- Wheeled luggage vs. backpack
- Luggage size/weight (will you be carrying up stairs?)
- Number of bags (easier with car vs. public transit)

## Output Format

```markdown
🏙️ DESTINATION LOGISTICS
Location: [Destination]

**Power & Electronics:**
- Outlet Type: [Letter(s)]
- Voltage: [X]V
- Adapter needed: [Yes/No, which type]
- Notes: [Dual voltage devices OK, or need converter]

**Water:**
- Tap water: [Safe / Filter recommended / Bottled only]
- Recommendation: [Bring reusable bottle / Buy bottled]

**Laundry:**
- Availability: [Widely available / Moderate / Limited]
- Type: [Coin laundry / Hotel service / Self-service]
- Cost: ~$[X-Y] per load
- Recommendation: [Plan laundry day X / Pack full wardrobe]

**Shopping:**
- Availability: [Excellent / Good / Moderate / Limited]
- Common stores: [List]
- Pricing: [Cheap / Moderate / Expensive vs. home]
- Pack vs. Buy: [Pack everything / Can buy basics]

**Transportation:**
- Primary: [Subway / Bus / Car / Walk]
- Quality: [Excellent / Good / Limited]
- Luggage consideration: [Easy handling / Challenging stairs/crowds]

**PACKING IMPLICATIONS:**
• Bring [Type X] power adapter
• [Reusable water bottle appropriate / Buy bottled]
• Laundry on Day [X] allows [Y]% less clothing
• [Minimal packing OK - good shopping / Pack everything]
• [Wheeled luggage / Backpack] recommended for transport
```

## Examples

**Tokyo, Japan:**
```
Power: Type A/B, 100V - US devices work
Water: Tap water excellent quality
Laundry: Coin laundry everywhere, ~$5-8/load
Shopping: Exceptional (Don Quijote, convenience stores)
Transit: World-class subway
Pack: Minimal OK, easy to replace forgotten items, wheeled luggage fine
```

**Marrakech, Morocco:**
```
Power: Type C/E, 220V - Need adapter
Water: Bottled only
Laundry: Hotel service, ~$10/load
Shopping: Souks for local items, limited Western products
Transit: Mostly walking/taxis in medina
Pack: Bring all essentials, backpack better for medina navigation
```

## Best Practices
- ✅ Research all 5 areas for complete picture
- ✅ Note cost implications (laundry vs. buying bottled water)
- ✅ Consider transportation when recommending luggage type
- ✅ Account for accommodation amenities
- ❌ Don't assume based on region (varies greatly by city)
- ❌ Don't overlook power adapter (critical for electronics)

## Integration
- Works with: Budget Calculator (laundry costs, buying on-site)
- Works with: Luggage Recommender (transportation considerations)
- Works with: Laundry Optimizer (availability and cost data)

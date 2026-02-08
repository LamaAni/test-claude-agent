# Airline Lookup Skill

## Purpose
Research specific airline baggage policies, allowances, fees, and restrictions to ensure packing recommendations comply with carrier rules.

## When to Use
- When airline is specified by user
- To provide cost estimates for baggage fees
- To determine carry-on vs. checked bag strategy
- When special items are involved (sports equipment, etc.)

## Input Parameters
- **Airline name or code** (e.g., "United" or "UA")
- **Route type**: Domestic, international, region
- **Cabin class**: Economy, business, first
- **Special items**: Surfboard, skis, musical instruments (optional)

## Research Process

### Step 1: Identify Airline and Route
- Look up airline's official baggage policy page
- Note: Policies differ by route (domestic vs. international)
- Check if codeshare affects policy

### Step 2: Gather Carry-On Limits
**Look up:**
- Dimensions (length × width × height in cm and inches)
- Weight limit (if any - many airlines don't have weight limits)
- Personal item dimensions and rules
- Liquid restrictions (typically 100ml per container)

### Step 3: Gather Checked Baggage Info
**Research:**
- Number of bags included by class
- Weight limits per bag (typically 23kg economy, 32kg business)
- Size limits (linear dimensions, typically 158cm)
- Fees for additional bags
- Overweight fees (23-32kg, 32-45kg tiers)
- Oversized fees

### Step 4: Special Items Research
If applicable, look up:
- Sports equipment policies (skis, surfboards, bikes, golf clubs)
- Musical instrument policies
- Medical device allowances
- Fee structures for special items

## Output Format

```markdown
✈️ AIRLINE BAGGAGE POLICY
Airline: [Name] ([Code])
Route: [Domestic/International]
Class: [Economy/Business/First]

**Carry-On:**
- Dimensions: [X×Y×Z cm] ([X×Y×Z inches])
- Weight limit: [Xkg] or [No limit]
- Personal item: [X×Y×Z cm], must fit under seat

**Checked Baggage ([Class]):**
- Included: [X] bag(s) free
- Weight limit: [X kg / X lbs] per bag
- Size limit: [X cm] linear dimensions
- First bag fee: $[X] (if charged)
- Second bag fee: $[X]
- Overweight (23-32kg): $[X] additional
- Overweight (32-45kg): $[X] additional
- Oversized (>158cm): $[X] additional

**Special Notes:**
- [Any airline-specific quirks]
- [Budget airline stricter enforcement]
- [Premium cabin benefits]

**PACKING IMPLICATIONS:**
• Comply with [X kg] limit per bag
• Buffer of [X kg] recommended (don't pack to exact limit)
• [Carry-on only viable / requires checked bag]
• Estimated baggage fees: $[X] for planned luggage
```

## Examples

**Example: United Airlines, Economy, International**
```
✈️ United Airlines (UA) - International Economy

Carry-On: 56×35×22cm, no weight limit
Personal item: 43×25×22cm
Checked: 1 bag free (23kg), $150 for 2nd bag
Overweight 23-32kg: +$100, 32-45kg: +$200

IMPLICATIONS:
• Pack to 22kg per bag (1kg buffer below 23kg limit)
• Carry-on has no weight limit - maximize use
• Second bag expensive ($150) - avoid if possible
```

**Example: Ryanair (Budget Carrier)**
```
✈️ Ryanair (FR) - European Budget

Carry-On: Small bag (40×20×25cm) free, must fit under seat
Priority bag: 55×40×20cm, 10kg, requires priority boarding (€6-30)
Checked: 10kg bag €12-60, 20kg bag €20-70 (varies greatly by booking time)

IMPLICATIONS:
• Very strict enforcement - size checked at gate
• Pack light or pay significant fees
• Book bags online (much cheaper than airport)
• Consider ultra-minimalist packing strategy
```

## Best Practices
- ✅ Always look up specific airline (policies vary greatly)
- ✅ Check official airline website (most current info)
- ✅ Note booking class differences
- ✅ Account for route type (domestic vs. international)
- ✅ Warn about budget carrier strict enforcement
- ✅ Calculate total fees for user's planned luggage
- ❌ Don't assume generic airline policies
- ❌ Don't forget to account for luggage empty weight

## Common Gotchas
- **US domestic:** Most charge for 1st bag ($30-35)
- **International:** Usually 1 free bag
- **Budget carriers:** Often charge for everything
- **Weight creep:** Luggage itself weighs 2-5kg
- **Oversized:** Even 1cm over can trigger $100+ fee

## Integration
- Works with: Budget Calculator (fee estimates)
- Works with: Luggage Recommender (size/weight matching)
- Informs: Total weight targets, carry-on feasibility

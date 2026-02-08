# Autonomous Lookup Rules

## Purpose
This document defines when and how the Packing Advisor agent should proactively research information without requiring the user to provide it explicitly.

## Core Principle
**"You provide the basics, I'll research the rest"**

The agent should minimize the burden on users by automatically gathering all relevant contextual information needed to make informed packing recommendations.

## When to Perform Autonomous Lookups

### Always Lookup (Required)
1. **Weather/Climate Data**
   - Lookup: Temperature ranges, precipitation probability, humidity levels, UV index
   - When: User provides destination and dates
   - Why: Essential for appropriate clothing and gear recommendations

2. **Cultural Norms**
   - Lookup: Dress codes, religious site requirements, local customs
   - When: Destination is in a different cultural region
   - Why: Prevents inappropriate packing that could cause issues

3. **Airline Policies** (if airline mentioned or can be inferred)
   - Lookup: Baggage dimensions, weight limits, fees, restrictions
   - When: Airline is specified or common route is known
   - Why: Ensures compliance and helps avoid unexpected costs

### Lookup When Relevant (Conditional)

4. **Destination Logistics**
   - Lookup: Power outlets, water potability, laundry availability, shopping options
   - When: International travel or significant cultural differences
   - Why: Affects what to pack vs. buy on-site

5. **Activity Requirements**
   - Lookup: Gear needs, difficulty levels, safety equipment
   - When: User mentions specific activities (hiking, diving, skiing, etc.)
   - Why: Specialized gear requirements vary significantly

6. **Health & Safety**
   - Lookup: Required vaccinations, recommended medications, travel advisories
   - When: Travel to regions with specific health concerns
   - Why: Critical for traveler safety and wellbeing

7. **Seasonal Events**
   - Lookup: Festivals, holidays, peak seasons, special events
   - When: Travel dates align with potential seasonal variations
   - Why: May affect crowd levels, dress requirements, or packing needs

## Data Source Priority

### Primary Sources (Most Reliable)
1. Official weather services and climate data repositories
2. Government travel advisories and health organizations
3. Official airline websites and policy documents
4. Official tourism boards and destination websites

### Secondary Sources (Supplementary)
1. Reputable travel guides and aggregators
2. Recent traveler reports and reviews
3. Cultural sensitivity guides from educational institutions
4. Industry standard references (e.g., CDC, WHO for health)

### Tertiary Sources (Context Only)
1. Social media trends and recommendations
2. Blog posts and personal travel accounts
3. General knowledge databases

## How to Handle Missing or Unavailable Data

### If Critical Data is Unavailable
1. **State clearly** what could not be found
2. **Provide fallback recommendations** based on:
   - Regional/seasonal averages
   - Similar destinations
   - Conservative assumptions
3. **Mark assumptions explicitly** in the output
4. **Recommend user verification** for critical items

### If Secondary Data is Unavailable
1. **Proceed without it** if not essential
2. **Note the limitation** briefly
3. **Provide general guidance** where applicable

## How to Present Research Findings

### Research Summary Section
Always include a dedicated section showing:
```
🔍 RESEARCH CONDUCTED
✓ Weather: [Source] - [Key findings]
✓ Cultural Norms: [Source] - [Key findings]
✓ Airline Policies: [Source] - [Key findings]
✓ Destination Logistics: [Source] - [Key findings]
⚠ [Item]: Could not verify - Using [fallback approach]
```

### Transparency Requirements
- **Show what was looked up**: List all research areas
- **Cite sources generically**: "Weather data from national meteorological service"
- **Indicate confidence**: Use ✓ for confirmed, ⚠ for assumed/fallback
- **Explain gaps**: Briefly note what couldn't be verified

### Integration into Recommendations
- Reference research findings when making specific recommendations
- Example: "Based on expected highs of 30°C and 70% humidity..."
- Example: "Given the conservative dress code at religious sites..."

## When to Ask Users vs. Lookup Autonomously

### Ask the User
- Personal preferences (packing style, comfort priorities)
- Specific medical needs or conditions
- Budget constraints (unless explicitly stated)
- Accommodation details (unless critical for decision)
- Activity participation level (casual vs. intensive)
- Special events they plan to attend

### Lookup Autonomously
- Factual destination information
- Standard requirements (visas, vaccinations)
- Climate and weather patterns
- Cultural norms and expectations
- General activity requirements
- Transportation and airline policies

## Validation Rules for Looked-Up Data

### Weather Data Validation
- Dates must be within reasonable forecast range (use historical averages for far-future dates)
- Temperature, precipitation, and humidity should align regionally
- Flag unusual patterns for user awareness

### Cultural Data Validation
- Cross-reference multiple sources for cultural norms
- Prioritize official or governmental sources
- Note regional variations within countries

### Airline Data Validation
- Verify currency of policy (check "last updated" dates)
- Note class-specific variations (economy, business, first)
- Include international vs. domestic differences
- Verify specific route restrictions

### Destination Data Validation
- Confirm current accuracy (political changes, infrastructure updates)
- Note seasonal variations
- Verify for specific regions within countries

## Fallback Strategies When Lookups Fail

### Weather Lookup Fails
1. Use historical climate data for the region and season
2. Reference climate zone general characteristics
3. Build in versatility (layers, adaptable items)
4. State: "Based on typical [season] conditions in [climate zone]"

### Cultural Lookup Fails
1. Default to conservative recommendations
2. Apply regional cultural patterns
3. Recommend versatile, respectful attire
4. Suggest: "Research local customs before visiting [specific sites]"

### Airline Lookup Fails
1. Use common industry standards (e.g., 23kg checked, 7kg carry-on)
2. Recommend checking with specific airline before travel
3. Suggest conservative packing to stay within typical limits
4. Note: "Verify current baggage policies with your airline"

### Destination Logistics Lookup Fails
1. Assume moderate availability of basics
2. Recommend packing essentials
3. Suggest: "Confirm [specific need] availability at accommodation"

## Error Handling Approaches

### When Data Conflicts
- Present the most conservative option
- Note the discrepancy: "Sources vary on [item]; recommending [safer option]"
- Suggest user verification if critical

### When Data is Outdated
- State the data age if known: "Most recent data from [time period]"
- Recommend user verification for time-sensitive information
- Provide general guidance: "Policies may have changed; verify before travel"

### When Data is Ambiguous
- Interpret conservatively
- Provide both interpretations if significantly different
- Recommend: "If in doubt, [safer approach]"

## Autonomous Lookup Workflow

1. **Parse User Input**: Extract destination, dates, travelers, purpose
2. **Identify Required Lookups**: Based on input and trip type
3. **Execute Lookups in Parallel**: Gather all necessary data
4. **Validate Results**: Cross-check and verify data consistency
5. **Apply Fallbacks**: For any failed lookups
6. **Synthesize Findings**: Integrate into coherent recommendation framework
7. **Present Transparently**: Show what was researched and found
8. **Generate Recommendations**: Based on research and rules

## Best Practices

### Do:
- ✅ Look up information proactively without being asked
- ✅ State clearly what was researched and sources used
- ✅ Provide fallback recommendations when data is unavailable
- ✅ Flag assumptions and uncertainties
- ✅ Integrate research findings into specific recommendations
- ✅ Keep research summary concise but informative

### Don't:
- ❌ Make up data or fabricate sources
- ❌ Present assumptions as confirmed facts
- ❌ Skip research because it seems obvious
- ❌ Overwhelm users with excessive research details
- ❌ Ignore gaps in data without acknowledging them
- ❌ Apply outdated information without noting the age

## Examples

### Good Autonomous Lookup
```
🔍 RESEARCH CONDUCTED
✓ Weather: Bangkok in July - Monsoon season, 28-32°C, 80% humidity, daily rain likely
✓ Cultural Norms: Thailand - Conservative dress at temples (shoulders/knees covered), removed footwear
✓ Airline: Thai Airways - 30kg checked (2 bags), 7kg carry-on, 56x45x25cm
✓ Destination: Bangkok - 220V power (Type A/B/C), tap water not potable, laundry widely available
```

### Good Fallback Communication
```
⚠ Airline Policy: Specific airline not provided. Using standard international limits (23kg checked, 7kg carry-on). Verify with your carrier before travel.
```

### Good Integration into Recommendations
```
💧 Rain Gear (Essential)
   - Compact travel umbrella (200g)
   - Lightweight rain jacket (300g)
   
   Why: July is peak monsoon season with daily afternoon showers expected.
```

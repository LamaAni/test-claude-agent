# Weather Lookup Skill

## Skill Purpose
Autonomously research weather and climate conditions for a destination during specified travel dates to inform appropriate packing recommendations.

## When to Use This Skill
- **Always** for every packing request
- Before making any clothing or gear recommendations
- When destination and travel dates are provided
- For both near-term (forecasts) and far-future trips (historical averages)

## Input Parameters

### Required
- **Destination**: City/region name
- **Country**: For disambiguation
- **Travel Dates**: Start and end date, or month/season
- **Coordinates** (optional): Latitude/longitude for precise location

### Optional
- **Activities**: Hiking, beach, skiing (affects detail level needed)
- **Accommodation type**: Hotel vs. camping (affects microclimate)

## Step-by-Step Process

### Step 1: Determine Forecast vs. Historical Data

**If travel dates are within 14 days:**
- Use current weather forecasts
- Sources: OpenWeatherMap, AccuWeather, Weather.com
- Confidence: High (70-90% accuracy)

**If travel dates are 15+ days away:**
- Use historical climate averages for the month
- Sources: Weatherbase, climate-data.org, Wikipedia climate tables
- Confidence: Moderate (based on historical patterns)
- **Note to user:** "Specific forecasts aren't available this far ahead. Based on typical [month] weather..."

### Step 2: Gather Core Weather Data

**Temperature:**
- Daily high and low (°C and °F)
- "Feels like" temperature (heat index or wind chill)
- Temperature trends (warming or cooling during trip)
- Nighttime temperatures (for camping/outdoor activities)

**Precipitation:**
- Chance of precipitation (%)
- Expected amount (mm or inches per day)
- Type (rain, snow, mixed)
- Pattern (scattered vs. all-day, monsoon season)

**Humidity:**
- Relative humidity percentage (%)
- Impact on comfort and clothing choices

**UV Index:**
- Daily UV index (0-11+ scale)
- Critical for sun protection recommendations

**Wind:**
- Average wind speed (km/h or mph)
- Wind chill factor if cold

### Step 3: Research Seasonal Patterns

**Look up:**
- Typical season (dry, wet, monsoon, hurricane)
- Historical weather patterns for the month
- Microclimates (coastal vs. inland, altitude effects)
- Day length (sunrise/sunset times)

**Sources:**
- National weather services
- Tourism board websites
- Climate data aggregators

### Step 4: Cross-Check and Validate

**Validation steps:**
1. Check 2-3 sources for consistency
2. Compare to historical averages (is forecast typical?)
3. Look for weather warnings or unusual patterns
4. Note any El Niño / La Niña effects

**Red flags:**
- Temperature 10°C+ different from normal → Investigate further
- Extreme weather warnings → Note to user, consider trip timing
- Conflicting data between sources → Use conservative estimate

### Step 5: Interpret for Packing

**Translate data to packing needs:**

**Temperature → Clothing Weight**
- <0°C: Heavy winter gear
- 0-10°C: Layering system, warm jacket
- 10-20°C: Light layers, long and short sleeve mix
- 20-30°C: Summer clothes, shorts, t-shirts
- >30°C: Minimal, breathable clothing

**Precipitation → Rain Gear**
- 10-30% chance: Light umbrella optional
- 30-60% chance: Rain jacket recommended
- >60% chance: Full rain gear essential

**Humidity → Fabric Choice**
- <40%: Any fabrics
- 40-60%: Standard
- 60-80%: Quick-dry, breathable
- >80%: Moisture-wicking only, pack extras

**UV → Sun Protection**
- 0-2: Minimal
- 3-5: Sunscreen for extended outdoor time
- 6-7: Sun protection important
- 8-10: Extra precautions, seek shade
- 11+: Maximum protection critical

## Output Format

### Weather Research Summary Template

```markdown
🌡️ WEATHER & CLIMATE RESEARCH
Destination: [City, Country]
Travel Dates: [Dates] ([X] days)
Data Source: [Forecast / Historical Average for [Month]]

**Temperature:**
- Daytime: [X-Y]°C ([X-Y]°F) - [Description: hot/warm/mild/cool/cold]
- Nighttime: [X-Y]°C ([X-Y]°F)
- Feels Like: [Consider humidity/wind effects]

**Precipitation:**
- Chance: [X]% per day
- Amount: [X]mm per day typical
- Pattern: [scattered showers / all-day rain / dry season]

**Humidity:**
- Average: [X-Y]% - [low/moderate/high/extreme]
- Impact: [comfortable / sticky / very uncomfortable]

**UV Index:**
- Level: [X-Y] - [low/moderate/high/very high/extreme]
- Protection needed: [none/basic/significant/maximum]

**Additional Factors:**
- Daylight hours: [sunrise to sunset times]
- Altitude: [elevation in meters, if relevant]
- Seasonal notes: [monsoon, dry season, etc.]

**PACKING IMPLICATIONS:**
• [Temperature-based clothing recommendations]
• [Rain gear recommendations]
• [Sun protection requirements]
• [Fabric preferences based on humidity]
• [Layering strategy]
• [Special considerations]
```

## Examples

### Example 1: Near-Term Beach Trip

**Input:**
- Destination: Cancun, Mexico
- Dates: June 15-22, 2026 (7 days)

**Process:**
1. Within 14 days → Use forecast
2. Look up AccuWeather or OpenWeatherMap
3. Gather data: 28-32°C, 70% humidity, 20% rain chance, UV 10
4. Cross-check with Weather.com → Consistent
5. Interpret: Hot and humid, minimal rain, extreme sun

**Output:**
```
🌡️ WEATHER RESEARCH
Cancun: June 15-22, 2026

Temperature: 28-32°C (82-90°F) - Hot
Humidity: 70% - High (sticky, uncomfortable)
Precipitation: 20% chance, <5mm - Low (brief afternoon showers possible)
UV Index: 10 - Extreme

PACKING IMPLICATIONS:
• Light, breathable cotton or linen clothing
• SPF 50+ sunscreen essential, reapply every 2 hours
• Wide-brimmed hat and UV sunglasses critical
• Minimal rain gear (light jacket or umbrella sufficient)
• Quick-dry fabrics preferred (humidity means clothing takes longer to dry)
• Pack extra tops (sweating in humidity requires more changes)
```

### Example 2: Far-Future Mountain Trip

**Input:**
- Destination: Chamonix, France (Alps)
- Dates: December 2026 (specific dates TBD)
- Activity: Skiing

**Process:**
1. Beyond 14 days → Use historical averages
2. Look up climate-data.org for Chamonix December averages
3. Gather: -5 to 5°C, 40% humidity, 15 days precipitation, UV 2
4. Note: High altitude increases UV, colder at ski elevations
5. Interpret: Cold, snowy, winter sports conditions

**Output:**
```
🌡️ CLIMATE DATA (Historical Average)
Chamonix: December (typical conditions)

Note: Specific forecasts not available this far ahead. Based on historical December averages.

Temperature: -5 to 5°C (23-41°F) at town level
- Higher elevations (ski areas): -10 to -5°C (14-23°F)
- Wind chill can make it feel 5-10°C colder
Humidity: 40% - Moderate (dry cold)
Precipitation: 15 days with snow, 100-150mm total
UV Index: 2-3 at town, 5-6 at high altitude (snow reflects UV)

PACKING IMPLICATIONS:
• Full winter gear: thermal base layers, insulated mid-layers, waterproof shell
• Ski-specific clothing (ski jacket, pants, gloves, goggles)
• Multiple layers for temperature regulation
• Warm accessories: hat, neck gaiter, hand/foot warmers
• Sunscreen SPF 30+ (UV stronger at altitude + snow reflection)
• Lip balm with SPF (dry cold + UV)
• Moisture-wicking fabrics (avoid cotton, use wool/synthetics)

Recommendation: Check forecast 1-2 weeks before trip for adjustments.
```

## Error Handling

### When Weather Data Is Unavailable

**Scenario 1: Small/Remote Destination**
- **Fallback:** Use data from nearest major city or regional averages
- **Note to user:** "Specific data for [small town] limited. Using [nearby city] as proxy, which is [X] km away in same region."

**Scenario 2: Very Far Future (12+ months)**
- **Fallback:** Seasonal/monthly historical averages only
- **Note to user:** "For trips this far ahead, recommendations based on typical seasonal patterns. Weather can vary significantly. Check forecast 2 weeks before travel."

**Scenario 3: Unusual Weather Pattern**
- **Action:** Note the anomaly
- **Note to user:** "Current forecasts show unusual [heat wave / cold snap / storm system]. This is [X]°C [above/below] normal for [month]. Recommendations account for this."

### When Data Conflicts

**Multiple sources show different information:**
1. **Prioritize:** Official government meteorological services > Major weather services > Aggregators
2. **Use conservative:** Pack for worst-case scenario
3. **Note to user:** "Sources vary slightly. Recommendations use conservative estimates to ensure preparedness."

## Best Practices

### ✅ Do This:
- Always look up weather, never assume
- Use multiple sources for important trips
- Note data source and confidence level in output
- Explain packing implications clearly
- Consider altitude, coastal vs. inland, urban heat island effects
- Check for weather warnings or unusual patterns
- Recommend rechecking forecast closer to trip

### ❌ Avoid This:
- Never guess weather without research
- Don't ignore humidity (significantly affects comfort)
- Don't forget UV index (critical for sun destinations)
- Don't overlook nighttime temperatures (camping, outdoor activities)
- Don't assume "tropical = always hot" (mountains, seasons vary)
- Don't provide false precision (e.g., "26.3°C" when using historical averages)

## Integration with Other Skills

**Weather Lookup connects to:**
- **Cultural Research:** Modest dress may be harder in hot weather
- **Activity Research:** Weather affects gear needs (rain gear for wet climate hiking)
- **Budget Calculator:** Rental vs. pack decisions (rent snow gear if unsure of conditions)
- **Laundry Optimizer:** Humid weather may require more frequent clothing changes

## Quick Reference: Weather to Packing

| Temperature | Primary Clothing | Layers |
|-------------|------------------|--------|
| <0°C | Heavy winter gear | 3-4 layers |
| 0-10°C | Warm clothes, jacket | 2-3 layers |
| 10-20°C | Mix long/short sleeve | 1-2 layers |
| 20-30°C | Summer clothes | 0-1 layer |
| >30°C | Minimal, breathable | No layers |

| Precipitation | Rain Gear |
|---------------|-----------|
| <30% chance | Optional light umbrella |
| 30-60% chance | Rain jacket + umbrella |
| >60% chance | Full rain gear (jacket, pants, waterproof shoes) |

| UV Index | Sun Protection |
|----------|----------------|
| 0-2 | Optional |
| 3-5 | Sunscreen for extended time outdoors |
| 6-7 | Sunscreen, hat, sunglasses |
| 8-10 | Full sun protection, seek shade |
| 11+ | Maximum protection, minimize midday exposure |

## Summary

**Key Takeaways:**
1. **Always research** - Never skip weather lookup
2. **Use forecasts** within 14 days, **historical data** beyond
3. **Cross-check** multiple sources
4. **Interpret** data into actionable packing recommendations
5. **Be transparent** about data sources and confidence
6. **Consider** all factors (temp, rain, humidity, UV, wind)
7. **Account for** altitude, location, and seasonal patterns

**Remember:** Weather is the foundation of good packing advice. Invest time in thorough research!

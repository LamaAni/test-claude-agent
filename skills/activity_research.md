# Activity Research Skill
## Purpose
Determine activity-specific packing requirements based on planned or typical destination activities.

## When to Use
- User specifies activities (hiking, skiing, snorkeling, business conference)
- Destination has typical activities (beach destination = swimming)
- Trip purpose implies activities (business trip = professional attire)

## Input
- Destination
- Stated activities or trip purpose
- Activity level (beginner, intermediate, advanced)
- Duration of activity within trip

## Process
1. **Identify Activities**: From user input or infer from destination/purpose
2. **Research Requirements**: Gear, clothing, safety equipment for each activity
3. **Level Appropriateness**: Beginner needs less specialized gear
4. **Rental vs. Pack**: Heavy/bulky items better rented?
5. **Safety Considerations**: Required safety equipment

## Output
```
🎯 ACTIVITY REQUIREMENTS
Activities: [List]

[Activity 1]:
- Gear needed: [Items]
- Clothing: [Specific needs]
- Safety: [Equipment]
- Rent vs. Pack: [Recommendation]
- Cost: [Rental/purchase estimate]

PACKING ADDITIONS:
• [Item 1 with weight]
• [Item 2 with weight]
```

## Examples
**Snorkeling (Beginner):**
- Gear: Snorkel mask optional (can rent)
- Clothing: Rash guard for sun, water shoes
- Safety: None additional
- Rent mask on-site: $10/day
- Pack: Water shoes (250g), rash guard (180g)

**Business Conference:**
- Gear: Laptop, business cards, notebook
- Clothing: 2-3 business suits, formal shoes
- Safety: None
- Pack: Professional attire (8-10kg)

## Best Practices
- ✅ Recommend rentals for heavy, specialized gear
- ✅ Include safety equipment (helmet for biking, etc.)
- ✅ Consider skill level (beginners need less)
- ❌ Don't assume user owns specialized equipment
- ❌ Don't forget clothing appropriate for activity

# Health & Safety Lookup Skill
## Purpose
Research health requirements, vaccinations, safety concerns, and medical preparations for destination.

## When to Use
- All international trips
- Destinations with health risks (malaria, altitude, etc.)
- When user has medical conditions
- Remote/adventurous destinations

## Research Areas
1. **Required Vaccinations**: Yellow fever, etc. (needed for entry)
2. **Recommended Vaccinations**: Hep A/B, typhoid, etc.
3. **Disease Risks**: Malaria, dengue, Zika, COVID
4. **Altitude Considerations**: Above 2500m
5. **Food/Water Safety**: Traveler's diarrhea risk
6. **Medical Facilities**: Quality and availability
7. **Travel Insurance**: Recommended coverage
8. **Safety Concerns**: Crime, natural disasters, political stability

## Sources
- CDC Travel Health Notices
- WHO travel advice
- Government travel advisories
- Destination health departments

## Output
```
🏥 HEALTH & SAFETY RESEARCH
Destination: [Location]

REQUIRED:
• [Vaccination/document if legally required]

RECOMMENDED:
• [Vaccination 1] - [reason]
• [Vaccination 2] - [reason]

RISKS & PRECAUTIONS:
• [Risk 1]: [Prevention strategy]
• [Risk 2]: [Prevention strategy]

MEDICAL FACILITIES: [Quality level]

PACKING ADDITIONS:
• Prescription malaria prophylaxis (if recommended)
• Insect repellent (DEET 30%+)
• Water purification tablets
• Comprehensive first aid kit
• Travel insurance documents
• Copies of prescriptions

INSURANCE RECOMMENDATION: [Coverage type, estimated cost]
```

## Best Practices
- ✅ Always check official health sites (CDC, WHO)
- ✅ Note time-sensitive items (vaccines take weeks)
- ✅ Include safety beyond just health (crime, etc.)
- ✅ Recommend travel insurance for risky destinations
- ❌ Don't provide medical advice (recommend consulting doctor)

# Event Calendar Lookup Skill
## Purpose
Research seasonal events, festivals, holidays, and peak seasons that might affect packing or travel plans.

## When to Use
- All trips (festivals affect crowds, prices, requirements)
- Specific event-driven travel
- To inform user of opportunities or challenges

## Research
1. **Major Festivals**: Dates, requirements, crowds
2. **Public Holidays**: Closures, crowds
3. **Religious Observances**: Ramadan, Lent, etc.
4. **Peak Tourist Season**: When is busy/expensive
5. **Weather Events**: Hurricane season, monsoon, etc.
6. **Local Events**: Marathons, conferences, etc.

## Output
```
📅 SEASONAL EVENTS & FACTORS
Destination: [Location]
Travel Dates: [Dates]

EVENTS DURING YOUR TRIP:
• [Event 1]: [Dates, impact, recommendations]
• [Event 2]: [Dates, impact]

SEASON: [Peak/Shoulder/Off season]
Impact: [Crowds, prices, availability]

PACKING CONSIDERATIONS:
• [Festival clothing if needed]
• [Book accommodations early - peak season]
• [Expect crowds at attractions]
```

## Examples
**Bali in July:**
- High season (dry, busy)
- No major festivals during dates
- Book ahead, expect crowds
- Standard beach packing

**Munich late September:**
- Oktoberfest (Sept 21 - Oct 6)
- Extremely crowded, expensive
- Traditional dress optional but fun
- Book months ahead

## Best Practices
- ✅ Check tourism board calendars
- ✅ Note if events require special clothing
- ✅ Warn about crowding/pricing impacts
- ❌ Don't assume events repeat yearly (confirm dates)

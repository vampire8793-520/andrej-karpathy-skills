---
name: fixed-envelope-unit-planning
description: Analyze, compare, optimize, and generate 2B2B residential unit floor-plan studies inside an unchanged exterior envelope, with CBC Chapter 11A-informed accessibility checks. Use when the user asks to redesign interior partitions, room organization, kitchens, bathrooms, storage, laundry, doors, furniture, circulation, or accessibility annotations while preserving the shell.
---

# Fixed-envelope 2B2B unit planning

## Purpose

Develop architectural schematic floor-plan options for a 2-bedroom / 2-bathroom multifamily unit while preserving the existing exterior shell exactly. Work as a design-analysis and drawing skill, not an implementation workflow.

## Operating boundary

Default to **analysis + drawing/diagram generation only**.

Do not proactively provide Revit workflows, modeling instructions, construction sequencing, implementation procedures, task lists, execution checklists, or next-step plans unless the user explicitly asks for them.

Make only the changes the user requests. Preserve all unrelated geometry, program, constraints, and design conditions.

## Priority order

When requirements conflict, follow this order:

1. User's explicit current-turn instruction.
2. Fixed exterior envelope and project-source geometry.
3. Required unit program.
4. Accessibility requirements supported by the supplied Chapter 11A source.
5. Residential planning quality and furniture fit.
6. Reference-image planning logic.

Never alter the exterior shell merely to make the interior easier to solve.

## Step 1 — Lock the shell before planning

Before proposing any option, identify and preserve:

- exterior wall locations and footprint;
- exterior recesses and projections;
- balcony / terrace geometry;
- exterior openings unless the user explicitly authorizes a change;
- main unit entry location;
- overall module dimensions.

For the current Sonoma B1 baseline, use `references/sonoma-2b2b-envelope.md`.

If an exact condition cannot be verified from the source drawing, label it as an assumption. Do not fabricate geometry or dimensions.

## Step 2 — Confirm the required program

Unless the user overrides it, keep a true 2B2B unit containing only the requested residential program:

- Primary bedroom.
- Walk-in closet for the primary bedroom.
- Primary bathroom with double sink.
- Bedroom 2 with closet.
- Full shared Bathroom 2.
- Kitchen.
- Dining area.
- Living room.
- Entry cabinet / drop zone for keys, shoes, and coats.
- Laundry.
- Balcony / terrace.
- Storage only where it fits without inventing unrelated rooms.

Do not add offices, dens, pantries, powder rooms, or other spaces unless requested.

## Step 3 — Establish the spatial sequence

Default planning intent:

**Entry → active/public zone → quieter/private bedroom zone**

Prefer:

- entry arriving first into kitchen / dining / living rather than directly into bedrooms;
- kitchen, dining, and living reading as one coherent active zone;
- living room maintaining a strong relationship to the balcony;
- bedroom zone located deeper in the unit and acoustically / visually calmer;
- primary bedroom having stronger privacy than Bedroom 2 where feasible;
- if the user requests it, Primary Bedroom and Bedroom 2 adjacent to each other and oriented toward the balcony;
- Primary Bedroom connected logically to WIC and Primary Bath.

Avoid:

- excessive corridor area;
- dead-end circulation;
- leftover slivers and unusable corners;
- door conflicts;
- furniture creating pinch points;
- oversized rooms that make adjacent spaces dysfunctional.

## Step 4 — Place the public zone first

Study the entry, kitchen, dining, and living relationship before fixing bedroom partitions.

Test kitchen types only when they fit the shell and circulation:

- one-wall;
- L-shaped;
- peninsula;
- island.

Measure aisles between actual cabinet, appliance, island, and furniture faces—not centerlines.

Keep dining chairs and island seating out of the continuous circulation route.

## Step 5 — Place the private zone

Organize both bedrooms at realistic residential proportions and with realistic furniture.

Primary bedroom should include:

- queen or king bed;
- nightstands;
- dresser / media element if space allows;
- usable path to WIC and Primary Bath.

Bedroom 2 should include:

- full or queen bed or another realistic residential arrangement;
- closet;
- usable circulation around furniture.

Do not shrink furniture to force a plan to work.

## Step 6 — Resolve wet core, WIC, laundry, and storage

Use bathroom modules and clearances supported by the supplied toolkit. See `references/chapter-11a-bathrooms.md`.

Primary Bath must retain double sinks unless the user changes that requirement.

Prefer efficient plumbing adjacency when it improves the plan, but do not let plumbing convenience override shell preservation, bedroom functionality, or accessibility.

Place laundry where it remains accessible and does not create a circulation pinch point.

Keep entry storage near the entry and dimension it as real cabinetry / closet depth rather than a symbolic line.

## Step 7 — Accessibility review

Treat the dwelling-unit study primarily as **CBC Chapter 11A residential accessibility**, not generic ADA terminology.

Check at minimum:

- continuous accessible circulation from entry to required common spaces, bedrooms, and bathrooms;
- door clear opening and maneuvering conditions;
- bathroom clear floor spaces;
- kitchen appliance and work-surface approach zones;
- furniture impact on required circulation.

Use approximately **36 in clear circulation** as a schematic planning baseline where the source does not require a larger condition.

Do **not** automatically insert a 60 in turning circle in every room. A turning circle may be used as a supplementary planning check only when relevant; it does not replace the actual Chapter 11A clearances.

Do not invent exact kitchen code dimensions that are not supported by the user's supplied kitchen reference. If the current source set supports only bathroom clearances, state that limitation and show only verified kitchen clearances plus clearly labeled schematic planning assumptions.

## Step 8 — Bathroom rules from the supplied toolkit

Use the project reference in `references/chapter-11a-bathrooms.md` as the first source for bath planning and annotation.

For a tub layout, the supplied toolkit identifies:

- 30 x 60 in bathtub;
- 30 x 48 in clear floor space at the tub;
- water-closet clearance 48 in wide x 36 in in front of fixture, with the toolkit's noted exception;
- lavatory forward and parallel approaches;
- 30 x 48 in clear maneuvering space outside the door swing.

For a shower layout, the supplied toolkit identifies:

- 36 x 60 in shower;
- 36 in wide opening;
- 30 x 48 in clear floor space outside, flush and parallel to the control wall;
- water-closet and lavatory clearances as above;
- 30 x 48 in clear maneuvering space outside the door swing.

Do not replace these with generic ADA diagrams when the user has asked to follow the supplied Chapter 11A toolkit.

## Step 9 — Evaluate before drawing

Before generating the plan, internally verify:

- shell is unchanged;
- unit remains 2B2B;
- no unrequested room has been added;
- primary bath still has double sinks;
- primary bedroom has WIC;
- entry storage and laundry are present;
- public-to-private sequence matches the user's intent;
- major furniture fits at realistic scale;
- bathroom and route clearances do not conflict with doors or furniture;
- dimensions shown are supported by the source or clearly labeled approximate / assumed.

If a proposed concept fails a hard requirement, revise the concept before presenting it.

## Step 10 — Drawing output

When the user requests a drawing, produce an **architectural schematic plan**, not a decorative AI floor-plan illustration.

Show, as applicable:

- fixed exterior walls;
- interior partitions;
- door swings;
- plumbing fixtures;
- kitchen cabinets and appliances;
- furniture;
- room names;
- major dimensions in feet and inches;
- 36 in clear route where relevant;
- bathroom 30 x 48 in clearances;
- WC clear zone;
- tub / shower clear floor space;
- key kitchen approach / aisle checks when supported.

If image generation would distort the fixed shell, prioritize geometric fidelity over visual styling. Do not allow generated dimensions to contradict the source plan.

## Reference-image adaptation

When the user provides a reference plan and says to use it as inspiration:

- study the reference's zoning, adjacency, circulation, and furniture logic;
- adapt those principles to the fixed project envelope;
- never copy the reference envelope over the project shell;
- do not move fixed project openings or entry simply because the reference plan differs;
- keep project program and Chapter 11A requirements authoritative.

## Multi-option studies

When multiple options are requested, make them genuinely different planning concepts rather than minor furniture variations.

Useful distinctions can include:

- centralized wet core;
- split vs. paired bedrooms;
- larger continuous public zone;
- stronger privacy gradient;
- alternate kitchen configuration.

Do not force these categories if a different strategy better matches the user's stated goal.

## Response style

Keep analysis compact and architectural. Focus on geometry, adjacency, circulation, privacy, accessibility, and furniture fit.

Do not add implementation advice or generic "next steps" unless explicitly requested.

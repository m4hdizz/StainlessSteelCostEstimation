# Stainless Steel Cost Estimation Reference Database

AI-ready stainless steel cost estimation database for **oil & gas, petrochemical, mining, and heavy industries**, based on **6,875 product records** with pricing references from publicly accessible online sources.

## Product coverage

The dataset includes a broad range of industrial stainless steel and related products, including:

- **Pipe:** seamless pipe, welded pipe and precut pipe
- **Pipe fittings:** 45° elbows, 90° elbows, short-radius elbows, equal tees, reducing tees, concentric reducers, eccentric reducers, caps, stub ends, nipples, sockets, plugs, adaptors, couplings, unions and Camlock fittings
- **Flanges:** blind, slip-on, weld-neck, socket-weld, threaded, RTJ, ANSI 150/300/600/900/1500 lb, AS 4087, EN 1092 and Table D/E/H flanges
- **Tube and tube fittings:** bends, tees, reducers, crosses, adaptors, compression fittings and related fittings
- **Sheet and plate:** sheet, plate, chequer plate and related flat products
- **Bar and structural sections:** round bar, flat bar, angle bar, square bar, hex bar, hollow bar, channel bar and reo bar
- **Valves and strainers:** ball valves, butterfly valves, check valves, relief valves, sample valves and Y-strainers
- **Hygienic fittings:** BSM, CIP, Triclover ferrules, clamps, unions, liners, caps and seals
- **Manways:** round, oval, rectangular and pressure manways
- **Copper-nickel products:** pipe, elbows, tees, reducers, sockets, nipples, plugs, flanges and caps
- **Balustrade and fabrication fittings:** base plates, covers, glass clamps, rail supports, joiners, post reducers and brackets
- **Other industrial hardware:** wire products, fasteners, marine hardware and related stainless steel components

## Material coverage

The database includes multiple stainless and corrosion-resistant material grades, including:

- 304 / 304L
- 316 / 316L
- 2205 Duplex
- 2507 Super Duplex
- 253MA
- 310
- 321
- 630
- 904L
- 90/10 Copper Nickel

## Cost coverage

The reference data spans a wide variety of:

- Product types
- Material grades
- Nominal sizes
- Schedules and wall thicknesses
- Pressure classes
- Weights
- Unit prices
- AUD/kg cost ranges

This allows the estimator to use exact product pricing where available, or derive a comparable cost using product category, material, size band, weight and specification similarity.

## Estimation features

- Catalog pricing references
- AUD/kg unit rates
- Size-band cost comparison
- Material, size, weight and specification deviation reporting
- Accuracy scoring for non-exact matches
- Exact-match-first estimation logic

The database is intended for engineering budgeting and cost-estimation reference. It is not a supplier quotation.

## How to use with AI

Use this database with **ChatGPT, Claude, or another AI assistant** for stainless steel cost estimation.

### Simple workflow

1. Upload your **Excel file, drawing, PDF, photo, isometric, GA, fabrication drawing, or BOM**.
2. Tell the AI to use this repository as the **primary cost reference**.
3. The AI should:
   - Extract/reconstruct the BOM if needed
   - Use exact catalog matches first
   - Otherwise use the closest defensible AUD/kg reference
   - Report accuracy and major deviations
   - Return the completed estimate as an **Excel file in the first response**
4. If information is missing, the AI should make the best defensible assumption, record it in the output, and continue without asking follow-up questions first.

### Sample prompt

```text
Use the Stainless Steel Cost Estimation Reference Database as the primary pricing source.

Estimate the attached Excel/BOM/drawing.

Rules:
- Extract the BOM first if required.
- Use exact catalog matches where available.
- Otherwise use the closest defensible comparable or AUD/kg rate.
- Preserve the original Excel data.
- Add the estimation results to the right of the original columns.
- Show accuracy and major deviations for non-exact matches.
- Do not invent prices.
- Do not ask follow-up questions before the first estimate.
- Return the completed result as an Excel file in your first response.
```

For the full detailed AI instruction set, use **[PROMPT.md](PROMPT.md)**.


## Files to use with ChatGPT or Claude

For reliable cost estimation, use these two repository files together:

1. **PROMPT.md**: the AI operating instructions.
2. **data/StainlessSteel_AI_Cost_Estimation.md**: the full pricing reference database containing the 6,875 product records, exact catalog prices, weights, AUD/kg rates, grades, sizes, categories and source URLs.

For each actual estimate, also provide the job-specific input such as an Excel BOM, drawing, PDF, photo, isometric or material list.

### Normal chat

At the start of a new ChatGPT or Claude conversation:

1. Upload or attach `PROMPT.md`.
2. Upload or attach `data/StainlessSteel_AI_Cost_Estimation.md`.
3. Upload the job-specific Excel/drawing/PDF/BOM.
4. Ask the AI to follow `PROMPT.md` and use the pricing database as the primary cost reference.

### Project setup

For repeated use, create a dedicated Project in ChatGPT or Claude and add these files to the Project knowledge/files:

- `PROMPT.md`
- `data/StainlessSteel_AI_Cost_Estimation.md`

Then keep the master pricing database and prompt in the Project permanently. For each estimate, upload only the new job-specific Excel, drawing, PDF, photo or BOM to the conversation.

Recommended Project instruction:

```text
Follow PROMPT.md for all cost-estimation work.
Use data/StainlessSteel_AI_Cost_Estimation.md as the primary pricing reference.
When I provide a job file, produce the first-pass estimate immediately and return the completed Excel workbook in the first response.
```

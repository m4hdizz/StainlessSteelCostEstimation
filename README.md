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

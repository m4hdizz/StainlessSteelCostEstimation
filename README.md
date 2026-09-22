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


## How to use with ChatGPT

1. Download or open the Markdown cost database from this repository.
2. Upload the Markdown file to ChatGPT, or provide the repository/file link if your ChatGPT setup can access it.
3. Tell ChatGPT to use the database as the primary pricing reference.
4. Ask for the item you want to estimate, including as much detail as possible:
   - Item type
   - Material grade
   - Size
   - Schedule / wall thickness
   - Pressure class
   - Weight
   - Quantity
5. Require ChatGPT to return:
   - Exact match or closest comparable
   - Reference item/category
   - AUD/kg rate
   - Estimated unit cost
   - Estimated total cost
   - Accuracy score
   - Size, material, weight and specification deviations

### Example ChatGPT prompt

```text
Use the Stainless Steel Cost Estimation Reference Database as the primary cost source.

Estimate the cost of:
8" 316L Sch 40 90° elbow
Weight: 12 kg
Quantity: 4

If there is an exact match, use the exact catalog price.
If there is no exact match, use the closest comparable item or AUD/kg rate.

Return:
- Match level
- Reference item
- Reference AUD/kg
- Estimated unit cost
- Estimated total cost
- Accuracy score
- Size deviation
- Material deviation
- Weight deviation
- Specification deviation

Do not present an estimated value as an exact catalog price.
```

## How to use with Claude

1. Download the Markdown database from this repository.
2. Upload the Markdown file to Claude as a project file or conversation attachment.
3. Instruct Claude to treat the file as the primary cost-estimation reference.
4. Ask for the required component with material, size, specification, weight and quantity.
5. Require Claude to follow the same exact-match-first and deviation-reporting rules.

### Example Claude prompt

```text
Use the attached Stainless Steel Cost Estimation Reference Database as the primary pricing source.

Estimate:
6" 316L Class 150 weld-neck flange
Weight: 8.5 kg
Quantity: 6

Use an exact catalog match if available.
Otherwise use the closest detailed category + grade + size-band rate.

Show:
- Match level
- Reference product/category
- AUD/kg
- Unit cost
- Total cost
- Accuracy score
- Size deviation
- Material deviation
- Weight deviation
- Specification deviation
- Short explanation of the estimate basis

Do not invent a price if the database does not contain a defensible comparable.
```

## Recommended AI instruction

For consistent results in ChatGPT or Claude, use this instruction at the start of the conversation:

```text
Use this database as a cost-estimation reference only.

Priority:
1. Exact catalog match
2. Near-exact product match
3. Detailed category + grade + size-band rate
4. Family + grade + size-band rate
5. Weak comparable only when no better data exists

For every non-exact estimate:
- Report the selected reference
- Report AUD/kg
- Calculate estimated cost
- Give an accuracy score from 0 to 100
- State size, material, weight and specification deviations
- Clearly label the result as an estimate
- Do not invent missing prices
```


## Excel output requirement

When the user provides an Excel file, drawing, PDF, photo, isometric, GA, fabrication drawing, marked-up image, or other BOM source, the AI must **produce the completed Excel estimate in the first response**.

Do not ask follow-up questions before producing the first estimate. Use the best defensible interpretation of the supplied data, make reasonable assumptions where necessary, and clearly record uncertainty in the output.

### Excel structure

For an original Excel workbook:

- Keep all original worksheets unless there is a strong reason not to.
- Keep all original columns unchanged.
- Keep original row/item references where possible.
- Add estimation columns to the **right side of the original data**.
- Do not overwrite the user's source data.
- Avoid duplicate counting when consolidating BOM lines.

Recommended added columns:

- `Match Level`
- `Reference Item`
- `Reference Category`
- `Reference Grade`
- `Reference Size Band`
- `Reference AUD/kg`
- `Estimated Weight kg`
- `Estimated Unit Cost AUD`
- `Quantity`
- `Estimated Total AUD`
- `Accuracy Score`
- `Accuracy Label`
- `Size Deviation %`
- `Material Deviation`
- `Weight Deviation %`
- `Specification Deviation`
- `Estimation Basis`
- `Notes`

If some source fields are missing or unclear, do not stop the workflow. Add the best estimate possible, reduce the accuracy score as required, and explain assumptions in `Notes` / `Estimation Basis`.

The first AI reply should include the resulting Excel workbook as a downloadable file.

### Updated sample prompt

```text
Use the Stainless Steel Cost Estimation Reference Database as the primary cost source.

If I provide an Excel file, drawing, PDF, photo, isometric, GA, fabrication drawing, marked-up image, or BOM:
- First extract/reconstruct the BOM.
- Do not ask follow-up questions before producing the first estimate.
- Use the best defensible assumptions and flag uncertainty.
- Preserve all original Excel columns and data.
- Add estimation columns to the right of the original data.
- Return the completed result as an Excel file in your first response.

For each item, return:
- Match Level
- Reference Item
- Reference Category
- Reference Grade
- Reference Size Band
- Reference AUD/kg
- Estimated Weight kg
- Estimated Unit Cost AUD
- Quantity
- Estimated Total AUD
- Accuracy Score
- Accuracy Label
- Size Deviation %
- Material Deviation
- Weight Deviation %
- Specification Deviation
- Estimation Basis
- Notes

Use an exact catalog match if available.
Otherwise use the closest defensible comparable or AUD/kg rate.
Do not present an estimated value as an exact catalog price.
Do not invent a price if the database does not contain a defensible comparable.
```


## Master AI prompt

For a ready-to-use instruction set for ChatGPT, Claude, or another AI assistant, use:

**[PROMPT.md](PROMPT.md)**

This prompt includes BOM extraction from Excel, drawings, photos and PDFs, exact-match-first pricing, AUD/kg fallback logic, accuracy/deviation reporting, no-follow-up first-pass estimation, and first-response Excel delivery.


# GEMS Design System — Components / Chart

> **MANDATORY:** All Charts MUST use official GEMS General Chart components from the connected Figma Design System. AI MUST select visualization types based on actual data, analytical purpose, product requirements, and relevant GEMS UX Patterns. CCM charts, invented data, unsupported variants, and custom visual styling are strictly prohibited.

## 1. Purpose & Source of Truth

Chart visualizes meaningful data relationships to support monitoring, comparison, analysis, and decision-making.

This guideline governs:
- Chart selection and analytical purpose.
- Official GEMS Chart components and variants.
- Dashboard and reporting usage.
- Data integrity, calculations, and visualization accuracy.
- Axes, legends, labels, and visual hierarchy.
- Interaction, filtering, responsive behavior, and accessibility.
- AI recommendations and Human Approval.

**Core Principle:**

> The number of charts does not determine dashboard quality. AI MUST use the most appropriate component to communicate information clearly—not add charts merely to fill space.

### 1.1 Source Priority

1. **GEMS General Chart Components:** Official component structure, properties, variants, and styling.
2. **GEMS Foundation:** Color, typography, spacing, radius, effects, and icons.
3. **GEMS Page Samples & UX Patterns:** Contextual usage, dashboard composition, hierarchy, and placement.
4. **Product HSD/BRD:** Business objectives, metrics, calculations, filters, workflows, and permissions.
5. **Actual System Data:** Values, categories, periods, units, and data availability.
6. **Human Approval:** Authorization for proposed visualizations or unsupported requirements.
7. **General Data Visualization Principles:** Fallback when GEMS has no specific usage guidance.

GEMS defines visual implementation. Product requirements and actual data determine what should be visualized.

Read only relevant references for the requested interface. Never use CCM sections as General design references.

---

## 2. Component Selection & Usage

### 2.1 When to Use Chart

Use Chart when:
- Data contains meaningful trends, comparisons, distributions, or relationships.
- Visualization helps users understand information faster than reading raw values.
- Dashboard or reporting requirements include analytical insights.
- Users need to monitor changes or performance over time.
- Chart usage is established by an approved product design or UX Pattern.

**Charts are not limited to Dashboards.** They MAY be used in Reports, Analytics, Detail Pages, and other relevant interfaces.

### 2.2 Chart Selection Matrix

| Data Purpose | Recommended Component | Example |
|---|---|---|
| Trend over time | Line Chart | Monthly requests |
| Compare categories | Bar Chart | Requests by department |
| Compare time periods | Line / Bar Chart | Monthly performance |
| Show part-to-whole distribution | Pie / Doughnut | Requests by category |
| Show achievement against target | Activity Gauge | Target completion |
| Compare multiple dimensions | Radar Chart | Assessment dimensions |
| Display one important value | KPI / Statistic Card | Total requests |
| Display exact records | Data Table | Detailed transactions |
| Display workflow status | Badge | Draft, Finished |
| Display operational progress | Progress Indicator | Upload completion |
| No meaningful data | Empty State | No records available |

### 2.3 When NOT to Use Chart

AI MUST NOT:
- Add charts merely because the page is a Dashboard.
- Convert every KPI into a visualization.
- Use charts when a simple value or Table communicates information more clearly.
- Duplicate identical insights across multiple charts without a reason.
- Invent trends, categories, percentages, or analytical relationships.
- Use decorative graphs without analytical purpose.
- Choose chart types solely based on visual attractiveness.
- Use charts to replace workflow Status, Notification, or operational Progress Indicator.

### 2.4 AI Recommendation & Human Approval

AI SHOULD identify opportunities to visualize meaningful product data.

**AI MAY implement directly when:**
- HSD/BRD explicitly requires a chart; or
- An approved product design or UX Pattern already establishes its usage.

**AI SHOULD recommend when:**
- Relevant data supports useful visualization.
- A chart could improve monitoring or decision-making.
- Chart usage is not included in approved requirements.

A recommendation MUST explain:
1. Proposed chart type.
2. Suggested placement.
3. Analytical purpose.
4. Required data source.
5. Expected user benefit.

AI MUST obtain Human Approval before introducing a newly proposed chart outside approved product requirements.

Approval to introduce a chart does NOT authorize fabricated data, CCM styling, or unsupported component variants.

---

## 3. Official GEMS Chart Components

| Component | Purpose |
|---|---|
| Line & Bar Chart | Trends and comparisons |
| Pie / Doughnut Chart | Composition and distribution |
| Activity Gauge | Measurable progress or target achievement |
| Radar Chart | Comparison across related dimensions |
| Chart Data | Supporting data visualization patterns |
| X-Axis | Horizontal scale and category/time labels |
| Y-Axis | Vertical measurement scale |
| Legend | Identifies chart series and categories |

### Component Rules

- MUST use existing GEMS General components.
- MUST preserve supported properties, variants, dimensions, and composition.
- MUST use official component references where available.
- MUST NOT recreate official charts manually merely to imitate their appearance.
- MUST NOT invent unsupported visualization variants.
- MUST NOT use components from CCM sections.

### Prohibited CCM Sections

The same GEMS Figma file contains CCM-specific chart sections, including:

- Bar & Line Chart CCM
- Vertical Bar Chart CCM
- Horizontal Bar Chart CCM
- Line Chart CCM
- Pie & Doughnut Chart CCM
- Count Card CCM

**All CCM components, chart templates, colors, and CCM-derived styling are strictly prohibited.**

Do not select components based solely on visual similarity or proximity within the Figma file.

---

## 4. Chart Selection by Analytical Purpose

### 4.1 Trends — Line Chart

Use when:
- Data changes across time.
- Users need to identify increases, decreases, or fluctuations.
- Comparing trends is more important than comparing isolated values.

Examples:
- Jumlah pesanan per bulan.
- Tren pemakaian transportasi.
- Perubahan aktivitas mingguan.

**Rules**
- Preserve chronological order.
- Use accurate and consistent time intervals.
- Do not invent intermediate data points.
- Do not imply continuous relationships between unrelated categories.
- Avoid excessive series that reduce readability.

### 4.2 Comparisons — Bar Chart

Use when:
- Comparing values across categories.
- Comparing organizational units, periods, locations, or services.
- Showing rankings or differences.

Examples:
- Total pengajuan per departemen.
- Jumlah penghuni per mess.
- Perbandingan penggunaan layanan.

**Rules**
- Use a meaningful category-value relationship.
- Preserve accurate numerical proportions.
- Use a zero baseline for quantitative bar comparisons unless an analytically justified exception is approved.
- Maintain understandable category ordering.
- Do not invent grouped, stacked, or horizontal variants without official support.

### 4.3 Composition — Pie / Doughnut Chart

Use when:
- Categories represent portions of the same whole.
- Users need to understand percentage distribution.
- The number of categories is suitable for the available GEMS component.

Examples:
- Distribusi pesanan berdasarkan kategori.
- Persentase penggunaan fasilitas.
- Komposisi data berdasarkan jenis.

**Rules**
- Categories MUST represent parts of a meaningful total.
- Percentages MUST follow actual data.
- Do not compare unrelated metrics using Pie/Doughnut.
- Avoid excessive segments.
- Prefer Bar Chart when precise category comparison is more important.

### 4.4 Target Achievement — Activity Gauge

Use when:
- A defined target or measurable reference exists.
- Users need to understand completion or achievement.
- Progress visualization improves monitoring.

**Rules**
- MUST use actual progress or achievement data.
- MUST have a meaningful reference or measurement scale.
- MUST NOT invent percentages or targets.
- MUST NOT assume every percentage represents target completion.
- Follow `components/progress-indicator.md` for related progress rules.

### 4.5 Multidimensional Comparison — Radar Chart

Use when:
- Several related dimensions require comparison.
- Measurements use compatible scales.
- An approved product requirement benefits from a multidimensional view.

**Rules**
- Use comparable or properly normalized dimensions.
- Preserve consistent scales.
- Do not combine incompatible units.
- Do not invent scores or weighting.
- Prefer Bar Chart when accurate individual comparisons are more important.
- Confirm that the intended Radar composition is supported by GEMS before implementation.

---

## 5. Line & Bar Chart — Official Variants

### 5.1 Available Properties

| Property | Official Values |
|---|---|
| `Chart style` | `Line`, `Bar` |
| `Legend` | `False`, `Top`, `Right` |
| `Axis labels` | `True`, `False` |
| `Breakpoint` | `Desktop`, `Mobile` |

Use supported combinations from the official GEMS component.

### 5.2 Chart Style

**Line**
- Trends over ordered time values.
- Continuous data development.
- Comparison of time-based series.

**Bar**
- Category comparisons.
- Period comparisons.
- Rankings and value differences.

Do not substitute Line for Bar or vice versa without considering analytical meaning.

### 5.3 Legend

| Variant | When to Use |
|---|---|
| `False` | Data remains understandable without legend |
| `Top` | Legend above chart improves readability |
| `Right` | Side legend fits the approved layout |

**Rules**
- Match legend labels and colors with actual datasets.
- Preserve official placement and styling.
- Do not add unnecessary legends to self-explanatory charts.
- Do not remove legends if multiple series become ambiguous.

### 5.4 Axis Labels

| Variant | When to Use |
|---|---|
| `True` | Axis information is needed for interpretation |
| `False` | Context already communicates the values clearly |

**Rules**
- Preserve relevant units and measurement meaning.
- Do not hide necessary axis information for aesthetic reasons.
- Do not invent unsupported scale or label properties.
- Follow official responsive variants.

---

## 6. Pie & Doughnut Chart — Official Variants

### 6.1 Available Properties

| Property | Official Values |
|---|---|
| `Size` | `xxs`, `xs`, `sm`, `md`, `lg` |
| `Series` | `2`, `3`, `4`, `5`, `6` |
| `Legend` | `True`, `False` |

Supporting `_Pie chart` Hole variants:

| Property | Official Values |
|---|---|
| `Hole` | `False`, `25%`, `50%`, `75%` |

### 6.2 Size Selection

- Select sizes according to available space and the relevant GEMS Page Sample.
- Preserve original dimensions and proportions.
- Maintain readable labels and legends.
- Do not manually resize internal chart geometry.
- Do not invent additional sizes.

### 6.3 Series Selection

- Match the variant to the number of categories.
- Do not fabricate categories to match a Series variant.
- Do not create unsupported Series values.
- If categories exceed supported values, prefer another suitable GEMS Chart.
- Category aggregation into "Lainnya" requires meaningful business justification.

### 6.4 Doughnut Hole

- Use only official Hole variants.
- Preserve official composition.
- Do not manually change the hole diameter.
- Do not add unsupported central content.
- Follow relevant GEMS Page Samples.

### 6.5 Legend

- `True`: Use when category identification requires it.
- `False`: Use when categories remain understandable through an approved alternative.

Do not sacrifice interpretation merely to create a cleaner appearance.

---

## 7. Activity Gauge — Official Variants

### 7.1 Available Properties

| Property | Official Values |
|---|---|
| `Size` | `xs`, `sm`, `md`, `lg` |
| `Label` | `True`, `False` |

### 7.2 Usage Rules

- Select the size according to the approved layout.
- Use `Label=True` when the numerical value is important.
- Use `Label=False` only when the measurement remains understandable.
- Reflect actual achievement or progress.
- Preserve GEMS styling, proportions, and label hierarchy.
- Do not add unsupported threshold colors or segments.
- Do not replace simple KPI values with gauges without analytical benefit.

---

## 8. Chart Data & Supporting Components

### 8.1 Chart Data

Official Chart Data patterns include:

| Chart Type | Available Pattern |
|---|---|
| Bar | `Bar desktop` |
| Bar | `Bar mobile` |
| Line | `Line volatile` |
| Line | `Line wavy` |
| Line | `Line gradual` |
| Line | `Flat line` |

**Rules**
- Use patterns compatible with actual data.
- Preserve correct values and visual relationships.
- Do not modify data to imitate a reference shape.
- Do not select Flat line if actual values fluctuate.
- Do not invent unsupported data-visual variants.

### 8.2 X-Axis

Official X-Axis configurations:

| Data | Breakpoint |
|---|---|
| `7 days` | `Desktop`, `Mobile` |
| `30 days` | `Desktop`, `Mobile` |
| `12 months` | `Desktop`, `Mobile` |

**Rules**
- Select the correct time range.
- Preserve chronological order.
- Match labels with actual dataset periods.
- Do not fabricate missing observations.
- Do not repurpose an existing axis for an incompatible period without approved support.

### 8.3 Y-Axis

Official supporting components include:
- `_Y-axis`
- `_Y-axis line`
- `_Y-axis label`

Supported Y-Axis and Y-Axis Line configurations include `Label=True` and `Label=False`.

**Rules**
- Use correct numerical values and units.
- Apply meaningful scale intervals.
- Preserve official gridline and label styling.
- Do not manipulate scale to exaggerate differences.
- Do not hide essential quantitative information.

### 8.4 Legend

Official `_Legend` orientations:
- `Vertical`
- `Horizontal`

**Rules**
- Use the appropriate orientation according to GEMS layout.
- Keep legend colors and text consistent with actual data.
- Preserve official spacing and typography.
- Do not invent additional marker styles.
- Do not add legends when they do not improve understanding.

---

## 9. Dashboard & Page Usage

### 9.1 Dashboard Core Principle

> Dashboard quality is determined by information clarity, relevance, and usability—not the number of charts displayed.

AI MUST evaluate each dataset before choosing a visual component.

**Do not force every metric into a Chart.**

### 9.2 Recommended Information Hierarchy

| Priority | Information | Recommended Component |
|---|---|---|
| 1 | Essential totals and metrics | KPI / Statistic Card |
| 2 | Trends and development | Line Chart |
| 3 | Comparisons | Bar Chart |
| 4 | Distribution or composition | Pie / Doughnut |
| 5 | Target achievement | Activity Gauge |
| 6 | Detailed records | Data Table |

This hierarchy is contextual, not a mandatory requirement to include every component.

### 9.3 Dashboard Composition Rules

- Prioritize information required for user decisions.
- Group related metrics and charts logically.
- Use meaningful titles and reporting periods.
- Place primary insights in prominent positions.
- Maintain a balanced layout without unnecessary visual elements.
- Follow GEMS Dashboard Page Samples.
- Use official GEMS Card and Section patterns.
- Do not automatically add shadows to Chart containers.
- Do not repeat the same metric across multiple charts without justification.
- Do not create unsupported dashboard compositions merely for decoration.

### 9.4 Usage Across Pages

| Page | Recommended Usage |
|---|---|
| Dashboard | High-level metrics, trends, comparisons |
| Reports | Historical performance, distributions |
| Analytics | Detailed analytical relationships |
| Detail Page | Record-specific or entity-specific performance |
| Data Table Page | Supporting analytics when relevant |
| Form Page | Only when analytical context is explicitly needed |

**Important:** Chart usage is determined by information needs, not page naming.

### 9.5 Empty Dashboard

When data is unavailable:
- Use official GEMS Empty State or Loading patterns.
- Do not populate charts with fabricated values.
- Do not introduce decorative charts to fill empty areas.
- Preserve existing layout consistency.

---

## 10. Data Integrity & Calculation

### 10.1 Data Requirements

Charts MUST use:
- Approved product metrics.
- Actual values or clearly identified sample data.
- Correct units and time periods.
- Consistent categories and labels.
- Approved aggregation and calculation rules.
- Authorized data based on user roles.

### 10.2 Calculation Rules

- Use defined HSD/BRD calculations.
- Distinguish counts, totals, averages, percentages, and rates.
- Preserve appropriate denominators.
- Do not invent metrics or business formulas.
- Do not assume all categories belong to a single total.
- Do not treat missing values as zero automatically.
- Do not modify values to create visually attractive patterns.

### 10.3 Prototype & Dummy Data

When developing a prototype:

- Prefer actual provided dummy data.
- Use realistic illustrative data only when prototype scope permits it.
- Clearly distinguish sample values from actual system results.
- Do not represent fabricated data as verified business performance.
- Do not invent analytical conclusions from sample data.

### 10.4 Data Consistency

- Chart values MUST match underlying datasets.
- Titles, units, legends, and axes MUST describe the same information.
- Filters MUST affect the appropriate data.
- Related KPI Cards, Charts, and Tables MUST remain numerically consistent.
- Do not mix incompatible reporting periods.
- Do not display inaccurate percentages or totals.

---

## 11. Interaction, Filters & States

### 11.1 Filters

Use supported filters when required by HSD/BRD or approved Page Samples.

Examples:
- Date range.
- Reporting period.
- Department.
- Location.
- Category.
- Status.

**Rules**
- Use official GEMS Input Dropdown, Date & Time Picker, or Button Group.
- Only offer filters supported by available data.
- Update chart data according to selected filters.
- Keep axis, legend, and metric context synchronized.
- Do not invent filtering or aggregation behavior.

### 11.2 Tooltip & Interaction

- Use official GEMS Tooltip when contextual data-point information is needed.
- Show accurate values, labels, and units.
- Follow `components/tooltip.md`.
- Do not assume all Charts require interactive tooltips.
- Do not invent zoom, drill-down, click navigation, or custom hover effects.
- Interactive actions require defined workflows and permissions.

### 11.3 State Handling

| State | Behavior |
|---|---|
| Loading | Official GEMS Loading / Skeleton |
| Loaded | Display actual chart data |
| Empty | Official Empty State or approved no-data display |
| Error | Official Error feedback |
| Filtered | Display values matching active filters |
| Updated | Refresh values and related information |

**Rules**
- Do not fabricate values to avoid Empty States.
- Do not treat unavailable data as actual zero.
- Do not invent new Chart states.
- Preserve previous valid information during recoverable errors when supported by product behavior.

---

## 12. Responsive Behavior

- Use existing GEMS Desktop and Mobile variants.
- Preserve chart readability and meaningful labels.
- Adapt layout according to GEMS Page Samples.
- Maintain correct legend and axis relationships.
- Use officially supported chart sizes.
- Do not manually shrink Desktop components to imitate Mobile variants.
- Do not hide critical data without an accessible alternative.
- Do not introduce unsupported Mobile chart compositions.

---

## 13. Foundation & Component Dependencies

All Chart components MUST follow existing GEMS Foundation guidelines.

### 13.1 Foundation Integration

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | Chart palette, semantic colors, contrast |
| `Foundation/typography.md` | Chart titles, labels, legends, values |
| `Foundation/spacing-dan-radius.md` | Chart containers, gaps, spacing, radius |
| `Foundation/effect-styles.md` | Approved effects |
| `Foundation/icons.md` | Chart controls and supporting icons |
| `Foundation/misc-icons.md` | Specialized icons when relevant |
| `Foundation/design-annotations.md` | Additional component specifications |

### 13.2 Related Components

| Requirement | Related Guideline |
|---|---|
| Data-point explanation | `components/tooltip.md` |
| Date/category filtering | Input Dropdown / Date & Time Picker |
| Period selection | Button Group |
| Status information | `components/badge.md` |
| Operational progress | `components/progress-indicator.md` |
| Important data issues | `components/alert.md` |
| Process feedback | `components/notification.md` |
| Exact records | GEMS Data Table |
| Summary values | GEMS KPI / Statistic Card |

Use actual repository paths where names differ.

### 13.3 Visual Rules

- Apply original GEMS General component styling.
- Use official GEMS Text Styles.
- Use colors and chart palettes from GEMS General.
- Preserve official spacing, radius, and effects.
- Preserve supported axis and legend styling.
- Do not add shadows merely to decorate Chart containers.
- Do not introduce external color palettes.
- Do not hardcode HEX/RGB/HSL, unsupported typography, or chart dimensions.
- Do not use CCM components or CCM-derived visual styles.

---

## 14. Accessibility

**MUST**
- Provide meaningful chart titles.
- Display correct units and reporting periods.
- Maintain readable labels and legends.
- Communicate meaning without relying solely on color.
- Preserve sufficient contrast.
- Use accurate and nonmisleading scales.
- Provide accessible data summaries or equivalent values when necessary.
- Support keyboard access for interactive chart controls.
- Maintain usability across Desktop and Mobile.

**MUST NOT**
- Hide critical information only in hover interactions.
- Remove necessary legends or data context.
- Use inaccessible custom interactions.
- Manipulate chart proportions to distort meaning.

---

## 15. Strict AI Rules

### MUST

1. Use existing GEMS General Chart components.
2. Determine chart necessity based on actual information needs.
3. Select visualization types according to analytical purpose.
4. Preserve supported properties, variants, and component structure.
5. Use accurate values, units, calculations, and reporting periods.
6. Follow GEMS Foundation Guidelines.
7. Reference relevant GEMS Page Samples and UX Patterns.
8. Maintain consistency between Charts, KPI Cards, and Data Tables.
9. Preserve accessibility and responsive behavior.
10. Obtain Human Approval before implementing newly proposed charts outside approved requirements.
11. Request Human Approval for unsupported chart types, variants, or interactions.

### MUST NOT

1. **Use CCM charts, CCM templates, or Count Card CCM.**
2. Create custom or duplicate chart components when GEMS General components exist.
3. Invent chart types, properties, or visual variants.
4. Add charts solely for visual decoration.
5. Automatically populate every Dashboard with charts.
6. Invent values, percentages, trends, targets, or analytical conclusions.
7. Manipulate scales or proportions to exaggerate results.
8. Use Pie/Doughnut for unrelated values.
9. Use Activity Gauge without a meaningful measurement reference.
10. Use Radar Chart with incompatible measurement scales.
11. Hide essential information for visual minimalism.
12. Add unsupported axes, legends, filters, or interactions.
13. Hardcode unsupported Chart styling.
14. Replace simpler components when a Chart adds no analytical benefit.
15. Implement unapproved visualization recommendations.

---

## 16. AI Implementation Workflow

When creating a Dashboard, Report, or analytical screen:

1. **Identify Purpose:** Determine the user's primary analytical question.
2. **Inspect Data:** Identify available metrics, dimensions, units, and periods.
3. **Determine Need:** Decide whether Chart, KPI Card, Data Table, or another component is most suitable.
4. **Choose Visualization:** Match trends, comparisons, composition, targets, or multidimensional relationships.
5. **Check Requirements:** Determine whether the Chart is approved or requires Human Approval.
6. **Select GEMS Component:** Use the corresponding official General component and supported variants.
7. **Configure Structure:** Apply appropriate axis, legend, labels, and responsive configuration.
8. **Apply Actual Data:** Preserve correct calculations, values, and business meaning.
9. **Follow GEMS Patterns:** Use relevant Dashboard Page Samples and UX Patterns.
10. **Apply Foundation:** Preserve official GEMS color, typography, spacing, radius, effects, and icons.
11. **Implement Supported Behavior:** Follow approved filtering, interaction, loading, empty, and error states.

These are implementation instructions, not a separate validation report.

### 16.1 Human Approval

Request Human Approval when:
- A newly proposed Chart is not part of approved requirements.
- No suitable GEMS General Chart exists.
- The product requires an unsupported chart type or visual variant.
- Essential metric definitions or calculations are unclear.
- A new interactive behavior or workflow would otherwise need to be invented.

Combine related approval questions into one confirmation to minimize Claude AI context usage.

### 16.2 Fallback

If a requested visualization is unsupported:

1. Prefer an existing GEMS General Chart that accurately represents the data.
2. If no Chart is appropriate, consider an official KPI Card or Data Table.
3. Request Human Approval before introducing unsupported chart designs or behavior.
4. Never use CCM components or fabricated data as a workaround.

---

## 17. Official Figma References

### Main Library

- [GEMS Chart Overview](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=23-789)
- [Line & Bar Chart](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-4196)
- [Pie & Doughnut Chart](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=786-2005)
- [Activity Gauge](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-3540)
- [Radar Chart](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-3666)

### Supporting Components

- [Chart Data](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-3302)
- [X-Axis](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-3232)
- [Y-Axis](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-3513)
- [Legend](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=441-3464)

### Page Samples & UX Patterns

Read relevant official GEMS references for:
- Dashboard
- Analytics and Reports
- Detail Pages
- Data Tables
- Filtering and Date Selection
- Empty, Loading, and Error States
- Responsive Layouts

Read only the references required for the current task. Do not repeatedly load the entire Chart library or unrelated Page Samples.

---

> **FINAL RULE:** Chart usage MUST be determined by actual data, analytical purpose, and user needs—not by decoration or dashboard size. AI SHOULD recommend useful visualizations when meaningful data exists, but MUST obtain Human Approval before implementing new charts outside approved requirements. Always use official GEMS General components, preserve accurate information, follow Foundation Guidelines, and strictly prohibit CCM.

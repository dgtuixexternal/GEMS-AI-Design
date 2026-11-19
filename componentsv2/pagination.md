
# GEMS Design System — Components / Pagination

> **MANDATORY:** All Pagination components MUST use official GEMS General Pagination components and supported Figma variants. AI MUST determine whether Pagination is needed based on actual dataset structure, page context, and HSD/BRD. CCM components, custom pagination designs, and unsupported variants are strictly prohibited.

> **CORE PRINCIPLE:** Pagination exists to help users navigate divided content. Do not add Pagination unless the dataset or approved content flow genuinely requires it.

## 1. Sources & Priority

**Official Figma References**
- [GEMS Pagination — Overview](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=483-1591)
- [GEMS Pagination — Main Component](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=483-2504)
- [Pagination Number Base](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=483-2346)
- [Pagination Button Group Base](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=483-2365)
- [Pagination Dot Indicator](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=483-2337)
- [Pagination Dot Group](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2741-32036)
- [Carousel Arrow](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=483-2396)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1105-7310)

**Verified Usage Reference**
- [Meals Management ISS — Pengajuan Pesanan Tamu](https://www.figma.com/design/FaD6En6EYVnjGzegaxhjzy/Meals-Management-ISS?node-id=159-43407)

**Priority Order**
1. **GEMS General Pagination:** Official components, types, shapes, states, and responsive variants.
2. **GEMS Foundation:** Color, typography, spacing, radius, effects, and icons.
3. **GEMS Page Samples & UX Patterns:** Contextual pagination usage and placement.
4. **HSD/BRD:** Data navigation requirements, filtering, page size, and user workflows.
5. **Actual System Data:** Total Items, Current Page, Page Size, and Total Pages.
6. **General UI/UX Principles:** Fallback when GEMS provides no specific guidance.

GEMS defines visual implementation. HSD/BRD and system data define functional behavior.

Read only the relevant references needed for the current interface.

---

## 2. Purpose & When to Use

Pagination divides a dataset or content collection into navigable pages.

**Use Pagination when:**
- Data is divided into multiple pages.
- Users need to move between result pages.
- A Data Table uses paginated records.
- Search or filter results span multiple pages.
- A Report or History page has paginated data.
- A Card collection uses approved page-based navigation.

### Component Selection

| Content Requirement | Recommended Component |
|---|---|
| Paginated Data Table | Card Pagination |
| Paginated page-level content | Page Pagination |
| Paginated records inside Card | Card Pagination |
| Paginated search/filter results | Page or Card Pagination according to container |
| Carousel or slide navigation | Carousel indicators/arrows |
| Form steps | GEMS Stepper or approved progress pattern |
| Tab navigation | GEMS Tabs |
| Infinite Scroll | Approved Infinite Scroll pattern |
| Single-page dataset | Pagination usually unnecessary |
| Empty dataset | Empty State |

### Selection Rules

- Determine whether the dataset actually requires pagination.
- Select Page or Card Pagination based on the content container.
- Do not use Page Pagination automatically just because a page contains a Table.
- Do not use Carousel indicators as Data Table pagination.
- Do not add Pagination merely for visual completeness.
- Do not combine Pagination with Infinite Scroll unless the workflow explicitly requires it.

---

## 3. Official Pagination Variants

### Available Properties

| Property | Official Values |
|---|---|
| `Type` | Official Page and Card Pagination variants |
| `Shape` | `Square`, `Circle` where supported |
| `Breakpoint` | `Desktop`, `Mobile` |

### Official Type Availability

| Type | Desktop | Mobile |
|---|---|---|
| `Page default` | Available | Available |
| `Page minimal center aligned` | Available | Available |
| `Card default` | Available | Available |
| `Card minimal left aligned` | Available | Available |
| `Card minimal center aligned` | Available | Available |
| `Card minimal right aligned` | Available | Available |
| `Card button group left aligned` | Available | Available |
| `Card button group center aligned` | Available | Available |
| `Card button group right aligned` | Available | Available |
| `Card button group right aligned with dropdown` | Available | Not available |

### Shape Availability

| Type | Shape |
|---|---|
| `Page default` | Square / Circle |
| `Page minimal center aligned` | Square / Circle |
| `Card default` | Square / Circle |
| `Card minimal` | Square |
| `Card button group` | Square |

Use only combinations explicitly available in the official GEMS component.

**Rules**
- MUST reuse the original GEMS General Pagination instance.
- MUST preserve the selected Type, Shape, and Breakpoint.
- MUST preserve official alignment, spacing, dimensions, typography, and icons.
- MUST NOT manually reconstruct Pagination.
- MUST NOT invent additional Type/Shape/Breakpoint combinations.
- MUST NOT create a Mobile variant with Page Size Dropdown when it is unavailable.

---

## 4. Strict CCM Restriction

The Pagination page contains CCM-specific components, including:

- `_Pagination dot indicator CCM`
- `_Pagination number base CCM`
- `_Pagination button group base CCM`
- `Pagination CCM` used in other GEMS component examples

**All CCM Pagination components and styling are prohibited.**

### Rules

- NEVER use Pagination CCM.
- NEVER use CCM Number Base, Button Group Base, or Dot Indicator.
- NEVER copy colors, spacing, icons, or structure from CCM Pagination.
- Do not select a component merely because it visually resembles General Pagination.
- If an existing page or Table contains Pagination CCM, replace its design reference with the appropriate GEMS General component when the task includes updating that design.
- If no appropriate General variant supports the required behavior, request Human Approval.

CCM is not an acceptable fallback.

---

## 5. Pagination Type Selection

### 5.1 Page Default

**Use for:**
- Page-level paginated content.
- Lists not contained within a Card.
- Standard content collections requiring visible page navigation.

**Rules**
- Follow official `Page default` structure.
- Select Square or Circle according to the relevant GEMS pattern.
- Use the correct Desktop/Mobile variant.
- Do not add unnecessary controls.

### 5.2 Page Minimal Center Aligned

**Use for:**
- Simple page-level navigation.
- Pages requiring a compact, centered pagination treatment.

**Rules**
- Preserve centered alignment.
- Use only supported Shapes.
- Do not replace full Pagination with Minimal merely for decoration.
- Maintain understandable page navigation.

### 5.3 Card Default

**Use for:**
- Data Tables inside Cards.
- Card-based record lists.
- Management components requiring standard pagination.

**Rules**
- Keep Pagination connected to the dataset it controls.
- Preserve official Card Pagination composition.
- Select Square or Circle only when available.
- Follow relevant GEMS Data Table patterns.

### 5.4 Card Minimal

**Available Alignments**
- Left
- Center
- Right

**Use for:**
- Compact pagination inside Cards.
- Data collections where a minimal navigation pattern is sufficient.

**Rules**
- Select alignment according to GEMS Page Samples.
- Maintain consistency across similar components.
- Do not invent custom alignment arrangements.
- Do not use Minimal when it hides information essential to navigation.

### 5.5 Card Button Group

**Available Alignments**
- Left
- Center
- Right

**Use for:**
- Data Tables with grouped pagination controls.
- Management interfaces requiring clear page navigation.

**Rules**
- Preserve the official Button Group structure.
- Follow the General Pagination Button Group Base.
- Do not substitute the CCM version.
- Do not manually rearrange internal controls.

### 5.6 Card Button Group with Dropdown

**Official Type:** `Card button group right aligned with dropdown`

**Availability:** Desktop.

**Use when:**
- The dataset is paginated.
- Users need an approved Page Size selection control.
- The Table/Card layout supports this variant.

**Rules**
- Use only when Page Size selection is required.
- Available Page Sizes MUST come from product/system requirements.
- Do not assume `10` is the mandatory default.
- Do not create an unsupported Mobile version.
- Do not add a dropdown to variants that do not support it.

---

## 6. Pagination Supporting Components

### 6.1 Number Base

Official properties:

| Property | Values |
|---|---|
| `Shape` | `Square`, `Circle` |
| `State` | `Default`, `Hover/active`, `Focused` |

**Rules**
- Preserve the official number button appearance.
- Use active styling for the Current Page.
- Maintain visible keyboard focus.
- Do not create custom shape or state values.

### 6.2 Button Group Base

Official properties:

| Property | Values |
|---|---|
| `Icon` | `False`, `Leading`, `Trailing`, `Only` |
| `State` | `Default`, `Active/hover`, `Focused` |

**Rules**
- Use the supported icon arrangement.
- Preserve the official Previous/Next button treatment.
- Do not invent additional button layouts.
- Do not use the CCM Button Group Base.

### 6.3 Dot Indicator

Official properties:

| Property | Values |
|---|---|
| `Current` | `True`, `False` |
| `Style` | `Dot`, `Line` |
| `Size` | `md`, `lg` |

### 6.4 Dot Group

Official properties:

| Property | Values |
|---|---|
| `Size` | `md`, `lg` |
| `Style` | `Dot`, `Line` |
| `Framed` | `True`, `False` |

**Usage Rules**
- Use indicators for supported multi-view or Carousel navigation.
- Current state MUST reflect the displayed item/page.
- Do not use Dot indicators as a substitute for record pagination without an approved pattern.
- Preserve official size, spacing, and active styling.

### 6.5 Carousel Arrow

Official properties:

| Property | Values |
|---|---|
| `Size` | `md`, `lg` |
| `Chevron` | `Left`, `Right` |

**Rules**
- Use only for appropriate Carousel or supported content navigation.
- Do not use Carousel arrows to replace the General Pagination component.
- Preserve official icon size and states.

---

## 7. Data & Pagination Configuration

Pagination requires functional data from the application.

These are **application data requirements, not Figma properties**.

| Data | Purpose |
|---|---|
| Current Page | Active page number |
| Total Items | Number of records in the active dataset |
| Page Size | Records displayed per page |
| Total Pages | Number of available pages |
| Available Page Sizes | Supported page size options, if applicable |
| Loading Status | Data loading state |

### Data Rules

- Use actual application data.
- Calculate `Total Pages = ceil(Total Items / Page Size)` for standard page-based pagination.
- `Page Size` MUST be greater than zero.
- Current Page MUST remain within the valid available range.
- Total Items MUST reflect active search/filter results.
- Do not treat example values from Figma as real data.
- Do not invent Page Size options or record totals.
- Follow the approved backend pagination mechanism.

### Example

If:
- Total Items = 95
- Page Size = 10

Then:
- Total Pages = 10
- Last Page contains 5 records.

This is illustrative only. Generated UI MUST use the actual dataset.

---

## 8. Pagination Content & States

### Component Elements

| Element | Usage |
|---|---|
| Previous | Navigate to the preceding page |
| Next | Navigate to the following page |
| Page Numbers | Direct page selection when supported |
| Active Page | Identify the currently displayed page |
| Page Indicator | Compact current/total page information |
| Ellipsis | Represent undisplayed page ranges when supported |
| Page Size Dropdown | Change records per page when supported |
| Button Group | Group navigation controls according to variant |

Not every variant includes every element.

### State Behavior

| State | Expected Behavior |
|---|---|
| Default | Controls reflect available pages |
| Current / Active | Exactly one active page |
| Hover | Official GEMS hover treatment |
| Focused | Official visible focus treatment |
| First Page | Previous cannot navigate backward |
| Last Page | Next cannot navigate forward |
| Loading | Follow the product's loading mechanism |
| Error | Show appropriate GEMS error feedback |
| Empty | Use Empty State; avoid meaningless pagination |
| Single Page | Usually omit Pagination unless required |

**Rules**
- Do not invent visual states absent from GEMS.
- Use official supporting control states for unavailable actions.
- Do not allow navigation outside valid pages.
- Do not display fictional pages to make controls look complete.
- Do not use Loading or Error as a reason to display inaccurate totals.

---

## 9. Navigation & Interaction Behavior

### Previous / Next

- Previous moves one page backward.
- Next moves one page forward.
- Previous MUST be unavailable on the first page.
- Next MUST be unavailable on the last page.
- Page content MUST correspond to the selected page.

### Page Number Selection

- Display the selected valid page.
- Update the Active Page indicator.
- Preserve relevant search, filter, and sorting parameters.
- Do not navigate to unavailable page numbers.

### Page Size Selection

When the official variant and requirements support it:

- Update Page Size.
- Recalculate Total Pages.
- Ensure Current Page remains valid.
- Return to the first page when appropriate, unless product behavior specifies another rule.
- Preserve active search/filter/sort context.
- Do not invent unsupported Page Size values.

### Search, Filter & Sorting

- Pagination MUST operate on the active filtered dataset.
- Recalculate page count when the result set changes.
- Prevent navigation to pages that no longer exist.
- Preserve sorting across page transitions.
- Reset or adjust Current Page appropriately after significant dataset changes.
- Do not mix records from different filter states.

### Data Changes

After Create, Edit, Delete, or Refresh:
- Update relevant totals.
- Recalculate available pages when necessary.
- Preserve a valid Current Page.
- Follow approved refresh behavior.
- Do not assume record creation or deletion always changes the current page.

### Error Handling

- Do not show navigation as successful if new page data failed to load.
- Preserve or restore an accurate visible state according to product behavior.
- Use official GEMS error feedback.
- Provide retry only when supported.
- Avoid repeated unnecessary navigation requests during loading.

---

## 10. Placement & Page Context

### Data Table

- Pagination SHOULD appear near the dataset it controls.
- Follow the official GEMS Data Table or Card composition.
- Keep its position consistent across comparable management pages.
- Do not separate Pagination from its related Table.
- Do not automatically display Pagination for small single-page datasets.

### Search & Filter Results

- Pagination MUST represent the currently filtered results.
- Use accurate Total Items and Total Pages.
- Do not display stale page counts after search/filter changes.

### Reports & History

- Preserve active reporting periods and sorting.
- Use the appropriate Page or Card Pagination pattern.
- Maintain data consistency across pages.

### Card-Based Content

- Use Card Pagination when the collection is page-based.
- Use Carousel indicators/arrows when the interaction is a Carousel.
- Do not confuse these navigation models.

---

## 11. Verified Usage — Meals Management ISS

**Reference:** [Meals Management ISS — Pengajuan Pesanan Tamu](https://www.figma.com/design/FaD6En6EYVnjGzegaxhjzy/Meals-Management-ISS?node-id=159-43407)

**Observed Pattern**
- Pagination located below a management table.
- Card button group with dropdown.
- Page Size control.
- Grouped page navigation.
- Example wording: `Tampilkan 10 data per halaman`.

**Usage Rules**
- MAY reference this layout for similar management tables.
- MUST still use the official GEMS General Pagination component.
- MUST NOT treat `10` as a mandatory Page Size.
- MUST NOT assume every Table requires a Page Size Dropdown.
- MUST NOT copy unrelated business data or workflow behavior.

The ISS file provides contextual usage. GEMS remains the visual source of truth.

---

## 12. Responsive Behavior

### Desktop

- Use official Desktop variants.
- Preserve approved alignment, grouping, and page numbers.
- Display Page Size controls only where supported.
- Do not manually redesign Button Groups.

### Mobile

- Use official Mobile variants.
- Preserve readable page position information.
- Use the compact navigation arrangement provided by GEMS.
- Do not force Desktop page-number layouts onto Mobile.
- Maintain usable touch targets.
- Do not invent Mobile dropdown combinations that are unavailable.

### Cross-Platform Rules

- Current Page and Total Pages MUST remain accurate.
- Desktop/Mobile behavior MUST refer to the same underlying dataset.
- Visual differences MUST follow official responsive variants.
- Do not assume every Desktop control has an identical Mobile equivalent.

---

## 13. Foundation & Component Dependencies

All Pagination components MUST follow GEMS Foundation.

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | General colors, active states, contrast |
| `Foundation/typography.md` | Page numbers, indicators, labels |
| `Foundation/spacing-dan-radius.md` | Padding, gaps, dimensions, radius |
| `Foundation/effect-styles.md` | Official effects if applicable |
| `Foundation/icons.md` | Previous, Next, Chevron icons |
| `Foundation/design-annotations.md` | Component specifications |

### Related Components

| Requirement | Guideline |
|---|---|
| Paginated records | `components/data-table.md` |
| Grouped controls | `components/button-group.md` |
| Page Size selection | `components/input-dropdown.md` |
| Loading states | Official GEMS Loading pattern |
| Empty results | GEMS Empty State |
| Error feedback | `components/alert.md` / `components/notification.md` |
| Carousel navigation | GEMS Carousel pattern |

Use actual repository paths where filenames differ.

**Visual Rules**
- Preserve official GEMS General component references.
- Apply existing Figma Text Styles directly.
- Use only GEMS General colors and effects.
- Preserve official icon sizes, spacing, radius, and alignment.
- Do not manually rebuild existing components.
- Do not hardcode unsupported HEX/RGB/HSL, typography, spacing, or dimensions.
- Never use CCM styling.

---

## 14. Accessibility

**MUST**
- Support keyboard navigation for interactive controls.
- Preserve visible focus indicators.
- Provide accessible names for Previous and Next.
- Identify the current page semantically, such as `aria-current="page"` in web implementations.
- Communicate current page information without relying only on color.
- Keep disabled controls functionally unavailable.
- Maintain logical focus order.
- Provide readable page information on Mobile.
- Preserve adequate touch targets through official GEMS sizing.

**MUST NOT**
- Make disabled navigation actionable.
- Hide the current page state.
- Rely only on hover to communicate important information.
- Use inaccessible custom navigation controls.
- Shrink Mobile controls outside official GEMS specifications.

---

## 15. Strict AI Rules

### MUST

1. Use existing **GEMS General Pagination** components.
2. Determine whether Pagination is actually needed.
3. Select Type based on Page or Card context.
4. Preserve supported Shape and Breakpoint combinations.
5. Use accurate Current Page, Total Items, Page Size, and Total Pages.
6. Apply correct first/last-page behavior.
7. Preserve search, filter, and sorting during navigation.
8. Use Page Size Dropdown only when supported and required.
9. Follow GEMS Page Samples and UX Patterns.
10. Apply official GEMS Foundation and responsive behavior.
11. Request Human Approval for unsupported variants or interactions.

### MUST NOT

1. **Use Pagination CCM or any CCM supporting components.**
2. Create custom, duplicate, or detached Pagination instances.
3. Add Pagination without actual page-based data.
4. Invent unsupported Type, Shape, or Breakpoint combinations.
5. Use fictional page counts, totals, or Page Size options.
6. Allow Previous on the first page or Next on the last page.
7. Lose active filters or sorting during page changes.
8. Add dropdown controls to unsupported variants.
9. Use Carousel indicators as Data Table pagination.
10. Combine Pagination and Infinite Scroll without approved requirements.
11. Show irrelevant Pagination for empty or single-page datasets.
12. Hardcode styling outside official GEMS.
13. Introduce unsupported behavior without Human Approval.

---

## 16. AI Pagination Selection Decision

When designing a page or data component:

1. **Identify Dataset:** Determine whether content is divided into pages.
2. **Determine Necessity:** If no page-based navigation is needed, do not add Pagination.
3. **Identify Container:** Choose Page or Card family.
4. **Select GEMS Type:** Use the appropriate Default, Minimal, or Button Group variant.
5. **Select Shape & Breakpoint:** Use an existing official combination.
6. **Configure Data:** Apply actual Current Page, Total Items, Page Size, and Total Pages.
7. **Define Behavior:** Apply Previous/Next, page selection, filters, sorting, and supported Page Size changes.
8. **Handle States:** Follow official Active, Focused, Loading, Empty, and Error patterns.
9. **Apply Foundation:** Preserve original GEMS component structure, styles, and accessibility.

### Human Approval

Request Human Approval when:
- No suitable General Pagination variant exists.
- A required Mobile combination is unavailable.
- A new pagination interaction is necessary.
- Page Size options or business behavior are undefined.
- A custom pagination composition would otherwise be required.

Combine related questions into one confirmation to minimize Claude AI context usage.

### Fallback

If the requested Pagination is unsupported:
1. Prefer the closest suitable GEMS General variant.
2. Preserve the required data-navigation behavior.
3. Request Human Approval before introducing new variants or workflows.
4. Never substitute CCM components.

> **FINAL INSTRUCTION:** Use official **GEMS General Pagination** only when content genuinely requires page-based navigation. Select the correct Page or Card variant, maintain accurate data and navigation behavior, follow GEMS Foundation and relevant usage patterns, and strictly prohibit CCM Pagination.


# GEMS Design System — Components / Date & Time Picker

> **MANDATORY:** All date and time selection interfaces MUST use official GEMS General Date & Time Picker components and their supported subcomponents. Preserve original component references, properties, visual states, and interaction behavior. **CCM components and CCM-derived styling are strictly prohibited, including Calendar, Date Picker Menu, Clock, and supporting elements.**

## 1. Purpose & Source of Truth

Date & Time Picker enables users to select dates, times, and supported date combinations through official GEMS controls.

This guideline covers:
- Date & Time Picker
- Calendar
- Date cells
- Date Picker Menu
- Select Time
- Clock
- AM/PM selection
- Date/time validation, states, and contextual usage

**Core Principle:** Select the official GEMS component according to the data requirement and interaction. Never recreate a picker manually or substitute a CCM component.

### Source Priority

1. **GEMS General Components:** Official variants, properties, states, and visual specifications.
2. **GEMS Page Samples & UX Patterns:** Contextual usage, placement, and behavior.
3. **Product HSD/BRD:** Date/time formats, constraints, permissions, and workflows.
4. **General UI/UX Principles:** Fallback when GEMS provides no specific guidance.

GEMS defines the component design. HSD/BRD defines the business rules.

Read only the relevant GEMS references for the requested interaction.

## 2. Component Selection Matrix

| Requirement | GEMS Component | Usage |
|---|---|---|
| Select one date | Date Picker / Single Date | Tanggal kunjungan |
| Select supported date range | Date Picker Menu / Dual Dates | Periode laporan |
| Select time | Time Picker / Select Time | Jam keberangkatan |
| Select date and time | Supported Date & Time Picker composition | Jadwal check-in |
| Display calendar | Calendar | Date selection interface |
| Choose a calendar day | Official date cell | Active/selected date |
| Choose time through clock | Clock | Supported time interaction |
| Choose AM or PM | Time Type | Supported 12-hour time format |

### Selection Rules

- MUST choose the component according to the required data and interaction.
- MUST use official GEMS General components.
- MUST follow supported Single Date, Dual Dates, and time-selection patterns.
- MUST NOT replace official pickers with free-text Input without approval.
- MUST NOT invent unsupported date-range, time-range, or scheduling behavior.
- MUST NOT use CCM components even when their appearance is similar.

## 3. Date & Time Picker

### 3.1 Available Properties

The main GEMS Date & Time Picker includes these identified configurations:

| Property | Official Values |
|---|---|
| `Type` | `Default`, `Date Open`, `Time Open` |
| `State` | `Default`, `Disabled` |

Observed combinations:

| State | Type |
|---|---|
| Default | Default |
| Default | Date Open |
| Default | Time Open |
| Disabled | Default |

**Important:**
- `Date Open` and `Time Open` are Type values, not State values.
- Do not invent `Focused`, `Filled`, `Success`, or other main-component State values.
- Do not assume unsupported combinations exist.

### 3.2 Type Usage Matrix

| Type | When to Use | Behavior |
|---|---|---|
| Default | Picker is closed | Displays selected value or supported placeholder |
| Date Open | Date-selection interface is open | Displays official date-selection UI |
| Time Open | Time-selection interface is open | Displays official time-selection UI |

### 3.3 Interaction Rules

**MUST**
- Use the original GEMS component.
- Preserve selected values when opening or closing the picker.
- Display the correct date/time selection interface.
- Follow official component spacing, typography, icons, and styling.
- Apply date/time restrictions only when defined by product requirements.

**MUST NOT**
- Create a custom popup or calendar.
- Invent additional Type or State properties.
- Automatically select the current date/time without requirements.
- Change saved values merely because the picker opens.

## 4. Calendar & Date Cells

### 4.1 Calendar

Use the official GEMS Calendar component for date selection.

**Rules**
- MUST preserve official calendar layout and navigation.
- MUST use the original GEMS date-cell components.
- MUST distinguish current date, selected date, available date, and unavailable date.
- MUST follow product requirements for selectable dates.
- MUST NOT invent calendar colors or interaction states.

### 4.2 Date Cell Types

The GEMS Calendar includes identified date-cell configurations such as:

| Type | Purpose |
|---|---|
| Active | Available date |
| Selected | Currently selected date |
| Today's date | Current calendar date |
| Inactive | Date outside the active context |

Supported states vary by cell configuration and include `Default`, `Hover`, and `Disabled`.

Use only combinations available in the official component.

### 4.3 Date Cell Rules

- MUST distinguish `Today's date` from `Selected`.
- MUST preserve selected-date styling.
- MUST use official Hover and Disabled appearances.
- MUST NOT allow selection of disabled dates.
- MUST NOT assume today's date is automatically selected.
- MUST NOT invent additional date-cell states.

### 4.4 Date Selection Behavior

- Selecting an available date MUST update the relevant value according to the approved interaction.
- The selected date MUST remain consistent between the field and calendar.
- Reopening the picker MUST reflect the current value.
- Date navigation MUST follow the official GEMS Calendar pattern.
- Date constraints MUST come from HSD/BRD.

## 5. Date Picker Menu

### 5.1 Available Configurations

The official GEMS Date Picker Menu includes:

| Property | Values |
|---|---|
| `Type` | `Single date`, `Dual dates` |
| `Breakpoint` | `Desktop`, `Mobile` |

### 5.2 Single Date

Use when the user must select one date.

**Examples**
- Tanggal kunjungan
- Tanggal keberangkatan
- Tanggal check-in
- Tanggal transaksi

**Rules**
- MUST use the official Single Date configuration.
- MUST preserve the selected date.
- MUST follow date restrictions from HSD/BRD.
- MUST NOT automatically select today unless required.

### 5.3 Dual Dates

Use when the approved product flow requires selecting two related dates, such as a start and end date, and the official GEMS configuration supports the interaction.

**Examples**
- Periode laporan
- Rentang tanggal kunjungan
- Tanggal mulai dan selesai

**Rules**
- MUST use the official Dual Dates configuration.
- MUST follow product requirements for start/end relationships.
- MUST preserve both selected values.
- MUST NOT assume a specific range-selection behavior beyond what the official component and UX Pattern support.
- MUST NOT invent maximum ranges, minimum ranges, or automatic end dates.

### 5.4 Desktop & Mobile

- MUST use the relevant official breakpoint configuration.
- MUST preserve usability and date-selection behavior.
- MUST NOT manually recreate mobile Calendar layouts.
- MUST NOT transfer desktop dimensions directly to mobile.
- MUST follow GEMS responsive patterns.

## 6. Time Picker & Supporting Components

### 6.1 Select Time

The official GEMS Select Time component includes:

| Property | Values |
|---|---|
| `Version` | `Default`, `V2` |

**Rules**
- Use the version supported by the relevant GEMS pattern.
- Preserve original time-selection structure.
- Do not assume V2 automatically replaces Default.
- Do not invent a new Select Time configuration.

### 6.2 Clock

Identified Clock configurations:

| State | Purpose |
|---|---|
| `default` | Standard clock appearance |
| `input` | Clock input-related appearance |

**Rules**
- Preserve exact GEMS property naming.
- Use the correct Clock configuration according to the selected Time Picker pattern.
- Do not invent Clock variants or interaction behavior.

### 6.3 Time Type

The GEMS Time Type component includes:

| Type | Purpose |
|---|---|
| `AM Selected` | AM is selected |
| `PM Selected` | PM is selected |

**Rules**
- Use only when the relevant time format requires AM/PM.
- Preserve the current selection.
- Do not force 12-hour formatting if product requirements specify another supported format.
- Do not create custom AM/PM controls.

### 6.4 Time Rules

**MUST**
- Follow HSD/BRD for hours, minutes, permitted intervals, and display format.
- Preserve user-selected time values.
- Use official GEMS time-selection components.
- Keep displayed and selected time consistent.

**MUST NOT**
- Automatically populate the current time without requirements.
- Infer a travel or event time from its date alone.
- Restrict selectable hours without business rules.
- Invent unsupported time intervals, formats, or AM/PM behavior.

## 7. States, Validation & Error Handling

### 7.1 Main Component State Matrix

| Condition | Component Configuration | Behavior |
|---|---|---|
| Picker closed | State=Default, Type=Default | Normal appearance |
| Calendar open | State=Default, Type=Date Open | Date selection |
| Time selector open | State=Default, Type=Time Open | Time selection |
| Interaction unavailable | State=Disabled, Type=Default | Non-interactive |

### 7.2 Disabled Rules

- MUST use the official Disabled configuration.
- MUST prevent value changes.
- MUST preserve relevant existing values.
- SHOULD explain unavailability when the reason is unclear.
- MUST NOT use Disabled as a substitute for validation errors.
- MUST NOT assume unsupported Disabled + Open combinations.

### 7.3 Validation Matrix

| Condition | Expected Behavior |
|---|---|
| Required date missing | Show specific required-date message |
| Required time missing | Show specific required-time message |
| Date outside permitted range | Explain allowed date range |
| Invalid start/end relationship | Explain the required relationship |
| Time outside permitted hours | Explain allowed time boundaries |
| Invalid date/time combination | Explain the conflicting values |
| Valid correction | Remove error feedback and preserve corrected values |

### 7.4 Validation Rules

**MUST**
- Apply validation rules from HSD/BRD.
- Follow verified GEMS validation and error-message patterns.
- Preserve user-selected values during recoverable validation errors.
- Keep error messages associated with the relevant field.
- Maintain clear focus and interaction behavior.

**MUST NOT**
- Invent unsupported `Destructive` or `Error` properties.
- Create a custom red border or icon when no official component variant supports it.
- Create a Success state or green validation border.
- Delete or modify selected values silently.
- Introduce business restrictions absent from requirements.

If the main Date & Time Picker has no verified error property, use an approved GEMS form-validation pattern rather than inventing a new component state.

## 8. Contextual Date & Time Patterns

### 8.1 Usage Matrix

| Context | Input Requirement | Recommended Pattern |
|---|---|---|
| Registration | Date of birth | Single Date |
| Visit scheduling | Visit date | Single Date |
| Travel scheduling | Departure time | Time Picker |
| Accommodation | Check-in date and time | Supported Date + Time composition |
| Reporting | Start/end dates | Dual Dates, when supported |
| Event scheduling | Event date range | Supported Dual Dates pattern |
| Transaction form | Transaction date | Single Date |
| Time-specific operation | Scheduled time | Select Time |

Examples are contextual illustrations, not universal business requirements.

### 8.2 Create Form

- Use relevant GEMS Date & Time Picker components.
- Apply required/optional rules from HSD/BRD.
- Follow GEMS Add New Data UX Pattern.
- Use official Button components for Save, Submit, and Cancel.
- Do not invent default dates or times.

### 8.3 Edit Form

- Display existing date/time values accurately.
- Preserve unchanged values.
- Follow edit permissions and status restrictions.
- Use the appropriate picker configuration for changes.
- Do not automatically replace existing values with current date/time.

### 8.4 Detail / Read-Only Page

- Use appropriate GEMS display components for non-editable date/time information.
- Use Disabled Picker only when the approved pattern requires it.
- Do not automatically represent every read-only value as a disabled field.

### 8.5 Search & Filter

- Use official GEMS Date Picker patterns for date-based filtering.
- Use approved Single Date or Dual Dates configurations.
- Follow GEMS Filter and Input guidelines.
- Do not invent preset periods or date ranges.
- Preserve selected filters according to the approved UX Pattern.

### 8.6 Dashboard & Reports

- Date-based periods MUST follow product reporting requirements.
- Use an appropriate GEMS Date Picker only when custom date selection is supported.
- Do not invent automatic periods, date limits, or refresh behavior.
- Keep displayed report data consistent with the selected period.
- Follow the relevant GEMS Dashboard and Page Samples.

### 8.7 Empty State

When no data exists for the selected date or period:

- Display the appropriate GEMS Empty State.
- Preserve the selected date or period.
- Provide contextual wording.
- Offer a recovery action only when supported.
- Do not automatically disable the picker simply because the result is empty.

### 8.8 Loading & Error States

- Follow official GEMS loading and error UX Patterns.
- Preserve selected date/time values during recoverable failures.
- Distinguish field-validation errors from data-loading errors.
- Do not invent custom picker loading states.
- Provide an approved retry or correction action where appropriate.

## 9. Product Rules & Accessibility

### 9.1 Business Requirements

All date/time behavior MUST follow HSD/BRD, including:

- Required or optional status
- Date and time formats
- Minimum and maximum values
- Allowed or restricted dates
- Start/end relationships
- Scheduling constraints
- User roles and permissions
- Default values, when explicitly defined

Do not invent these rules from visual examples.

### 9.2 Labels & Helper Text

- Use specific labels matching product terminology.
- Keep format guidance clear and concise.
- Follow official GEMS Typography.
- Do not rely on placeholders as the only field labels.
- Show validation messages close to relevant fields.
- Do not copy unrelated labels from Page Samples.

### 9.3 Accessibility

**MUST**
- Preserve visible focus indication.
- Support applicable keyboard interaction.
- Maintain readable date and time values.
- Differentiate selected, available, and disabled dates.
- Associate labels and error messages with relevant controls.
- Follow GEMS color contrast and typography rules.

**MUST NOT**
- Communicate invalid selections through color alone when text feedback is required.
- Allow interaction with disabled dates or controls.
- Remove official focus treatment.
- Invent unsupported interaction behavior.

### 9.4 Responsive Layout

- Follow official GEMS Desktop and Mobile picker configurations.
- Preserve component-defined spacing, typography, and touch usability.
- Adapt the surrounding layout rather than modifying the original component.
- Do not invent custom Calendar or Time Picker layouts.

## 10. Strict GEMS General & CCM Exclusion

### 10.1 Component Origin Rules

**MANDATORY:** A component is compliant only when it uses the official GEMS General component or its approved implementation.

Visual similarity is not sufficient.

**MUST**
- Use GEMS General Date & Time Picker components.
- Use GEMS General supporting elements.
- Preserve original component references and supported properties.
- Follow GEMS Foundation Guidelines.
- Use approved GEMS semantic colors, typography, icons, spacing, radius, and effects.

### 10.2 CCM Restrictions

**MUST NOT**
- Use Date & Time Picker CCM.
- Use Calendar CCM.
- Use CCM-specific date cells, clock controls, or time selectors.
- Use CCM-specific colors, typography, borders, effects, or states.
- Copy CCM styling from Page Samples or unrelated product designs.
- Duplicate or recreate CCM components as General components.
- Use CCM as a fallback when the required General component is unavailable.

If a reference includes CCM components, use it only for relevant business context. Implement the interface using official GEMS General components.

### 10.3 Unsupported Properties

**MUST NOT**
- Create new picker Type or State values.
- Treat `Date Open` or `Time Open` as main-component states.
- Add `Focused`, `Filled`, `Success`, or `Destructive` properties to the main picker without verified support.
- Transfer supporting-component properties to the main component.
- Invent custom date cells, menus, or time-selection controls.
- Hardcode component styling outside official GEMS tokens.

## 11. AI Implementation Rules

When implementing date/time selection:

1. **Read HSD/BRD:** Identify date/time requirements, formats, restrictions, permissions, and workflow.
2. **Select GEMS General Component:** Choose Single Date, Dual Dates, Time Picker, or an approved composition.
3. **Apply Official Properties:** Use only supported Type, State, Version, and Breakpoint values.
4. **Apply Supporting Elements:** Use official Calendar, date cells, Clock, and Time Type when required.
5. **Apply Contextual Pattern:** Follow relevant GEMS Components, Page Samples, and UX Patterns.
6. **Apply Validation:** Use approved error patterns and product-defined constraints.
7. **Preserve Behavior:** Keep selected values, display, permissions, and interaction states consistent.
8. **Resolve Exceptions:** Request Human Approval if an unsupported component or essential business rule is required.

These are implementation instructions, not a separate validation report.

### Human Approval

Request confirmation when:

- No suitable GEMS General component exists.
- A required interaction needs an unsupported variant.
- Date/time business constraints are essential but undefined.
- A new scheduling or selection workflow would otherwise need to be invented.

Combine related clarification questions into one confirmation.

**Fallback:** Use the closest existing GEMS General component that supports the required interaction. If the requirement cannot be met without inventing a component or business rule, request Human Approval. Never use CCM.

## 12. Official Figma References & Related Guidelines

### 12.1 Main Components

| Component | Reference |
|---|---|
| Date & Time Picker Library | [GEMS Date & Time Picker](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1146-1533) |
| Main Date & Time Picker | [GEMS Main Picker](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1146-1678) |

### 12.2 Supporting Components

The GEMS Date & Time Picker Library contains:

- Calendar
- Date cells
- Date Picker Menu
- Select Time
- Clock
- Time Type

Use these elements through their official GEMS General component references.

### 12.3 Related Guidelines

Apply the relevant repository guidelines:

- `foundation/color.md`
- `foundation/typography.md`
- `foundation/spacing-radius.md`
- `foundation/effects.md`
- `components/input.md`
- `components/button.md`
- `components/icons.md`
- `components/input-dropdown.md`

Use actual repository paths if filenames differ.

### 12.4 Page Samples & UX Patterns

Use the connected GEMS Design System for relevant:

- Form Pages
- Detail Pages
- Dashboard & Reports
- Search & Filter
- Add New Data
- Edit Data
- Empty & Error States

Read only references applicable to the requested product and screen.

---

**FINAL RULE:** Every Date & Time Picker, Calendar, Date Picker Menu, Select Time, Clock, and supporting element MUST originate from the official GEMS General Design System. Follow supported properties, product requirements, and contextual UX Patterns. Never use CCM or invent unsupported variants, states, or business behavior.


# GEMS Design System — Components / Progress Indicator

> **MANDATORY:** Use official GEMS General Progress Indicator components. Select components based on actual product needs, measurable data, and contextual GEMS UX Patterns. Preserve original variants, visual properties, and behavior. **CCM components are strictly prohibited.**

## 1. Purpose & Source of Truth

Progress Indicator communicates the completion level of a measurable task, process, operation, or supported media interaction.

This guideline governs:

- When Progress Indicator should be used.
- Progress Bar and Video Indicator selection.
- Progress values, calculations, and completion criteria.
- Component variants and label placement.
- Contextual usage, loading, empty, and error behavior.
- AI recommendations and Human Approval.

**Core Principle:**

> Progress Indicator represents measurable progress—not business status, arbitrary percentages, or decorative UI.

### 1.1 Source Priority

1. **GEMS General Components:** Official variants, styling, and component properties.
2. **GEMS Page Samples & UX Patterns:** Usage, positioning, and contextual behavior.
3. **Product HSD/BRD:** Data, calculation, completion criteria, and business workflows.
4. **Human Approval:** Authorization for additional usage outside approved requirements.
5. **General UI/UX Principles:** Fallback when GEMS has no specific guidance.

GEMS defines component design. HSD/BRD defines progress meaning.

Read only relevant references for the requested interface.

## 2. Component Selection & Usage

### 2.1 Component Selection Matrix

| User Requirement | Component | Example |
|---|---|---|
| Display measurable completion | Progress Bar | 70% completed |
| Display task completion | Progress Bar | 7 of 10 tasks |
| Display actual upload progress | Progress Bar | File upload |
| Display processing progress | Progress Bar | Data processing |
| Display video progress | Video Indicator | Video playback |
| Display stopped video condition | Video Indicator | Video Stop |
| Display loading without known progress | GEMS Loading / Skeleton | Fetching data |
| Display business status | GEMS Status component | Draft, Finished |
| Display workflow stages | Approved workflow/step component | Multi-stage workflow |

### 2.2 When to Use

Use Progress Indicator when:

- Meaningful progress data is available.
- Completion can be calculated using defined rules.
- The user benefits from seeing progress or remaining work.
- HSD/BRD explicitly requires progress monitoring.
- An approved GEMS UX Pattern includes progress visualization.

### 2.3 When NOT to Use

**MUST NOT**
- Replace Status Badges with Progress Bars.
- Convert workflow statuses into percentages without defined calculations.
- Display arbitrary or fabricated progress.
- Use Progress Bar as a substitute for unknown loading.
- Add progress purely for visual decoration.
- Assume every Dashboard, Table, or Form requires progress visualization.
- Use Progress Indicator for unrelated actions or navigation.

### 2.4 AI Recommendation & Human Approval

AI SHOULD proactively identify opportunities to use Progress Indicator when meaningful data exists.

**AI MAY implement directly when:**
- HSD/BRD explicitly requires Progress Indicator; or
- An approved design or UX Pattern already establishes its use for the product.

**AI SHOULD recommend when:**
- Measurable progress data exists.
- A Progress Indicator could improve monitoring or user understanding.
- Its usage is not explicitly included in approved requirements.

**Recommendations MUST specify:**
1. Suggested placement.
2. Purpose and user benefit.
3. Available data source.
4. Progress value or calculation method.

AI MUST obtain Human Approval before implementing a newly proposed Progress Indicator outside approved requirements.

Approval does not authorize invented data, custom variants, or CCM components.

## 3. Progress Bar Component

### 3.1 Available Properties

| Property | Official Values |
|---|---|
| `Progress` | `0%`, `10%`, `20%`, `30%`, `40%`, `50%`, `60%`, `70%`, `80%`, `90%`, `100%` |
| `Label` | `Right`, `Bottom`, `Top floating`, `Bottom floating`, `False` |

Use exact GEMS Figma property names and supported variants.

### 3.2 Progress Variants

| Progress | Meaning |
|---|---|
| 0% | No measurable completion |
| 10%–90% | Partial completion |
| 100% | Completion criteria fulfilled |

**Rules**
- Display actual progress values.
- Preserve the official GEMS component structure.
- Do not assume all processes start at 0%.
- Do not invent progress variants.
- Do not automatically treat 100% as business approval or workflow completion unless requirements define it.

### 3.3 Intermediate Percentages

The referenced Figma component provides variants in 10% increments.

- Use officially supported dynamic behavior when the product requires more precise values.
- Do not create custom Figma variants.
- Do not silently round actual business data merely to fit a visual variant.
- If required precision cannot be represented through a supported implementation, request Human Approval.

## 4. Progress Label & Visual Hierarchy

### 4.1 Available Label Variants

| Label | Usage |
|---|---|
| `Right` | Percentage beside the bar |
| `Bottom` | Percentage beneath the bar |
| `Top floating` | Floating label above progress |
| `Bottom floating` | Floating label beneath progress |
| `False` | No visible percentage label |

### 4.2 Label Rules

- Follow relevant GEMS component and Page Sample usage.
- Preserve original Text Styles, alignment, and spacing.
- Maintain consistent label placement for equivalent components.
- Use supported positioning appropriate to available space.
- Do not invent additional label positions.
- Do not manually recreate floating labels.

### 4.3 Label=False

Use only when the approved GEMS context supports progress without a visible percentage.

- Preserve an understandable progress context.
- Provide accessible progress information.
- Do not hide percentages when users need precise values.

### 4.4 Visual Hierarchy

- Progress Indicator MUST support the information hierarchy.
- Do not make Progress Bar more visually dominant than the page's primary purpose unless required.
- Maintain consistency with surrounding Cards, Tables, and Dashboard components.
- Avoid unnecessary progress visualization when equivalent information is already clear.

## 5. Progress Data & Calculation

### 5.1 Data Sources

Progress values MUST originate from approved sources:

- Completed and total tasks.
- Processed and total records.
- Actual upload progress.
- Defined workflow completion data.
- Supported processing information.

### 5.2 Calculation Rules

When the approved definition is completed units divided by total units:

`Progress (%) = (Completed Units / Total Units) × 100`

**Rules**
- Use actual product data.
- Follow approved rounding and calculation methods.
- Handle zero or unavailable totals.
- Do not assume equal weighting across workflow stages.
- Do not create calculations absent from HSD/BRD.
- Do not estimate progress without an authorized method.

### 5.3 Data Consistency

- Visual progress MUST match the represented value.
- Labels MUST match actual data.
- Updates MUST reflect real process changes.
- Do not fabricate percentage increments.
- Preserve valid progress data during recoverable errors.

### 5.4 Completion Criteria

100% is allowed only when the defined completion criteria are satisfied.

**MUST NOT**
- Mark a process completed solely because a bar appears full.
- Equate 100% with approval, verification, or submission without business rules.
- Change workflow status based only on visual representation.

## 6. Video Indicator

### 6.1 Available Variants

| Property | Official Values |
|---|---|
| `Property 1` | `Video progress`, `Video Stop` |

### 6.2 Video Progress

Use for supported video playback progress.

- Use the official GEMS Video Indicator.
- Reflect actual playback data.
- Preserve original component styling.
- Follow the approved video interaction.

### 6.3 Video Stop

Use for the supported stopped-video condition.

- Preserve the official `Video Stop` variant.
- Distinguish stopped from completed.
- Do not invent unsupported video states.

### 6.4 Component Distinction

| Component | Purpose |
|---|---|
| Progress Bar | General measurable process completion |
| Video Indicator | Video-specific progress or stopped condition |

Do not use these components interchangeably.

## 7. Contextual Usage — Page Samples & UX Patterns

### 7.1 Usage Matrix

| Context | Usage | Restriction |
|---|---|---|
| Dashboard | Measurable completion metrics | Use approved calculations |
| Task Management | Completed vs total tasks | Use actual task data |
| Upload | Actual file-upload progress | No artificial percentages |
| Data Processing | Measurable processing progress | Use Loading if unknown |
| Report Generation | Supported generation progress | Do not invent progress |
| Form Completion | Approved completion calculation | No automatic field weighting |
| Table / Data List | Per-record progress | Follow GEMS Table layout |
| Detail Page | Process/task completion | Use defined progress data |
| Video | Video Indicator | Use video-specific behavior |

### 7.2 Dashboard

- Use Progress Bar for meaningful progress metrics.
- Follow GEMS Dashboard, Card, and Chart patterns.
- Do not add Progress Indicator to every metric.
- Do not replace Status Badges with progress values.
- Recommend additional progress visualization only when useful data exists.

### 7.3 Task & Workflow Management

- Follow actual task or process data.
- Preserve business completion rules.
- Do not assume equal progress weight for every workflow stage.
- Do not represent approval status as percentage without explicit requirements.

### 7.4 Upload & Data Processing

- Use actual processing information.
- Update progress from confirmed data.
- Use GEMS Loading/Skeleton if progress is unknown.
- Follow official success and error UX Patterns.
- Do not simulate arbitrary progress.

### 7.5 Form Completion

- Use only when approved requirements define completion progress or Human Approval authorizes its addition.
- Follow approved calculations.
- Do not add Progress Bar to every form.
- Do not automatically calculate progress from filled fields.

### 7.6 Table & Data List

- Use only when each relevant record has meaningful progress information.
- Follow GEMS Table sizing and density.
- Preserve consistent label placement.
- Do not overcrowd table cells.

### 7.7 Detail Page

- Display progress related to the current record.
- Use actual data and approved calculations.
- Do not invent completion metrics.

### 7.8 CRUD

**Create:** Progress MAY represent supported creation/processing progress; it does not replace success feedback.

**Read:** Display actual recorded or calculated progress.

**Update:** Reflect confirmed changes and respect permissions.

**Delete:** Use GEMS Button and confirmation patterns. Progress Indicator does not replace destructive confirmation.

## 8. Empty, Loading & Error Handling

### 8.1 Empty State

- Use the appropriate GEMS Empty State when no progress data exists.
- Distinguish missing progress from actual 0%.
- Do not automatically display 0%.
- Do not fabricate records or progress values.

### 8.2 Loading State

- Use GEMS Loading/Skeleton when progress is unknown.
- Use Progress Bar when a meaningful measurable value exists.
- Do not invent indeterminate Progress Bar variants.
- Do not display artificial percentages.

### 8.3 Error State

- Follow official GEMS Error and Notification patterns.
- Explain processing failures when necessary.
- Preserve valid progress values.
- Do not display 100% after an unsuccessful operation.
- Use approved retry actions where applicable.

### 8.4 Interrupted Processes

- Follow HSD/BRD for paused or interrupted processes.
- Preserve the last confirmed value when appropriate.
- Do not invent Pause, Failed, Interrupted, or Cancelled Progress Bar variants.
- Use appropriate GEMS Status components for separate business conditions.

## 9. Foundation & Component Integration

### 9.1 Foundation Guidelines

All Progress Indicator visuals MUST follow:

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | Official GEMS General semantic colors |
| `Foundation/typography.md` | Official GEMS Text Styles |
| `Foundation/spacing-dan-radius.md` | Spacing and radius |
| `Foundation/effect-styles.md` | Approved effects |
| `Foundation/icons.md` | General icons when applicable |
| `Foundation/design-annotations.md` | Additional approved specifications |

### 9.2 Color

- Use official GEMS General semantic colors.
- Preserve component-defined fill and background colors.
- Do not create custom success, warning, or error colors.
- Do not use CCM tokens.
- Do not hardcode HEX, RGB, or HSL.

### 9.3 Typography

- Use official GEMS Figma Text Styles.
- Preserve label styling and hierarchy.
- Maintain readable percentages.
- Do not invent font sizes, weights, or line heights.

### 9.4 Spacing & Radius

- Preserve component proportions, spacing, and radius.
- Use official GEMS spacing variables.
- Maintain consistent alignment.
- Do not manually modify internal dimensions.

### 9.5 Effects & Icons

- Use only approved GEMS effects.
- Do not add decorative shadows, gradients, or icons.
- Use official GEMS Icons only when supported by surrounding components.

### 9.6 Related Components

| Requirement | GEMS Component |
|---|---|
| Business status | Status |
| Unknown loading | Loading / Skeleton |
| Retry or Cancel | Button |
| Progress explanation | Tooltip |
| Completion feedback | Alert / Notification |
| Dashboard visualization | Chart / Card |

Use the relevant official component guidelines.

## 10. Accessibility & Responsive Rules

### 10.1 Accessibility

**MUST**
- Provide an accessible name identifying the process.
- Communicate measurable progress values.
- Maintain readable percentage labels.
- Preserve sufficient contrast.
- Avoid relying on color alone.
- Keep progress information accurate.

**MUST NOT**
- Use animation as the only progress information.
- Display misleading completion values.
- Invent unsupported interaction behavior.

### 10.2 Responsive

- Follow GEMS Page Samples and UX Patterns.
- Preserve component-defined styling and proportions.
- Maintain readable labels on smaller screens.
- Use supported Label variants according to layout.
- Adapt surrounding containers instead of creating custom sizes.
- Do not invent mobile-specific Progress Indicator variants.

## 11. AI Implementation Rules

### 11.1 Implementation Workflow

When creating Progress Indicator:

1. **Identify Purpose:** Determine whether measurable progress, loading, status, or video indication is required.
2. **Read Requirements:** Identify data source, calculation, completion criteria, and permissions.
3. **Select Component:** Choose official GEMS General Progress Bar or Video Indicator.
4. **Apply Properties:** Use supported Progress, Label, or Video Indicator variants.
5. **Apply Data:** Use actual values and approved calculations.
6. **Apply Foundation:** Preserve official color, typography, spacing, radius, and effects.
7. **Follow Context:** Use relevant GEMS Components, Page Samples, and UX Patterns.
8. **Handle States:** Apply appropriate empty, loading, completion, and error behavior.
9. **Recommend When Relevant:** Suggest Progress Indicator when meaningful data exists.
10. **Request Approval:** Obtain Human Approval before adding usage outside approved requirements.

These are implementation instructions, not a separate validation report.

### 11.2 Strict Rules

**MUST**
- Use official GEMS General Progress Indicator components.
- Preserve original Figma component references.
- Use supported Progress and Label variants.
- Represent actual measurable data.
- Follow GEMS Foundation guidelines.
- Respect business calculations and completion criteria.
- Maintain accessibility.
- Obtain Human Approval for newly proposed usage.

**MUST NOT**
- Use CCM Progress Indicator or CCM-derived styling.
- Create custom Progress or Label variants.
- Invent intermediate Figma variants.
- Hardcode component styling.
- Display fabricated percentages.
- Replace business status with Progress Bar.
- Replace Loading/Skeleton when progress is unknown.
- Assume all workflow steps have equal weight.
- Show 100% before completion criteria are satisfied.
- Invent unsupported Pause, Failed, or Success variants.
- Treat Video Indicator and Progress Bar as interchangeable.
- Implement new recommendations without Human Approval.

### 11.3 Human Approval

Request Human Approval when:

- Progress Indicator is recommended outside approved requirements.
- No suitable GEMS General component exists.
- Unsupported progress precision or visual properties are required.
- Calculations or completion criteria are undefined.
- A new workflow would otherwise need to be invented.

Combine related questions into one confirmation.

**Fallback:** Use the closest supported GEMS General component that accurately represents available information. If progress is unknown, use appropriate Loading or Status components. Never fabricate percentages or use CCM.

## 12. Official Figma References

### 12.1 Main Components

| Component | Reference |
|---|---|
| Progress Indicator Library | [GEMS Progress Indicator](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=297-22400) |
| Progress Bar | [GEMS Progress Bar](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=297-22817) |
| Video Indicator | [GEMS Video Indicator](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1870-15636) |

### 12.2 Related Guidelines

**Foundation**
- `Foundation/color.md`
- `Foundation/typography.md`
- `Foundation/spacing-dan-radius.md`
- `Foundation/effect-styles.md`
- `Foundation/icons.md`
- `Foundation/design-annotations.md`

**Components**
- `components/button.md`
- `components/tooltip.md`
- Relevant GEMS Status, Loading, Table, and Chart guidelines when available.

### 12.3 GEMS Page Samples & UX Patterns

Read only relevant references for:

- Dashboard and Metrics
- Task and Workflow Management
- Forms and Upload
- Data Tables
- Loading and Processing
- Empty and Error States
- Responsive Layouts

---

**FINAL RULE:** Progress Indicator MUST represent meaningful and measurable progress using official GEMS General components. AI SHOULD recommend it when relevant data exists, but MUST obtain Human Approval before implementing it outside approved requirements. Preserve accurate data, supported variants, GEMS Foundation styling, and accessibility. Never use CCM or invent unsupported behavior.

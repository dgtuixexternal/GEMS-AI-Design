
# GEMS Design System — Components / Progress Steps

> **MANDATORY:** All multi-step progress interfaces MUST use official GEMS General Progress Steps components and supported variants. Preserve original component structure, sizes, states, icons, typography, spacing, and responsive behavior. Custom and CCM-specific components are prohibited.

## 1. Sources & Priority

**Official References**
- [GEMS Progress Steps](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-11327)
- [GEMS Step Icon Base](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-35052)
- [GEMS Step Base](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-35134)
- [Progress Icons Centered](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-36119)
- [Progress Minimal Icons](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-35997)
- [Progress Minimal Icons Connected](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-35945)
- [Progress Text with Line](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-36088)
- [Progress Icons with Text](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=240-36288)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1105-7310)

**Priority Order**
1. **Official Progress Steps Components:** Source of truth for structure, variants, properties, and states.
2. **GEMS Foundation & Components:** Source of truth for typography, icons, spacing, colors, and related controls.
3. **Page Samples & UX Patterns:** Reference for contextual application and navigation behavior.
4. **Product Requirements (HSD/BRD):** Define process stages, status transitions, and user permissions.
5. **General UI/UX Principles:** Fallback only when GEMS provides no specific guidance.

**Restrictions**
- MUST use official GEMS General Progress Steps components.
- MUST NOT use CCM-specific components or patterns.
- MUST NOT recreate Progress Steps with custom lines, circles, or icons.
- MUST NOT invent unsupported states, variants, or visual properties.

---

## 2. Purpose & Usage

Progress Steps communicates a user's position within a structured multi-step process.

It helps users understand:
- Which steps are completed.
- Which step is currently active.
- Which steps remain incomplete.
- How stages relate to the overall workflow.

### When to Use

| Context | Recommendation |
|---|---|
| Multi-step Form | Use Progress Steps when users complete stages sequentially |
| Onboarding / Registration | Use when the process has defined stages |
| Setup / Configuration Wizard | Use for meaningful sequential tasks |
| Data Submission Workflow | Use when multiple stages require user interaction |
| Process Detail | Use only when displaying defined stages improves understanding |
| Approval Workflow | Use only if the product defines supported stages and transitions |
| Single-step Form | Do not use Progress Steps |
| General CRUD Action | Do not automatically use Progress Steps |
| Percentage Completion | Use Progress Indicator |
| Simple Status | Use Badge |
| Status History / Audit Trail | Follow the relevant history or timeline pattern |
| Navigation Between Sections | Use Tabs or Application Navigation when appropriate |

### Usage Rules

- MUST use Progress Steps only when the process contains meaningful stages.
- MUST define stages based on HSD/BRD.
- MUST communicate the actual current process position.
- MUST maintain consistent step labels and order.
- MUST follow GEMS Page Samples and UX Patterns.
- MUST NOT invent additional business stages to justify the component.
- MUST NOT use Progress Steps merely as decoration.

**Core Principle:** A process having multiple statuses does not automatically mean it requires Progress Steps.

---

## 3. Official Step States

### Step Icon Base

**Component:** `_Step icon base`  
**Figma Node:** `240:35052`

### Available Properties

| Property | Available Values |
|---|---|
| `Status` | `Incomplete`, `Current`, `Complete`, `Rejected` |
| `Size` | `sm`, `md`, `lg` |
| `State` | `Default`, `Hover`, `Focused` |

**Note:** The `Rejected` examples are shown for specific `sm` configurations. Do not assume every combination of `Rejected`, Size, and State is available; use only variants confirmed in the official component.

### Status Meaning

| Status | Meaning |
|---|---|
| `Incomplete` | Step has not been completed |
| `Current` | Step currently active |
| `Complete` | Step successfully completed |
| `Rejected` | Step rejected when supported by the workflow and component |

### State Rules

- MUST use official status visuals and GEMS color tokens.
- MUST show the actual current stage.
- MUST represent completed steps accurately.
- MUST distinguish incomplete and completed stages.
- MUST use Rejected only when the actual workflow has a rejection outcome.
- MUST NOT treat Rejected as a universal Error state.
- MUST NOT mark steps Complete before their completion criteria are satisfied.
- MUST NOT create custom status colors or icons.

### Interaction States

| State | Usage |
|---|---|
| `Default` | Normal display |
| `Hover` | Supported pointer interaction |
| `Focused` | Supported keyboard focus |

A visual Hover or Focused variant does not automatically mean users may navigate to that step.

Step navigation permissions MUST follow HSD/BRD and the approved UX Pattern.

---

## 4. Official Step Base

**Component:** `_Step base`  
**Figma Node:** `240:35134`

### Available Properties

| Property | Available Values |
|---|---|
| `Status` | `Incomplete`, `Current`, `Complete` |
| `Size` | `sm`, `md`, `lg` |
| `Type` | `Text line`, `Icon only`, `Icon left`, `Icon top`, `Featured icon left`, `Featured icon top` |
| `State` | `Default`, `Hover`, `Focus` |

### Type Selection

| Type | Recommended Usage |
|---|---|
| `Text line` | Text-focused stage with line-based progress |
| `Icon only` | Compact progress visualization |
| `Icon left` | Stage content with supporting icon positioned left |
| `Icon top` | Stage content with supporting icon positioned above |
| `Featured icon left` | Stage requiring an official Featured Icon on the left |
| `Featured icon top` | Stage requiring an official Featured Icon above |

### Selection Rules

- MUST choose Type based on content complexity and visual hierarchy.
- MUST use official GEMS Icons and Featured Icons.
- MUST preserve the original icon size and placement.
- MUST use official Text Styles.
- MUST select a supported Size.
- MUST NOT manually rearrange icon and text positions.
- MUST NOT invent Type combinations or unsupported states.

**Important:** `_Step base` and `_Step icon base` have different supported properties. Do not assume a Status available in one is available in the other.

---

## 5. Available Progress Steps Patterns

GEMS provides multiple official compositions.

| Pattern | Primary Usage |
|---|---|
| Progress Icons Centered | Multi-step process with centrally arranged stage icons |
| Progress Minimal Icons | Compact visual progress |
| Progress Minimal Icons Connected | Compact connected stages |
| Progress Text with Line | Text-based stages with progress lines |
| Progress Icons with Text | Stage icons accompanied by labels or descriptions |

AI MUST select the pattern according to the information users need—not visual preference alone.

---

## 6. Progress Icons Centered

**Figma Node:** `240:36119`

### Available Properties

| Property | Available Values |
|---|---|
| `Size` | `sm`, `md`, `lg` |
| `Steps` | `3`, `4` |
| `Type` | `Icon`, `Featured icon` |
| `Breakpoint` | `Desktop`, `Mobile` |

### Usage

Use when a process has three or four defined stages and an icon-centered representation improves comprehension.

### Rules

- MUST use `Steps=3` or `Steps=4` according to the actual workflow.
- MUST choose `Icon` or `Featured icon` based on official usage.
- MUST use supported Desktop/Mobile variants.
- MUST preserve stage sequence and alignment.
- MUST NOT force a process with a different number of stages into an unsupported configuration.
- MUST NOT add artificial stages to reach three or four steps.

---

## 7. Progress Minimal Icons

**Figma Node:** `240:35997`

### Available Properties

| Property | Available Values |
|---|---|
| `Size` | `sm`, `md`, `lg` |
| `Text` | `True`, `False` |
| `Breakpoint` | `Desktop`, `Mobile` |

### Usage

Use when compact progress representation is appropriate.

**Rules**
- MUST use `Text=True` when progress text is needed.
- MUST use `Text=False` only when users can understand progress through the supported surrounding context and accessible labeling.
- MUST preserve official icon spacing and appearance.
- MUST NOT remove necessary progress information merely to save space.

### Progress Minimal Icons Connected

**Figma Node:** `240:35945`

**Available Properties**

| Property | Available Values |
|---|---|
| `Size` | `sm`, `md`, `lg` |
| `Breakpoint` | `Desktop`, `Mobile` |

Use when a compact connected sequence is appropriate.

- MUST preserve official connectors.
- MUST maintain accurate completion and current-step indication.
- MUST NOT add custom connector lines.

---

## 8. Progress Text with Line

**Figma Node:** `240:36088`

### Available Properties

| Property | Available Values |
|---|---|
| `Size` | `sm`, `md`, `lg` |
| `Breakpoint` | `Desktop`, `Mobile` |

### Usage

Use when step names and short explanations are essential to understanding the workflow.

Examples:
- Multi-stage registration.
- Structured setup process.
- Sequential data-entry workflow.

### Rules

- MUST use meaningful stage titles.
- SHOULD provide descriptions only when they improve understanding.
- MUST preserve the official line, text hierarchy, and status appearance.
- MUST use the approved Desktop/Mobile layout.
- MUST NOT overload every step with long descriptions.
- MUST NOT invent stages or progress details.

---

## 9. Progress Icons with Text

**Figma Node:** `240:36288`

### Available Properties

| Property | Available Values |
|---|---|
| `Size` | `sm`, `md`, `lg` |
| `Connector` | `True`, `False` |
| `Type` | `Icon`, `Icon featured` |

### Usage

Use when each stage requires a recognizable icon and supporting text.

### Rules

- MUST use `Connector=True` only when the connected presentation is appropriate.
- MUST use `Connector=False` when the official unconnected presentation is required.
- MUST use official GEMS Icons or Featured Icons.
- MUST preserve icon placement, spacing, and text hierarchy.
- MUST NOT add manual connectors.
- MUST NOT invent a Breakpoint property for this component when it is not defined.

---

## 10. Choosing the Correct Pattern

| User Need | Recommended Pattern |
|---|---|
| Compact progress without extensive descriptions | Progress Minimal Icons |
| Compact progress with visible connected sequence | Progress Minimal Icons Connected |
| Three or four clearly defined stages | Progress Icons Centered |
| Stage titles and descriptions are important | Progress Text with Line |
| Icons and supporting stage text are important | Progress Icons with Text |
| Continuous percentage or quantity | Progress Indicator |
| Single process status | Badge |
| Historical list of events | Approved History/Timeline pattern |

### Pattern Selection Rules

- MUST consider stage count, information density, viewport, and workflow purpose.
- MUST use the simplest official pattern that communicates the process clearly.
- MUST NOT use a more complex pattern without a meaningful benefit.
- MUST NOT substitute Progress Steps for unrelated status or navigation components.

**Core Principle:** The best Progress Steps pattern is the one that makes the process understandable with the least unnecessary visual complexity.

---

## 11. Progress Steps in CRUD & Workflows

Progress Steps MAY support CRUD workflows when those workflows genuinely contain multiple stages.

### CRUD Usage Matrix

| Operation | Usage |
|---|---|
| Create | Use for approved multi-step data creation |
| Read | Display current stage when the process itself is important |
| Update | Use for approved multi-step editing |
| Delete | Usually use Modal confirmation, not Progress Steps |
| Approval / Revision | Use only when supported by defined workflow stages |

### Create & Update

- MUST show the correct current step.
- MUST preserve entered data when moving between supported steps.
- MUST validate required fields before allowing progression when specified.
- MUST use official GEMS Buttons for Next, Back, Save, or Submit.
- MUST prevent users from bypassing required steps.
- MUST NOT automatically save or submit merely because the step indicator changes.

### Process Detail

- MAY show progress stages when users need to understand the current process position.
- MUST reflect actual backend/business statuses.
- MUST NOT invent progress stages or completion conditions.
- MUST NOT misrepresent a historical status timeline as an interactive wizard.

### Approval / Revision / Rejection

- MUST follow HSD/BRD for stage transitions.
- MUST distinguish active, completed, incomplete, and supported rejected outcomes.
- MUST NOT show Rejected unless that outcome exists in the workflow.
- MUST NOT assume every rejection restarts the process.
- MUST NOT change workflow behavior based solely on the visual component.

---

## 12. Step Navigation & Validation

Step navigation behavior MUST follow the approved workflow.

### Navigation Rules

- Completed steps MAY be revisited only when permitted.
- Future steps MUST NOT be accessible when prerequisites are unmet.
- Current step MUST match the actual active stage.
- Back navigation MUST preserve relevant entered data.
- Next navigation MUST respect required validation.
- Final submission MUST use a separate approved action.

### Validation Rules

- MUST use official GEMS Input and validation components.
- MUST show errors within the relevant step.
- MUST prevent invalid progression when required.
- MUST preserve valid information.
- MUST NOT mark a step Complete merely because the user visited it.
- MUST NOT skip validation to make the progress indicator advance.

### Completion

A step becomes Complete only when its required completion conditions have been satisfied.

**Important:** UI navigation state and business process state are related but not always identical. Follow the actual workflow definition.

---

## 13. Responsive Behavior

### Desktop

- MUST use official Desktop variants when available.
- MUST preserve stage order, spacing, connectors, and text hierarchy.
- MUST maintain readable labels and accessible controls.

### Mobile

- MUST use official Mobile variants when available.
- MUST preserve the supported responsive presentation.
- MUST maintain access to relevant progress information.
- MUST preserve logical stage order.
- MUST NOT manually shrink Desktop variants to simulate Mobile.
- MUST NOT hide required stages without an approved alternative.

For components without a defined Breakpoint property, follow their official usage and approved GEMS Page Samples.

Request Human Approval if the required responsive behavior is unsupported.

---

## 14. Accessibility

Progress Steps MUST:

- Communicate the current stage programmatically when appropriate.
- Preserve a logical reading order.
- Provide meaningful stage names.
- Support keyboard focus for genuinely interactive steps.
- Maintain visible focus indicators.
- Distinguish Completed, Current, and Incomplete beyond color alone.
- Provide accessible labels for icon-only presentations.
- Maintain adequate contrast using official GEMS colors.
- Avoid presenting non-interactive stages as clickable controls.
- Follow the project's accessibility requirements.

---

## 15. Foundation & Component Dependencies

Progress Steps MUST follow existing GEMS guidelines.

### Foundation

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | Official General and semantic colors |
| `Foundation/typography.md` | Official GEMS Text Styles |
| `Foundation/spacing-dan-radius.md` | Spacing, dimensions, and radius |
| `Foundation/effect-styles.md` | Focus rings, borders, and effects |
| `Foundation/icons.md` | Standard step icons and official sizes |
| `Foundation/misc-icons.md` | Featured Icons when applicable |
| `Foundation/design-annotations.md` | Applicable layout and interaction annotations |

### Related Components

Follow the corresponding GEMS guidelines when applicable:

- `button.md`
- `input.md`
- `dropdown.md`
- `modal.md`
- `progress-indicator.md`
- `badge.md`
- `alert.md`
- `notification.md`

Use the repository's actual filenames if different.

### Dependency Rules

- MUST use official GEMS General and semantic colors.
- MUST preserve official Text Styles.
- MUST preserve component sizes, connectors, spacing, and alignment.
- MUST use approved GEMS Icons and Featured Icons.
- MUST use official nested components for navigation, forms, and feedback.
- MUST NOT hardcode HEX/RGB/HSL or unsupported typography, spacing, and effects.
- MUST NOT introduce CCM-specific components or styling.
- MUST NOT override original component properties.

---

## 16. Strict Rules

### MUST

- Use official GEMS General Progress Steps components.
- Select the appropriate pattern based on workflow purpose.
- Use only supported Sizes, Types, States, and component properties.
- Display accurate Current, Complete, and Incomplete stages.
- Use Rejected only where officially supported and relevant.
- Preserve original component structure and visual properties.
- Follow HSD/BRD for step order and business transitions.
- Follow GEMS Page Samples and UX Patterns.
- Use official GEMS Buttons and Inputs for step interactions.
- Apply relevant Foundation guidelines.

### MUST NOT

- Use CCM-specific components or patterns.
- Create custom step indicators, icons, or connectors.
- Invent unsupported States, Sizes, Types, or Breakpoints.
- Add artificial steps to match an available visual variant.
- Use Progress Steps for ordinary statuses or percentage values.
- Mark incomplete stages as completed.
- Skip required validation.
- Make non-interactive steps clickable without a defined requirement.
- Invent approval, rejection, or revision workflow stages.
- Replace Progress Indicator, Badge, Tabs, or History components without contextual justification.
- Recreate official instances with manually constructed frames.
- Introduce unsupported responsive layouts or interactions.

---

## 17. AI Implementation Instructions

When generating UI using GEMS:

1. **Identify Process:** Determine whether the task contains meaningful sequential stages.
2. **Determine Necessity:** Use Progress Steps only when it improves workflow understanding.
3. **Retrieve Official Component:** Select the appropriate Progress Steps composition from the official Figma references.
4. **Select Properties:** Use supported Size, Type, Steps, Status, Connector, Text, State, and Breakpoint values as applicable.
5. **Define Workflow:** Apply actual stage names, order, completion conditions, and permissions from HSD/BRD.
6. **Configure Navigation:** Follow official Button, Input, validation, and submission patterns.
7. **Preserve GEMS:** Maintain original component structure and relevant Foundation guidelines.

**Human Approval Required When:**
- The required stage count cannot be represented by an official composition.
- A required progress state or interaction is unsupported.
- Step-navigation rules cannot be determined from HSD/BRD.
- A necessary responsive behavior is not specified by GEMS.
- Product requirements conflict with official component specifications.

Combine related clarification questions into one confirmation whenever possible.

If the official component or property cannot be accessed or verified, request the required Figma access or specifications. Do not invent unsupported details.

---

## Final Instruction

**AI MUST use official GEMS General Progress Steps components, select the correct pattern and supported properties, and display accurate stages based on the actual product workflow.**

**Progress Steps represents structured process stages—not arbitrary status labels, percentage indicators, or decorative navigation.**

**Step completion, navigation, validation, and rejection behavior MUST follow HSD/BRD.**

**Custom components, unsupported variants, invented stages, and CCM-specific patterns are strictly prohibited.**

**GEMS Design System is the single source of truth for Progress Steps visual specifications and supported interaction behavior.**

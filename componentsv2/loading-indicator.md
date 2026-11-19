
# GEMS Design System — Components / Loading Indicator

> **MANDATORY:** All loading indicators MUST use the official GEMS General Loading Indicator component. Preserve supported Styles, Sizes, colors, typography, and visual behavior. Custom spinners, unsupported variants, and CCM-specific patterns are prohibited.

## 1. Sources & Priority

**Official References**
- [GEMS Loading Indicator](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=743-3914)
- [GEMS Loading Indicator Variants](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=743-4321)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1105-7310)

**Priority Order**
1. **Official Loading Indicator:** Source of truth for Styles, Sizes, visual appearance, and supported properties.
2. **GEMS Components:** Follow loading behavior defined by Button, Input, Data Table, Modal, and other components.
3. **GEMS Foundation:** Source of truth for colors, typography, spacing, and effects.
4. **Page Samples & UX Patterns:** Reference for contextual loading placement.
5. **Product Requirements (HSD/BRD):** Determine processing behavior and user feedback.
6. **General UI/UX Principles:** Fallback only when GEMS provides no specific guidance.

**Component Restrictions**
- MUST use official GEMS General Loading Indicator at node `743:4321`.
- MUST NOT create custom spinner components.
- MUST NOT use unsupported styles, sizes, or animation patterns.
- MUST NOT use CCM-specific components or styling.

---

## 2. Purpose & Usage

Loading Indicator communicates that an operation is in progress and its result is not yet available.

It helps users understand that the application is processing a request.

### When to Use

| Context | Recommendation |
|---|---|
| Initial Page Loading | Use when essential content is being retrieved |
| Data Table Loading | Use when table data is being fetched or refreshed |
| Form Submission | Follow official Button/Modal loading behavior |
| Data Fetching | Use within the affected content area |
| File Upload | Use Loading Indicator or Progress Indicator based on available progress |
| Search Results | Use when asynchronous results are being retrieved |
| Dashboard Data Loading | Use within the relevant widget or content area |
| Background Processing | Use when user feedback is necessary |
| Instant Interaction | No loading indicator required |
| Completed Operation | Use appropriate success feedback |
| Failed Operation | Use appropriate error feedback |
| Measurable Progress | Prefer Progress Indicator when the progress value is known |

### Usage Rules

- MUST display loading only while an operation is genuinely in progress.
- MUST communicate loading within the relevant interaction scope.
- MUST follow GEMS Page Samples and UX Patterns.
- MUST preserve existing content when appropriate.
- MUST remove loading when the operation completes or fails.
- MUST NOT display loading merely for visual decoration.
- MUST NOT use Loading Indicator as a substitute for success, error, or empty states.

**Core Principle:** Loading feedback must match the operation being performed—not automatically cover the entire screen.

---

## 3. Available Styles & Sizes

**Official Component:** `Loading indicator`  
**Figma Node:** `743:4321`

### Component Properties

| Property | Available Values |
|---|---|
| `Style` | `Line simple`, `Line spinner`, `Dot circle` |
| `Size` | `sm`, `md`, `lg`, `xl` |

### Official Variants

| Style | sm | md | lg | xl |
|---|---|---|---|---|
| `Line simple` | Available | Available | Available | Available |
| `Line spinner` | Available | Available | Available | Available |
| `Dot circle` | Available | Available | Available | Available |

**Total:** 12 official configurations.

### Variant Rules

- MUST use one of the 12 supported configurations.
- MUST preserve the original loading animation and visual appearance.
- MUST preserve official dimensions for the selected Size.
- MUST use official GEMS General color tokens.
- MUST NOT invent additional Styles or Sizes.
- MUST NOT manually scale loading graphics.
- MUST NOT alter stroke width, dot geometry, or animation without an approved component specification.

---

## 4. Loading Style Selection

Select Style according to the official GEMS pattern and surrounding UI.

| Style | Visual Characteristic | Usage Guidance |
|---|---|---|
| `Line simple` | Circular loading indicator with a track | Use when the approved GEMS pattern calls for a tracked spinner |
| `Line spinner` | Circular line-based spinner | Use when the approved GEMS pattern calls for a simpler spinner |
| `Dot circle` | Circular sequence of dots | Use when the approved GEMS pattern calls for a dot-based indicator |

### Style Rules

- MUST follow the relevant GEMS Component, Page Sample, or UX Pattern when selecting Style.
- MUST maintain consistency for equivalent loading contexts.
- MUST NOT mix different loading Styles arbitrarily within the same interface.
- MUST NOT select Style solely based on decorative preference.
- MUST NOT create custom animation timing or motion effects.

**Important:** Style names describe official visual variants. They do not define separate business-processing states.

---

## 5. Loading Size Selection

Choose Size based on the official component layout and the available content area.

### General Guidance

| Size | Context |
|---|---|
| `sm` | Compact loading areas when supported |
| `md` | Standard content-level loading |
| `lg` | Larger content areas |
| `xl` | Prominent loading areas when appropriate |

These are contextual recommendations. Exact placement and dimensions MUST follow the official GEMS implementation.

### Size Rules

- MUST preserve official Size definitions.
- MUST select Size according to the containing component and viewport.
- MUST ensure sufficient space for the loading indicator and label.
- MUST NOT enlarge a small indicator manually.
- MUST NOT use oversized indicators inside compact components.
- MUST NOT force all loading contexts to use the same Size.

---

## 6. Loading Scope & Placement

Loading Indicator placement MUST correspond to the operation's actual scope.

### Scope Matrix

| Operation | Recommended Loading Scope |
|---|---|
| Entire page cannot render yet | Page-level loading |
| One table is fetching data | Table content area |
| One card is refreshing | Affected card |
| One dashboard widget is loading | Affected widget |
| Search is processing | Search results area or supported search control |
| Modal is submitting | Modal action/loading state |
| Button triggers an async action | Official Button loading state |
| File upload is processing | Upload component area |

### Placement Rules

- MUST display loading near the affected content or action.
- MUST preserve the surrounding layout where possible.
- MUST prevent unnecessary layout shifts.
- MUST keep unrelated areas usable when they are not affected.
- MUST NOT block the entire application for a local operation.
- MUST NOT display duplicate indicators for the same operation unless an approved pattern requires them.
- MUST NOT place loading arbitrarily inside Page Header, Card Header, or other components.

**Core Principle:** Local operations should generally use local loading feedback.

---

## 7. Loading in CRUD Operations

### CRUD Usage Matrix

| Operation | Loading Behavior |
|---|---|
| Create | Display processing feedback during submission |
| Read | Display loading while retrieving data |
| Update | Display processing feedback while saving changes |
| Delete | Display processing feedback after confirmation |
| Bulk Action | Display feedback for the active bulk operation |

### Create & Update

- MUST use official GEMS Button loading states when available.
- MUST prevent unintended duplicate submission.
- MUST preserve entered data during processing.
- MUST display success or error feedback after receiving the result.
- MUST NOT clear form fields before successful submission unless the approved workflow specifies otherwise.
- MUST NOT show success while the request is still processing.

### Read / Fetch

- MUST display loading in the affected data region.
- MUST use official Data Table or content loading patterns when available.
- MUST replace loading with actual data, an empty state, or an error state when appropriate.
- MUST NOT show an empty-state message while data is still being retrieved.

### Delete

- MUST follow the approved Delete confirmation workflow.
- MUST NOT execute deletion before confirmation.
- MUST display processing feedback after confirmation when needed.
- MUST prevent repeated Delete requests.
- MUST update the affected data after successful deletion.
- MUST NOT treat loading completion as proof of successful deletion.

### Bulk Operations

- MUST communicate that the selected operation is processing.
- MUST prevent accidental repeated execution.
- MUST preserve accurate selection and operation state.
- MUST follow the approved handling of partial failures.
- MUST NOT invent success feedback before the backend confirms the result.

---

## 8. Loading in Forms & Modals

### Form Submission

- MUST follow the official GEMS Button and Input specifications.
- MUST validate required fields before submission.
- MUST show processing feedback only after a valid operation starts.
- MUST prevent repeated submission while processing.
- MUST preserve entered values if the operation fails.

### Modal Submission

- MUST follow `modal.md`.
- MUST use the official Modal action loading behavior.
- MUST preserve the Modal and its context during processing when required.
- MUST prevent duplicate confirmation actions.
- MUST display relevant error feedback when the request fails.
- MUST NOT automatically close the Modal merely because the loading animation stops.

### Rules

- Do not add a separate large Loading Indicator when the official Button loading state already provides sufficient feedback.
- Do not create custom loading overlays inside Modal without an approved GEMS pattern.
- Keep loading behavior consistent with the actual action.

---

## 9. Loading vs. Progress Indicator

Loading Indicator and Progress Indicator serve different purposes.

| Component | Usage |
|---|---|
| Loading Indicator | Operation in progress; exact completion progress is unavailable |
| Progress Indicator | Quantifiable completion or progress is available |
| Progress Steps | Structured sequential workflow stages |
| Notification / Alert | Operation result or important system feedback |
| Empty State | No data exists after loading completes |

### Selection Rules

- MUST use Loading Indicator for indeterminate processing.
- SHOULD use Progress Indicator when reliable progress measurements are available and useful.
- MUST use Progress Steps for structured workflow stages.
- MUST use official feedback components for success and errors.
- MUST NOT display fabricated percentages.
- MUST NOT use Loading Indicator as a permanent placeholder.

**Core Principle:** Loading communicates activity; Progress Indicator communicates measurable completion.

---

## 10. Loading States & Lifecycle

### Functional States

| State | Expected Behavior |
|---|---|
| Idle | No loading indicator |
| Loading | Official indicator is visible |
| Success | Indicator stops; successful result appears |
| Error | Indicator stops; relevant error feedback appears |
| Empty Result | Indicator stops; official empty state appears when appropriate |

### Behavior Rules

- MUST synchronize loading visibility with the actual operation state.
- MUST remove loading after success or failure.
- MUST prevent stale operations from incorrectly replacing newer results.
- MUST preserve relevant user input and page context.
- MUST avoid unnecessary flickering for very brief operations when the approved UX pattern supports it.
- MUST NOT leave an indicator running indefinitely after an operation has resolved.
- MUST NOT use arbitrary loading durations to simulate processing.
- MUST NOT display success before the request succeeds.

### Long-running Operations

When an operation takes longer than expected:

- Keep users informed through an appropriate approved feedback pattern.
- Allow cancellation or retry only when the operation supports it.
- Communicate meaningful errors or timeouts.
- Do not invent a completion estimate or percentage.

---

## 11. Loading Text & UX Writing

The official GEMS examples include a loading label.

### Usage Rules

- MUST preserve the official Typography and layout when a label is used.
- MUST use concise, meaningful loading messages.
- SHOULD describe the operation when additional clarity is useful.
- MUST NOT show misleading completion statements during processing.
- MUST NOT use animated text or custom typography outside GEMS.

### Examples

| Context | Suggested Label |
|---|---|
| General Loading | Memuat... |
| Fetching Data | Memuat data... |
| Saving | Menyimpan perubahan... |
| Submitting | Mengirim data... |
| Uploading | Mengunggah file... |
| Deleting | Menghapus data... |
| Searching | Mencari data... |

These labels are contextual examples, not fixed component variants.

Use terminology matching the product and its approved language conventions.

---

## 12. Responsive Behavior

- MUST preserve official Loading Indicator Size and Style.
- MUST position loading according to the relevant Desktop or Mobile layout.
- MUST maintain readable labels.
- MUST preserve adequate spacing around the indicator.
- MUST NOT manually resize the spinner for different breakpoints.
- MUST NOT invent a `Breakpoint` property for the Loading Indicator component.
- MUST NOT create unsupported mobile-specific loading animations.

Responsive positioning MUST follow the parent component and the relevant GEMS Page Samples.

---

## 13. Accessibility

Loading Indicator implementations MUST:

- Communicate processing state to assistive technologies.
- Provide meaningful accessible status information.
- Avoid relying solely on visual animation.
- Preserve keyboard access to unaffected interface areas.
- Prevent duplicate actions when processing.
- Maintain sufficient contrast using official GEMS tokens.
- Respect reduced-motion requirements where supported by the implementation.
- Avoid unnecessary focus movement.
- Communicate success or failure after processing completes.

Loading feedback MUST remain understandable even when animation cannot be perceived.

---

## 14. Foundation & Component Dependencies

Loading Indicator MUST follow existing GEMS guidelines.

### Foundation

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | Official General and semantic colors |
| `Foundation/typography.md` | Official GEMS Text Styles |
| `Foundation/spacing-dan-radius.md` | Spacing, dimensions, and layout |
| `Foundation/effect-styles.md` | Official visual effects when applicable |
| `Foundation/design-annotations.md` | Relevant component and interaction annotations |

### Related Components

Follow the corresponding GEMS guidelines when applicable:

- `button.md`
- `input.md`
- `modal.md`
- `data-table.md`
- `progress-indicator.md`
- `progress-steps.md`
- `alert.md`
- `notification.md`

Use the repository's actual filenames if different.

### Dependency Rules

- MUST use official GEMS General color tokens.
- MUST preserve original Loading Indicator Styles and Sizes.
- MUST use official Text Styles for loading labels.
- MUST preserve spacing and positioning defined by the parent component.
- MUST use official nested loading states where available.
- MUST NOT hardcode HEX/RGB/HSL or unsupported dimensions.
- MUST NOT introduce CCM-specific styling or components.

---

## 15. Strict Rules

### MUST

- Use official GEMS General Loading Indicator.
- Select one of the 12 supported configurations.
- Choose Style and Size according to the relevant GEMS component context.
- Display loading only while an operation is genuinely in progress.
- Match loading placement to the affected content or action.
- Prevent unintended repeated submissions.
- Remove loading after success or failure.
- Use official success, error, and empty-state feedback.
- Follow GEMS Page Samples and UX Patterns.
- Apply relevant Foundation guidelines.

### MUST NOT

- Create custom spinners or loading animations.
- Use unsupported Styles or Sizes.
- Modify original spinner geometry or styling.
- Display loading without an actual processing state.
- Block an entire page for an unrelated local operation.
- Add redundant indicators when the parent component has adequate loading feedback.
- Use Loading Indicator for known percentage completion.
- Use Loading Indicator as success or error feedback.
- Show empty states before loading completes.
- Invent loading durations, completion estimates, or progress percentages.
- Leave loading visible after an operation resolves.
- Use CCM-specific components or visual patterns.

---

## 16. AI Implementation Instructions

When generating UI using GEMS:

1. **Identify Operation:** Determine whether an asynchronous process requires loading feedback.
2. **Determine Scope:** Identify whether the process affects a Button, Form, Modal, Table, Card, Widget, or entire page.
3. **Retrieve Official Component:** Use Loading Indicator at node `743:4321` or the parent component's official loading state when appropriate.
4. **Select Variant:** Choose supported `Style` and `Size` values according to the GEMS reference.
5. **Configure Behavior:** Display loading during processing and remove it after resolution.
6. **Apply Result Feedback:** Use official success, error, empty-state, or progress components as appropriate.
7. **Preserve GEMS:** Follow original component properties, Foundation tokens, Page Samples, and UX Patterns.

**Human Approval Required When:**
- A necessary loading pattern is unavailable in the official components.
- A new animation or custom loading behavior is requested.
- The required operation feedback conflicts with official GEMS specifications.
- A responsive loading layout cannot be represented by approved patterns.

Combine related clarification questions into one confirmation whenever possible.

If the official component cannot be accessed or verified, request the required Figma access or specifications. Do not invent unsupported details.

---

## Final Instruction

**AI MUST use official GEMS General Loading Indicator components or supported parent-component loading states, selecting only approved Styles and Sizes.**

**Loading MUST represent a real processing operation and appear within the appropriate interaction scope.**

**Use Progress Indicator for measurable completion and Progress Steps for structured workflow stages.**

**Custom spinners, unsupported animations, fabricated progress, and CCM-specific patterns are strictly prohibited.**

**GEMS Design System is the single source of truth for Loading Indicator visual specifications and supported interaction behavior.**

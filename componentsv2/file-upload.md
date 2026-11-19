
# GEMS Design System — Components / File Upload

> **MANDATORY:** All file-upload interfaces MUST use official GEMS File Upload components, supported variants, and existing Design System properties. AI MUST select the appropriate upload pattern based on product requirements, file context, and GEMS UX references. Never recreate or substitute the official component.

## 1. Sources & Priority

**Official Figma References**
- [GEMS File Upload](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=743-2500)
- [File Upload Base](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=743-2936)
- [File Upload Item Base](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=743-2964)
- [File Upload Main Component](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=743-3089)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1105-7310)

**Priority Order**
1. **Official File Upload Components:** Source of truth for structure, properties, sizes, states, and variants.
2. **GEMS Foundation:** Source of truth for colors, typography, spacing, radius, effects, and icons.
3. **GEMS Page Samples & UX Patterns:** Reference for placement, interaction, hierarchy, and contextual usage.
4. **HSD/BRD:** Source of truth for business requirements, supported file formats, permissions, and upload behavior.
5. **General UX Principles:** Fallback only when GEMS does not define a specific usage pattern.

If references differ, official GEMS component specifications take visual priority. Business rules MUST follow approved HSD/BRD.

**Strict Exclusion:** CCM components, CCM variants, and CCM-specific styling are prohibited.

---

## 2. Available Components & Variants

AI MUST use only variants available in the connected GEMS Figma library.

### 2.1 File Upload Base

Official component: `_File upload base`

**Available States**

| State | Usage |
|---|---|
| `Default` | Upload area ready for user interaction |
| `Hover` | Pointer interaction when supported |
| `Loading` | Upload area is processing an operation |
| `Uploaded` | Upload area displays its uploaded condition |
| `Disabled` | Upload interaction is unavailable |

**Rules**
- Use `Default` before interaction.
- Use `Hover` only for supported pointer interaction.
- Use `Loading` when the operation is actually processing.
- Use `Uploaded` according to the official component behavior after successful upload.
- Use `Disabled` when interaction is restricted by permissions, workflow, or form state.
- Do not manually recreate these states using custom colors, borders, or icons.

`Uploaded` is a state of the upload base; it is not interchangeable with the `Complete` state of an individual file item.

### 2.2 File Upload Item Base

Official component: `_File upload item base`

**Available Properties**

| Property | Supported Values |
|---|---|
| `Type` | `Progress bar`, `Progress fill` |
| `Icon type` | `File type`, `Simple` |
| `State` | `In progress`, `Error`, `Complete` |

These properties form the supported file-item combinations.

**State Usage**

| State | When to Use |
|---|---|
| `In progress` | File upload is actively processing |
| `Error` | File validation or upload has failed |
| `Complete` | File upload has successfully completed |

**Icon Type Selection**
- `File type`: Use when the official file-type visual helps users identify the uploaded document.
- `Simple`: Use when the simpler official icon presentation is appropriate.
- Preserve the icon treatment defined by the selected GEMS variant.
- Do not replace existing file-type visuals with arbitrary emoji or external icons.

**Progress Type Selection**
- `Progress bar`: Use the official progress-bar presentation.
- `Progress fill`: Use the official progress-fill presentation.
- Select the type using relevant GEMS examples and interface context.
- Keep the same progress treatment for equivalent file items within the same upload experience.
- Do not invent additional progress styles.

### 2.3 Main File Upload Component

Official component: `File upload`

**Available Properties**

| Property | Supported Values |
|---|---|
| `Files queued` | `True`, `False` |
| `Type` | `Progress bar`, `Progress fill` |
| `Breakpoint` | `Desktop`, `Mobile` |

**Usage Rules**
- `Files queued=False`: Use the official presentation when no file is queued.
- `Files queued=True`: Use the official presentation when files are present in the queue.
- Select `Progress bar` or `Progress fill` based on supported component usage.
- Select `Desktop` or `Mobile` based on the target breakpoint.
- Preserve responsive structure and spacing provided by GEMS.
- Do not manually scale a desktop variant to imitate the mobile variant.

**Important:** A queued file is not automatically a successfully uploaded file. File status MUST reflect actual upload progress and results.

---

## 3. When to Use File Upload

Use File Upload when users need to attach or submit actual files as part of a product workflow.

### Usage Matrix

| Context | Recommended Usage |
|---|---|
| Create Data | Attach supporting files before submission |
| Edit Data | Add or replace attachments when permitted |
| Document Submission | Upload required documents |
| Approval Workflow | Attach evidence or supporting documents |
| Report Submission | Upload reports or supporting files |
| Profile / Settings | Upload an image or document when required |
| Import Data | Select files for an approved import workflow |
| Detail Page | Display existing attachments; enable upload only when editing is permitted |

Examples:
- Upload invoice or receipt.
- Attach approval evidence.
- Submit supporting documents.
- Upload report files.
- Replace an existing attachment.
- Import supported data files.

**AI MUST determine whether file upload is actually required by the product.**

Do not add File Upload merely because a page contains a form, modal, or CRUD actions.

### When NOT to Use

Do not use File Upload for:
- Ordinary text entry.
- Selecting an existing record from the system.
- Displaying read-only file information without an upload action.
- Status visualization unrelated to file processing.
- Decorative document illustrations.
- Image galleries that require viewing rather than uploading.

Use the appropriate GEMS component instead.

---

## 4. File Selection & Upload Behavior

### 4.1 Before Upload

AI MUST determine requirements from HSD/BRD or approved product specifications:

- Whether file attachment is required or optional.
- Accepted file formats.
- Maximum file size.
- Minimum or maximum file count.
- Single-file or multiple-file behavior.
- User permissions.
- Whether replacement or removal is allowed.
- When uploaded files are submitted or persisted.

Never invent upload limitations or capabilities.

### 4.2 Upload Instructions

Use concise, contextual labels and helper text.

Examples:

| Context | Suggested Label |
|---|---|
| Supporting Document | Upload Dokumen Pendukung |
| Payment Evidence | Upload Bukti Pembayaran |
| Report | Upload Laporan |
| Employee Document | Upload Dokumen Karyawan |
| Import Workflow | Upload File Import |

**Rules**
- Use terminology consistent with the product.
- Display supported formats and limits when officially defined.
- Clearly distinguish required and optional attachments.
- Use official GEMS typography and text colors.
- Do not display invented format or size restrictions.

### 4.3 Interaction

- Use the supported file-selection behavior of the GEMS component.
- Support drag-and-drop only when the component and product implementation support it.
- Provide an accessible file-selection alternative where drag-and-drop is available.
- Do not imply a file has been uploaded merely because it has been selected.
- Prevent duplicate submissions while an upload request is processing.
- Preserve other valid form data when an upload fails.

---

## 5. File Upload States & Error Handling

AI MUST distinguish file selection, upload processing, and successful completion.

| Condition | Required Behavior |
|---|---|
| Empty | Display the supported upload area without queued files |
| File Selected | Reflect the selected or queued file according to GEMS |
| Uploading | Show supported loading or progress state |
| Upload Complete | Show the official completed/uploaded presentation |
| Validation Error | Show clear file-specific validation feedback |
| Upload Error | Show the official error presentation |
| Disabled | Prevent interaction and use the official disabled state |

### Progress Rules

- Progress MUST represent real upload activity.
- Use `In progress` while the request is processing.
- Use `Complete` only after successful completion is confirmed.
- Use `Error` when validation or upload fails.
- Show numerical progress only when reliable progress data exists.
- Never fabricate percentages or simulate success.
- Use official GEMS Loading Indicator for unrelated indeterminate loading situations when appropriate.

### Validation & Recovery

When a file is invalid or upload fails:
- Explain the specific error when available.
- Preserve valid files and other completed form inputs.
- Allow correction, replacement, removal, or retry when the product supports the action.
- Do not discard unrelated files automatically.
- Do not mark failed files as completed.
- Do not submit a required attachment if its upload has not succeeded.

If several files are uploaded, handle each file's status independently where supported.

---

## 6. File Upload in CRUD & UX Patterns

### 6.1 Create

- Add File Upload only when the create flow requires attachments.
- Place it in the relevant form section according to GEMS patterns.
- Apply required-field behavior based on HSD/BRD.
- Ensure required uploads complete before final submission.
- Preserve the selected files and form context when validation fails.

### 6.2 Read / View Detail

- Display existing attachments using the appropriate GEMS data-display pattern.
- Provide preview or download actions only when supported and permitted.
- Do not display an editable upload area on a read-only screen without a valid user action.
- Use official file-type icons and related components where applicable.

### 6.3 Update

- Allow adding, replacing, or removing attachments only when authorized.
- Distinguish existing saved files from newly selected files.
- Clearly represent replacement or pending changes.
- Preserve existing files if an update fails.
- Do not overwrite an existing file merely because a new file has been selected.

### 6.4 Delete / Remove

Distinguish two operations:

1. **Remove queued file:** Removes a selected file before successful persistence.
2. **Delete saved file:** Removes an attachment already stored in the system.

**Rules**
- Follow approved permissions and HSD/BRD.
- Do not treat removing a queued file as automatically equivalent to deleting persisted data.
- Use GEMS destructive confirmation when the approved flow requires confirmation for deletion.
- Do not delete a persisted file before the required confirmation.
- Update the file list and status after a successful operation.

### 6.5 Approval, Rejection & Revision

- Upload may support approval evidence or revision attachments when required.
- File Upload does not replace the official confirmation Modal.
- Approval, rejection, and revision actions MUST follow the corresponding GEMS UX Patterns.
- Required supporting files MUST meet business requirements before the decision is submitted.

---

## 7. Layout, Placement & Responsive Usage

AI MUST follow GEMS Page Samples and UX Patterns for contextual placement.

**Placement Rules**
- Place File Upload near the related field or document requirement.
- Keep its label, helper text, file list, and feedback logically grouped.
- Maintain the official upload-area and file-item structure.
- Follow GEMS Form Section patterns when used inside a form.
- Use official responsive variants for Desktop and Mobile.
- Ensure long filenames and error messages remain readable within supported layouts.
- Follow the component's official spacing, dimensions, and alignment.

**Do Not**
- Stretch or compress official variants arbitrarily.
- Add decorative upload cards or custom drop zones.
- Insert unsupported controls into the upload component.
- Change upload icons, borders, radius, or effects manually.
- Force File Upload into every form or modal.

---

## 8. Related GEMS Guidelines

All visual and supporting components MUST follow the existing GEMS guidelines.

### Foundation Dependencies

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | Upload states, semantic colors, borders, and feedback |
| `Foundation/typography.md` | Labels, helper text, filenames, and error messages |
| `Foundation/spacing-dan-radius.md` | Internal spacing, layout gaps, and radius |
| `Foundation/effect-styles.md` | Official effects when defined by the component |
| `Foundation/icons.md` | Actions and general upload icons |
| `Foundation/misc-icons.md` | Official file-type visual assets when applicable |
| `Foundation/design-annotations.md` | Component behavior and implementation guidance |

### Related Component Guidelines

Use the relevant existing guideline when the workflow involves:
- **Button:** Browse, Submit, Retry, or supported file actions.
- **Input:** Surrounding form requirements and validation.
- **Modal:** Confirmation or file-related dialog workflows.
- **Alert / Notification:** Relevant feedback and operation results.
- **Loading Indicator:** Indeterminate processing.
- **Progress Indicator:** Progress visualization outside the built-in File Upload pattern, when appropriate.
- **Data Table:** Existing attachment records in a list.
- **Page Header / Section Header:** Placement within pages and sections.

Related guidelines apply only when the corresponding component is actually used.

**Do not replace the built-in File Upload progress presentation with another progress component merely for visual preference.**

---

## 9. Image Preview & Related Components

[Official GEMS Image Carousel](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=2741-31536)

Image Carousel is a separate component, not a File Upload variant.

Use it only when:
- Users need to view or navigate multiple images.
- The product requires image preview or gallery behavior.
- The relevant GEMS pattern supports that presentation.

Do not automatically attach Image Carousel to every upload area.

Other supplied Figma references belonging to Breadcrumbs MUST NOT be interpreted as File Upload variants.

---

## 10. Accessibility & Content Rules

AI MUST:
- Provide meaningful labels for upload controls.
- Communicate required fields clearly.
- Use readable error messages with actionable guidance.
- Preserve visible keyboard focus and accessible interaction.
- Communicate processing, completion, and failure without relying on color alone.
- Keep filename, file status, and available actions understandable.
- Respect disabled and permission-based restrictions.
- Follow supported responsive behavior.

AI MUST NOT:
- Use color as the only indication of upload status.
- Hide relevant validation feedback.
- Show false progress or completion.
- Expose unauthorized file actions.
- Add unsupported drag-and-drop or preview capabilities.
- Invent file names, upload requirements, or backend results.

---

## 11. Strict GEMS Compliance

**MUST**
- Reuse official GEMS File Upload instances when the integration supports them.
- Preserve official component structure and library references.
- Use only available properties and variants.
- Select states based on actual upload conditions.
- Match file requirements and actions to HSD/BRD.
- Use GEMS Foundation and related components consistently.
- Follow GEMS Page Samples and UX Patterns for contextual placement.
- Preserve Desktop and Mobile variant behavior.
- Use GEMS General components and styling.

**MUST NOT**
- Use CCM File Upload components, CCM variants, or CCM styling.
- Create custom upload components when the official one is available.
- Invent variants, states, sizes, icons, or progress styles.
- Hardcode unsupported HEX/RGB/HSL, typography, spacing, radius, or shadow.
- Detach official component instances without an approved need.
- Treat queued files as successfully uploaded files.
- Show success before upload completion is confirmed.
- Change business validation or permissions for visual convenience.
- Add File Upload when the product does not require it.
- Substitute Breadcrumbs or Image Carousel for File Upload.

---

## 12. AI Selection & Human Approval

Before implementing File Upload, AI MUST determine:

1. **Necessity:** Does this workflow actually require file upload?
2. **Business Requirements:** What files, constraints, permissions, and submission rules apply?
3. **Component:** Which official GEMS File Upload variant fits the context?
4. **State:** Is the file empty, queued, uploading, completed, failed, or disabled?
5. **Placement:** How is File Upload used in the relevant GEMS Page Sample or UX Pattern?
6. **Supporting Components:** Are buttons, feedback, file previews, or confirmation actions required?

Use available HSD/BRD and product context to resolve these decisions.

**Human Approval Required**

If critical requirements are missing, or the approved workflow requires behavior not supported by the existing GEMS component, AI MUST request Human Approval before introducing a new interaction or visual solution.

Combine unresolved questions into one concise confirmation covering:
- Accepted file types and limits.
- Single or multiple uploads.
- Required or optional attachments.
- Upload, replacement, and removal behavior.
- Any unsupported component requirements.

Do not repeatedly ask for information already established in the product documentation.

**Fallback:** If the official File Upload variant cannot meet a required use case, retain the closest valid GEMS pattern and explain the limitation. Do not invent or implement an unsupported variant without Human Approval.

---

## 13. Final AI Instruction

**AI MUST use official GEMS File Upload components for every supported file-upload interaction.**

Select component variants and states according to actual upload behavior, approved business requirements, and relevant GEMS Page Samples and UX Patterns.

Preserve official GEMS component properties, responsive variants, typography, colors, icons, spacing, radius, and effects.

Never use CCM components, create unsupported visual states, fabricate upload progress, or introduce custom upload patterns without Human Approval.

**GEMS Design System is the single source of truth for File Upload visual specifications.**

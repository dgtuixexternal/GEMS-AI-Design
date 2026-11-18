
# GEMS Design System — Components / Notification

> **MANDATORY:** All Notifications MUST use existing GEMS General Notification components and official Figma variants. AI MUST determine when Notification is appropriate based on product context, HSD/BRD, and GEMS Page Samples & UX Patterns. CCM components, unsupported variants, and custom Notification designs are strictly prohibited.

## 1. Sources & Priority

**Official Figma References**
- [GEMS Notification — Overview](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1813-97486)
- [GEMS Notification — Variants](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1813-98074)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1105-7310)

**Priority Order**
1. **GEMS Notification:** Official component structure, variants, dimensions, and responsive layout.
2. **GEMS Foundation:** Official color, typography, spacing, radius, effects, and icons.
3. **GEMS Page Samples & UX Patterns:** Contextual usage, positioning, and interaction examples.
4. **HSD/BRD & System Data:** Business events, messages, results, permissions, and workflow behavior.
5. **General UI/UX Principles:** Fallback only when GEMS has no specific guidance.

GEMS is the visual source of truth. HSD/BRD and actual system data define business behavior and message accuracy.

---

## 2. Purpose & When to Use

Notification provides contextual feedback about completed actions, failed operations, relevant updates, or ongoing processes without unnecessarily interrupting the user's workflow.

**Use Notification for:**
- Create, update, delete, or submit feedback.
- Confirmed success or failure of an action.
- Relevant system or activity updates.
- Important but nonblocking feedback.
- Process progress when supported and useful.

**Do not automatically display Notification for every interaction.**

### Component Selection

| User Need | Correct Component |
|---|---|
| Brief feedback after an action | **Notification** |
| Create/update/delete/submit result | **Notification** |
| Short relevant system update | **Notification** |
| Ongoing process feedback | **Notification with Progress indicator** when appropriate |
| Persistent contextual warning | **Alert** |
| Complex validation results beside data | **Alert + Field/Row Validation** |
| Confirm before deletion or submission | **Modal** |
| Error on an individual field | **Input Validation** |
| Status inside a table | **Badge** |
| No data available | **Empty State** |
| Primary action control | **Button** |

Notification MUST NOT replace Modal confirmation, persistent Alert information, or field-level validation.

---

## 3. Available Variants & Properties

Use the original GEMS Notification component instance and preserve its component reference.

### Official Properties

| Property | Available Values |
|---|---|
| `Type` | `Primary icon`, `Success icon`, `Error icon`, `Warning icon`, `Gray icon`, `No icon`, `Avatar`, `Image`, `Progress indicator` |
| `Breakpoint` | `Desktop`, `Mobile` |
| `Position` | `Top`, `Bottom` |

**Important:** These values are not freely interchangeable. Use only combinations that exist in the official GEMS component.

### Available Combinations

| Type | Desktop Top | Desktop Bottom | Mobile Top | Mobile Bottom |
|---|---|---|---|---|
| `Primary icon` | Available | Available | Available | Not available |
| `Success icon` | Available | Available | Available | Not available |
| `Error icon` | Available | Available | Available | Not available |
| `Warning icon` | Available | Available | Available | Not available |
| `Gray icon` | Available | Available | Available | Not available |
| `No icon` | Available | Available | Available | Not available |
| `Avatar` | Available | Available | Available | Not available |
| `Image` | Available | Available | Not available | Not available |
| `Progress indicator` | Available | Available | Available | Not available |

This matrix reflects the variants identified in the linked GEMS Notification component.

**Component Rules**
- MUST use existing supported Type, Breakpoint, and Position combinations.
- MUST preserve official component structure, spacing, dimensions, and visual styles.
- MUST use the correct variant instead of manually restyling another.
- MUST NOT create missing Mobile Bottom or Mobile Image variants.
- MUST NOT detach, duplicate, or reconstruct Notification instances.
- **MUST NOT use CCM components, CCM variants, or CCM styling.**

---

## 4. Notification Types & Semantic Usage

| Type | Purpose | Recommended Context |
|---|---|---|
| `Success icon` | Confirm successful action | Save, update, delete, submit completed |
| `Error icon` | Report failed action | Save failed, submission failed, processing error |
| `Warning icon` | Communicate attention or partial problem | Partial failure, relevant warning |
| `Primary icon` | Emphasized general information | System update, important activity |
| `Gray icon` | Neutral notification | General information, noncritical update |
| `No icon` | Simple text-based feedback | Short message without visual indicator |
| `Avatar` | Person-related activity | User activity, message, identity-related update |
| `Image` | Visual-content notification | Relevant image-based activity or content |
| `Progress indicator` | Ongoing operation | Upload, import, synchronization, processing |

### Semantic Selection Rules

- Choose Type according to actual meaning and content.
- `Success icon` requires confirmed successful completion.
- `Error icon` requires an actual failure.
- `Warning icon` requires a relevant risk or attention condition.
- `Primary icon` and `Gray icon` are for informational messages, not replacements for semantic errors.
- `No icon` is appropriate only when text remains understandable independently.
- `Avatar` requires a relevant person or entity identity.
- `Image` requires meaningful visual content, never decorative filler.
- `Progress indicator` requires a real ongoing process.

All icons, colors, and visual treatments MUST follow the original GEMS variant and Foundation guidelines.

---

## 5. Notification Structure & Content

Follow the actual structure supported by the selected GEMS variant.

| Element | Purpose | Rule |
|---|---|---|
| Container | Main Notification structure | Required |
| Title | Main feedback or condition | Clear and specific |
| Description | Supporting details or next step | When relevant |
| Icon | Semantic indicator | According to Type |
| Avatar | Person/entity identity | Avatar variant only |
| Image | Relevant visual content | Image variant only |
| Progress Indicator | Ongoing process feedback | Progress variant only |
| Close | Dismiss Notification | Only when supported |
| Action | Relevant follow-up action | Only when supported and required |

Not all elements must appear together. Preserve the official GEMS component composition.

### Message Formula

**Action / Condition → Result → Next Step (if needed)**

**Examples**
- "Data berhasil disimpan."
- "Perubahan gagal disimpan. Silakan coba kembali."
- "Pesanan tamu berhasil diajukan."
- "Dokumen sedang diunggah."

**Writing Rules**
- Use concise, clear, product-appropriate language.
- State the actual action or condition.
- Match business terminology in HSD/BRD.
- Avoid repeating the same information in Title and Description.
- Do not invent causes, outcomes, permissions, or next steps.
- Do not expose unnecessary technical details.
- Do not claim that a submitted request has been approved or completed unless the workflow confirms it.

---

## 6. CRUD & Workflow Usage

Use Notification after actual system events, not merely after button clicks.

| Event | Recommended Type | Example |
|---|---|---|
| Create succeeded | Success icon | Data berhasil ditambahkan |
| Create failed | Error icon | Data gagal ditambahkan |
| Update succeeded | Success icon | Perubahan berhasil disimpan |
| Update failed | Error icon | Perubahan gagal disimpan |
| Delete succeeded | Success icon | Data berhasil dihapus |
| Delete failed | Error icon | Data gagal dihapus |
| Submit succeeded | Success icon | Pengajuan berhasil dikirim |
| Submit failed | Error icon | Pengajuan gagal dikirim |
| Partial processing issue | Warning icon | Sebagian data belum diproses |
| General system update | Primary / Gray icon | Informasi telah diperbarui |
| Process running | Progress indicator | Mengimpor data |

### CRUD Behavior Rules

- Show Success only after the operation succeeds.
- Show Error when the operation fails.
- Preserve user input after failed submission when applicable.
- Provide retry guidance only when retry is available and meaningful.
- Do not assume every failure can be resolved by retry.
- Do not equate successful submission with final workflow approval.
- Destructive actions requiring confirmation MUST use Modal before execution.
- Notification reports the result; it MUST NOT replace confirmation.

### Example — Delete Flow

1. User selects **Hapus**.
2. GEMS Modal requests confirmation if required.
3. User confirms the action.
4. System processes deletion.
5. Notification displays confirmed Success or Error.

Notification MUST NOT display a success message before deletion has completed.

---

## 7. Progress Notification

Use `Type=Progress indicator` only when a process is ongoing and progress feedback is relevant.

**Recommended Context**
- Uploading documents.
- Importing records.
- Synchronizing data.
- Processing large files.
- Long-running background operations.

### Progress States

| State | Expected Behavior |
|---|---|
| Started | Inform that processing has begun |
| In Progress | Update available progress information |
| Completed | Show confirmed completion result |
| Failed | Report actual failure and next step |
| Cancelled | Reflect cancellation if supported |

**Rules**
- MUST follow actual process state.
- MUST NOT invent percentages, elapsed time, or completion estimates.
- Display determinate progress only when actual progress data exists.
- Use the supported GEMS progress pattern for indeterminate processing.
- Do not show Completed before system confirmation.
- Do not assume cancellation is supported.
- Use `Foundation` and official Progress Indicator guidelines for visual consistency.
- Do not independently introduce progress notifications when the requirement calls for a different progress pattern.

---

## 8. Position & Responsive Behavior

### Desktop

Official GEMS Notification provides `Top` and `Bottom` positions.

### Mobile

The linked GEMS component provides `Top` positioning for Mobile variants.

### Position Rules

- Use only positions supported by the selected Type and Breakpoint.
- Follow established positioning in relevant GEMS Page Samples and UX Patterns.
- Maintain a consistent notification position across comparable workflows.
- Do not place Notifications randomly.
- Avoid covering important buttons, navigation, forms, or page content.
- Respect viewport dimensions and safe areas.
- Do not implement unsupported Mobile Bottom placement without Human Approval.

### Responsive Rules

- Use official `Desktop` and `Mobile` component variants.
- Preserve Title and Description readability.
- Avoid excessively long messages on Mobile.
- Do not manually shrink Desktop components to create Mobile variants.
- Do not recreate unavailable variants from primitive components.

---

## 9. Trigger, Duration & Dismiss Behavior

### Trigger Logic

Notification appears only when an event or condition justifies user feedback.

**Examples**
- System confirms save → Success.
- System rejects submission → Error.
- Processing begins → Progress indicator when appropriate.
- Relevant activity update arrives → Informational Notification.

### Duration & Auto-Dismiss

- Follow existing product behavior and GEMS usage patterns.
- Do not invent exact display durations without requirements.
- Do not assume every Notification auto-dismisses.
- Allow enough time for users to understand the message.
- Important errors must remain accessible or have an appropriate recovery path.
- Do not remove ongoing progress feedback before the operation reaches a meaningful state.

### Dismiss

- Close is permitted only when supported and appropriate.
- Dismissal hides feedback; it does not undo actions or change business status.
- Do not assume all Notifications have Close controls.
- Close controls MUST remain accessible by keyboard.

### Action

Actions may include:
- Coba Lagi
- Lihat Detail
- Buka Pengajuan

**Rules**
- Actions require actual workflow support.
- Labels MUST describe available functionality.
- Use official GEMS Button or corresponding action components.
- Do not add actions merely for visual completeness.
- Do not execute destructive actions without necessary confirmation.
- Do not navigate automatically unless the workflow explicitly requires it.

---

## 10. Duplicate & Multiple Notifications

- Avoid showing identical Notifications repeatedly for one event.
- Do not display contradictory Success and Error messages for the same operation.
- Follow established product behavior for multiple simultaneous events.
- Preserve logical ordering and readability.
- Avoid excessive Notification stacking.
- Do not invent stacking limits, queues, or animations without existing specifications or Human Approval.
- Notifications MUST NOT automatically redirect users merely because they appear.

---

## 11. Foundation & Component Dependencies

All Notification elements MUST follow GEMS Foundation guidelines.

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | Official General colors, semantic meaning, contrast |
| `Foundation/typography.md` | Official Text Styles for titles, descriptions, actions |
| `Foundation/spacing-dan-radius.md` | Padding, spacing, gaps, radius |
| `Foundation/effect-styles.md` | Official effects where present |
| `Foundation/icons.md` | Semantic/action icon style and size |
| `Foundation/misc-icons.md` | Specialized visual icons where relevant |
| `Foundation/design-annotations.md` | Component specifications and annotations |

### Related Component Rules

- **Alert:** Use for important persistent information within page context.
- **Modal:** Use for confirmation and decisions requiring explicit user approval.
- **Button:** Use official GEMS action controls.
- **Input / Dropdown:** Field-level errors remain close to the affected fields.
- **Badge:** Use for status labels in tables and details.
- **Avatar:** Avatar Notifications MUST use official GEMS Avatar components.
- **Progress Indicator:** Progress Notifications MUST follow official progress styling.

**Visual Requirements**
- Preserve original Figma component and Text Style references.
- Use GEMS General colors and Foundation tokens.
- Apply official spacing, radius, icon dimensions, and effects.
- Do not add arbitrary shadows, colors, or animations.
- Do not introduce external icon families or custom visual treatments.
- Never use CCM-specific components or styling.

---

## 12. Accessibility

- Text MUST communicate meaning without relying only on icon or color.
- Maintain readable contrast using GEMS tokens.
- Keep Title and Description in logical reading order.
- Use `role="status"` for nonurgent feedback when appropriate.
- Use `role="alert"` for urgent failure information when appropriate.
- Do not announce every Notification as urgent.
- Close and Action controls MUST support keyboard interaction and accessible names.
- Avoid unexpected focus changes.
- Allow sufficient reading time.
- Do not make critical information available only through short-lived messages.
- Ensure visual and screen-reader behavior works across supported breakpoints.

---

## 13. Strict AI Rules

### MUST

1. Use existing **GEMS General Notification** components.
2. Preserve official Type, Breakpoint, and Position combinations.
3. Determine whether a Notification is genuinely needed.
4. Select Type based on actual event meaning.
5. Trigger messages from real system outcomes.
6. Follow GEMS Foundation and related component guidelines.
7. Follow GEMS Page Samples and UX Patterns for contextual usage.
8. Preserve official layout, content structure, and responsive behavior.
9. Follow actual workflow, permissions, duration, and dismiss requirements.
10. Request Human Approval before introducing unsupported variants or behavior.

### MUST NOT

1. **Use CCM components, variants, or styles.**
2. Create custom, detached, or duplicate Notification components.
3. Invent unsupported Type, Position, or Breakpoint combinations.
4. Create Mobile Bottom or Mobile Image variants without approval.
5. Hardcode styling outside official GEMS styles.
6. Add Notifications automatically for every interaction.
7. Replace Alert, Modal, Badge, Input Validation, or Empty State without valid reasons.
8. Display Success before confirmed completion.
9. Invent process results, business states, or progress values.
10. Assume all Notifications auto-dismiss or have Close controls.
11. Add unsupported actions, navigation, animations, or stacking behavior.
12. Treat dismissal as cancelling or reversing a business operation.
13. Show duplicate or conflicting messages for the same event.
14. Introduce unsupported patterns without Human Approval.

---

## 14. AI Usage Decision

When designing a screen:

1. **Identify Event:** Read HSD/BRD and actual system conditions.
2. **Determine Necessity:** Decide whether the event needs user feedback.
3. **Choose Component:** Confirm Notification is more appropriate than Alert, Modal, Badge, or Input Validation.
4. **Select Type:** Choose the supported semantic or content-based Type.
5. **Select Breakpoint & Position:** Use an existing GEMS combination.
6. **Write Message:** Describe the actual condition, outcome, and next action when relevant.
7. **Define Behavior:** Follow supported trigger, duration, dismiss, and action requirements.
8. **Apply Official Styling:** Preserve original GEMS components, Foundation styles, and responsive behavior.

**Fallback:** If the required Type, position, interaction, or business behavior is unsupported or undefined, request Human Approval. Do not independently create a replacement variant.

> **FINAL INSTRUCTION:** Use official **GEMS General Notification** components only when relevant feedback is needed. Actual system events determine message content and semantic Type; available GEMS variants determine Breakpoint and Position. Preserve component references, follow Foundation guidelines, and never use CCM.

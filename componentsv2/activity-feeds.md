
# GEMS Design System — Components / Activity Feeds

> **MANDATORY:** All activity feeds, chronological activity lists, and supported message-feed interfaces MUST use official GEMS Activity Feed components and available variants. AI MUST determine necessity, content, ordering, and presentation based on product requirements, GEMS Page Samples, and UX Patterns. CCM components and styling are strictly prohibited.

## 1. Sources & Priority

**Official Figma References**
- [GEMS Activity Feeds](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=611-413)
- [Feed Item Base](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=611-5398)
- [Activity Feed](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=611-5619)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1105-7310)

**Priority Order**
1. **Official Activity Feed Components:** Structure, variants, properties, and visual specifications.
2. **GEMS Foundation:** Colors, typography, spacing, radius, icons, and effects.
3. **GEMS Page Samples & UX Patterns:** Contextual placement and usage.
4. **HSD/BRD:** Business events, content, permissions, and data behavior.
5. **General UX Principles:** Fallback when GEMS does not specify a pattern.

Official GEMS components have visual priority. Event content and functionality MUST follow approved business requirements.

**Strict Exclusion:** Never use CCM components, CCM variants, or CCM-specific styling.

---

## 2. Available Components & Variants

AI MUST use only variants available in the official GEMS Figma library.

### 2.1 Feed Item Base

**Component:** `_Feed item base`

| Property | Available Values |
|---|---|
| `Size` | `sm`, `md` |
| `Supporting item` | `False`, `File`, `Labels`, `Text` |
| `Connector` | `True`, `False` |

### Supporting Item Usage

| Variant | When to Use |
|---|---|
| `False` | Activity requiring only its main information |
| `File` | Activity associated with an attachment or document |
| `Labels` | Activity requiring additional structured labels |
| `Text` | Activity requiring additional descriptive text |

**Rules**
- Select supporting content according to the actual event.
- Use `False` when additional content is unnecessary.
- Use official GEMS file and label components where applicable.
- Do not add supporting content merely to make every activity item visually identical.
- Preserve the selected variant's original structure and spacing.

### Size Selection

| Size | Recommended Usage |
|---|---|
| `sm` | Compact activity lists and constrained interfaces |
| `md` | Standard activity feeds requiring more visual space |

The official GEMS component and relevant Page Samples determine final sizing.

Use consistent sizing for equivalent items within the same feed unless the official pattern specifies otherwise.

### Connector

| Value | Usage |
|---|---|
| `True` | Display the official connector treatment |
| `False` | Display the item without a connector |

**Rules**
- Use connectors only when supported by the selected feed pattern.
- Preserve the official connector alignment, size, and color.
- Do not manually draw timeline lines.
- Do not combine custom connectors with the official component.

---

## 3. Activity Feed Variants

**Component:** `Activity feed`

### Available Properties

| Property | Available Values |
|---|---|
| `Type` | `Notifications`, `Messages` |
| `Divider` | `Line`, `Connector`, `False` for Notifications |
| `Divider` | `Divider`, `Connector`, `False` for Messages |

**Important:** The available divider value depends on the selected `Type`. AI MUST preserve the exact supported combinations rather than treating all divider values as interchangeable.

### 3.1 Notifications

Use `Type=Notifications` for activity or notification-style feeds when supported by the product.

Examples:
- Data created.
- Data updated.
- Status changed.
- Approval completed.
- Revision requested.
- Document uploaded.
- Process completed.

**Rules**
- Present events according to their actual business meaning.
- Use the appropriate GEMS feed-item composition.
- Apply the official divider variant based on the relevant design pattern.
- Do not use Notifications as a substitute for every Alert or Toast.

### 3.2 Messages

Use `Type=Messages` when the interface displays a sequence of messages or communication-related entries.

Examples:
- Discussion history.
- Process-related communication.
- Comments associated with a record.
- Message activity within a workflow.

**Rules**
- Use only when the product requires message-related content.
- Preserve the official Messages structure.
- Display participant information and content according to available data and the supported component.
- Do not interpret Messages as permission to invent a complete chat interface.
- Do not create chat bubbles, attachment controls, or message actions outside approved GEMS patterns.

### 3.3 Divider Selection

| Divider | Intended Treatment |
|---|---|
| `Line` / `Divider` | Official visual separation between feed entries |
| `Connector` | Official connected activity presentation |
| `False` | No divider |

Choose the exact variant supported for the selected feed type.

Do not introduce custom lines, separators, or connector styles.

---

## 4. When to Use Activity Feeds

**Core Principle:**

> Use Activity Feeds when users need to understand what happened, who was involved, and how information or a process changed over time.

### Usage Matrix

| Context | Recommended Usage |
|---|---|
| Detail Page | History associated with a specific record |
| Approval Workflow | Approval, rejection, and revision activity |
| Data Management | Relevant create, update, and delete history |
| Document Management | Upload and document-related activity |
| Request Management | Process updates and user actions |
| Monitoring | Chronological operational events |
| Communication | Messages and relevant discussions |
| Audit History | User-visible event history when the component is appropriate |

### When NOT to Use

Do not use Activity Feeds for:
- General lists of records without a chronological purpose.
- Standard data tables.
- Current status displayed without historical context.
- Dashboard metrics or KPI values.
- Step-by-step form navigation.
- Upload progress.
- Temporary loading indicators.
- One-time success or error messages.

Use the corresponding GEMS component instead.

**Activity Feed is not automatically required on every Detail Page.** Include it only when history or communication adds meaningful value.

---

## 5. Activity Content & Information Hierarchy

Each feed item MUST accurately represent the associated event.

### Recommended Information

| Information | Purpose |
|---|---|
| Actor | Person or system responsible for the activity |
| Action | What happened |
| Object | Related record, document, or process |
| Timestamp | When the event occurred |
| Supporting Content | Additional file, label, or description when needed |

Include only information available from the product's data source and supported by the selected component.

### Content Rules

AI MUST:
- Use actual business events defined by HSD/BRD.
- Use clear and consistent terminology.
- Distinguish user actions from automated system activities.
- Display relevant timestamps when available.
- Keep activity descriptions concise.
- Preserve the relationship between the main event and its supporting information.
- Respect data visibility and role-based permissions.

AI MUST NOT:
- Invent actors, timestamps, or activity records.
- Present planned actions as completed events.
- Show internal audit information to unauthorized users.
- Add unrelated descriptions or decorative labels.
- Assume every event requires an icon, file, or supporting text.

### Example Content

| Event | Suggested Activity Text |
|---|---|
| Create | Amanda menambahkan data baru |
| Update | Amanda memperbarui informasi data |
| Approve | Data disetujui oleh Approver |
| Reject | Permintaan ditolak |
| Revision | Revisi diminta |
| Upload | Dokumen pendukung ditambahkan |
| Delete | Data dihapus |

These are examples only. Actual actor names, actions, and wording MUST come from product data and approved terminology.

---

## 6. Chronology & Feed Behavior

AI MUST determine event ordering according to the product's requirements.

### Chronological Rules

- Present events in a consistent chronological order.
- Follow official Page Samples and UX Patterns for ordering and visual hierarchy.
- Preserve the relationship between related events.
- Display timestamps consistently.
- Use the correct connector and divider variant.
- Do not imply that events belong to one continuous process when they are unrelated.
- Do not reorder events solely to improve visual appearance.

### Interaction Rules

- Provide supported actions only when required.
- Use official GEMS components for interactive elements.
- Preserve navigation context when an activity links to another page or record.
- Respect permissions for viewing files, details, or related records.
- Do not make every feed item clickable unless the product defines a valid destination.

### Long Activity Histories

When many records exist:
- Follow the approved GEMS pattern for displaying lengthy activity histories.
- Use pagination, progressive loading, or another mechanism only when supported by the product.
- Preserve chronological consistency.
- Do not silently omit important activities.
- Do not invent custom feed navigation patterns.

---

## 7. Activity Feeds in CRUD & UX Patterns

### 7.1 Create

When the product records creation activity:
- Display the creation event after successful persistence.
- Identify the actor and record when available.
- Do not log a completed creation before the operation succeeds.

### 7.2 Read / Detail

- Display relevant activity history in the appropriate Detail Page section.
- Use official GEMS Section Header or Tabs where supported.
- Preserve contextual information about the current record.
- Do not repeat the same information unnecessarily across sections.

### 7.3 Update

- Record meaningful changes according to the product's audit requirements.
- Show updated information only after the operation succeeds.
- Display additional details using the supported `Text` or `Labels` presentation when appropriate.
- Do not invent a before-and-after comparison if the required data is unavailable.

### 7.4 Delete

- Display deletion history only when the record or audit log remains accessible.
- Follow permissions and data-retention rules.
- Use the official GEMS Modal for required destructive confirmation.
- Do not imply deleted records remain accessible when the product does not support it.

### 7.5 Approval / Rejection / Revision

Activity Feeds are especially relevant when users need to understand a decision history.

| Event | Relevant Information |
|---|---|
| Approval | Approver, action, timestamp, optional note |
| Rejection | Actor, decision, timestamp, reason when available |
| Revision | Actor, requested changes, timestamp |
| Resubmission | Actor, new submission event, timestamp |

**Rules**
- Follow the actual approval workflow.
- Preserve event ordering.
- Display supporting explanations only when available and authorized.
- Do not treat Activity Feed as the component that performs approval actions.
- Use GEMS Modal and Button guidelines for decision interactions.

---

## 8. Empty, Loading & Error States

Activity Feeds MUST distinguish actual empty data from loading and request failures.

| Condition | Required Pattern |
|---|---|
| No activities | Official GEMS Empty State |
| Activities loading | Official GEMS Loading Indicator |
| Request failed | Appropriate GEMS error feedback |
| Activities available | Official GEMS Activity Feed |
| Restricted access | Approved permission-based presentation |

### Empty State Example

**Title:** Belum Ada Riwayat Aktivitas  
**Description:** Aktivitas yang berkaitan dengan data ini akan ditampilkan di sini.

Use product-specific wording where appropriate.

**Rules**
- Do not create placeholder activities to fill the feed.
- Do not display an empty state before data loading finishes.
- Do not treat API errors as an empty history.
- Do not display unauthorized activity data.
- Follow the official `empty-state.md` guideline.

---

## 9. Layout & Placement

AI MUST follow official GEMS Page Samples and UX Patterns.

### Recommended Placement

Activity Feeds may appear in:
- Detail Page sections.
- Activity History tabs.
- Approval history areas.
- Supporting information panels.
- Official Slide Out Menu patterns.
- Communication-related interfaces.

**Important:** The GEMS reference also includes an Activity Feed inside a Slide Out Menu. This is an example of a supported composition, not a requirement to place every Activity Feed inside a slide-out panel.

### Layout Rules

- Preserve the official Activity Feed structure.
- Follow the selected `Size`, `Supporting item`, `Connector`, `Type`, and `Divider` properties.
- Use GEMS spacing and typography.
- Keep chronological entries visually consistent.
- Maintain readable timestamps and supporting content.
- Follow responsive examples and supported component behavior.
- Do not manually resize or reconstruct the component outside approved properties.
- Do not add custom background effects, borders, or shadows.

---

## 10. Related GEMS Guidelines

### Foundation Dependencies

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | Brand General, semantic colors, and neutral styling |
| `Foundation/typography.md` | Activity descriptions, labels, and timestamps |
| `Foundation/spacing-dan-radius.md` | Item spacing, padding, and radius |
| `Foundation/effect-styles.md` | Official effects when applicable |
| `Foundation/icons.md` | General activity and action icons |
| `Foundation/misc-icons.md` | Featured and file-type icons where supported |
| `Foundation/design-annotations.md` | Component behavior and specifications |

### Related Components

- **Avatar:** User or actor identity when supported.
- **Badge / Tag:** Relevant status or structured labels.
- **File Upload:** Uploaded supporting documents.
- **Button:** Available activity actions.
- **Modal:** Confirmation for consequential actions.
- **Tabs:** History or activity sections.
- **Section Header:** Activity Feed section titles.
- **Empty State:** No activity records.
- **Loading Indicator:** Data loading.
- **Alert / Notification:** Separate feedback or notification interactions.
- **Data Table:** Structured records better presented in rows and columns.

Related components MUST follow their respective GEMS guidelines.

---

## 11. Activity Feed vs Other Components

AI MUST choose components according to their actual purpose.

| User Need | Preferred Component |
|---|---|
| View chronological activity | Activity Feed |
| View structured records | Data Table |
| View current status | Badge |
| View a notification message | Notification |
| View an important warning | Alert |
| View process stages | Progress Steps |
| View activity history within a section | Activity Feed with relevant page structure |
| View no activity records | Empty State |

**Core Rule:** Activity Feed represents historical events or message sequences. It MUST NOT replace status indicators, transaction tables, workflow steps, or temporary notifications.

---

## 12. Strict GEMS Compliance

**MUST**
- Use official GEMS Activity Feed components.
- Preserve official component instances and properties.
- Select supported Feed Item and Activity Feed variants.
- Use contextual supporting content.
- Display accurate event information.
- Follow approved chronological ordering.
- Respect role-based permissions and HSD/BRD.
- Follow GEMS Page Samples and UX Patterns.
- Use GEMS Foundation and related components consistently.

**MUST NOT**
- Use CCM components, variants, or styling.
- Recreate Activity Feed using custom Frames when official instances are available.
- Invent additional Feed Item or Activity Feed variants.
- Create custom connectors, timelines, dividers, or icons.
- Hardcode unsupported colors, typography, spacing, radius, or effects.
- Fabricate activity records, actors, timestamps, or process outcomes.
- Display unauthorized audit information.
- Use Activity Feed for unrelated data lists.
- Add unsupported messaging or interaction features.
- Change chronological order for visual preference.
- Introduce decorative Activity Feeds without functional purpose.

---

## 13. AI Selection & Human Approval

AI MUST determine:

1. **Necessity:** Does the interface require activity history or messages?
2. **Context:** Which business events should be presented?
3. **Type:** `Notifications` or `Messages`?
4. **Presentation:** Which official size, divider, and connector variants apply?
5. **Supporting Content:** None, File, Labels, or Text?
6. **Data:** Which actors, actions, timestamps, and details are available?
7. **Placement:** Where does the feed belong according to GEMS Page Samples and UX Patterns?
8. **Permissions:** Which activities and interactions can the current user access?

Use approved HSD/BRD and product context to resolve these decisions.

**Human Approval Required**

If the requested workflow needs an unsupported variant, layout, connector, message interaction, or component behavior, AI MUST request Human Approval before creating a custom solution.

Combine unresolved questions into one concise confirmation. Do not repeatedly request details already provided in the product documentation.

**Fallback:** Use the closest suitable official GEMS Activity Feed pattern. Do not invent unsupported variants or visual properties.

---

## 14. Final AI Instruction

**AI MUST use official GEMS Activity Feed components whenever chronological activity or supported message-feed presentation is required.**

Select component variants, supporting content, size, connector, divider, and placement according to official GEMS specifications and relevant product requirements.

Activity Feed MUST communicate meaningful and accurate events. It is not required on every page or Detail Page.

Preserve all official GEMS component properties, typography, colors, icons, spacing, radius, and effects.

Never use CCM components, fabricate activity records, or introduce unsupported visual or interaction patterns without Human Approval.

**GEMS Design System is the single source of truth for Activity Feed visual specifications.**

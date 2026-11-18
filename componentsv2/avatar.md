
# GEMS Design System — Components / Avatar

> **MANDATORY:** All Avatars MUST use official GEMS General components from the connected Figma Design System. Preserve original component references, supported variants, sizes, states, status indicators, typography, colors, and spacing. **CCM components and CCM-derived styling are strictly prohibited.**

## 1. Purpose & Source of Truth

Avatar visually represents an individual or supported identity through a profile image, initials, or official placeholder.

This guideline covers:

- Avatar
- Avatar Label Group
- Avatar Group
- Avatar Profile Photo
- Avatar Image
- Avatar Add Button
- Online Indicator
- Company Indicator
- Verified Tick
- Identity fallback, interaction, and accessibility

**Core Principle:**

> Use Avatar when visual identity helps users recognize a person or relevant entity. Avatar MUST represent actual identity data, not decorative content.

### 1.1 Reference Priority

1. **Official GEMS General Components:** Variants, sizes, properties, and styling.
2. **GEMS Components:** Avatar usage within existing UI components.
3. **GEMS Page Samples & UX Patterns:** Contextual placement and behavior.
4. **Product HSD/BRD:** Identity requirements, permissions, and workflows.
5. **System Data:** Actual photos, names, status, and attributes.
6. **General UI/UX Principles:** Fallback when GEMS provides no specific guidance.

GEMS governs component design. Product requirements and system data govern represented identities.

Read only references relevant to the requested interface.

## 2. Component Selection Matrix

| Requirement | GEMS Component | Example |
|---|---|---|
| Display individual identity | Avatar | Table, Header |
| Display avatar with name/details | Avatar Label Group | User List, PIC |
| Display multiple members | Avatar Group | Team, Participants |
| Display prominent profile identity | Avatar Profile Photo | Profile Page |
| Display an image within Avatar | Avatar Image | Image source |
| Add a member to a group | Avatar Add Button | Team Member |
| Show actual online presence | Online Indicator | Online user |
| Show supported company attribute | Company Indicator | Organization identity |
| Show verified identity | Verified Tick | Verified user |

### 2.1 Component Selection Rules

- Select the component according to the identity context.
- Prefer Avatar Label Group when avatar and text form one identity unit.
- Use Avatar Group for multiple related identities.
- Use Avatar Profile Photo for prominent profile presentation.
- Use Avatar Add Button only for supported member-addition actions.
- Do not use internal Avatar Image as a replacement for the main Avatar component.
- Do not add Avatar merely for decoration.

## 3. Component Properties & Variants

### 3.1 Avatar

**Official properties**

| Property | Available Values |
|---|---|
| `Size` | `xs`, `sm`, `md`, `lg`, `xl`, `2xl` |
| `Placeholder` | `True`, `False` |
| `Text` | `True`, `False` |
| `Status icon` | `False`, `Online indicator`, `Company`, `Verified` where supported |

**Official sizes**

| Size | Dimensions |
|---|---|
| `xs` | 24 × 24 px |
| `sm` | 32 × 32 px |
| `md` | 40 × 40 px |
| `lg` | 48 × 48 px |
| `xl` | 56 × 56 px |
| `2xl` | 64 × 64 px |

**Rules**
- Use official supported property combinations.
- Do not assume every Status icon is available for every Placeholder/Text configuration.
- Preserve original component proportions.
- Do not create custom sizes.

### 3.2 Avatar Label Group

| Property | Available Values |
|---|---|
| `Size` | `sm`, `md`, `lg`, `xl` |
| `Status icon` | `False`, `Online indicator`, `Company`, `Verified` |

Use when an Avatar and supporting identity text form one component.

**Rules**
- Preserve the official text hierarchy and layout.
- Use actual names and supporting information.
- Do not invent position titles, departments, or identity details.
- Do not transfer unsupported size variants from the main Avatar.

### 3.3 Avatar Group

| Property | Available Values |
|---|---|
| `Size` | `xs`, `sm`, `md` |

Use to display multiple members within a compact group.

**Rules**
- Use actual member data.
- Preserve official arrangement and spacing.
- Follow supported member-count and overflow behavior.
- Do not add fictional members.
- Do not invent custom overflow configurations.

### 3.4 Avatar Profile Photo

| Property | Available Values |
|---|---|
| `Size` | `sm`, `md`, `lg` |
| `Placeholder` | `True`, `False` |
| `Text` | `True`, `False` within supported combinations |

**Official sizes**

| Size | Dimensions |
|---|---|
| `sm` | 72 × 72 px |
| `md` | 96 × 96 px |
| `lg` | 160 × 160 px |

**Available configurations**
- Image: `Placeholder=False`, `Text=False`
- Placeholder: `Placeholder=True`, `Text=False`
- Initials: `Placeholder=True`, `Text=True`

**Rules**
- Use for prominent identity presentation.
- Preserve official image proportions and cropping.
- Do not invent photo-upload or editing features.

### 3.5 Avatar Image

| Property | Available Values |
|---|---|
| `Type` | `Square`, `Portrait` |

**Rules**
- Use only within appropriate official Avatar compositions.
- Match image treatment to the available source.
- Preserve official clipping and image behavior.
- Do not stretch or distort profile images.
- Do not use Avatar Image as a general-purpose Image component.

### 3.6 Avatar Add Button

| Property | Available Values |
|---|---|
| `Size` | `xs`, `sm`, `md` |
| `State` | `Default`, `Hover`, `Focus`, `Disabled` |

**Official sizes**

| Size | Dimensions |
|---|---|
| `xs` | 24 × 24 px |
| `sm` | 32 × 32 px |
| `md` | 40 × 40 px |

**Rules**
- Use only for supported member-addition interactions.
- Follow product permissions.
- Preserve official icon, sizing, and interaction states.
- Do not use Avatar Add Button as a general Add Data button.
- Do not invent additional states or dimensions.

## 4. When to Use Avatar

### 4.1 Data Table — Web

Use Avatar when a table column represents an individual's identity.

**Examples**
- Nama Pengguna
- Nama Karyawan
- Penanggung Jawab
- Anggota Tim

**Recommended pattern:** `Avatar + Nama`

**Rules**
- Prefer Avatar + Name when supported by the relevant GEMS Table pattern.
- Keep the person's name as primary readable information.
- Maintain consistent Avatar sizes and alignment across rows.
- Do not add Avatar to document names, locations, or ordinary categories.

### 4.2 List & Card — Web

Use Avatar for lists or cards representing people.

**Recommended pattern:** `Avatar + Nama + Informasi Pendukung`

- Prefer Avatar Label Group when appropriate.
- Preserve name hierarchy.
- Include only available supporting information.
- Follow official GEMS List and Card patterns.

### 4.3 List & Card — Mobile

Use Avatar when visual identity improves recognition in mobile lists or cards.

**Rules**
- Preserve readable names on small screens.
- Select supported Avatar sizes.
- Maintain consistent fallback behavior.
- Follow relevant GEMS mobile patterns.
- Do not hide important names to make room for larger photos.

### 4.4 Header & Account Menu

Use Avatar to identify the currently signed-in account.

- Use actual account identity.
- Preserve image fallback.
- Follow GEMS Application Navigation and account-menu patterns.
- Do not make Avatar clickable unless the product defines an action.

### 4.5 Profile & Detail Page

Use Avatar Profile Photo when the person's identity is prominent.

- Display the correct photo or fallback.
- Follow the official GEMS Profile/Detail pattern.
- Do not invent upload, replace, crop, or edit actions.

### 4.6 Team & Member Group

Use Avatar Group when displaying multiple related individuals.

- Use actual member identities.
- Preserve official grouping and spacing.
- Follow supported overflow behavior.
- Do not invent members or hidden-member counts.

### 4.7 Activity & Notification

Use Avatar when an activity or notification has an identifiable individual actor.

- Display the correct sender or actor.
- Follow the official Notification component.
- Do not add personal Avatar to generic system notifications without a relevant identity.

### 4.8 Member Addition

Use Avatar Add Button for adding members to a team or group.

- Follow approved permissions and member-selection workflow.
- Use official GEMS Button/Add behavior.
- Do not replace general Create actions with Avatar Add Button.

## 5. When NOT to Use Avatar

| Context | Reason | Appropriate Component |
|---|---|---|
| Workflow status | Not an identity | Status Badge |
| System error | System feedback | Alert / Notification |
| Document name | Not a person | Text / File Icon |
| Location | Not a person | Text / Relevant Icon |
| General navigation | Not identity-related | Navigation / Icon |
| Illustration | Not user identity | Image / Illustration |
| General Create action | Not member addition | Button |

**Rules**
- Do not assume every field containing a name needs Avatar.
- Distinguish people from products, locations, documents, and categories.
- Do not replace Status, Icon, Button, or Notification components with Avatar.
- Do not add Avatar without a meaningful identity purpose.

## 6. Avatar Content & Fallback

### 6.1 Image Available

When a valid, authorized photo exists:

- Display the correct person's photo.
- Preserve original proportions.
- Use official image clipping.
- Keep a fallback available if loading fails.
- Do not substitute another person's photo.

### 6.2 Image Unavailable — Name Available

When a photo is unavailable but a valid name exists, use official initials presentation.

**Examples**

| Name | Initials |
|---|---|
| Amanda Aprilia | AA |
| Muhammad Yusron | MY |
| Silvia | S |

**Rules**
- Prefer a maximum of two initials when the official pattern supports it.
- Use a consistent name-to-initials rule.
- Use actual identity data.
- Do not invent names or initials.

### 6.3 Image & Name Unavailable

When neither valid photo nor name exists:

- Use the official GEMS placeholder.
- Preserve the Avatar's dimensions.
- Do not display broken images, `null`, or unrelated photos.

### 6.4 Image Loading

- Keep Avatar dimensions stable.
- Use approved fallback/loading treatment.
- Replace the temporary presentation when the image loads.
- Do not create unsupported Avatar loading variants.

### 6.5 Image Error

- Fall back to initials when valid name data exists.
- Otherwise use the official placeholder.
- Do not expose broken-image UI.

### 6.6 Fallback Priority

| Priority | Available Data | Display |
|---|---|---|
| 1 | Valid authorized photo | Image |
| 2 | Valid name without usable photo | Initials |
| 3 | Neither photo nor name | Placeholder |

Apply consistently across Web and Mobile unless an approved product rule specifies otherwise.

## 7. Status Indicators

Avatar indicators represent supported identity attributes—not general workflow status.

### 7.1 Available Indicators

| Indicator | Meaning |
|---|---|
| `False` | No indicator |
| `Online indicator` | Actual presence status |
| `Company` | Supported company attribute |
| `Verified` | Verified identity |

### 7.2 Online Indicator

The official supporting component provides:

- `Size`: `xs`, `sm`, `md`, `lg`, `xl`, `2xl`
- `Online`: `True`, `False`

**Rules**
- Use only when actual presence data exists.
- Do not infer online status from recent activity.
- Preserve official indicator styling and position.
- Do not use presence indicators as workflow Status Badges.

### 7.3 Company Indicator

The official Company Indicator supports sizes `xs` through `2xl`.

- Use only when the product defines a meaningful company attribute.
- Preserve official size and alignment.
- Do not use Company Indicator as decoration.
- Follow actual entity and organization data.

### 7.4 Verified Tick

The supporting Verified Tick component includes sizes:

`xs`, `sm`, `md`, `lg`, `xl`, `2xl`, `3xl`, `4xl`

**Rules**
- Show Verified only when identity verification is confirmed.
- Use only supported combinations in the parent Avatar component.
- Do not assume all Verified Tick sizes are valid for every Avatar.
- Do not use Verified to represent approval status.

### 7.5 Status Indicator Restrictions

- Status indicators MUST reflect actual authorized data.
- Do not show Online without presence information.
- Do not show Verified without verified status.
- Do not invent Company indicators.
- Do not convert process statuses into Avatar indicators.
- Follow supported GEMS component combinations.

## 8. Interaction States & Behavior

### 8.1 Static Avatar

Use when Avatar only displays identity.

**Rules**
- No action or navigation.
- No unnecessary click affordance.
- No keyboard focus unless required by an approved pattern.
- Keep identity information readable.

### 8.2 Interactive Avatar

Use only when product requirements define a specific interaction, such as opening a profile.

**Rules**
- Provide a clear interaction purpose.
- Follow an approved GEMS interactive component pattern.
- Support keyboard access and visible focus.
- Respect user permissions.
- Do not make all Avatars clickable by default.

### 8.3 Avatar Add Button States

| State | Behavior |
|---|---|
| `Default` | Available for interaction |
| `Hover` | Official pointer-hover appearance |
| `Focus` | Visible keyboard-focus treatment |
| `Disabled` | Interaction unavailable |

**Rules**
- Preserve official GEMS states.
- Prevent actions when Disabled.
- Provide an accessible action name.
- Do not invent additional states.
- Use the exact state name `Focus`, not `Focused`.

### 8.4 Permissions & Business Behavior

- Avatar visibility and interaction MUST follow HSD/BRD.
- Do not provide profile access without authorization.
- Do not expose restricted identity information.
- Do not invent profile editing or member-management functionality.

## 9. Layout & Responsive Guidelines

### 9.1 Web

- Select official sizes based on component context.
- Preserve alignment with names and supporting text.
- Keep table-row Avatar sizes consistent.
- Follow GEMS Table, List, Card, and Header patterns.
- Do not manually resize Avatar beyond supported variants.

### 9.2 Mobile

- Use supported Avatar sizes appropriate to available space.
- Preserve readable names.
- Keep fallback presentation consistent.
- Maintain appropriate interaction usability.
- Follow official GEMS mobile Page Samples.

### 9.3 Cross-Platform Consistency

- Use the same identity source across platforms.
- Apply consistent initials and placeholder fallback.
- Status indicators MUST reflect the same actual data.
- Sizes MAY vary according to official layouts.
- Do not change represented identity because the platform differs.

## 10. Accessibility & Foundation Integration

### 10.1 Accessibility

**MUST**
- Maintain readable names and initials.
- Provide appropriate text alternatives for informative identity images.
- Avoid duplicate screen-reader announcements when an adjacent name already identifies the person.
- Provide accessible names for interactive Avatars.
- Support keyboard access and visible focus when interactive.
- Communicate identity status without relying solely on color.

**MUST NOT**
- Treat photos as the only source of identity information.
- Add keyboard focus to static Avatars without reason.
- Use status color without accessible meaning.
- Display inaccessible Avatar Add Buttons.

### 10.2 Foundation Guidelines

Avatar styling MUST follow:

| Guideline | Responsibility |
|---|---|
| `Foundation/color.md` | GEMS General colors and semantic status |
| `Foundation/typography.md` | Name, initials, and supporting Text Styles |
| `Foundation/spacing-dan-radius.md` | Spacing, layout, and radius |
| `Foundation/effect-styles.md` | Approved effects when specified |
| `Foundation/icons.md` | General icons |
| `Foundation/misc-icons.md` | Specialized identity-related icons when applicable |
| `Foundation/design-annotations.md` | Additional approved specifications |

### 10.3 Visual Rules

- Preserve component-defined size, radius, clipping, and layout.
- Use existing GEMS General semantic colors.
- Apply official GEMS Text Styles.
- Do not hardcode HEX, RGB, HSL, typography, or spacing.
- Do not add decorative effects without GEMS support.
- Never use CCM styling.

## 11. AI Decision Logic

When implementing Avatar:

1. **Identify Identity:** Determine whether the data represents a person or relevant identity group.
2. **Identify Context:** Table, List, Card, Header, Profile, Notification, or Team.
3. **Select Component:** Choose the appropriate official GEMS Avatar component.
4. **Apply Properties:** Use supported Size, Placeholder, Text, Status icon, and State combinations.
5. **Apply Content:** Use real photo, initials, or placeholder according to available data.
6. **Apply Indicators:** Show only verified identity attributes.
7. **Determine Interaction:** Static, profile navigation, or approved member addition.
8. **Follow GEMS Context:** Use relevant Components, Page Samples, and UX Patterns.
9. **Apply Foundation:** Preserve official colors, typography, spacing, radius, and effects.
10. **Resolve Exceptions:** Request Human Approval before introducing unsupported variants or behavior.

These are implementation instructions, not a separate validation report.

## 12. Strict AI Rules & Human Approval

### 12.1 Mandatory Rules

**MUST**
- Use official GEMS General Avatar components.
- Preserve original Figma component references.
- Select the correct component for each identity context.
- Use supported sizes, properties, and states.
- Display actual identity information.
- Apply photo-to-initials-to-placeholder fallback.
- Preserve readable names where needed.
- Use valid status data.
- Maintain Web/Mobile consistency.
- Follow GEMS Foundation and related component guidelines.
- Respect product permissions and accessibility.

### 12.2 Prohibited Rules

**MUST NOT**
- Use Avatar CCM or CCM-derived styling.
- Create unsupported Avatar variants, sizes, or states.
- Recreate existing GEMS Avatar components manually.
- Invent real-person photos or identity data.
- Display unrelated or incorrect profile images.
- Show broken-image placeholders.
- Remove fallback behavior.
- Display unverified status indicators.
- Replace workflow Status Badges with Avatar indicators.
- Make all Avatars clickable.
- Invent profile navigation or editing actions.
- Use Avatar Add Button for general Create actions.
- Add fictional members to Avatar Groups.
- Invent overflow patterns.
- Remove important names solely to emphasize photos.
- Use Avatar for non-identity content without a valid purpose.
- Hardcode visual styling outside official GEMS components.

### 12.3 Human Approval

Request Human Approval when:

- No suitable GEMS General Avatar component exists.
- An unsupported variant, status indicator, or interaction is required.
- Identity data or access permissions are essential but undefined.
- A new Avatar workflow would otherwise need to be invented.

Combine related clarification questions into one confirmation.

**Fallback:** Use the closest supported GEMS General component appropriate to the identity context. If no appropriate implementation exists, request Human Approval. Never use CCM or fabricated identities.

## 13. Official Figma References

### 13.1 Avatar Library

| Component | Reference |
|---|---|
| Avatar Overview | [GEMS Avatars](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=320-3569) |
| Avatar | [GEMS Avatar](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=421-3857) |
| Avatar Label Group | [GEMS Avatar Label Group](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1868-30580) |
| Avatar Group | [GEMS Avatar Group](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1868-30704) |
| Avatar Profile Photo | [GEMS Avatar Profile Photo](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1868-30661) |
| Avatar Image | [GEMS Avatar Image](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=421-4089) |
| Avatar Add Button | [GEMS Avatar Add Button](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=421-4120) |

### 13.2 Supporting Indicators

| Component | Reference |
|---|---|
| Online Indicator | [GEMS Avatar Online Indicator](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=421-4100) |
| Company Indicator | [GEMS Avatar Company Icon](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=421-4113) |
| Verified Tick | [GEMS Verified Tick](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=421-4164) |

### 13.3 Related Guidelines

**Foundation**
- `Foundation/color.md`
- `Foundation/typography.md`
- `Foundation/spacing-dan-radius.md`
- `Foundation/effect-styles.md`
- `

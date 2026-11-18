
# GEMS Design System — Authentication

> **MANDATORY:** All authentication interfaces MUST use official GEMS Figma Authentication components. AI MUST obtain human confirmation of login requirements in one consolidated step before generating or modifying authentication flows.

## 1. Sources & Priority

**Source of Truth**
- [GEMS Authentication](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=1245-27612)
- [GEMS Branded Login Form](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3189-28770)
- GEMS Components, Page Samples & UX Pattern Samples within the same Figma Design System.
- GEMS Foundation `logo.md` for product branding.

**Priority Order**
1. **GEMS Components:** Use official Authentication component instances, variants, and states.
2. **Human-Confirmed Requirements:** Follow approved login fields, methods, actions, and user flows.
3. **GEMS Examples:** Read relevant Authentication examples, Page Samples, and UX Patterns for actual usage.
4. **General UX & Security Principles:** Apply only when GEMS has no specific guidance.

Read only references relevant to the current task. Do not scan unrelated pages or components.

GEMS defines visual specifications. Human-confirmed requirements define authentication functionality.

## 2. Official Authentication Components

**Available Components**
- [Base Logo](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3189-28475)
- [Base Captcha](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3173-24669)
- [Captcha States](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3173-24722)
- [Login Action](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3179-27957)
- [Login Footer](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3179-28080)
- [Branded Login Form](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671/GEMS-Design-System?node-id=3189-28770)

**Rules**
- Use official GEMS Authentication component instances.
- Preserve original component properties, variants, and responsive behavior.
- Use existing GEMS Input, Button, Checkbox, Captcha, and supporting components.
- Include only elements required by confirmed authentication requirements.
- Do not recreate official components manually or introduce external component libraries.

## 3. Product Identity & Branding

AI MUST identify the product and use the corresponding GEMS branding.

**Selection Priority**
1. Explicit product specified by the user.
2. Existing approved product design.
3. Approved HSD/BRD or project documentation.
4. Available GEMS Branded Login Form variants.

**Rules**
- Use the matching Branded Login Form variant when available.
- Follow Foundation `logo.md` for logo selection and approval.
- Preserve official logo proportions, colors, and visual identity.
- Do not automatically use BIB, Digitech, or another product as default.
- Do not copy product-specific branding into unrelated applications.
- Existing GEMS login variants are visual references, not automatic authentication requirements.

If the product logo is unavailable, obtain human approval to use an existing GEMS logo or upload an official custom logo.

## 4. Authentication Requirements & Human Confirmation

AI MUST obtain explicit user confirmation of authentication requirements before generating or modifying an Authentication flow.

Identifying a product or finding an existing GEMS login variant does NOT replace this confirmation.

### Required Confirmation

Ask all relevant questions in ONE consolidated confirmation step.

| Requirement | Confirmation |
|---|---|
| Product / Module | Which application or module requires authentication? |
| Login Identifier | Username, Email, NIK, Employee ID, or another identifier? |
| Authentication Method | Password, SSO, OTP, Social Login, or another method? |
| Required Fields | Which fields must appear in the form? |
| Additional Verification | Is Captcha or MFA required? |
| Supporting Actions | Remember Me, Forgot Password, Register, or other actions? |
| Post-Login Destination | Where should users be directed after successful login? |
| User Roles | Do different roles require different login flows? |

**Confirmation Rules**
- Ask only for information not already explicitly confirmed by the user.
- Present known HSD/BRD or existing design requirements as proposed selections.
- Allow the user to confirm, modify, add, or remove requirements.
- Consolidate related questions into one message.
- Do not repeatedly ask questions that have already been answered.
- Use only confirmed fields, methods, and supporting actions.
- Do not assume GEMS sample forms define the actual product requirements.
- Do not add Captcha, OTP, SSO, Social Login, or registration without confirmation.
- Do not finalize authentication flows while essential requirements remain unresolved.

**After Confirmation**
1. Select the appropriate official GEMS Authentication components.
2. Configure fields, methods, and actions based on confirmed requirements.
3. Apply corresponding GEMS component states and variants.
4. Preserve approved product branding and responsive behavior.

## 5. Form Behavior & States

All Authentication forms MUST provide appropriate user feedback.

**Required UI States**
- Default
- Focused
- Filled
- Disabled
- Loading / Submitting
- Validation Error
- Authentication Error
- Success

Use official GEMS component states where available.

**Form Rules**
- Use official GEMS Input and Button components.
- Display clear labels and required-field indicators.
- Validate fields according to confirmed product requirements.
- Display relevant errors near affected fields.
- Provide clear authentication failure feedback without exposing sensitive information.
- Mask password inputs and use official visibility controls when supported.
- Prevent duplicate submissions during processing.
- Preserve appropriate non-sensitive input when validation fails.
- Support keyboard navigation and visible focus indicators.
- Do not display success until the authentication process succeeds.

## 6. Captcha & Additional Verification

Use official GEMS Captcha components only when required by confirmed product requirements.

**Available Captcha States**
- Default
- Disabled
- Verified
- Error

**Rules**
- Apply official Captcha component variants and visual properties.
- Display states according to actual verification results.
- Do not invent custom Captcha interfaces or verification mechanisms.
- Do not treat a visual Verified state as proof of backend verification.
- Do not bypass required verification steps.
- If Captcha is not required, do not add it.

## 7. Login Actions & Footer

Use official GEMS Login Action and Login Footer components.

**Rules**
- Primary login action MUST match the confirmed authentication method.
- Display only approved secondary actions and authentication providers.
- Use official loading, disabled, and error states.
- Use relevant approved footer links and supporting content.
- Do not copy sample footer content when unrelated to the product.
- Do not invent policies, support contacts, identity providers, or destination links.
- Keep action labels and messages consistent with product terminology.

## 8. Layout & Responsive Behavior

- Use official GEMS Authentication layouts and component compositions.
- Read relevant GEMS Authentication examples for desktop and mobile usage.
- Preserve official typography, colors, spacing, radius, effects, and responsive variants.
- Maintain accessible form controls and readable content.
- Do not add the main Application Navigation Sidebar to dedicated login pages.
- Do not invent additional authentication pages unless required by the confirmed flow.
- Do not create custom responsive patterns when official GEMS patterns exist.

If an essential layout is unsupported, request human approval before introducing an alternative.

## 9. Authentication UX & Security

**MUST**
- Follow confirmed authentication methods and business rules.
- Provide clear validation, error, loading, and success feedback.
- Protect passwords, tokens, and sensitive account information.
- Maintain accessible labels, keyboard navigation, and focus indicators.
- Follow approved account recovery and verification requirements.
- Respect product authorization and security architecture.

**MUST NOT**
- Invent authentication credentials, identity providers, or backend functionality.
- Expose sensitive information in visible UI messages.
- Simulate successful authentication as real production functionality.
- Bypass verification requirements.
- Add unsupported authentication methods.
- Treat UI visibility as a substitute for backend authorization.

## 10. Human Approval & Missing Requirements

Human Approval is REQUIRED when:
- Product branding or logo is unavailable.
- A new authentication method is proposed.
- Official GEMS components cannot support required behavior.
- A custom component or responsive layout is necessary.
- Authentication requirements conflict or materially affect the approved flow.

**Rules**
- Explain the missing requirement or limitation.
- Present available GEMS-compatible options.
- Ask all related approval questions in one consolidated message.
- Never interpret silence as approval.
- Do not introduce unapproved alternatives.

## 11. Strict Authentication Rules

**MUST**
- Use official GEMS Authentication components and variants.
- Obtain human confirmation of login requirements in one consolidated step.
- Configure authentication content according to confirmed product requirements.
- Follow Foundation `logo.md` for branding.
- Preserve official GEMS visual specifications.
- Apply appropriate component states and feedback.
- Read only relevant GEMS Page Samples and UX Patterns.
- Maintain accessible and security-conscious authentication UX.

**MUST NOT**
- Create custom Authentication components when official GEMS components exist.
- Invent login fields, methods, actions, or user flows.
- Add unconfirmed Captcha, OTP, SSO, Social Login, or registration.
- Substitute product branding without approval.
- Modify official colors, typography, spacing, radius, or effects.
- Introduce unsupported interaction states or responsive patterns.
- Repeatedly ask for information already confirmed.
- Use sample authentication content as final product requirements without confirmation.

**Fallback:** If GEMS does not support a required authentication configuration, preserve available official components and request Human Approval before introducing an alternative.

**Core Principle:** GEMS defines HOW authentication looks and behaves. Human-confirmed requirements define WHAT login fields, authentication methods, actions, and user flows are required. Confirm once, then implement consistently.

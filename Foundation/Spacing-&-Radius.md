
# GEMS Design System — Foundation / Spacing & Radius

> **MANDATORY:** All UI spacing and corner radius MUST use official GEMS Figma Variables. Applies to all layouts, pages, dashboards, forms, tables, components, and UX patterns.

## 1. Sources & Priority

**Source of Truth**
- [GEMS Spacing & Radius](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=237-4046) — Official Figma Variables
- [GEMS Components](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=12-1129)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1105-7310)

**Priority Order**
1. **Official Variables:** Gunakan existing GEMS Figma Spacing & Radius Variables secara langsung.
2. **GEMS Components:** Ikuti spacing dan radius bawaan komponen, termasuk variant, size, dan breakpoint.
3. **Page Samples & UX Patterns:** Gunakan sebagai referensi penerapan layout, alignment, spacing, dan radius.
4. **General UI/UX Principles:** Digunakan hanya jika GEMS belum memiliki ketentuan spesifik.

Official GEMS Variables dan component specifications memiliki prioritas tertinggi.

## 2. Available Spacing Variables

| Variable | Value |
|---|---|
| `spacing/0` | 0px |
| `spacing/1` | 4px |
| `spacing/2` | 8px |
| `spacing/3` | 12px |
| `spacing/4` | 16px |
| `spacing/5` | 20px |
| `spacing/6` | 24px |
| `spacing/7` | 32px |
| `spacing/10` | 40px |
| `spacing/12` | 48px |

**Spacing Rules**
- Apply existing GEMS Spacing Variables directly from Figma.
- Gunakan spacing variables untuk padding, gap, dan jarak antar elemen yang relevan.
- Ikuti spacing bawaan komponen resmi GEMS.
- Gunakan spacing yang konsisten untuk elemen dengan fungsi dan hierarchy yang sama.
- Pilih spacing berdasarkan layout, content hierarchy, dan referensi GEMS Page Samples.
- Jangan membuat intermediate spacing values yang tidak tersedia dalam GEMS.
- Jangan mengubah spacing bawaan komponen hanya berdasarkan visual preference.

## 3. Available Radius Variables

| Variable | Value |
|---|---|
| `radius-none` | 0px |
| `radius-xxs` | 2px |
| `radius-xs` | 4px |
| `radius-sm` | 6px |
| `radius-md` | 8px |
| `radius-lg` | 10px |
| `radius-xl` | 12px |
| `radius-2xl` | 16px |
| `radius-3xl` | 20px |
| `radius-4xl` | 24px |
| `radius-full` | 9999px |

**Radius Rules**
- Apply existing GEMS Radius Variables directly from Figma.
- Prioritize semantic Brand Radius Variables when available; preserve their references to Primitive.
- Gunakan radius sesuai spesifikasi komponen resmi GEMS.
- Pertahankan radius yang konsisten pada komponen dengan fungsi dan variant yang sama.
- Gunakan `radius-full` hanya pada elemen yang memang membutuhkan bentuk pill atau circular.
- Jangan membuat radius baru atau mengubah existing radius values.
- Jangan menerapkan radius berdasarkan preferensi visual jika komponen sudah memiliki ketentuan resmi.

## 4. Spacing & Radius Usage

Select spacing and radius based on official GEMS component specifications, page context, and layout hierarchy.

### Component Application

| UI Element | Usage Reference |
|---|---|
| Button | Official Button component |
| Input & Dropdown | Official Input and Dropdown components |
| Card | Official Card components |
| Table | Official Table components |
| Modal | Official Modal component |
| Navigation & Sidebar | Official Navigation components |
| Tabs & Filters | Official GEMS component variants |
| Page Header & Section | Official Page Header and Section components |
| Form Layout | GEMS Form Page and Input components |

**Rules**
- Gunakan spacing dan radius dari component instance yang digunakan.
- Jangan mengubah internal padding, gap, atau radius komponen resmi.
- Untuk custom layout, pilih existing variables berdasarkan konteks dan hierarchy.
- Pertahankan konsistensi spacing antar section dan elemen sejenis.
- Gunakan Auto Layout dan variable bindings jika didukung oleh lingkungan desain.
- Jangan menggunakan fixed spacing values untuk menggantikan variables yang tersedia.

## 5. Page Samples & UX Patterns

Gunakan contoh resmi GEMS sebagai referensi penerapan spacing, radius, alignment, dan layout composition.

**Page Samples**
- [Dashboard](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1170-3296)
- [List / Data Table](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=912-2563)
- [Detail Page](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=904-19934)
- [Form Page](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1175-82923)
- [Empty / Error State](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1253-25922)
- [Settings / Configuration](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1282-27704)

**UX Patterns**
- [Add New Data](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1161-481)
- [Edit Data](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1161-1938)
- [View Detail](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1259-37459)
- [Delete Data](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1161-2976)
- [Approve](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1161-4014)
- [Reject](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=3359-89283)
- [Revision](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1205-26388)
- [Export Data](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1214-42984)
- [Import Data](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1284-6558)

**Usage Rules**
- Ikuti struktur spacing dan radius dari contoh GEMS yang relevan.
- Pertahankan alignment, content spacing, dan layout hierarchy.
- Untuk reusable components, gunakan variables dan konfigurasi komponen aslinya.
- Jangan menyalin manual spacing atau radius dari sample jika tidak sesuai dengan official Variables.
- Jangan menggunakan spacing atau radius khusus CCM sebagai standar General.

## 6. Strict Spacing & Radius Rules

**MUST**
- Use existing GEMS Figma Spacing & Radius Variables.
- Preserve original variable references and values.
- Follow official GEMS component spacing and radius specifications.
- Reference Page Samples and UX Patterns for contextual usage.
- Maintain consistent spacing and radius across related UI screens.
- Use appropriate variables for responsive layouts.

**MUST NOT**
- Create new or duplicate spacing and radius variables.
- Hardcode spacing or radius values when official variables exist.
- Invent intermediate spacing or radius values.
- Modify official GEMS variable values.
- Override internal spacing or radius of official components.
- Detach existing variable bindings unnecessarily.
- Introduce arbitrary spacing scales or radius systems from external UI libraries.

**Fallback:** Jika komponen atau layout belum memiliki ketentuan spesifik, gunakan existing GEMS Spacing & Radius Variables yang paling sesuai berdasarkan fungsi, hierarchy, dan referensi Page Samples. Jangan membuat token baru.

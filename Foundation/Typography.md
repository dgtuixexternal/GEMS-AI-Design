
# GEMS Design System — Foundation / Typography

> **MANDATORY:** All text elements in GEMS UI MUST use official GEMS Figma Text Styles. Applies to all pages, dashboards, forms, tables, components, and UX patterns.

## 1. Typography Sources & Priority

**Source of Truth**
- [GEMS Typography](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=12-1127) — Official Figma Text Styles & Typography Variables
- [GEMS Components](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=12-1129)
- [GEMS Page Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=904-9049)
- [GEMS UX Pattern Samples](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1105-7310)

**Priority Order**
1. **Official Text Styles:** Apply existing GEMS Figma Text Styles directly, preserving all typography properties.
2. **GEMS Components:** Ikuti Text Style pada komponen resmi, termasuk variant, size, dan breakpoint.
3. **Page Samples & UX Patterns:** Gunakan sebagai referensi hierarchy dan penerapan typography dalam halaman.
4. **General UI/UX Hierarchy:** Digunakan hanya jika tidak ada ketentuan spesifik dari GEMS.

Jika terjadi perbedaan, official GEMS Text Styles dan component specifications memiliki prioritas tertinggi.

## 2. Available Text Styles

**Font Family:** Inter

| Text Style | Font Size | Line Height |
|---|---|---|
| `display 2xl` | 72px | 90px |
| `display xl` | 60px | 72px |
| `display lg` | 48px | 60px |
| `display md` | 36px | 44px |
| `display sm` | 30px | 38px |
| `display xs` | 24px | 32px |
| `text xl` | 20px | 30px |
| `text lg` | 18px | 28px |
| `text md` | 16px | 24px |
| `text sm` | 14px | 20px |
| `text xs` | 12px | 18px |

**Available Font Weights**

| Weight | Value |
|---|---|
| `regular` | 400 |
| `medium` | 500 |
| `semibold` | 600 |
| `bold` | 700 |

- Gunakan hanya kombinasi Text Style dan weight yang tersedia pada GEMS Figma Design System.
- Apply complete existing Text Styles, bukan mengatur properti typography secara manual.
- Font size, weight, line height, letter spacing, dan font family MUST mengikuti style aslinya.

## 3. Typography Usage & Hierarchy

Select Text Styles based on GEMS component usage, page context, and visual hierarchy.

### GEMS Component Reference

Contoh penerapan dari GEMS Page Header:

| UI Element | Text Style |
|---|---|
| Page Header Title | `display xs / semibold` |
| Page Header Description | `text md / regular` |
| Page Header Navigation | `text sm / medium` |
| Page Header Action Label | `text sm / semibold` |
| Page Header Search Text | `text md / regular` |

Reference: [GEMS Page Header](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=240-7175)

### General Hierarchy

Untuk elemen yang belum memiliki ketentuan khusus:

- **Display:** Gunakan `display *` untuk heading berskala besar.
- **Heading:** Pilih Text Style sesuai level hierarchy dan konteks halaman.
- **Body:** Gunakan `text *` untuk konten utama dan pendukung.
- **Label & Caption:** Gunakan `text *` sesuai fungsi, kepadatan informasi, dan readability.

General hierarchy merupakan fallback, bukan pengganti spesifikasi GEMS.

## 4. Page Samples & UX Patterns

Gunakan contoh resmi GEMS sebagai referensi penerapan typography dalam konteks halaman dan alur pengguna.

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
- Ikuti hierarchy typography pada contoh GEMS yang relevan.
- Untuk reusable components, gunakan Text Style dari komponen aslinya.
- Pertahankan konsistensi Text Style pada elemen dengan fungsi yang sama.
- Jangan menyalin ukuran manual dari sample yang tidak sesuai dengan official Text Styles.
- Jangan menggunakan typography khusus CCM sebagai standar General.

## 5. Typography Application Rules

- Apply existing GEMS Figma Text Styles directly; preserve their original style references.
- Gunakan Text Style sesuai fungsi, hierarchy, variant, dan breakpoint.
- Komponen dengan typography specification MUST mengikuti style resmi komponen tersebut.
- Jangan mengubah properti Text Style untuk menyesuaikan layout; sesuaikan container, spacing, atau text wrapping.
- Text color MUST follow GEMS Foundation Color Guidelines.
- Gunakan Text Styles resmi yang konsisten antara desktop dan mobile, kecuali GEMS menentukan perbedaan pada breakpoint tertentu.

## 6. Strict Typography Rules

**MUST**
- Use existing GEMS Figma Text Styles from the connected Design System.
- Preserve original Text Style references and properties.
- Follow official GEMS component typography specifications.
- Reference Page Samples and UX Patterns for contextual usage.
- Maintain consistent typography hierarchy.

**MUST NOT**
- Create new or duplicate Text Styles.
- Hardcode typography values outside existing GEMS Text Styles.
- Invent font sizes, weights, line heights, or letter spacing.
- Modify or override official Text Style properties.
- Detach Text Styles from their original GEMS references.
- Copy unsupported manual typography values from sample designs.
- Introduce external font families or typography scales.

**Fallback:** Jika belum ada ketentuan komponen atau contoh yang sesuai, gunakan existing GEMS Text Style yang paling sesuai berdasarkan fungsi dan visual hierarchy. Jangan membuat style baru.

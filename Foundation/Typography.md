
# GEMS Design System — Foundation / Typography

> **Mandatory:** Applies to all text elements in GEMS UI designs, dashboards, forms, tables, and components.

## 1. Typography Source

All UI text MUST use existing GEMS Text Styles defined in `design-tokens.tokens.json`.

- **Source:** `font/*` — official Figma Text Styles.
- **Reference:** `typography/*` — corresponding typography properties.
- **Font Family:** Inter.
- Gunakan Text Style yang tersedia, bukan membuat typography secara manual.
- Setiap teks wajib menggunakan kombinasi font size, weight, line height, dan letter spacing sesuai style aslinya.

## 2. Available Text Styles

| Style | Font Size | Line Height |
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

Each style supports these weights:

- `regular` — 400
- `medium` — 500
- `semibold` — 600
- `bold` — 700

Use the exact style combinations defined in JSON.

## 3. Typography Usage

Select Text Styles according to content hierarchy and UI purpose.

| UI Element | Recommended Style |
|---|---|
| Hero / Large Display | `display 2xl` – `display md` |
| Page Title | `display sm` – `display xs` |
| Section Title | `text xl` – `text lg` |
| Card Title | `text lg` – `text md` |
| Body Text | `text md` – `text sm` |
| Form Label & Input Text | `text sm` – `text md` |
| Button & Navigation | `text sm` – `text md` |
| Table Header & Cell | `text sm` |
| Helper Text & Caption | `text xs` – `text sm` |
| Badge & Status Label | `text xs` – `text sm` |

- Gunakan hierarchy yang konsisten antarhalaman.
- Pilih weight sesuai emphasis dan fungsi teks.
- Utamakan readability untuk dashboard, form, dan data table.
- Gunakan style komponen resmi jika sudah ditentukan dalam component guideline.

## 4. Text Style Application

- Apply the complete existing Text Style, not individual typography properties.
- Gunakan style yang sama untuk elemen dengan fungsi dan hierarchy yang sama.
- Gunakan `regular` untuk body text, `medium` untuk emphasis ringan, serta `semibold` atau `bold` untuk heading dan penekanan sesuai kebutuhan.
- Jangan memperbesar atau memperkecil font secara manual untuk menyesuaikan layout.
- Sesuaikan layout, spacing, atau text wrapping tanpa mengubah definisi Text Style.
- Text color MUST follow GEMS Foundation Color Guidelines.

## 5. Strict Typography Rules

**MUST**
- Use only existing GEMS Text Styles.
- Prioritize official component typography specifications.
- Preserve exact font family, size, weight, line height, and letter spacing.
- Maintain consistent text hierarchy across all UI screens.
- Use exact style names and values from JSON.

**MUST NOT**
- Create custom typography styles.
- Hardcode font sizes or weights outside the provided Text Styles.
- Modify existing typography token values.
- Use font families other than the official Text Style font.
- Invent new font sizes, line heights, weights, or letter spacing.
- Override typography defined by official GEMS components.

**Fallback:** Jika tidak ada Text Style yang sesuai, gunakan style terdekat yang tersedia berdasarkan hierarchy dan fungsi teks tanpa mengubah propertinya.

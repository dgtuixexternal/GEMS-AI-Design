# GEMS Design System — Foundation / Color

> **Mandatory:** Applies to all GEMS UI designs, dashboards, and components.

## 1. Color Sources

All UI colors MUST use official GEMS color tokens.

| Collection | Allowed Source |
|---|---|
| Brand | `General.tokens.json` only |
| Primitive | `Mode 1.tokens.json`, except `Color/Brand-CCM/*` |

- Semua Brand collections selain **General** dilarang.
- `Primitive/Color/Brand/*` diperbolehkan, tetapi `Primitive/Color/Brand-CCM/*` dilarang.
- File JSON merupakan **single source of truth** untuk seluruh warna.

## 2. Color Priority

1. **Semantic First:** Gunakan `Brand/General/Color/*` sesuai fungsi elemen UI.
2. **Primitive Fallback:** Gunakan `Primitive/Color/*` yang diizinkan hanya jika tidak tersedia semantic token yang sesuai.
3. **Exact Reference:** Pertahankan nama token, path, nilai, dan alias persis sesuai JSON.

Jangan mengganti semantic color dengan Primitive hanya berdasarkan preferensi visual.

## 3. Color Categories & Usage

| UI Element | Brand General Token |
|---|---|
| Text, Label, Placeholder | `Color/Text/*` |
| Page, Card, Table, Surface | `Color/Background/*` |
| Border, Divider, Outline | `Color/Border/*` |
| Icon, Foreground | `Color/Foreground/*` |
| Button Icon | `Color/Button/*` |
| Chart, Data Visualization | `Color/Utility/*` |
| Overlay, Transparency | `Color/Alpha/*` atau `Background/bg-overlay` |
| Status (Error, Success, Warning, Info) | Semantic tokens terkait pada Text, Background, Border, dan Foreground |

Semua kategori Primitive boleh digunakan kecuali `Color/Brand-CCM/*`. Gunakan hanya shade yang benar-benar tersedia di JSON.

## 4. Component States

Gunakan token yang sesuai untuk setiap state komponen:

`Default` · `Hover` · `Active` · `Selected` · `Disabled` · `Error` · `Success` · `Warning` · `Information`

- Gunakan state-specific tokens hanya jika tersedia di JSON.
- Dilarang membuat warna hover, disabled opacity, shade, atau variant secara manual.
- Pastikan kombinasi foreground/background tetap terbaca.

## 5. Strict Color Rules

**MUST**
- Use only existing GEMS color tokens.
- Prioritize Brand General semantic colors.
- Preserve exact token names, paths, values, and aliases.
- Apply colors based on UI purpose and component state.

**MUST NOT**
- Use Brand collections other than General.
- Use Primitive `Color/Brand-CCM/*`.
- Hardcode HEX, RGB, HSL, or named colors.
- Invent or modify colors, gradients, shades, opacity, or token values.
- Introduce external library color palettes.

**Fallback:** Jika token yang sesuai tidak tersedia, jangan membuat warna baru. Minta definisi token yang dibutuhkan.

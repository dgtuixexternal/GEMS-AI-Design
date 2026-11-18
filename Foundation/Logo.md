
# GEMS Design System — Foundation / Logo

> **MANDATORY:** All product logos MUST use official GEMS Figma Logo Components or user-approved custom logos. Logo selection MUST match the product identity and project context.

## 1. Logo Sources

**Source of Truth**
- [GEMS Logo — Digitech, iSafe, BIB](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=526-4237)
- [GEMS Logo — Sicantik, RPPJ](https://www.figma.com/design/vaAJgd6yZ7l9TrIuF04671?node-id=1870-12445)

**Available Official Logos**

| Product / Brand | Figma Logo Component |
|---|---|
| Digitech | `Logo=Digitech` |
| iSafe | `Logo=iSafe` |
| BIB | `Logo=BIB` |
| Sicantik | `Name=Sicantik` |
| RPPJ | `Name=RPPJ` |

Use existing logo components directly from the connected GEMS Figma Design System.

## 2. Context-Based Logo Selection

AI MUST select the appropriate logo based on product identity and project context.

**Selection Priority**
1. **Explicit User Instruction:** Jika user menentukan produk atau logo, gunakan logo tersebut.
2. **Project Context:** Jika tidak disebutkan secara eksplisit, identifikasi produk berdasarkan nama project, deskripsi, kebutuhan bisnis, atau konteks desain.
3. **Existing Design:** Jika melanjutkan desain, pertahankan logo produk yang sudah digunakan.
4. **Unclear Identity:** Jika identitas produk tidak dapat dipastikan, tanyakan kepada user.

**Rules**
- Gunakan logo yang sesuai dengan identitas produk.
- Jangan memilih logo berdasarkan warna atau visual preference.
- Jangan otomatis menggunakan Digitech atau BIB sebagai default.
- Pertahankan konsistensi logo pada seluruh halaman produk.
- Untuk multi-product systems, gunakan logo sesuai konteks masing-masing produk.
- Jika identitas produk sudah jelas dan logo tersedia di GEMS, gunakan langsung tanpa meminta konfirmasi tambahan.

## 3. Logo Application

- Apply official GEMS Logo Components directly from Figma.
- Gunakan component instance, bukan menggambar ulang logo.
- Preserve original logo proportions, shapes, colors, and visual identity.
- Gunakan variant, size, dan configuration resmi apabila tersedia.
- Ikuti ketentuan layout dan responsive behavior pada komponen GEMS.
- Jika logo sudah tersedia dalam komponen Sidebar, Navigation, atau Authentication, gunakan logo dan konfigurasi resmi yang sesuai.
- Gunakan logo secara konsisten pada area yang membutuhkan identitas produk.
- Jangan menambahkan logo pada elemen yang tidak memerlukan branding.
- Custom logos hanya boleh digunakan berdasarkan keputusan dan aset resmi yang diberikan atau disetujui user.

## 4. Logo Consistency

- Gunakan identitas logo utama sesuai produk yang sedang didesain.
- Pertahankan penggunaan logo yang konsisten pada seluruh halaman dan UX flows.
- Gunakan responsive variants resmi jika tersedia.
- Jika melanjutkan existing design, pertahankan logo sebelumnya kecuali user meminta perubahan.
- Jangan mencampurkan logo produk berbeda tanpa kebutuhan bisnis atau instruksi yang jelas.
- Jangan mengganti logo yang sudah disetujui tanpa persetujuan user.

## 5. Human Approval — Missing Product Logo

If the requested product logo is unavailable in GEMS, AI MUST obtain explicit human approval before selecting or substituting a logo.

**Required Flow**

1. Identify the product and check available GEMS Logo Components.
2. Jika logo produk tidak tersedia, informasikan kepada user.
3. Minta user memilih salah satu opsi:
   - **Use Existing GEMS Logo:** User memilih salah satu logo resmi GEMS sebagai pengganti.
   - **Upload Custom Logo:** User mengunggah logo resmi produk yang akan digunakan.
4. Jika memilih existing GEMS logo, gunakan hanya logo yang secara eksplisit disetujui user.
5. Jika memilih custom logo, gunakan aset yang diunggah tanpa mengubah identitas visualnya.
6. Apply the selected logo only after user confirmation.

**Approval Rules**
- Human approval is REQUIRED for missing or substituted product logos.
- MUST NOT automatically choose another product logo as a replacement.
- MUST NOT interpret silence or missing information as approval.
- MUST NOT generate a replacement logo without explicit authorization.
- Jika user belum memberikan keputusan, logo tetap berstatus pending dan AI dapat melanjutkan bagian desain yang tidak bergantung pada logo.
- Jangan menggunakan placeholder yang menyerupai identitas brand lain.

## 6. Strict Logo Rules

**MUST**
- Use official GEMS Logo Components or user-approved custom logos.
- Select logos based on product identity and user context.
- Prioritize explicit user instructions.
- Preserve original logo proportions, colors, shapes, and visual identity.
- Maintain consistent branding across related UI screens.
- Reuse existing logo instances and official component variants.
- Obtain human approval when a matching product logo is unavailable.

**MUST NOT**
- Create, redraw, or generate product logos without authorization.
- Replace official logos with text, emoji, or generic icons.
- Modify logo colors, proportions, shapes, or typography.
- Stretch, distort, crop, or rotate logos arbitrarily.
- Substitute another product logo without explicit approval.
- Mix different product logos without clear business requirements.
- Assume a default logo when product identity is unclear.
- Detach or recreate official GEMS Logo Components unnecessarily.
- Override a previously approved logo without user confirmation.

**Fallback:** Jika logo produk tidak tersedia di GEMS, wajib meminta persetujuan user untuk menggunakan logo GEMS yang sudah ada atau mengunggah custom logo. Jangan menentukan identitas brand pengganti secara otomatis.

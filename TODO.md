# Photo Print Tool — Future Features

## High Priority

### 1. Image Crop Tool
- Interactive crop overlay on the photo preview
- Aspect ratio lock (free, 1:1, 3:4, 4:5, passport ratio)
- Drag handles to resize crop box
- Apply crop as non-destructive transform (store crop rect, bake on export)
- Crop button in photo card (Group 2, alongside fit mode)

### 2. Background Removal
- Client-side ML model (`@imgly/background-removal` or similar)
- Auto-detect person, remove background
- Replace with white / solid color / custom color
- Essential for passport photos with non-white backgrounds

### 3. Brightness / Contrast / Saturation
- Per-photo sliders (-100 to +100)
- CSS `filter` for preview, Canvas `ctx.filter` for export
- "Apply to all" batch option
- Reset per-photo button

### 4. Border / Frame
- Per-photo or global border
- Width slider (0-5mm)
- Color picker (white, black, custom)
- Rounded corners option

### 5. Batch Edit
- "Apply to all" button for: size, rotation, fit mode, position, brightness/contrast
- Select multiple photos, edit once
- Apply changes to selected group

---

## Medium Priority

### 6. Auto Enhance
- One-click auto brightness/contrast/sharpness
- Canvas-based histogram equalization or simple curve adjustment
- Preview before/after toggle

### 7. Grayscale / Sepia Filter
- Per-photo filter selector
- Grayscale for ID photos
- Sepia for vintage look
- CSS `filter: grayscale(1)` / `filter: sepia(1)` for preview, canvas for export

### 8. Save / Load Project
- Export full state as JSON (photos as data URLs + all settings)
- Import JSON to restore session
- Auto-save to `localStorage` every change
- "Resume last project" prompt on load

### 9. PDF Export
- Direct PDF download via jsPDF or pdf-lib
- A4 page size, 300 DPI
- Multi-page support
- No print dialog needed

### 10. White Background Fill Color
- In cover mode, choose letterbox color (white, blue, grey, custom)
- Affects export only (preview already shows white)

---

## Low Priority

### 11. Red-Eye Removal
- Canvas-based detection and correction
- Manual click-to-fix on detected red eyes

### 12. Image Sharpening
- Unsharp mask via canvas convolution
- Strength slider

### 13. Color Temperature / White Balance
- Warm/cool slider
- Canvas pixel manipulation

### 14. Exposure Adjustment
- Highlights / Shadows / Midtones sliders
- Canvas pixel manipulation

### 15. Face Detection
- Auto-detect faces for centering crop
- Auto-arrange passport photos with face in correct position

### 16. Watermark
- Text or image watermark overlay
- Position, opacity, font controls
- Optional on export

### 17. Photo Retouching
- Blemish removal (clone stamp)
- Skin smoothing

### 18. Multi-Language Support
- Hindi, English, Tamil, etc.
- i18n framework integration

### 19. Template Presets
- Save custom size + layout combinations
- Quick-apply common layouts (e.g., "6 passport on A4")

### 20. Cloud Backup
- Save projects to cloud storage
- Share project links

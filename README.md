# 🪪 Bulk ID Card Generator Pro — Chrome Extension

A powerful, fully-featured Chrome Extension for generating professional bulk ID cards with a single click.

---

## 🚀 Features

### Data Import
- **CSV / Excel import** — Bulk load hundreds of records at once
- **Manual entry form** — Add individual records with rich fields
- **Paste CSV** — Paste data directly from clipboard
- **Sample data** — Try the extension with built-in demo records
- **CSV Template download** — Get the exact column format

### Design & Customization
- **6 built-in templates** — Corporate, University, Hospital, Event, School, Government
- **Custom card sizes** — CR80 (standard credit card), A4 sheet, or custom dimensions
- **Organization branding** — Logo upload, org name, tagline, website
- **Full color control** — Primary, secondary, background, and text colors with color picker
- **Font selection** — 7 font families to choose from
- **Feature toggles** — Show/hide QR code, barcode, photo, blood group, email, phone, validity, address, website, shadow, rounded corners

### Security Features
- **QR Code generation** — Encoded with employee/student data
- **Barcode rendering** — ID-encoded barcode strip
- **Watermark** — Custom text watermark overlay
- **Security patterns** — Guilloche, dot grid, fine lines, micro text band

### Preview
- **Live card preview** — See exactly how cards will look before export
- **Navigation** — Browse through all records with Prev/Next
- **Card flip** — Preview the back side if enabled
- **Zoom** — Zoom in/out on the preview canvas

### Export
- **PDF** — Print-ready multi-card layout (opens print dialog, save as PDF)
- **PNG** — High-resolution individual card images
- **JPG** — Compressed image format
- **HTML Gallery** — Self-contained gallery page with all cards + download buttons
- **DPI control** — 72 / 150 / 300 / 600 DPI
- **Cards per page** — 1, 2, 4, 8, or 10 cards per PDF page
- **Export scope** — All records, selected only, or page range
- **Session history** — Track all exports in the current session

### Other
- **Settings** — Persists organization defaults across sessions
- **Chrome Storage** — Saves preferences via chrome.storage.local
- **Search & filter** — Search through records in the data table
- **Edit / Delete** — Modify or remove individual records

---

## 📦 Installation (Developer Mode)

1. Extract the ZIP file to a folder.
2. Open Chrome and go to `chrome://extensions/`.
3. Enable **Developer Mode** (top right toggle).
4. Click **Load Unpacked** and select the extracted folder.
5. The extension icon will appear in your toolbar.

---

## 📤 Publishing to Chrome Web Store

1. Go to [Chrome Web Store Developer Dashboard](https://chrome.google.com/webstore/devconsole)
2. Click **+ New Item**
3. Upload the `.zip` file
4. Fill in:
   - Description (copy from above)
   - Screenshots (take from the extension popup)
   - Category: **Productivity**
   - Language: English
5. Set Privacy Policy URL (required)
6. Submit for review

---

## 📋 CSV Format

```
name,id,department,designation,email,phone,blood_group,dob,address,photo_url,valid_from,valid_until
John Doe,EMP-001,Engineering,Developer,john@company.com,+1-555-0100,O+,1990-01-01,123 Main St,,2024-01-01,2025-12-31
```

**Required columns:** `name`, `id`

**Optional:** `department`, `designation`, `email`, `phone`, `blood_group`, `dob`, `address`, `photo_url`, `valid_from`, `valid_until`

---

## 🛠 Technical Stack

- **Manifest V3** Chrome Extension
- **Vanilla JS** (no frameworks, maximum performance)
- **HTML5 Canvas** for card rendering
- **QRCode.js** for QR code generation
- **Chrome Storage API** for settings persistence
- **Chrome Downloads API** for file export
- **FileReader API** for CSV/image import

---

## 📁 File Structure

```
bulk-id-generator/
├── manifest.json           # Chrome Extension manifest v3
├── icons/                  # Extension icons (16,32,48,128px)
├── lib/
│   └── qrcode.min.js       # QR code generator
├── popup/
│   ├── popup.html          # Main UI
│   ├── popup.css           # All styles (dark theme)
│   ├── popup.js            # Core: tabs, data import, form
│   ├── renderer.js         # Canvas card drawing engine
│   ├── exporter.js         # Export: PDF/PNG/JPG/HTML
│   └── modals.js           # Settings & help modals
└── background/
    └── service_worker.js   # Background tasks, download handling
```

---

## 📝 License

MIT License — Free to use, modify, and distribute.

---

## 👤 Author

Built with ❤️ using Bulk ID Card Generator Pro

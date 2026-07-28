# Fincalcfree.com - AI Hardcore Operational Rules & Guidelines

## Core Directive
Protect the functional integrity of the main English website at all times. Never overwrite, delete, or break working core files when adding new features or language translations.

---

## 1. Absolute Don'ts (Hard Constraints)
- ❌ **DO NOT modify main English root files directly** (`index.html`, `loan.html`, `finance-calculator.html`, `investment.html`, `retirement.html`, `about.html`, `contact.html`, etc.) when creating translations or experimenting.
- ❌ **DO NOT alter HTML `id` attributes, JavaScript variable names, or formula logic** during translation. UI text changes must never touch computational logic.
- ❌ **DO NOT replace or delete core files** without creating a backup copy or git commit first.
- ❌ **DO NOT assume code works** after translation or refactoring; calculation engines and navigation must be verified.

---

## 2. Mandatory Dos (Safeguards & Workflow Rules)
- ✅ **Isolated Subdirectories for Languages**: All non-English versions MUST live in dedicated subfolders (e.g., `/fr/` for French, `/es/` for Spanish).
- ✅ **Backup Before Editing**: Always make a snapshot or git commit of working files before performing edits across multiple pages.
- ✅ **Copy-First Strategy**: To create a French page (e.g., French Loan Calculator), copy `loan.html` into `/fr/loan.html` first. Never edit root `loan.html` to translate it.
- ✅ **Strict Functional Parity**: Translated pages must maintain identical calculator responsiveness, charts, print features, and script bindings as their English counterparts.
- ✅ **Explicit Approval for Core Changes**: Any change to shared root assets (navbars, language toggles, global CSS) requires explicit approval.

---

## 3. Translation & Modification Checklist
1. **Snapshot/Backup**: Ensure root files are backed up.
2. **Target Isolation**: Work strictly inside the target subfolder (`/fr/`).
3. **Text-Only Translation**: Translate user-visible headers, paragraphs, labels, and tooltips. Preserve all tag attributes (`id="..."`, `class="..."`, `onchange="..."`, `data-*`).
4. **Path & Link Verification**: Ensure asset paths (`style.css`, scripts) and page links resolve correctly.
5. **Calculator Verification**: Test calculations on the newly generated page.

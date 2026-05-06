<p align="center">
  <img src="banner.svg" alt="Templates Banner" width="100%"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Format-PDF-EC1C24?style=flat-square&logo=adobeacrobatreader&logoColor=white" alt="PDF"/>
  <img src="https://img.shields.io/badge/Format-DOCX-2B579A?style=flat-square&logo=microsoftword&logoColor=white" alt="DOCX"/>
  <img src="https://img.shields.io/badge/Use-Pen_Testing-58a6ff?style=flat-square&logo=hackthebox&logoColor=white" alt="Pen Testing"/>
  <img src="https://img.shields.io/badge/Use-Auditing-8b5cf6?style=flat-square&logo=files&logoColor=white" alt="Auditing"/>
  <img src="https://img.shields.io/badge/Metadata-Stripped-22c55e?style=flat-square&logo=shieldsdotio&logoColor=white" alt="Metadata Stripped"/>
  <img src="https://img.shields.io/badge/License-MIT-blue?style=flat-square" alt="License"/>
  <img src="https://img.shields.io/badge/Author-SkyzFallin-ce9178?style=flat-square&logo=github&logoColor=white" alt="Author"/>
</p>

# Templates — Pen Testing &amp; Auditing Document Templates

By [SkyzFallin](https://github.com/SkyzFallin) | [GitHub Repo](https://github.com/SkyzFallin/Templates)

A small, growing collection of reusable document templates for pen testing, auditing, and the business side of running engagements — work orders, scoping docs, reports, checklists, and forms. Every file is published with metadata scrubbed so you can drop your own branding in without leaking the previous author, machine, or revision history.

## Available Templates

| Template | PDF | DOCX | Description |
|---|---|---|---|
| Printer / Copier Service Work Order | [PDF](Printer_Repair_Workorder_Template.pdf) | [DOCX](Printer_Repair_Workorder_Template.docx) | Single-page service work order for printer / copier repair calls — customer + equipment, reported issue, parts &amp; labor, post-service verification, totals, and signatures. |

## Usage

1. Pick a template from the table above.
2. Open the DOCX in Word / LibreOffice and replace the `[Business Name]` / `[Business Address]` / `[Business Phone Number]` placeholders with your own.
3. Swap in your own logo / branding — these templates ship with generic, text-only headers on purpose. Drop your company logo into the header (Insert → Picture) and restyle the title to match your brand.
4. Customize fields to fit the engagement.
5. Export to PDF when you're ready to send it.

The PDF copies are provided for reference / printing. The DOCX is the editable source.

## Metadata Hygiene

All files in this repo have been scrubbed of identifying metadata before commit:

**PDF** — `/Author`, `/Title`, `/Subject`, `/Keywords`, `/Producer`, `/Creator`, `/CreationDate`, `/ModDate` all blanked out.

**DOCX** — `core.xml` (author, lastModifiedBy, title, subject, keywords, etc.) blanked, `app.xml` (Application, Company, Manager, AppVersion) blanked, timestamps reset to `2000-01-01T00:00:00Z`, embedded thumbnail removed.

Why this matters: when you take one of these files, edit it, and ship it to a client, your editor will overwrite *its own* metadata fields — but anything left over from a prior author would still be there. Starting from a clean baseline means you only ever leak your own data, not someone else's.

If you fork this repo and add new templates, run them through a metadata stripper (e.g. `exiftool -all= file.pdf`, or open in Word → File → Info → Inspect Document → Remove All) before committing.

## Disclaimer &amp; Authorized Use

These templates are provided **as-is, for lawful use only**, with no warranty of any kind. They are administrative documents — work orders, scoping forms, reports, checklists — and do not themselves perform any testing or grant any authority.

**If you are using these for a pen test, vulnerability assessment, red-team engagement, or any other security testing activity:** you are solely responsible for ensuring that the engagement is properly scoped, authorized in writing by the asset owner, and conducted within the bounds of all applicable laws (including but not limited to the Computer Fraud and Abuse Act in the US, the Computer Misuse Act in the UK, and equivalent statutes elsewhere). A signed scope-of-work, rules-of-engagement document, and explicit written authorization from someone with legal authority over the target systems must be in place **before any testing begins**.

Filling out a work order or report from this repo is **not** a substitute for that authorization. Unauthorized access, scanning, or testing of systems you do not own or have not been explicitly permitted to test is illegal in most jurisdictions and may result in criminal and civil liability.

The author of this repository (SkyzFallin) makes no representation that any template here is fit for a particular purpose, complies with any specific regulatory framework, or constitutes legal advice. **Consult a qualified attorney** before relying on any of these documents in a contractual or legal context. By using these templates you agree that the author bears no liability for any damages, losses, or legal consequences arising from your use of them.

See [LICENSE](LICENSE) for the full terms.

## Contributing

Pull requests for new templates are welcome. Guidelines:

- Provide both PDF and DOCX (or PDF only if it's a fillable form).
- Strip metadata before committing — see above.
- Keep placeholders generic (`[Business Name]`, `[Client]`, `[Date]`) so others can drop their own info in.
- One template per PR with a short note in the README table.

## License

MIT — Made by [SkyzFallin](https://github.com/SkyzFallin)

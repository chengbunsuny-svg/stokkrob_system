

## រចនាសម្ព័ន្ធ (main)
```
stokkrob/
├─ index.html              ← បញ្ជី <script> (លំដាប់សំខាន់!)
├─ README.md  CONTRIBUTING.md  package.json  .prettierrc.json  .editorconfig  .gitignore
├─ assets/
│  ├─ icons/               ← icon SVG ១៤ + preview.html + README   [ស្រីណា]
│  └─ fonts/               ← ពុម្ពអក្សរ .woff2 (self-host) + README  [ស្រីណា]
├─ css/
│  ├─ fonts.css  tokens.css           ← ពណ៌/ទំហំ/ពុម្ពអក្សរ (dark/light)          [ស្រីណា]
│  ├─ base.css  layout.css  components.css                          [ស្រីណា]
│  └─ pos.css  print.css                                            [ប៊ុនសុង]
├─ js/
│  ├─ core/   schema · money · storage · data · helpers · auth      [ប៊ុនសុង]
│  │          i18n [ស្រីណា] · export [ស្រីយ៉ុង]
│  ├─ ui/     escape · icons · shared · modal · toast                       [ស្រីណា]
│  ├─ views/  ១ ទំព័រ = ១ ឯកសារ (បង្ហាញ)
│  ├─ actions/ ១ ផ្នែក = ១ ឯកសារ (ឥរិយាបថ ប៊ូតុង data-a)
│  └─ app.js · events.js · main.js                                  [ប៊ុនសុង]
├─ tests/                  ← node:test (money, sales, stock, reports, debt, schema)
├─ docs/                   ← PLAN, ARCHITECTURE, DATA-MODEL, GIT-WORKFLOW, TEST-CHECKLIST
└─ .github/                ← CODEOWNERS, PR/Issue template, workflows/check.yml
```
ម្ចាស់ឯកសារ: **ប៊ុនសុង**, **ស្រីយ៉ុង**, **ស្រីណា** (ឃើញ `docs/MEMBERS.md`)។



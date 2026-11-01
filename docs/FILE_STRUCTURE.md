# រចនាសម្ព័ន្ធឯកសារ — ឯកសារនីមួយៗប្រើសម្រាប់អ្វី

> **ស្ថានភាពបច្ចុប្បន្ន៖** ឯកសារក្នុង `css/` និង `js/` ទទេ (មានតែក្បាលពន្យល់ម្ចាស់ និងកិច្ចការ) កូដដែលដំណើរការរួចស្ថិតក្នុង `reference/StokKrob_v3_1.html` រង់ចាំត្រូវបានបំបែកចូលឯកសារទាំងនេះ។
>
> ម្ចាស់ និងកិច្ចការលម្អិតនៃឯកសារនីមួយៗ មើល `docs/FILE_OWNERS.md`។

## របៀបគិត៖ Website នេះមាន ៣ ស្រទាប់

| ស្រទាប់ | ថត | ប្រៀបដូចជា |
|---|---|---|
| **រចនាសម្ព័ន្ធ** | `index.html` | គ្រោងផ្ទះ |
| **រូបរាង** | `css/` | ពណ៌ថ្នាំលាប និងការតុបតែង |
| **ការគិត / ដំណើរការ** | `js/` | ប្រព័ន្ធភ្លើង ទឹក ដែលធ្វើឲ្យផ្ទះប្រើបាន |

## ផែនទីទាំងមូល

```
stokkrob/
├── index.html
├── README.md · CONTRIBUTING.md · .gitignore
├── css/
│   ├── tokens.css · fonts.css · base.css · layout.css · components.css
│   └── screens/   login · dashboard · pos · products · receive · customers · reports · settings
├── js/
│   ├── main.js
│   ├── core/      state · helpers · events · i18n · theme · icons · router
│   └── screens/   login · dashboard · pos · products · receive · customers · reports · settings
├── assets/        fonts/ · icons/
├── design/        screens/ · design-tokens.json · COLORS.md
├── reference/     StokKrob_v3_1.html (កូដដើម)
├── docs/          TEAM_PLAN · GIT_GUIDE · FILE_OWNERS · ARCHITECTURE · FILE_STRUCTURE
└── .github/       CODEOWNERS · pull_request_template.md · ISSUE_TEMPLATE/
```

## ១. ឯកសារនៅ root

| ឯកសារ | ប្រើសម្រាប់ |
|---|---|
| `index.html` | **ទំព័រមេ** Browser បើកឯកសារនេះមុន។ វាមានប្រអប់ទទេ ៣ (`#app` ទំព័រ, `#modal` ផ្ទាំងលោត, `#toast` សារ) ហើយភ្ជាប់ CSS និង JS តាមលំដាប់ |
| `README.md` | ទំព័រស្វាគមន៍លើ GitHub៖ គម្រោងអ្វី, ក្រុម, ចាប់ផ្តើមយ៉ាងណា |
| `CONTRIBUTING.md` | ក្បួនចូលរួម ៦ ជំហាន (Branch → កែ → Pull Request) |
| `.gitignore` | បញ្ជីឯកសារដែល Git មិនត្រូវតាមដាន (`.psd`, `.mp4`, `.zip`...) កុំឲ្យ repo ធ្ងន់ |

## ២. `css/` — រូបរាង

| ឯកសារ | ប្រើសម្រាប់ | ម្ចាស់ |
|---|---|---|
| `tokens.css` | **ឃ្លាំងតម្លៃ**៖ ពណ៌ ទំហំអក្សរ Radius គម្លាត (Light + Dark) កែទីនេះបន្ទាត់មួយ ប្តូរទាំង Website | ប៊ុនសុង |
| `fonts.css` | `@font-face` ភ្ជាប់ឯកសារពុម្ពអក្សរក្នុង `assets/fonts` | ប៊ុនសុង |
| `base.css` | ស្ទីលមូលដ្ឋានបំផុត៖ reset, `body`, `input`, `label` | ប៊ុនសុង |
| `layout.css` | **ក្របខ័ណ្ឌទំព័រ**៖ Sidebar, របារខាងលើ, ក្រឡាចត្រង្គ, Responsive | ប៊ុនសុង |
| `components.css` | **ធាតុប្រើរួម**៖ ប៊ូតុង, កាត, Badge, តារាង, Modal, Toast, Animation | ប៊ុនសុង |
| `screens/*.css` | ស្ទីល**តែអេក្រង់នោះ** | តាមអេក្រង់ |

**ក្បួនចាំ៖** ប្រើច្រើនកន្លែង → `components.css`; ប្រើតែអេក្រង់មួយ → `screens/`។

## ៣. `js/` — ដំណើរការ

### `js/core/` — ស្នូលប្រើរួម (ម្ចាស់៖ ប៊ុនសុង)

| ឯកសារ | ប្រើសម្រាប់ |
|---|---|
| `state.js` | **ទិន្នន័យ**៖ ទំនិញ អតិថិជន បិល (`D`), អ្នកប្រើបច្ចុប្បន្ន (`U`), អេក្រង់បច្ចុប្បន្ន (`V`), កន្ត្រក; ទិន្នន័យសាកល្បង `seed()`, រក្សាទុក/ទាញយក `localStorage` |
| `helpers.js` | អនុគមន៍ជំនួយប្រើគ្រប់កន្លែង៖ `toast()`, `modal()`, ត្រង `filt()`, នាំចេញ CSV |
| `events.js` | **ទទួលការចុច / វាយ / ក្តារចុច** ហើយបញ្ជូនទៅ Action ត្រឹមត្រូវ (តាម `data-a`) |
| `i18n.js` | ភាសា ខ្មែរ ↔ English (តារាងបកប្រែ និង `T()`) |
| `theme.js` | Dark ↔ Light |
| `icons.js` | តារាង SVG Icon និង `ic('ឈ្មោះ')` |
| `router.js` | ម៉ឺនុយ, ជ្រើសថាបង្ហាញអេក្រង់មួយណា, ស៊ែល (Sidebar + Topbar), `render()` |

### `js/screens/` — មួយឯកសារ = មួយអេក្រង់

| ឯកសារ | អេក្រង់ | ម្ចាស់ |
|---|---|---|
| `login.js` | ចូលប្រើ, ពាក្យសម្ងាត់, ចាកចេញ | ប៊ុនសុង |
| `pos.js` | លក់៖ កន្ត្រក, បង់ប្រាក់, វិក្កយបត្រ | ប៊ុនសុង |
| `settings.js` | ការកំណត់៖ Backup/Restore, ប្តូរពាក្យសម្ងាត់, Reset | ប៊ុនសុង |
| `products.js` | ទំនិញ៖ បន្ថែម កែ ឈប់លក់ កែតម្រូវស្តុក | ស្រីយ៉ុង |
| `receive.js` | ទទួលទំនិញចូល | ស្រីយ៉ុង |
| `customers.js` | អតិថិជន និងជំពាក់ | ស្រីយ៉ុង |
| `dashboard.js` | ទំព័រដើម៖ កាតស្ថិតិ, ក្រាហ្វិច | ស្រីណា |
| `reports.js` | របាយការណ៍, បោះបង់បិល | ស្រីណា |

ឯកសារអេក្រង់នីមួយៗមាន ២ ផ្នែកធំ៖ **(១) អនុគមន៍បង្កើត HTML** និង **(២) Actions** (អ្វីដែលកើតឡើងពេលចុចប៊ូតុង)។

### `js/main.js`
ចាប់ផ្តើម៖ ហៅ `render()` ម្តង និងដំណើរការនាឡិកាក្នុងរបារខាងលើ។ ខ្លីបំផុត (ប្រហែល ២ បន្ទាត់)។

## ៤. ថតផ្សេងៗ

| ថត | ប្រើសម្រាប់ |
|---|---|
| `assets/fonts/` | ពុម្ពអក្សរ Plus Jakarta Sans + Noto Sans Khmer៖ `woff2/` សម្រាប់ Website, `ttf/` សម្រាប់ដំឡើងក្នុង Figma, `variable/`, `licenses/` |
| `assets/icons/` | Icon SVG ១៤ (`nav/` ម៉ឺនុយ, `ui/` កណ្តឹង, `kpi/` កាតស្ថិតិ) + `EMOJI.md` + `ICONS-SHEET.png` |
| `design/` | រូបគំរូ ១៦ សន្លឹក (`screens/`), `design-tokens.json`, `COLORS.md`៖ គោលដៅរូបរាងដែលត្រូវសម្រេច |
| `reference/` | កូដដើមដែលដំណើរការរួច (ឯកសារតែមួយ) **កុំកែ** ប្រើជាគំរូចម្លង/ប្រៀបធៀប |
| `docs/` | `TEAM_PLAN.md` ផែនការ, `GIT_GUIDE.md` របៀបប្រើ Git, `FILE_OWNERS.md` ម្ចាស់ឯកសារ, `ARCHITECTURE.md` ឯកសារភ្ជាប់គ្នាយ៉ាងណា, `FILE_STRUCTURE.md` ឯកសារនេះ |
| `.github/` | `CODEOWNERS` (ឲ្យម្ចាស់ពិនិត្យ PR), `pull_request_template.md` (បញ្ជីត្រួតពិនិត្យ), `ISSUE_TEMPLATE/` (គំរូ Task/Bug) |

## ៥. ពេលចុចប៊ូតុងមួយ តើឯកសារអ្វីធ្វើការ?

1. `events.js` ចាប់ការចុច អាន `data-a="..."` ពីប៊ូតុង
2. ហៅ **Action** ដែលនៅក្នុង `screens/<ឈ្មោះអេក្រង់>.js`
3. Action កែទិន្នន័យ `D` (ដែល `state.js` កំណត់រចនាសម្ព័ន្ធ)
4. ហៅ `sv()` រក្សាទុក ហើយ `render()` (នៅ `router.js`)
5. `render()` ហៅអនុគមន៍អេក្រង់ ដើម្បីសាងសង់ HTML ថ្មី ហើយ CSS ធ្វើឲ្យស្អាត

## ៦. ចង់កែអ្វី → កែឯកសារណា

| ចង់ | កែនៅ |
|---|---|
| ប្តូរពណ៌ ទំហំអក្សរ ឬ Radius ទាំង Website | `css/tokens.css` |
| ប្តូររូបរាងប៊ូតុង ឬកាត | `css/components.css` |
| កែរូបរាងតែទំព័រមួយ | `css/screens/<ឈ្មោះ>.css` |
| កែអ្វីដែលកើតឡើងពេលចុចប៊ូតុងក្នុងទំព័រមួយ | `js/screens/<ឈ្មោះ>.js` |
| បន្ថែមពាក្យ English ថ្មី | ក្នុងឯកសារអេក្រង់នោះ (មើល `docs/ARCHITECTURE.md`) |
| បន្ថែមវាលទិន្នន័យថ្មី (ឧ. អ៊ីមែលអតិថិជន) | ប្រាប់ ប៊ុនសុង (`state.js`) |
| បន្ថែម Icon ថ្មី | `assets/icons/` + `js/core/icons.js` |
| ប្តូរពុម្ពអក្សរ | `assets/fonts/` + `css/fonts.css` + `css/tokens.css` |

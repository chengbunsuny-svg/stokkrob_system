# Fonts
ស្រីណា

ពេលនេះកម្មវិធីផ្ទុកពុម្ពអក្សរពី Google Fonts (ក្នុង `index.html`) ដែលមិនដំណើរការពេលអ៊ីនធឺណិតដាច់។ ថតនេះសម្រាប់ **ពុម្ពអក្សរក្នុងកម្មវិធីខ្លួនឯង (self-host)** ដើម្បីឱ្យ POS ដំណើរការ offline។

## ឯកសារត្រូវមាន (ទម្រង់ .woff2)
| ឯកសារ | Family | Weight |
|---|---|---|
| `NotoSansKhmer-Regular.woff2` | Noto Sans Khmer | 400 |
| `NotoSansKhmer-Medium.woff2` | Noto Sans Khmer | 500 |
| `NotoSansKhmer-SemiBold.woff2` | Noto Sans Khmer | 600 |
| `NotoSansKhmer-Bold.woff2` | Noto Sans Khmer | 700 |
| `PlusJakartaSans-Regular.woff2` | Plus Jakarta Sans | 400 |
| `PlusJakartaSans-Medium.woff2` | Plus Jakarta Sans | 500 |
| `PlusJakartaSans-SemiBold.woff2` | Plus Jakarta Sans | 600 |
| `PlusJakartaSans-Bold.woff2` | Plus Jakarta Sans | 700 |

## របៀបទាញយក
១. ទៅ fonts.google.com → ស្វែងរក Noto Sans Khmer និង Plus Jakarta Sans → Download family (license: SIL OFL — ប្រើ/ចែកចាយបានសេរី)។
២. បំលែង .ttf ទៅ .woff2 (ឧ. ឧបករណ៍ក្នុង fontsource.org ឬ google-webfonts-helper) រួចដាក់ក្នុងថតនេះ។
៣. ដាក់ឯកសារ `LICENSE-OFL.txt` ទៅជាមួយ។
៤. កែ `css/fonts.css` ឱ្យបង្ហាញឯកសារទាំងនេះ ហើយលុយ `<link>` Google Fonts ក្នុង `index.html` (ជា PR ដាច់ដោយឡែក — សួរប៊ុនសុងដោយសារ `index.html` ជាឯកសារចែករំលែក)។
៥. សាកល្បង: បិទអ៊ីនធឺណិត ហើយបើកកម្មវិធី អក្សរខ្មែរ និងលេខត្រូវបង្ហាញត្រឹមត្រូវ។

ចំណាំ: ទំហំ Noto Sans Khmer ធំជាងអក្សរឡាតាំង — ទាញយកតែ weight ដែលប្រើ (៤ ខាងលើ)។

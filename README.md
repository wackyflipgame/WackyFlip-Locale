# 🌍 WackyFlip-Locale

Localization & Internationalization
This repository contains all language files, translation tools, and region-specific settings used to make [Wacky Flip](https://wackyflip.com) a global gaming experience.

---

## 🌐 Overview

`WackyFlip-Locale` powers the multilingual capabilities of the Wacky Flip platform, enabling support for players worldwide. It includes translation dictionaries, automated localization scripts, and configuration files tailored for specific languages, regions, and cultural preferences.

By centralizing localization assets here, we ensure consistent translations across games, UI components, and platform features.

---

## 🗂️ Directory Structure

```
WackyFlip-Locale/
├── locales/
│   ├── en-US.json        # English (US)
│   ├── vi-VN.json        # Vietnamese
│   ├── es-ES.json        # Spanish (Spain)
│   └── fr-FR.json        # French
├── scripts/
│   ├── extract-keys.js   # Tool to extract translatable strings from source code
│   └── sync-locales.js   # Script to sync new keys across all language files
├── region-config/
│   ├── date-formats.json
│   └── currencies.json
├── i18n-config.js        # Integration setup for WackyFlip-Web and WackyFlip-Mobile
├── CONTRIBUTING.md
├── README.md
└── LICENSE
```

---

## 📋 Features

### ✍️ Translation Files

* JSON-based language packs for UI strings, in-game text, tutorials, and error messages.
* Each locale file follows a consistent key-value structure to ensure compatibility across frontends.

### 🔄 Automation Scripts

* **Key Extractor**: Parses game and platform code to identify new text needing translation.
* **Locale Sync Tool**: Adds missing keys to all locale files with placeholders (`"__TODO__"`).

### 🌏 Regional Configs

* Date/time formats, numeric styles, and currency display settings.
* Enables culturally appropriate formatting per user location.

### ⚙️ Framework Integration

* Works with `i18next`, `react-i18next`, and similar libraries used in WackyFlip-Web and WackyFlip-Mobile.
* Easily extendable to backend APIs for localized responses.

---

## 🧪 Supported Languages

* 🇺🇸 English (Default)
* 🇻🇳 Vietnamese
* 🇪🇸 Spanish
* 🇫🇷 French

> Want to add a new language? See [CONTRIBUTING.md](./CONTRIBUTING.md)

---

## 🚀 Usage in Projects

To use WackyFlip-Locale in a frontend repo:

```js
import i18n from 'i18next';
import en from 'WackyFlip-Locale/locales/en-US.json';
import vi from 'WackyFlip-Locale/locales/vi-VN.json';

i18n.init({
  resources: {
    en: { translation: en },
    vi: { translation: vi },
  },
  lng: 'en',
  fallbackLng: 'en',
});
```

> Full integration examples available in `i18n-config.js`.

---

## 🤝 Contributing Translations

We welcome contributions from the community!

1. Fork the repo
2. Create or update the relevant `.json` file under `locales/`
3. Submit a pull request with the language code in the branch name
4. Optional: Add your name to the translators section

---

## 🧾 License

MIT License © Wacky Flip Studios

---

## 📎 Related Repositories

* [`WackyFlip-Web`](https://github.com/wackyflipgame/WackyFlip-Web) – Uses this repo for multi-language UI
* [`WackyFlip-Mobile`](https://github.com/wackyflipgame/WackyFlip-Mobile) – Localizes UI and game prompts
* [`WackyFlip-Docs`](https://github.com/wackyflipgame/WackyFlip-Docs) – Developer documentation translations (planned)

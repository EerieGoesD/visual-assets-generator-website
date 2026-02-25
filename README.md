Generate all platform visual assets from a single source image — Windows Store, Android, iOS & Chrome Extension.

**[→ Hosted Here]([https://your-username.github.io/visual-assets-generator](https://eeriegoesd.com/visual-assets-generator-website/))**

---

## What it does
Upload one icon image. Select your target platforms. Download a ZIP with every asset pre-sized, named, and organized into folders. Ready to drop into your project.

| Platform | Assets included |
|---|---|
| 🪟 Windows (Microsoft Store) | 43 assets — badge logos, tiles, splash screen, store listing screenshots |
| 🤖 Android (Play Store) | 7 assets — mipmap densities + feature graphic |
| 🍎 iOS (App Store) | 16 assets — iPhone & iPad icon sizes |
| 🌐 Chrome Extension | 7 assets — extension icons + Web Store promo tiles |

The ZIP will contain folders like:

```
visual-assets.zip
├── Assets/                        ← Windows Store visual assets
│   ├── BadgeLogo.png
│   ├── Square150x150Logo.png
│   ├── Wide310x150Logo.png
│   └── ...
├── Screenshots/                   ← Windows Store listing images
│   ├── Poster 9x16.png
│   ├── Box 1x1.png
│   └── ...
├── Android/
│   ├── app-icon-512.png
│   ├── mipmap-hdpi/ic_launcher.png
│   └── ...
├── iOS/
│   ├── AppStore-1024.png
│   ├── iPhone-180.png
│   └── ...
└── Chrome/
    ├── icon-128.png
    ├── small-promo-tile-440x280.png
    └── ...
```

## Windows Store — Badge Logo note

Badge logos must pass [WACK](https://learn.microsoft.com/en-us/windows/uwp/debug-test-perf/windows-app-certification-kit) validation:
- All non-transparent pixels must be **pure white**
- Background must be **transparent**

This tool ports the background-removal algorithm from the companion Windows app, using dominant color detection, Otsu thresholding, and foreground cropping to produce compliant badge logos automatically.

## License

[MIT](LICENSE)

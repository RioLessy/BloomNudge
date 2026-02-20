# BloomNudge Chrome Extension

A Manifest V3 Chrome Extension that detects High-Arousal Negative Affect (HANA) on social media platforms and triggers non-intrusive breathing overlays to promote digital wellbeing.

## Features

- **HANA Detection**: Monitors text and metadata on YouTube, Instagram, TikTok, Facebook, and Twitter/X
- **Non-intrusive Nudges**: Abstract-only breathing animations (pulsing circle or full-screen haze)
- **Home Dashboard**: Local extension page for settings, analysis data, and educational resources
- **UI Customization**: Optional grayscale after N videos, remove engagement elements, blur HANA comments
- **Privacy-first**: All processing is local-only with automatic cleanup
- **Robust Design**: Fallback selectors for site changes, Shadow DOM isolation

## Installation

1. Clone this repository
2. Open Chrome and go to `chrome://extensions/`
3. Enable "Developer mode"
4. Click "Load unpacked" and select this directory

## Development

### Folder Structure
```
├── manifest.json
├── src/
│   ├── content/
│   │   ├── main.js
│   │   ├── domObserver.js
│   │   ├── sentimentEngine.js
│   │   ├── uiNotifier.js
│   │   └── siteAdapters/
│   ├── vendor/
│   ├── background/
│   │   └── serviceWorker.js
│   └── shared/
│       ├── constants.js
│       └── utils.js
├── assets/
└── options/
    ├── dashboard.html
    ├── dashboard.js
    └── dashboard.css
```

### MVP Milestones
- [x] Milestone A: MV3 skeleton loads on target platforms
- [ ] Milestone B: SentimentEngine scoring + threshold triggers
- [ ] Milestone C: UINotifier overlay shows/hides reliably
- [ ] Milestone D: Home dashboard functional and styled
- [ ] Milestone E: Tune weights + add data export/import

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Submit a pull request

## License

MIT License - see LICENSE file for details

## Privacy

All data processing is local-only. No data leaves the device. Automatic cleanup of old data with configurable retention periods.

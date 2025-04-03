# Einsatzlicht – Webbasierte Storytelling-Anwendung

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![CreateJS](https://img.shields.io/badge/CreateJS-1A1F2D?style=for-the-badge)

Eine responsive Web-Anwendung zur Darstellung interaktiver Storys über Einsatzkräfte, basierend auf HTML5 Canvas und CreateJS.

## Technische Merkmale

### Kernkomponenten
- **Scene Manager System**: Dynamisches Szenenhandling mit automatischen/manuellen Übergängen
- **Responsive Design**: Anpassbare Schriftgrößen (vmax-Einheiten) für alle Geräte
- **Barrierefreiheit**: Tastatursteuerung (Pfeiltasten, Leertaste) und Touch-Support
- **Performance**: 60 FPS Animationen via `requestAnimationFrame`

### Technologien
| Bereich          | Technologie               |
|------------------|---------------------------|
| Rendering        | HTML5 Canvas + CreateJS   |
| Animation        | GSAP/TweenJS              |
| Struktur         | Vanilla JavaScript (ES6)  |
| Responsiveness   | CSS Viewport Units (vmax) |

## Installation & Nutzung
1. **Lokale Ausführung**:
   ```bash
   git clone https://github.com/marcdziersan/einsatzlicht.git
   cd einsatzlicht
   python3 -m http.server 8000
   ```
   Öffne `http://localhost:8000` im Browser.

2. **Produktivsetzung**:
   - Einfacher Upload aller Dateien auf einen Webhost
   - Keine Server-Side-Dependencies erforderlich

## Steuerung
| Aktion               | Tastatur     | Touch          |
|----------------------|--------------|----------------|
| Nächste Szene        | →            | Wisch nach links|
| Vorherige Szene      | ←            | Wisch nach rechts|
| Pause/Weiter        | Leertaste    | -              |

## Projektstruktur
```
/einsatzlicht
│── index.html          # Hauptdatei
│── styles.css          # Zentrale Styles
│── script.js           # Scene-Logik
└── assets/             # (Optional) Medien
```

## Customization
### Szenen anpassen
1. Neue Szene erstellen:
   ```html
   <div class="scene" id="sceneX">
     <div class="time">UHRZEIT</div>
     <div class="story">INHALT</div>
   </div>
   ```
2. Szene zur Timeline hinzufügen:
   ```javascript
   const scenes = [
     ...
     { id: "sceneX", duration: 30000 }
   ];
   ```

### Styling
- Farben: Ändere CSS-Variablen in `:root`
- Animationen: Anpassung der `@keyframes` Regeln

## Lizenz
MIT License – Freie Nutzung mit Quellenangabe

---

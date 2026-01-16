## Hi, I'm Gary Coleman

**Senior Software Engineer** — Android/Kotlin, Unity/C#, cross-platform work

I'm looking for my next role after 6+ years at Ergatta building fitness gaming apps. Most of my experience is Android (Kotlin, Jetpack Compose, MVVM), but I've also spent the last 3 years working in Unity/C# and bridging data between the two platforms.

I'm open to Android, Unity, or honestly any language — I enjoy learning new things.

📍 Kingsport, TN (remote preferred)  
📧 gryclmn.work@gmail.com  
🔗 [LinkedIn](https://www.linkedin.com/in/garycoleman/)

---

### Side Project: InvikeyPrototype

I've been building this experimental keyboard for about 2 years. It's my attempt to rethink mobile text input.

---

# InvikeyPrototype

An experimental Android keyboard I've been building with Kotlin and Jetpack Compose. Instead of a traditional key layout, it uses zone-based interaction — the goal is a keyboard that can disappear completely while still giving you precise control.

## Technical Architecture

**Active prototype with 2 years of daily personal use**  
*Live demonstration available upon request*

### Technology Stack
- **Language**: Kotlin
- **UI Framework**: Jetpack Compose (Material Design)
- **Build System**: Gradle with Kotlin DSL
- **Data Persistence**: Protocol Buffers + DataStore

### Key Design Patterns
- **Repository Pattern**: Abstracted data access through KeyboardSettingsRepository
- **State Management**: Flow-based reactive state with StateFlow
- **Composition**: Modular UI components with Jetpack Compose
- **Type Aliases**: Simplified proto references
- **Extension Functions**: Enhanced proto types with convenient utilities

### Key Technical Achievements
- Novel zone-based input system running as performant background service
- Visually transparent UI with full interaction capability
- State machine tracking compound commands across sequential zone traversals
- Validated through 2 years of continuous daily use

---

## What It Does

InvikeyPrototype is an experimental Android input method editor (IME). Traditional mobile keyboards force a trade-off: either take up half your screen or lose functionality. I wanted to see if I could build something different — a keyboard that can become completely invisible while still giving you the precision of a physical keyboard.

### The core ideas:

1. **Invisibility** — Once you learn the input patterns, you don't need the UI anymore. The whole screen stays usable while you type.

2. **Eyes-free typing** — Like touch typing on a physical keyboard, the goal is confident text entry without looking at your device. Muscle memory replaces visual hunting.

3. **Precise editing** — Character-by-character cursor movement, exact text selection, intelligent deletion with easy undo. The kind of control mobile keyboards usually don't give you.

4. **Full keyboard functionality** — Modifier keys, shortcuts, function keys. Still working on some of this, but the goal is everything a physical keyboard can do.

5. **Customization** — Per-keyboard settings for visibility, behavior, and layout. The keyboard adapts to how you use it.

---

## Development Journey

### Novel Technical Challenges

Building a keyboard designed to be invisible presented technical problems I couldn't find addressed in existing Android documentation or tutorials. Standard IME resources focus entirely on how to *show* keyboards — there was no guidance on creating zone-based input that could function while visually transparent.

The solution required adapting existing Android APIs in ways they weren't really designed for: developing a zone-based detection system that tracks state changes across screen regions without traditional visual elements. The challenge was maintaining accurate recognition while running as a background service without killing performance.

### The Zone Configuration Problem

Early implementations used 8 screen zones to maximize input options. Real-world testing revealed a problem: 8 zones were too many to navigate confidently without looking at the device — directly contradicting the eyes-free goal.

Reducing to **4 zones** was painful but necessary. It meant rethinking the entire input model to maintain the same expressive power with fewer zones. The solution came through treating multiple sequential zone traversals as compound state changes, effectively creating complex commands from simple zone movements. This preserved functionality while dramatically improving eyes-free accuracy.

### Validation Through Daily Use

**InvikeyPrototype has been my daily keyboard for 2 years**. Every feature and design decision has been stress-tested through thousands of real messages, emails, and documents.

What works well:
- **Fine-grained controls** — Cursor movement and deletion are precise and intuitive
- **Eyes-free accuracy** — Muscle memory develops quickly; extended typing without looking is genuinely achievable
- **Hard to go back** — After extended use, returning to traditional QWERTY feels limiting

What remains challenging:
- **Feature completeness** — Many envisioned capabilities remain unimplemented due to time constraints
- **Refinement** — Continuous daily use reveals ongoing opportunities for improvement

I work on this when I have time, which isn't as often as I'd like. Family and a full-time job come first. But using it every day means I'm constantly running into what needs work next.

---

## Author

Gary Coleman

---

*Development continues when time allows.*

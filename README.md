# Basic Dice Game — Swift / UIKit

A small **two-dice iOS practice app** built with **Swift, UIKit and Storyboard** in January 2024. Tap the roll button to display two independently randomized dice.

> **Project scope:** A historical learning/demo project, not a published game or production-ready app. It is intended to illustrate UIKit outlets/actions, image assets and basic randomization.

## How it works

- The app starts from [`Main.storyboard`](Dice%20Game/Base.lproj/Main.storyboard), which contains two dice image views and a roll button.
- Tapping **Roll** calls `ViewController.Roll(_:)`.
- Each die independently selects one of the six available faces using `Int.random(in: 0...5)`.
- The corresponding dice images come from the asset catalog (`DiceOne` through `DiceSix`).

The UI does **not** implement a scoring system, turn-taking, multiplayer play or saved roll history. The two images may show the same value.

## Project structure

| File / folder | Purpose |
| --- | --- |
| [`Dice Game/ViewController.swift`](Dice%20Game/ViewController.swift) | Roll button action and random image selection |
| [`Dice Game/Base.lproj/Main.storyboard`](Dice%20Game/Base.lproj/Main.storyboard) | Interface and connections to the controller |
| [`Dice Game/Assets.xcassets`](Dice%20Game/Assets.xcassets) | Dice faces, background, app icons and other UI images |
| [`Dice Game/AppDelegate.swift`](Dice%20Game/AppDelegate.swift) | UIKit app lifecycle |
| [`Dice Game/SceneDelegate.swift`](Dice%20Game/SceneDelegate.swift) | Scene lifecycle |

**Platform settings in the checked-in project:** Swift 5 and **iOS 17.2+**. No CocoaPods or third-party Swift Package is configured.

## Build and run

1. On a Mac with compatible Xcode, clone the repository:
   ```bash
   git clone https://github.com/fatihemres/Basic-Dice-Game-Swift.git
   cd Basic-Dice-Game-Swift
   ```
2. Open [`Dice Game.xcodeproj`](Dice%20Game.xcodeproj).
3. Select the shared **Dice Game** scheme and a compatible iOS simulator.
4. Build/run and use the roll button to change the two dice.

### Cloud build verification

[GitHub Actions](.github/workflows/ios-build.yml) is configured to compile the iOS application for a generic **iOS Simulator on macOS 15 with Xcode 16.4**. A successful run verifies compilation in that environment only; the project currently contains **no XCTest target**, so there is no automated UI/behavior testing or real-device verification. See the workflow's current status before relying on a result.

## Assets and rights

The repository includes dice imagery and the `DiceeLogo` asset. Their third-party origin and permission terms are **not established by the files in this repository**; verify these separately before redistribution or use in a commercial product. Do not assume that bundled learning assets are original or freely reusable.

The current [LICENSE](LICENSE) reserves rights for the owner's original material while preserving third-party rights and previous valid permissions. It does not assign ownership of third-party graphics or tutorial materials to the repository owner.

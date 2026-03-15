# PlantQuest

React Native plant explorer built in TypeScript. Browse newly discovered plants, save favourites, view care requirements, and see what friends are sharing.

[![React Native](https://img.shields.io/badge/React%20Native-0.71-61DAFB?style=flat&logo=react&logoColor=black)](https://reactnative.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=flat&logo=typescript&logoColor=white)](https://typescriptlang.org/)

---

## Screens

**Home** — three sections stacked vertically:
- New Plants carousel with favourite toggle
- Today's Share photo grid
- Added Friends row with overflow count

**Plant Detail** — full plant profile with a banner image and care requirement bars for sunlight, water, temperature, soil, and fertiliser. Each metric shows both a visual fill bar and a precise value (e.g. 15°C, 250ML/day).

## Components worth noting

`RequirementBar` — reusable percentage-fill bar that takes a `0-100` value prop. Used for all 5 care metrics so the display logic stays in one place.

`RequirementDetail` — icon + label + value row, composing each metric entry on the detail screen.

## Stack

React Native 0.71, TypeScript, React Navigation (Stack + 5-tab Bottom Nav), react-native-safe-area-context

## Structure

```
plantquest/
├── src/
│   ├── screens/
│   │   ├── Home.tsx
│   │   └── PlantDetail.tsx
│   ├── navigation/
│   │   └── tabs.tsx
│   └── constants/
│       ├── theme.ts
│       ├── images.ts
│       └── icons.ts
├── App.tsx
└── package.json
```

## Run it

```bash
git clone https://github.com/ifeanyimuogbo/plantquest.git
cd plantquest
npm install

# iOS
npx pod-install && npx react-native run-ios

# Android
npx react-native run-android
```

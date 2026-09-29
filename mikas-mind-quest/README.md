# Mika's Mind Quest

A learning game for Grade 2 (ages 7 to 8). Mika the meerkat guides children through five stops in the Kalahari:

| Stop | Practises | Question types |
|---|---|---|
| Number Burrow | Numbers to 99 | Add, take away, missing number, count in 2s/5s/10s, biggest number, doubles |
| Puzzle Path | Problem solving | Word sums with pictures, equal groups, patterns, odd one out |
| Word Waterhole | Phonics and spelling | Missing letter, pick the right spelling, rhymes |
| Emoji Story Stage | Reading and thinking | Match an emoji story to a sentence, what happens next |
| Solid, Liquid, Gas Lab | Natural science | Sort solids, liquids and gases; melting, freezing and steam |

Every round is 8 questions. Mika says why the answer is right, so a wrong tap teaches instead of punishing. There is no timer and no way to lose. Stars are saved on the device only. The game works offline and sends nothing anywhere.

## Play it now

Open `www/index.html` in any browser. On a Mac:

```bash
cd mikas-mind-quest
npm start          # then open http://localhost:3000 on your Mac or phone (same Wi-Fi)
```

## Build the Android app

Every push to GitHub builds a test APK automatically (see `.github/workflows/android.yml`). Open the run under the repo's **Actions** tab, download `mikas-mind-quest-test-apk`, copy `app-debug.apk` to an Android phone and open it to install. That is enough for family testing.

To build on your Mac instead, install [Android Studio](https://developer.android.com/studio), then:

```bash
npm install
npm run android:add     # once
npm run android:sync    # after every change to www/
npm run android:open    # opens Android Studio; press Run
```

## Build the iPhone app

Needs a Mac with Xcode and an Apple Developer account (US$99 a year):

```bash
npm run ios:add
npm run ios:sync
npm run ios:open
```

## App icon and splash screen

Put a 1024×1024 PNG at `assets/icon.png` and a 2732×2732 PNG at `assets/splash.png`, then run `npm run icons`. Both must be your own artwork (or artwork you have a licence for).

## Before publishing: change the app ID

`capacitor.config.json` has `appId: "za.co.mikasmindquest.app"`. This becomes the app's permanent identity on both stores and can never be changed after the first upload. Set it to a domain you control, reversed (for example `com.yourname.mikasmindquest`), **before** running `cap add` for the first time.

## Launch plan

See [LAUNCH_PLAN.md](LAUNCH_PLAN.md) for the step-by-step path to Google Play and the App Store, the rules for children's apps, and how the game makes money.

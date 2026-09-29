# Launch plan: from prototype to the stores

This is the end-to-end path. Steps marked **(you)** need your accounts or identity; everything else Claude can do with you.

## 1. The name and the rules you asked about

**Names like Paw Patrol, Bluey or Peppa Pig cannot be used.** They are trademarks. Using them in a title, description, icon or screenshot gets the app removed and can lead to a legal claim. This also applies to look-alike characters and to "inspired by" wording. The same goes for emoji from third-party sets and any images pulled from Google.

What works instead: **your own character**. Mika the meerkat is original, South African, and yours to build a brand on. Over time a character you own is worth far more than a borrowed one, because you can add more games, merchandise and a YouTube channel around it.

The game uses the phone's own emoji, which is allowed because they are part of the operating system.

## 2. Costs (once-off unless stated)

| Item | Cost | Notes |
|---|---|---|
| Google Play developer account | US$25 once | Needed to publish on Android |
| Apple Developer Program | US$99 per year | Needed to publish on iPhone/iPad |
| Domain name for the privacy policy page | about R150 per year | The stores need a public web page. A free GitHub Pages site also works |
| Building the app | R0 | Capacitor is free; GitHub Actions builds the Android app for free |
| Artwork | R0 to R1 500 | Draw Mika yourself, or hire an illustrator on Fiverr for the icon and splash screen |

Realistic total to be on Google Play: **under R500**. Adding Apple: about R1 900 per year.

## 3. Rules for children's apps (this game is built to pass them)

Both stores treat an app for under-13s as a children's app and check it harder. The rules that matter:

- **No data collection.** The game collects nothing and works offline. Keep it that way. If you ever add analytics, use a kids-certified provider only.
- **No ads, or only kids-certified ads.** For a game earning a small amount, ads are not worth the risk and the review hassle. Sell the full version instead (see section 5).
- **Parental gate.** Anything that leads out of the game or to a purchase must sit behind a gate a child cannot pass. The game has a "Grown-ups" multiplication gate already; the buy button goes behind the same gate.
- **Privacy policy on a public web page.** `PRIVACY.md` is written; it needs to be put on a web page and the link entered in both store consoles.
- **Google Play "Designed for Families" and "Teacher Approved".** Opt in when you fill in the store listing; "Teacher Approved" is a badge Google awards after review and it helps a lot with downloads.
- **Apple "Kids Category".** Pick the 6–8 age band. Apple checks that no links or purchases are reachable without the gate.
- **Content rating questionnaire.** Answer truthfully; with no violence, no chat and no ads it rates "Everyone" / "4+".

## 4. Testing before launch

1. **Family test, this week.** Push to GitHub, download the APK from the Actions tab, install it on your phones. Watch your Grade 2 play without helping. Write down every place they got stuck or bored. That list drives the next version.
2. **Google Play closed test (you).** New personal developer accounts must run a closed test with at least 12 testers for 14 days before they may publish publicly. Google changes this rule from time to time; the Play Console shows the current requirement. Use parents from the class WhatsApp group, family and colleagues. Claude can write the invitation message.
3. **Apple TestFlight (you).** Up to 10 000 testers, no waiting period, but each build is reviewed lightly first.

## 5. How it makes money

Keep it simple and honest for parents. The model that works for small educational apps:

**Free with a once-off unlock.**
- Free: Number Burrow and Puzzle Path, 8 questions each.
- Paid unlock, R49.99 to R79.99 once-off (US$2.99 to US$4.99): all five stops, more question types, extra difficulty, and every future stop added.
- No subscription, no ads. Parents in South Africa distrust both, and a once-off price is what teachers recommend to each other.

What R50 looks like in practice: at R59.99 the stores keep 15% (both have small-developer programmes), so about R51 per sale reaches you. Ten sales a month is R500. Fifty schools' worth of parents buying is a real side income. The path to those numbers is section 6, not luck.

Later, once there is an audience: a "Grade 1" and a "Grade 3" version, an Afrikaans version, and a school licence sold directly to schools (outside the stores, so no 15% cut).

## 6. Getting downloads (the market side)

Kids' apps are crowded. What actually moves the needle for a small app:

1. **Curriculum alignment in the listing.** Say "Grade 2 CAPS" in the title or description. Parents search for the curriculum name; almost no app targets South African terms, so you can rank for them cheaply.
2. **Teacher Approved badge on Google Play.** Apply for it. It is the single biggest free boost for kids' apps.
3. **Teachers first, then parents.** One Grade 2 teacher recommending the app in a class group reaches 30 families at once. Give teachers the full version free.
4. **Screenshots that show the learning.** Five phone screenshots with one line of text each: "Adds and subtracts to 99", "Sorts solids, liquids and gases", and so on. Parents decide from screenshots, not the description.
5. **Reviews from the closed testers.** Ask every tester family to leave a review on launch day. Ten five-star reviews in week one matters more than anything else you can do.
6. **A tiny website** (one page, GitHub Pages, free) with the privacy policy, the store links and a short video of a child playing.

## 7. Order of work

- [x] Prototype with all five stops (this commit)
- [ ] Push to GitHub and download the first APK **(you: fix GitHub access)**
- [ ] Family test; collect feedback
- [ ] Round 2: fix what testers found, add difficulty levels, add sound effects and recorded voice
- [ ] Original icon and splash artwork
- [ ] Set the final app ID, build signed release
- [ ] Privacy policy page online
- [ ] Google Play account **(you)**, store listing, closed test
- [ ] Add the paid unlock (Capacitor in-app purchase plugin) behind the parental gate
- [ ] Public launch on Google Play
- [ ] Apple Developer account **(you)**, TestFlight, App Store launch

# Primal Dash: Dino Run - project status

Last updated: 2026-11-06.

This is a public summary, so AI assistants and helpers can follow the project. The game's source code is private and is **not** in this repository. This repository holds only the store website and the privacy policy.

## The game
A colorful, offline, kid-friendly (ages 6+) prehistoric runner for Android and iOS.
- **Adventure mode:** 5 worlds, 25 levels and 5 friendly bosses.
- **Creatures:** 8 playable prehistoric creatures, with power moves and a triple jump.
- **Extras:** a Creature Book with fossils, a Practice mode and the classic Endless Run.
- **Talking dinosaur:** it says short English phrases.
- **Music:** original background music that can be switched off.
- **Dino Friends** (new, in testing): a mini-game of short interactive stories with a baby dinosaur. Children can say the words out loud, tap them, or just watch. **There is no microphone** and the game never claims to hear the child.
- **Privacy:** no ads, no accounts, no data collection, and it works completely offline.

## Release status
| | |
|---|---|
| On Google Play | **1.0.1** (build 2), live for **internal testing** and **closed testing** |
| Next update | **1.2.0**: no startup flicker confirmed on the owner's Huawei. New, more natural narrator voice made; **rollout on hold** until the owner approves it on the phone |
| Public release | Not yet. Google requires 12+ closed testers for 14 days first |
| Store listing | Done: description, graphics, content rating, audience 6+ |
| Privacy policy | https://adnanmn5.github.io/primaldash/privacy.html |
| iOS (App Store) | Project prepared; not built yet (needs a Mac) |

### History of the next update
- **1.1.0** (test build only, never uploaded): a first version of Dino Friends (3 short scenes) and a startup fix. On the owner's Huawei phone the start still flickered three times, and Dino Friends looked too plain: small characters, no banner, little to do besides word buttons.
- **1.2.0** (current test build) reworks both:
  - **Startup flicker, root cause** (confirmed fixed on the owner's Huawei Mate 20 X): on slower phones the game automatically lowers its drawing resolution in the first seconds, and each change briefly showed an empty frame (twice), plus the launch screen fade: the three flickers. The game now redraws immediately when this happens, and on Android 11 and older the launch screen is a plain, steady background with no jumping icon.
  - **Dino Friends, rebuilt as a mini-game:**
    - A welcome screen with a big animated banner, a friendship meter (New / Good / Best / Super friends) and five illustrated story tiles. Finished stories get a gold star.
    - A close-up camera, so the dinosaurs are about twice as big.
    - Five stories, played by tapping the scene itself:
      1. **Hello, little buddy!** Tap the bush to find a shy baby, then tickle it.
      2. **Picnic time!** Choose a food and feed the baby.
      3. **Peekaboo!** Find the baby hiding behind one of three bushes.
      4. **Help! The egg is stuck.** Push the rock away, then tap the egg to hatch a tiny baby.
      5. **Stuck in the mud!** Pull the baby out, then pop bubbles to wash it clean.
    - Lots of feedback: confetti, sparkles, hearts, bubbles, butterflies and a dancing celebration at the end.
    - Every story also finishes on its own if the child just watches, and a bouncing arrow shows where to tap.
  - **"Screen stays on"** (new setting): the phone no longer dims or locks while a child watches a story. After 10 minutes without a touch it sleeps normally.
  - **Narrator:** a friendly male narrator voice guides the stories. The first version sounded robotic, so all 50 lines were remade with a newer open-source AI voice model (Chatterbox, MIT licence), run on the developer's own computer. The owner chose the voice from six candidates. No real person's voice was copied, and the app still has no speech engine or internet access: it only plays the bundled clips.
  - **Dino voice:** the talking dinosaur also sounded robotic, so all 140 of its phrases were remade with the same tool in a new "jolly, big dino" voice the owner chose. Every clip was checked with speech recognition, so the words come out clearly. This voice is used everywhere the dino talks.
  - **Dialogue timing:** a line never starts while another is still playing. The dino now waits about 0.8 seconds before answering the narrator (it used to reply too quickly), and the narrator about 0.6 seconds after the dino. The music dips under every voice.
  - **Credits & licences:** a new screen in Settings and a new page, https://adnanmn5.github.io/primaldash/credits.html, list who made what and under which licence (original game, music, AI voices, software).

## Open items
1. **After the new voice, testers check 1.2.0 on other phones:** startup (no flicker, both fresh start and returning to the app), all five stories with sound, and the screen staying on. The flicker fix is already confirmed on the Mate 20 X.
2. **Voices (block the rollout):** the new narrator and dino voices are made and built in; the owner liked them on the web version and will check them on the phone. A real recorded narrator can still replace it later under the same file names.
3. **Map report:** a tester reported that, after level 2-1, tapping level 1 on the map doesn't start it. We can't reproduce it yet and are waiting for a screen recording.
4. **Closed test:** keep 12+ testers in the closed test for 14 days, then apply for the public release.
5. **Dino Friends, later:** the baby dinosaur as a companion in Adventure mode, a sound "echo" playground and short play-together tips for parents.
6. **iOS:** build and test the iOS version on a Mac.

## How the project is maintained
- **Code:** it's kept privately, on the developer's computer only.
- **Updates:** they're built and tested there, then uploaded to Google Play.
- **This file:** it's updated at each milestone.

# Hero's Codex - Public

A fantasy RPG habit tracker for your phone. Check off daily quests, level up skills and abilities, earn medals and achievements, and collect pixel-art companions.

**Open the app:** https://davisdwm.github.io/Heros-Codex-Public/

## Put it on your iPhone

1. Open the link above in **Safari**.
2. Tap **Share**, then **Add to Home Screen**, then **Add**.
3. Open it from the new icon. It runs full-screen and works offline.

Android: open the link in Chrome and choose **Add to Home screen** from the menu.

Your progress is saved on your own phone. Nobody else can see it, including whoever shared this link. Use **Hero tab → Save backup** now and then. Removing the app from your home screen deletes its data.

## How it works

- **Quests** come in four kinds: **daily** (count toward your day's medal), **weekly** (aim for a few times a week; XP only), **side quests** (one-time; XP only), and **bubble quests** that log an amount, like 15 / 30 / 50 pages.
- **Exercise group:** quests marked "counts as exercise" share one slot toward the day's medal. Do one; extras still earn XP.
- **Medals:** a day is Bronze at 50%, Silver at 75% and Gold at 90% of that day's daily-quest XP, before streak bonuses. The total scales with whatever daily quests you set up.
- **Streaks:** +10% XP from day 2 of a streak, +20% from day 7.
- **Skills** each belong to one of six **abilities** (Strength, Dexterity, Constitution, Intelligence, Wisdom, Charisma). Quest XP goes to the skill, its ability and your character level. Levels need 1.5x more XP each time (1.2x from level 10 on), rounded up to the nearest 50.
- **Weekly and side quests** are grouped by ability in collapsible lists, so long lists stay tidy.
- **Friends:** create a friend card in the Friends tab and share your code. Friends see your name, title, level, companion, ability levels and up to three achievement badges you choose in the Hero tab. Nothing else is shared.
- **Conditions** (Poisoned, Exhausted, Happy, or your own) are logged per day.

## Starting skills

| Skill | Ability |
|---|---|
| Exercise | Strength |
| Pliability | Dexterity |
| Hygiene, Health | Constitution |
| Intellectualism | Intelligence |
| Self-Concept, Culture | Wisdom |
| Creativity, Connection | Charisma |

The app starts with no quests. Use the **Add a new daily / weekly / side quest** buttons on the Quests tab (or the Hero tab) to add your own and attach each one to a skill. You can also rename skills, change their ability, add new skills, and delete skills you don't use.

## Companions

When you first open the app you choose a starter companion: **Cat**, **Dog** or **Parrot**. Then:

- **Each skill** has companions at levels 5, 10 and 15 (a golden legend), plus a **shiny** version of the level 5 companion. Each quest you complete has a 1 in (1,000 × that skill's daily quests) chance, so adding more quests never improves the odds.
- **Each ability** has its own companions at levels 5, 10 and 15. Once you find one, its shiny version can appear (1 in 1,000 per quest for that ability); until then it stays hidden.
- **Skills you create yourself get their own companions automatically.** If the skill's name suggests a theme (cooking, piano, gardening, swimming, coding and many more) you get a matching set; otherwise the app picks creatures you aren't already using. Creatures that appear elsewhere get a new color, and every companion is named after your skill (for example *Cooking Mimic*, *Grand Cooking Turtle*, *Legendary Cooking Hermit Crab*). Renaming the skill renames its companions.

Choose a companion to travel with you from the Hero tab. It appears on your character card.

## Make your own version

This is a single web page with no server and no accounts.

- `src/app.html` is the whole app: styles, logic and sprites.
- `src/sw.js` is the offline helper.
- `./build.sh` builds `index.html`, `preview.html` (with sample data), `sw.js` and `version.json`, stamping a new version number each time.
- Rules such as XP curve, streak bonuses, medal thresholds and shiny odds are in `RULES` near the top of the script.
- Companion sprites are 32x32 text grids in `SPR`. `tools/sheet3.html` previews them all.

To host your own copy: fork this repository, run `./build.sh`, commit, then turn on **Settings → Pages → Deploy from a branch → main / root**.

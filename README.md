[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)


# Un-Limited Reborn (RimWorld 1.5 - 1.6)

Un-Limited Reborn removes RimWorld’s built-in caps on various **pawn capacities** and **stats**, letting bionics and other enhancements scale beyond vanilla limits. It also includes optional “advanced” settings to push post-process curves and skill-based stat scaling even further.

---

## Features

- **Remove stat & capacity caps**
  - Lifts the “limit” on pawn capacities (Manipulation, Sight, etc.)
  - Removes `maxValue` constraints on stats so values can exceed vanilla maximums
- **Optional: Unlimited PostProcessCurves**
  - Lets you exceed vanilla curve endpoints for things like **Melee Hit Chance**, **Melee Dodge Chance**, and **Shooting Accuracy**
- **Optional: Linear skill scaling (Skill Need Factors)**
  - Switches certain skill-driven stats to a linear “base + bonus per level” model so they can scale past level 20
  - Some values can be tweaked **mid-game** (real-time) when enabled
- **In-game mod settings menu**
  - Tune how “unlimited” you want things to be without editing XML

For detailed per-stat coverage and explanations, see the **Wiki**.

---

## Requirements

- **XML Extensions** (dependency)

> XML Extensions typically expects **Harmony** as well.

---

## Installation

### Steam Workshop
1. Subscribe to **Un-Limited Reborn**
2. Subscribe to **XML Extensions**
3. Launch RimWorld and enable the mods.

### Manual / GitHub
1. Download the repo as a ZIP (or clone it).
2. Extract into your RimWorld `Mods/` folder so you end up with something like:
   - `RimWorld/Mods/Unlimited-Reborn/...`
3. Launch RimWorld and enable:
   - Harmony (if needed)
   - XML Extensions
   - Un-Limited Reborn

---

## Load Order

Recommended order:

1. Core + DLCs  
2. Harmony (if needed)  
3. **XML Extensions**  
4. **Un-Limited Reborn**  
5. Everything else

---

## Compatibility

| Compatible | Incompatible |
|---|---|
| Combat Extended<br>EndlessGrowth<br>SYR Harvest Yield | Un-Limited / Un-Limited (Unofficial) / Un-Un-Limited<br>UnLimitedArmor<br>Impactful Skills Mod Support<br>Better Talking and Hearing Matters |

**Notes**
- If you’re using multiple stat/curve mods, you may need to adjust **load order**. When in doubt, try placing Un-Limited Reborn **after** other mods that touch the same stats.
- If you hit odd behavior, disable advanced options first (Unlimited PostProcessCurve / Skill Need Factors) and re-test.

---

## Advanced Settings (Read This First)

These options can produce **extreme** results and can break balance (or lead to weird curve behavior) with very high values.

- If something goes wrong:
  1. disable the option that caused it,
  2. restart RimWorld,
  3. re-test with smaller values.

### Unlimited PostProcessCurve
Vanilla “soft caps” you generally need to exceed to feel the effect (examples):

| Stat | Vanilla limit reference | What happens in vanilla |
|---|---:|---|
| Melee Hit Chance | ~60 | approaches high hit chance |
| Melee Dodge Chance | ~60 | approaches dodge cap behavior |
| Shooting Accuracy | ~60 | approaches ~99.9% accuracy behavior |

(See the Wiki for more explanation and practical guidance.)

### Change Skill Need Factors (Linear skill scaling)
This replaces per-level lists (0–20) with:
- **Base value**
- **Bonus per skill level**

This can slightly reduce early skill power while enabling scaling past level 20.

---

## FAQ

### “Can this mod uncap the Gear UI ‘overall armor’ display?”
Not fully. UI/logic caps like that generally require C# changes to RimWorld internals; this mod focuses on XML/stat definitions and patching.

### “Is this safe to add/remove mid-save?”
Usually yes for XML-driven changes, but if you’re using extreme advanced settings, test carefully and keep backups.

---

## Troubleshooting

- Make sure **XML Extensions** is loaded and above this mod.
- Check the RimWorld log for XML patch errors.
- If using Combat Extended or other big combat overhauls, test with Un-Limited Reborn toggled off to confirm overlap.

If you can reproduce an issue, include:
- your mod list (in order),
- your RimWorld version,
- your Player.log / output log.

---

## Links

- Steam Workshop: https://steamcommunity.com/sharedfiles/filedetails/?id=3295368629
- GitHub Repo: https://github.com/NuanKi/Unlimited-Reborn
- Wiki: https://github.com/NuanKi/Unlimited-Reborn/wiki

---

## Credits

- Original inspiration: “Un-Limited”
- Translations: Chinese by Day29 (see Workshop/Wiki for details)

---

## License

Licensed under **CC BY-NC-SA 4.0** (Attribution–NonCommercial–ShareAlike 4.0 International).

- You may share and adapt this mod for **non-commercial** purposes only.
- **Attribution is required** — credit must be given to **NuanKi** (format is up to you).
- **Derivatives must use the same license** (CC BY-NC-SA 4.0).

See [`LICENSE`](LICENSE) or https://creativecommons.org/licenses/by-nc-sa/4.0/

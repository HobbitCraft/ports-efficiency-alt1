# Ports Efficiency for Alt1

An Alt1 app for finding an efficient ship setup for Player-owned Ports voyages in RuneScape 3.

Scan your crew, enter your captain totals and unlocked ship parts, then scan a selected voyage. The app immediately checks the available captain, crew, and ship-upgrade combinations and shows the best complete setup.

## Requirements

- [Alt1 Toolkit](https://runeapps.org/alt1)
- Alt1's **Screen pixels** and **Overlay** permissions enabled for the app
- The Player-owned Ports Crew Roster visible when scanning crew
- The complete Voyage List visible at 100% interface scale when scanning a voyage

## Install

Open this appconfig URL in Alt1:

`alt1://addapp/https://hobbitcraft.github.io/ports-efficiency-alt1/appconfig.json`

## Set up the roster

1. Open the Player-owned Ports **Crew Roster**.
2. Keep the complete Crew Roster interface visible, then use step 1 on the **Optimise** tab or open **Scan crew** directly.
3. Select the matching RuneScape interface scale and click **Scan screen**.
4. The app searches the full RuneScape capture for the roster, then matches known portraits, reads the bottom-right crew levels, and records top-left ship assignments. The compact review grid shows every icon, level, and calculated M/C/S total together; check highlighted matches before saving.
5. If automatic location fails, use **Fallback: calibrate with Alt+1**, hover the centre of the first captain icon, and press Alt+1.
6. In **Roster**, enter the current Morale, Combat, Seafaring, and Speed totals for each of your four captains.

Crew stats use the base value plus exactly 10% of that base for each level; boosts do not compound. For example, a Smuggler has 70 base Seafaring, gains 7 per level, and has 140 at level 10. Captains are kept separate because their displayed totals include their generated stats, level, traits, and personal bonuses.

## Optimise a voyage

1. Follow the four steps on the **Optimise** tab: scan crew, enter captain totals, and fill out Ship unlocks.
2. In **Ship unlocks**, select the Fort Forinthy Command Centre tier and current shipwright, then mark every ram/figurehead, deck item/rigging, hull, and rudder you own.
3. Open the Voyage List and select any voyage so its Adversity panel is visible.
4. Click **Scan voyage**. The app reads Morale, Combat, and Seafaring and immediately calculates the recommended setup. Alt+1 performs the same scan-and-optimise action.
5. Leave the resources/trade-goods checkbox enabled for reward voyages; those setups always include an available merchant.

The app maximises the lowest required stat percentage across crew and every non-dominated unlocked ship setup. It includes the two deck hotspots, shipwright total-stat multipliers, Solidarity, Command Centre reductions, and mandatory merchants on marked reward voyages. Once capped success is tied, it favours the setup strongest in the voyage's required stats so a specialist captain is not displaced by an unrelated captain. Recommended ship parts are always displayed with the crew setup.

Roster and unlock data stay in Alt1 browser storage. Open the gear icon and use **Export JSON** before clearing that storage or changing the app host.

The app does not click RuneScape, assign crew, or send voyages.

## Sources

- [RuneScape Wiki — Captains and crew](https://runescape.wiki/w/Player-owned_port/Captains_and_crew)
- [RuneScape Wiki — Player-owned port strategies](https://runescape.wiki/w/Player-owned_port/Strategies)
- [RuneScape Wiki — Optimal set-up calculator](https://runescape.wiki/w/Module:Player-owned_ports_voyage_calculator)
- [Kags' Player Owned Ports Encyclopedia V7](https://runescape.wiki/w/User:Kags)
- [Jasper72 — Player Owned Ports as Easy as Possible](https://www.youtube.com/watch?v=2QliZmT1T0I)
- [ChevalricRS — The Ultimate Player Owned Ports Guide](https://www.youtube.com/watch?v=3OU62tJaTkg)

The Crew Roster screenshot was used as a development reference and is not included in this repository.

## Files

- `appconfig.json` - Alt1 app manifest
- `index.html` - app page
- `app.bundle.js` - compiled application and Alt1 scanner
- `style.css` - interface styles
- `assets/` - app icon
- `THIRD_PARTY_NOTICES.md` - attribution and dependency notices

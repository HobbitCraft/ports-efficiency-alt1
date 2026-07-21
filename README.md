# Ports Efficiency for Alt1

An Alt1 app for finding an efficient ship setup for Player-owned Ports voyages in RuneScape 3.

Scan a supported selected voyage or enter its adversity, record the ship parts you own, then press Alt+1 or **Optimise**. The app checks your available captain, crew, and ship-upgrade combinations and shows the best complete setup.

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
2. Keep the complete Crew Roster interface visible, then open **Scan crew** and select the matching RuneScape interface scale.
3. Click **Scan screen**.
4. The app searches the full RuneScape capture for the roster, then matches known portraits, reads the bottom-right crew levels, and records top-left ship assignments. The compact review grid shows every icon, level, and calculated M/C/S total together; check highlighted matches before saving.
5. If automatic location fails, use **Fallback: calibrate with Alt+1**, hover the centre of the first captain icon, and press Alt+1.
6. In **Roster**, enter the current Morale, Combat, Seafaring, and Speed totals for each of your four captains.
7. Mark unavailable crew or enter optional exact-stat overrides for visible bonuses and traits.

Crew stats use the base value plus exactly 10% of that base for each level; boosts do not compound. For example, a Smuggler has 70 base Seafaring, gains 7 per level, and has 140 at level 10. Captains are kept separate because their displayed totals include their generated stats, level, traits, and personal bonuses.

## Optimise a voyage

1. Open the Voyage List and select one of the five captured voyage layouts: **Siege Mentality**, **For the Good of All**, **Troubled Waters**, **The Whale Whisperer**, or **A Joint Acquisition**.
2. Click **Scan voyage** to fill its Morale, Combat, and Seafaring adversity. Other voyages can still be entered manually.
3. In **Ship unlocks**, mark every ram/figurehead, deck item/rigging, hull, and rudder you own, then select the shipwright currently built in your port.
4. Select the Command Centre tier. Leave the resources/trade-goods checkbox enabled for reward voyages; those setups always include an available merchant.
5. Press Alt+1 or click **Optimise**. Alt+1 also tries to scan a visible supported voyage before calculating.

The app maximises the lowest required stat percentage across crew and every non-dominated unlocked ship setup. It includes the two deck hotspots, shipwright total-stat multipliers, Solidarity, Command Centre reductions, mandatory merchants on marked reward voyages, and optional lower-level crew training. Once capped success is tied, it favours the setup strongest in the voyage's required stats so a specialist captain is not displaced by an unrelated captain.

Roster data and preferences stay in Alt1 browser storage. Use **Settings → Export JSON** before clearing that storage or changing the app host.

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

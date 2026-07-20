# Ports Efficiency for Alt1

An Alt1 app for finding an efficient ship setup for Player-owned Ports voyages in RuneScape 3.

Enter the selected voyage's adversity and current ship stats, then press Alt+1 or **Optimise**. The app checks the available captain and crew combinations saved in your roster and shows the best result.

## Requirements

- [Alt1 Toolkit](https://runeapps.org/alt1)
- Alt1's **Screen pixels** and **Overlay** permissions enabled for the app
- The Player-owned Ports Crew Roster visible when scanning crew

## Install

Open this appconfig URL in Alt1:

`alt1://addapp/https://hobbitcraft.github.io/ports-efficiency-alt1/appconfig.json`

## Set up the roster

1. Open the Player-owned Ports **Crew Roster**.
2. Open **Scan crew** and select the matching RuneScape interface scale.
3. Click **Scan screen**.
4. If the grid is not aligned, click **Arm Alt+1 calibration**, hover the centre of the first captain icon, and press Alt+1.
5. Check the captured portraits, identities, and levels before saving them.
6. Use **Roster** to mark unavailable crew or enter exact stats that include visible bonuses and traits.

Reviewed crew portraits are remembered for later scans. Ports uses a generic captain portrait, so captain tier and speciality must always be selected manually.

## Optimise a voyage

1. Enter the voyage's Morale, Combat, and Seafaring adversity.
2. Enter the ship contribution from fitted parts and port buildings, excluding captain and crew.
3. Select the Command Centre tier and whether the voyage gives resources or trade goods.
4. Press Alt+1 or click **Optimise**.

The app maximises the lowest required stat percentage. Solidarity, Command Centre reductions, merchant tie-breaking, and optional lower-level crew training are included.

Roster data and preferences stay in Alt1 browser storage. Use **Settings → Export JSON** before clearing that storage or changing the app host.

The app does not click RuneScape, assign crew, or send voyages.

## Sources

- [RuneScape Wiki — Captains and crew](https://runescape.wiki/w/Player-owned_port/Captains_and_crew)
- [RuneScape Wiki — Player-owned port strategies](https://runescape.wiki/w/Player-owned_port/Strategies)
- [RuneScape Wiki — Optimal set-up calculator](https://runescape.wiki/w/Module:Player-owned_ports_voyage_calculator)
- [Kags' Player Owned Ports Encyclopedia V7](https://runescape.wiki/w/User:Kags)

The Crew Roster screenshot was used as a development reference and is not included in this repository.

## Files

- `appconfig.json` - Alt1 app manifest
- `index.html` - app page
- `app.bundle.js` - compiled application and Alt1 scanner
- `style.css` - interface styles
- `assets/` - app icon
- `THIRD_PARTY_NOTICES.md` - attribution and dependency notices

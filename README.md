# Pokémon Type Calculator

A single-file, zero-dependency web app that helps you plan a Pokémon route. Select the elemental types found in an area and instantly see which attacking types hit hardest and which defensive types keep you safest.

## Features

- **Multi-select type picker** — toggle any combination of the 18 Pokémon types present in a route/area.
- **Best attackers** — ranks types that land a super-effective (2x) hit against the most selected types, flagging any that would be immune (0x) against part of the selection.
- **Best defenders** — ranks types that resist (0.5x) or nullify (0x) the area's types, prioritizing zero weaknesses.
- **Threats to avoid** — highlights types that would take super-effective (2x) damage from the area, so you know what *not* to bring.
- Dark-themed, responsive UI with official type colors, built with plain HTML/CSS/JS — no build step, no frameworks, no external dependencies.

## Usage

Open [index.html](index.html) directly in any modern browser (double-click the file, or serve it with any static file server). Click the type chips to toggle the elements present in the location; the results update automatically. Use **Limpar Seleção** to clear the selection.

## How it works

The app embeds a type effectiveness chart (attacker → defender multipliers) covering all 18 types. For each selected combination it computes, per candidate type:

- **Offense score**: how many of the selected types it hits for 2x damage.
- **Defense score**: how many of the selected types it resists/nullifies vs. how many hit it for 2x.

Results are sorted and rendered live with no page reloads or network requests.

## Tech stack

- Vanilla HTML, CSS and JavaScript (ES6+)
- No build tools, package manager, or external libraries required

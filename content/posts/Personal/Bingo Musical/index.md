---
title: "Bingo Musical"
date: 2026-08-26
description: Musical Bingo Creator
theme: Toha
menu:
  sidebar:
    name: Bingo Musical
    identifier: bingo_musical
    parent: personal
    weight: 400
draft: false
tags: ["TypeScript", "React", "Vite"]
---

## The project

[Bingo Musical](https://miquelt9.github.io/bingo-musical/) is a desktop-first static app for creating, editing, printing, and hosting interactive Musical Bingo games. It is built with Vite, React, TypeScript, Tailwind CSS, [@miquelt9/pc-ui](https://github.com/miquelt9/pc-ui), jsPDF, the YouTube IFrame API, and Deezer preview metadata. The app is hosted on GitHub Pages, with no backend required for local play and no Google account required.

A deck can be built by searching a song or artist (catalog autocomplete from iTunes, then Deezer or MusicBrainz), by pasting a YouTube video or playlist URL, or by pasting an `Artist - Title` list. Decks are either YouTube or Deezer. Deezer tracks use the catalog’s short preview, normally 30 seconds, and do not need a Deezer login. Cards print on a grid from 3×3 to 6×6, and the same cards can be downloaded as a vector PDF. The host calls the next song from a non-repeating shuffle and can open an audience display. Decks stay in the browser and can be exported or imported as JSON, shared with a short link, or edited together through a separate collaboration link.

The repository is [bingo-musical](https://github.com/miquelt9/bingo-musical) (`Crea el teu bingo musical`), released under the MIT License. A fresh visit to the live site opens the built-in Deezer deck, All-Time Pop & Rock Classics.

{{< line_break >}}

#### [Open the live site ](https://miquelt9.github.io/bingo-musical/)

#### [Project's code on Github <i class="fab fa-github"></i> ](https://github.com/miquelt9/bingo-musical)

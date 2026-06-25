# MIDI & Clone Hero .chart Master Utility

A lightweight, zero-dependency (server-side) web application designed to help rhythmic game charters bridge the gap between raw MIDI files and playable `.chart` files. 

This tool runs entirely in your browser, meaning there are no file upload limits, no server delays, and your data remains entirely local.

click here to use ---------> https://n3rdy13.github.io/Mid2drumcharts/

## 🚀 Features

### 1. Clone Hero `.chart` Converter
* **Smart Pitch Mapping:** Automatically analyzes your selected MIDI track and identifies all active pitches. 
* **General MIDI Detection:** Attempts to identify the instrument based on standard GM drum maps, giving you a head start on charting.
* **In-Browser Auditioning:** Not sure what MIDI Note 46 is? Click the play button to hear a synthesized preview of the pitch before you map it.
* **Custom Timeline Offsets:** Easily add default lead-in silence (padding) or dynamically override the first note start time to perfectly sync your chart with the audio track.
* **Multi-Instrument Support:** Built-in preset mappings for both Pro Drums (Kick, Snare, Toms, Cymbals) and standard Guitar/Bass lanes (Green, Red, Yellow, Blue, Orange, Forced/Tap flags).

### 2. MIDI Track Exporter (Isolate & Save)
* **Track Filtering:** View all embedded tracks within a dense MIDI file alongside their total note counts and assigned instruments.
* **Clean Exports:** Select only the tracks you want to keep (e.g., isolating just the snare and kick drums) and instantly export a clean, filtered `.mid` file while preserving the original tempo and time signature headers.

## 🛠️ How to Use

### Installation
There is no build step required. Simply download or clone this repository and open the `index.html` file in any modern web browser.

### Workflow: Creating a .chart
1. **Upload:** Drag and drop your `.mid` or `.midi` file into the upload zone.
2. **Select Track & Mode:** Choose the specific MIDI track you want to convert and select your target instrument (e.g., Expert Drums).
3. **Adjust Timing (Optional):** Add lead-in silence or define the exact second the first note should hit.
4. **Map Pitches:** Go through the detected MIDI notes. Use the dropdowns to assign them to their corresponding Clone Hero lanes. Use the play icon to audition the pitch if you are unsure what drum/note it represents.
5. **Generate:** Click "Generate & Download .chart" to instantly save your converted file.

### Workflow: Exporting MIDI
1. Switch to the **MIDI Track Exporter** tab.
2. Upload your source MIDI file.
3. Uncheck any tracks you want to strip from the file.
4. Click **Export Selection to .mid File** to download the new, isolated MIDI file.

## 💻 Tech Stack

* **HTML5 / Vanilla JavaScript:** Core logic and DOM manipulation.
* **[Tailwind CSS](https://tailwindcss.com/):** Sourced via CDN for modern, responsive UI styling and dark mode.
* **[@tonejs/midi](https://github.com/Tonejs/Midi):** Sourced via unpkg for fast, robust parsing and binary compilation of MIDI files.
* **Web Audio API:** Used for the localized pitch-auditioning synthesizer.

## 📜 License

Distributed under the MIT License. Feel free to fork, modify, and use this utility for all your charting needs.

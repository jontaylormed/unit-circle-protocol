# The Unit Circle Protocol

Students explore the unit circle, radians and special right triangles, then practice exact trig values, in six short missions.

**Live site:** <https://jontaylormed.github.io/unit-circle-protocol/>

**Source:** <https://github.com/jontaylormed/unit-circle-protocol>

**Site created by Claude and Jon Taylor.**

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

---

## What it does

| Mission | What the student does |
|---|---|
| Unit Circle Explorer | Drags a point around the circle and reads its angle, radians, coordinates, sine, cosine, tangent and signs |
| Radian Visualizer | Grows an arc and sees how many radii fit along it, with degrees alongside |
| Triangle Morphing | Slides between angles to see the 30-60-90 and 45-45-90 side ratios and trig values |
| Trig Whack-a-Mole | Taps the right exact value before it disappears, in degrees and then radians |
| Trig Navigation | Finds how far a ship travels north, south, east or west, using sine and cosine on a drawn triangle |
| Trig Practice | Types exact values, and new sets of angles unlock as they go |

A progress report lists which missions are done and what is still to try. It can be printed.

## Who it's for

Geometry through precalculus, usually grades 9–12.

Common Core State Standards for Mathematics:

| Standard | What it asks |
|---|---|
| HSG.SRT.C.6 | Understand that side ratios in right triangles are properties of the angles, leading to the trig ratios |
| HSG.SRT.C.8 | Use trig ratios and the Pythagorean Theorem to solve right triangles in applied problems |
| HSF.TF.A.1 | Understand radian measure as the arc length on the unit circle |
| HSF.TF.A.2 | Explain how the unit circle extends the trig functions to all real numbers |
| HSF.TF.A.3 (+) | Use special triangles to find sine, cosine and tangent of π/3, π/4 and π/6 |

## How it teaches

- **See it first.** The three explorers draw the circle, the arc and the triangles. They come first in the mission list, and the report points to any that haven't been visited.
- **Structure before numbers.** Triangle Morphing shows that the side ratios belong to the angle, so the exact values have a reason. Navigation labels the known leg as an expression, such as "2 cos 30°," before the student finds the other one.
- **No one feels remedial.** A name is optional. The report lists what a student did, with no grades, percentages or judging lines. The game missions still keep a running score.
- **Check every claim.** Every equivalent exact form of a right answer is accepted. An angle on an axis is shown as being in no quadrant.

## How the math was checked

- **Checks page:** [`checks.html`](https://jontaylormed.github.io/unit-circle-protocol/checks.html) runs 552 checks in the browser. It compares every value against JavaScript's own sine and cosine, reading each exact value such as √3/2 as a number. All 552 pass. The checks cover:
  - all 45 Whack-a-Mole answers, their wrong choices and the extra wrong values;
  - all 52 practice questions, every form they accept, and that every right form is accepted;
  - the practice reference table;
  - all 8 navigation missions: answer, wording, hint, choices, diagram labels and measurements;
  - the special right triangles;
  - all 17 special angles on the unit circle, plus free dragging with the angle lock off;
  - every radian preset;
  - the progress report;
  - keyboard use of the mission cards, the unit circle and Whack-a-Mole, plus grey-text contrast in all five parts, button names and the reduced-motion rule;
  - a scan of the page for network requests and storage.
- **Fixed after checking:** an earlier version had these errors, and all are fixed:
  - it accepted "∞" for tan 90°;
  - it rejected right forms such as 1/√2;
  - it called 180° Quadrant II and 360° Quadrant IV;
  - it showed exact values for angles near, but not at, a special angle;
  - it labeled navigation legs "cos θ" instead of "2 cos 30°";
  - its report counted missions that weren't finished.
- **Known limits:**
  - Whack-a-Mole and Navigation use fixed question sets.
  - Practice asks for exact values, so 0.866 is not accepted for √3/2. 0.5 is accepted for 1/2, since it is exact.
  - Navigation angles are measured from the east–west line, as each mission says.

## Accessibility

- **Keyboard:** every mission works with the keyboard, and focus outlines are visible.
  - Mission cards are selected with Tab and Enter.
  - In the Unit Circle Explorer, the arrow keys step to the next special angle (30°, 45°, 60° and so on). With the angle lock off, they move 1°, or 15° with Shift.
  - The Radian Visualizer and Triangle Morphing sliders and buttons are standard controls.
  - Navigation's choices are buttons, and Practice takes typed answers and Enter.
  - Whack-a-Mole holes can be chosen with Tab and Enter. The game is timed, so it is harder to play this way.
- **Contrast:** main text has 16.7:1 contrast, the bright accent colors run 5.7:1 to 15.9:1, and the grey labels 4.9:1 or better. All meet the WCAG 2.1 AA target of 4.5:1.
- **Screen readers:**
  - The Unit Circle Explorer reads out its angle, radians, sine, cosine, tangent and quadrant.
  - The sliders read their values, in radians and degrees.
  - Navigation and Practice feedback, hints, and each new Whack-a-Mole question are read aloud.
  - Whack-a-Mole's right/wrong flashes are visual only.
- **Motion:** when the device asks for reduced motion, the blinking cursor, flashes and pop-ups stop animating. Whack-a-Mole's right/wrong labels still appear.
- **Text size:** there is no separate setting; the page follows browser zoom.

## Privacy

No accounts, no tracking, no cookies and no stored data. A name, if a student types one, appears only on the screen and on the printed report. It is never saved or sent, and closing the tab clears it. The missions report their progress to the home screen inside the same page, so nothing leaves the browser. The page makes no network requests: its typefaces are built into the file, and `checks.html` confirms nothing loads from outside.

## Running it

Open `index.html` in any modern browser.

`checks.html` reads the tool, so open it from the live site or any local web server, not as a file.

**Publishing:** GitHub Pages, deployed from the `main` branch at the repository root. There is no build step.

## License

[CC BY-NC-SA 4.0](LICENSE). Free to share and adapt for non-commercial use, with credit, under the same license.

The bundled typefaces have their own license, and their license files are in [`fonts/`](fonts/). The home screen and report use the device's own monospace font.

| Typeface | Used for | Designer | License |
|---|---|---|---|
| VT323 | Mission headings and readouts | The VT323 Project Authors | [SIL Open Font License 1.1](fonts/OFL-vt323.txt) |
| Share Tech Mono | Mission text and diagram labels | Carrois Type Design (Ralph du Carrois) | [SIL Open Font License 1.1](fonts/OFL-sharetechmono.txt) |
| Press Start 2P | Whack-a-Mole titles | The Press Start 2P Project Authors | [SIL Open Font License 1.1](fonts/OFL-pressstart2p.txt) |

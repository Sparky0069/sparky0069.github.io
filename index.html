<!DOCTYPE html>
<html lang="en">
<head>
  <meta ch
arset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Fretboard Visualizer</title>
  <style>
    body { font-family: Arial, sans-serif; text-align: center; }
    canvas { border: 2px solid black; margin-top: 20px; }
    label, select { margin: 10px; }
    .legend { margin-top: 20px; font-size: 14px; }
  </style>
</head>
<body>
  <h1>Fretboard Visualizer</h1>

  <label for="rootNote">Root Note:</label>
  <select id="rootNote"></select>

  <label for="scaleType">Scale:</label>
  <select id="scaleType">
    <option value="ionian">Ionian (Major)</option>
    <option value="dorian">Dorian</option>
    <option value="phrygian">Phrygian</option>
    <option value="lydian">Lydian</option>
    <option value="mixolydian">Mixolydian</option>
    <option value="aeolian">Aeolian (Minor)</option>
    <option value="locrian">Locrian</option>
    <option value="major_pent">Major Pentatonic</option>
    <option value="minor_pent">Minor Pentatonic</option>
  </select>

  <label for="handedness">Handedness:</label>
  <select id="handedness">
    <option value="right">Right</option>
    <option value="left">Left</option>
  </select>

  <canvas id="fretboardCanvas" width="1800" height="400"></canvas>

  <div class="legend">
    <p><strong>Mode Degrees:</strong> Ionian (1), Dorian (2), Phrygian (3), Lydian (4), Mixolydian (5), Aeolian (6), Locrian (7)</p>
  </div>

  <script>
    const noteNames = ['C', 'C#', 'D', 'D#', 'E', 'F', 'F#', 'G', 'G#', 'A', 'A#', 'B'];
    const tuning = ['E', 'A', 'D', 'G', 'B', 'E'];
    const frets = 24;
    const canvas = document.getElementById("fretboardCanvas");
    const ctx = canvas.getContext("2d");

    const scalePatterns = {
      ionian:       [0, 2, 4, 5, 7, 9, 11],
      dorian:       [0, 2, 3, 5, 7, 9, 10],
      phrygian:     [0, 1, 3, 5, 7, 8, 10],
      lydian:       [0, 2, 4, 6, 7, 9, 11],
      mixolydian:   [0, 2, 4, 5, 7, 9, 10],
      aeolian:      [0, 2, 3, 5, 7, 8, 10],
      locrian:      [0, 1, 3, 5, 6, 8, 10],
      major_pent:   [0, 2, 4, 7, 9],
      minor_pent:   [0, 3, 5, 7, 10]
    };

    function fillDropdown(id, options) {
      const select = document.getElementById(id);
      options.forEach(opt => {
        const el = document.createElement("option");
        el.value = el.textContent = opt;
        select.appendChild(el);
      });
    }

    fillDropdown("rootNote", noteNames);

    document.querySelectorAll("select").forEach(el => el.addEventListener("change", drawFretboard));

    function getNoteAt(stringNote, fret) {
      const index = (noteNames.indexOf(stringNote) + fret) % 12;
      return noteNames[index];
    }

    function drawFretboard() {
      ctx.clearRect(0, 0, canvas.width, canvas.height);
      const root = document.getElementById("rootNote").value;
      const scaleType = document.getElementById("scaleType").value;
      const handedness = document.getElementById("handedness").value;
      const pattern = scalePatterns[scaleType];
      const rootIndex = noteNames.indexOf(root);

      const width = canvas.width / (frets + 1);
      const height = canvas.height / tuning.length;

      tuning.forEach((stringNote, stringIdx) => {
        const y = height * (handedness === 'left' ? stringIdx : tuning.length - 1 - stringIdx);
        for (let fret = 0; fret <= frets; fret++) {
          const x = width * fret;
          const note = getNoteAt(stringNote, fret);
          const noteIndex = (noteNames.indexOf(note) - rootIndex + 12) % 12;
          let fill = 'white';
          let text = 'black';

          if (note === root) fill = '#226622'; // dark green for root
          else if (pattern.includes(noteIndex)) {
            fill = '#66cc66'; // green for scale notes
          }

          ctx.fillStyle = fill;
          ctx.strokeStyle = "black";
          ctx.lineWidth = 1;
          ctx.fillRect(x, y, width, height);
          ctx.strokeRect(x, y, width, height);

          ctx.fillStyle = text;
          ctx.font = "bold 14px sans-serif";
          ctx.textAlign = "center";
          ctx.textBaseline = "middle";
          ctx.fillText(note, x + width / 2, y + height / 2);
        }
      });

      // Draw fret numbers on top
      for (let fret = 0; fret <= frets; fret++) {
        const x = width * fret;
        ctx.fillStyle = [3, 5, 7, 9, 12, 15, 17, 19, 21, 23].includes(fret) ? 'black' : 'gray';
        ctx.font = "bold 12px sans-serif";
        ctx.fillText(fret.toString(), x + width / 2, 10);
      }
    }

    drawFretboard();
  </script>
</body>
</html>

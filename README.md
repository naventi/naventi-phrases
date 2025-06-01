<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Naventi</title>
  <style>
    body {
      background-color: black;
      color: white;
      font-family: "Courier New", monospace;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      padding: 0 1rem;
    }
    h1 {
      font-size: 3rem;
      margin-bottom: 2rem;
    }
    #phrase {
      font-size: 2rem;
      text-align: center;
      white-space: pre-line;
      min-height: 6rem;
    }
    button {
      margin-top: 2rem;
      padding: 0.5rem 1rem;
      font-size: 1rem;
      background: none;
      border: 1px solid white;
      color: white;
      cursor: pointer;
    }
    button:hover {
      background-color: white;
      color: black;
    }
  </style>
</head>
<body>
  <h1>naventi</h1>
  <div id="phrase"></div>
  <button onclick="newPhrase()">generate</button>

  <script>
    const phrases = [
      "Muted. For now.",
      "Power doesn’t raise its voice.",
      "The lightning without thunder.",
      "Disruption looks quiet from a distance.",
      "For those who say nothing—and change everything.",
      "Intent over impulse.",
      "Move different.",
      "Less shown. More known.",
      "Silence is strategy.",
      "Presence without performance.",
      "Built in the background.",
      "Invisible isn’t inactive.",
      "Quiet is loud when you know where to listen.",
      "Design, distilled.",
      "Be the signal, not the noise.",
      "Stillness doesn’t mean stagnation.",
      "Some storms don’t need thunder.",
      "Seen by few. Felt by all.",
      "Soft-spoken. Sharp-minded.",
      "Truth doesn’t need volume.",
      "Echoes without sound.",
      "Minimal words, maximal weight.",
      "Subtle is sovereign.",
      "The loudest move is no movement.",
      "Discipline disguised as ease.",
      "Unseen, but unmistakable.",
      "The work whispers. The results shout.",
      "The art of restraint.",
      "Underexposed, overdelivering.",
      "Measured silence, intentional impact.",
      "Direction, not attention.",
      "Noise fades. Intention stays.",
      "The shift before the quake.",
      "Precision, not performance.",
      "Elegance in anonymity.",
      "Calm before every conquest.",
      "Control that doesn’t need control.",
      "Moved by meaning, not motion.",
      "More than seen. Understood.",
      "Purpose, without punctuation.",
      "Quiet storms leave the deepest marks.",
      "Authority doesn’t ask permission.",
      "Not loud. Just certain.",
      "Energy held, not spent.",
      "The weight of what isn’t said.",
      "Power as posture, not volume.",
      "Proof over profile.",
      "Absence, then arrival.",
      "Still water cuts deepest.",
      "The shape of subtle strength.",
      "No need to shout when you're sure.",
      "Unsaid, but undeniable.",
      "Intent writes louder than speech.",
      "Not revealed. Remembered.",
      "Built for silence. Wired for impact.",
      "All signal. No noise.",
      "Louder in motion than in words.",
      "Pressure moves in silence.",
      "Clarity whispers.",
      "Mastery is quiet.",
      "Muted force. Full intent.",
      "Walk softly. Leave marks.",
      "Felt but not featured.",
      "Controlled burn.",
      "Disrupt softly.",
      "Tuned to silence.",
      "Hidden hands guide louder paths.",
      "Soundless strikes.",
      "Presence without spotlight.",
      "Power in pause.",
      "Influence doesn't beg.",
      "Restraint is rebellion.",
      "Silent doesn’t mean still.",
      "Steady is strong.",
      "Every detail, intentional.",
      "Let the work speak.",
      "Dark-horse energy.",
      "Visibility is optional. Vision isn’t.",
      "The uncelebrated edge.",
      "Every move considered.",
      "Signal coded in silence.",
      "Strength sits quietly.",
      "Quiet doesn’t mean small.",
      "Pressure moves underground.",
      "No noise. Just clarity.",
      "Presence is louder than voice.",
      "Refined and relentless.",
      "Minimal by design. Maximal in impact.",
      "Move unseen. Speak through result.",
      "Gravity in minimalism.",
      "Every shadow holds shape.",
      "Motion, unannounced.",
      "Leave nothing loud. Leave nothing missed.",
      "Obscured, never overlooked.",
      "Posture over pose.",
      "The signal in the silence.",
      "Markless, but not missed.",
      "Composed, not controlled.",
      "The art of unspoken presence.",
      "Speak less. Echo longer.",
      "Shape without being seen.",
      "Substance in every shadow.",
      "Invisible doesn’t mean idle."
    ];

    function typeEffect(element, text, speed = 40) {
      element.innerHTML = "";
      let i = 0;
      const timer = setInterval(() => {
        if (i < text.length) {
          element.innerHTML += text.charAt(i);
          i++;
        } else {
          clearInterval(timer);
        }
      }, speed);
    }

    function newPhrase() {
      const phrase = phrases[Math.floor(Math.random() * phrases.length)];
      const element = document.getElementById("phrase");
      typeEffect(element, phrase);
    }

    window.onload = newPhrase;
  </script>
</body>
</html>

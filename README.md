<!DOCTYPE html!>
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
      text-transform: lowercase;
    }
    #phrase {
      font-size: 2rem;
      text-align: center;
      white-space: pre-line;
      min-height: 6rem;
      text-transform: lowercase;
    }
    button {
      margin-top: 2rem;
      padding: 0.5rem 1rem;
      font-size: 1rem;
      background: none;
      border: 1px solid white;
      color: white;
      cursor: pointer;
      text-transform: lowercase;
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
  <button onclick="newPhrase()">more phrases</button>

  <script>
    const phrases = [
      "muted. for now.",
      "power doesn’t raise its voice.",
      "the lightning without thunder.",
      "disruption looks quiet from a distance.",
      "for those who say nothing—and change everything.",
      "intent over impulse.",
      "move different.",
      "less shown. more known.",
      "silence is strategy.",
      "presence without performance.",
      "built in the background.",
      "invisible isn’t inactive.",
      "quiet is loud when you know where to listen.",
      "design, distilled.",
      "be the signal, not the noise.",
      "stillness doesn’t mean stagnation.",
      "some storms don’t need thunder.",
      "seen by few. felt by all.",
      "soft-spoken. sharp-minded.",
      "truth doesn’t need volume.",
      "echoes without sound.",
      "minimal words, maximal weight.",
      "subtle is sovereign.",
      "the loudest move is no movement.",
      "discipline disguised as ease.",
      "unseen, but unmistakable.",
      "the work whispers. the results shout.",
      "the art of restraint.",
      "underexposed, overdelivering.",
      "measured silence, intentional impact.",
      "direction, not attention.",
      "noise fades. intention stays.",
      "the shift before the quake.",
      "precision, not performance.",
      "elegance in anonymity.",
      "calm before every conquest.",
      "control that doesn’t need control.",
      "moved by meaning, not motion.",
      "more than seen. understood.",
      "purpose, without punctuation.",
      "quiet storms leave the deepest marks.",
      "authority doesn’t ask permission.",
      "not loud. just certain.",
      "energy held, not spent.",
      "the weight of what isn’t said.",
      "power as posture, not volume.",
      "proof over profile.",
      "absence, then arrival.",
      "still water cuts deepest.",
      "the shape of subtle strength.",
      "no need to shout when you're sure.",
      "unsaid, but undeniable.",
      "intent writes louder than speech.",
      "not revealed. remembered.",
      "built for silence. wired for impact.",
      "all signal. no noise.",
      "louder in motion than in words.",
      "pressure moves in silence.",
      "clarity whispers.",
      "mastery is quiet.",
      "muted force. full intent.",
      "walk softly. leave marks.",
      "felt but not featured.",
      "controlled burn.",
      "disrupt softly.",
      "tuned to silence.",
      "hidden hands guide louder paths.",
      "soundless strikes.",
      "presence without spotlight.",
      "power in pause.",
      "influence doesn't beg.",
      "restraint is rebellion.",
      "silent doesn’t mean still.",
      "steady is strong.",
      "every detail, intentional.",
      "let the work speak.",
      "dark-horse energy.",
      "visibility is optional. vision isn’t.",
      "the uncelebrated edge.",
      "every move considered.",
      "signal coded in silence.",
      "strength sits quietly.",
      "quiet doesn’t mean small.",
      "pressure moves underground.",
      "no noise. just clarity.",
      "presence is louder than voice.",
      "refined and relentless.",
      "minimal by design. maximal in impact.",
      "move unseen. speak through result.",
      "gravity in minimalism.",
      "every shadow holds shape.",
      "motion, unannounced.",
      "leave nothing loud. leave nothing missed.",
      "obscured, never overlooked.",
      "posture over pose.",
      "the signal in the silence.",
      "markless, but not missed.",
      "composed, not controlled.",
      "the art of unspoken presence.",
      "speak less. echo longer.",
      "shape without being seen.",
      "substance in every shadow.",
      "invisible doesn’t mean idle."
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

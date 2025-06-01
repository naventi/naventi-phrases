<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Naventi Thought</title>
  <style>
    body {
      background: #111;
      color: #eee;
      font-family: 'Courier New', Courier, monospace;
      display: flex;
      align-items: center;
      justify-content: center;
      height: 100vh;
      margin: 0;
      text-align: center;
      padding: 20px;
      font-size: 1.5rem;
      user-select: none;
      flex-direction: column;
    }
    #phrase {
      max-width: 600px;
      line-height: 1.4;
      font-weight: 300;
      letter-spacing: 0.03em;
      min-height: 80px;
      white-space: pre-wrap;
    }
    button {
      margin-top: 40px;
      padding: 10px 20px;
      font-size: 1rem;
      font-family: 'Courier New', Courier, monospace;
      background: transparent;
      border: 1px solid #eee;
      color: #eee;
      cursor: pointer;
      border-radius: 4px;
      transition: background 0.3s ease;
    }
    button:hover {
      background: #eee;
      color: #111;
    }
  </style>
</head>
<body>
  <div id="phrase">Loading...</div>
  <button onclick="typeRandomPhrase()">Another Thought</button>

  <script>
    const phrases = [
      "The silence holds weight.",
      "Form over noise.",
      "Quiet strength in every detail.",
      "Minimal moves, maximal intent.",
      "Design that speaks without shouting.",
      "Shadows reveal more than light.",
      "Intentional disruption.",
      "Crafted for those who see beyond.",
      "Power in restraint.",
      "Subtle but undeniable.",
      "Stillness is the source of movement.",
      "Less noise, more meaning.",
      "The unseen shapes the visible.",
      "Actions speak beyond words.",
      "Strength thrives in the quiet.",
      "Purpose fuels every choice.",
      "Where detail lives, power follows.",
      "Discipline is the silent architect.",
      "Intent over impulse.",
      "Change happens in shadows.",
      "Quiet does not mean weak.",
      "The storm whispers its coming.",
      "In darkness, light is revealed.",
      "Silence carves the path forward.",
      "Mastery hides behind humility.",
      "A quiet mind is a sharp mind.",
      "Depth over display.",
      "The unseen moves mountains.",
      "Invisible hands guide the flow.",
      "A thought can reshape worlds.",
      "Restraint is a form of power.",
      "Patience is the ultimate strength.",
      "Control without force.",
      "Presence is felt, not heard.",
      "Less said, more done.",
      "The quiet disruptors rewrite rules.",
      "In subtlety lies revolution.",
      "Invisible but indispensable.",
      "Power speaks softly, moves swiftly.",
      "The calm before impact.",
      "A spark unseen ignites the change.",
      "Silence is the loudest message.",
      "Understated yet unstoppable.",
      "Details build the invisible framework.",
      "Quiet confidence commands respect.",
      "Simplicity reveals complexity.",
      "The quiet forge of progress.",
      "Strength wrapped in stillness.",
      "The shadows hold the blueprint.",
      "Silence breeds clarity.",
      "Invisible forces shape destiny.",
      "Power resides in the pause.",
      "Silent steps leave the deepest marks.",
      "The unseen hand moves the world.",
      "Calm waters run deep.",
      "The quiet mind shapes the future.",
      "Discipline whispers success.",
      "Less noise, more focus.",
      "Shadows cast the strongest outlines.",
      "Stealth is a form of strength.",
      "Mastery demands silence.",
      "Unseen, yet undeniably present.",
      "In silence, clarity grows.",
      "Minimal effort, maximal effect.",
      "The quiet architect of change.",
      "Soft power, hard impact.",
      "Stillness fuels momentum.",
      "The invisible pulse of progress.",
      "Silent influence, loud results.",
      "The calm at the center of the storm.",
      "Quiet resolve breaks barriers.",
      "The shadows are never empty.",
      "In silence, power accumulates.",
      "Invisible threads bind the world.",
      "Quiet strength moves mountains.",
      "Silence sharpens vision.",
      "Stillness precedes the storm.",
      "The unseen changes everything.",
      "Power wrapped in patience.",
      "Soft whispers shift paradigms.",
      "Quiet courage sparks revolutions.",
      "Silence carves paths unseen.",
      "Invisible forces shape futures.",
      "Quiet does not mean absent.",
      "Silent tides reshape shores.",
      "Still minds move the masses.",
      "The silent storm gathers strength.",
      "Quiet hands build empires.",
      "Invisible strength, visible change.",
      "The calm voice of power.",
      "Silence is the first step.",
      "Power lives between the words.",
      "Quiet hands, loud results.",
      "Silent roots grow the strongest trees.",
      "In stillness, there is power."
    ];

    function typeRandomPhrase() {
      const phrase = phrases[Math.floor(Math.random() * phrases.length)];
      const phraseDiv = document.getElementById('phrase');
      phraseDiv.textContent = "";
      let i = 0;

      const typing = setInterval(() => {
        if (i < phrase.length) {
          phraseDiv.textContent += phrase.charAt(i);
          i++;
        } else {
          clearInterval(typing);
        }
      }, 40); // Adjust speed here (milliseconds per character)
    }

    // Type on initial load
    typeRandomPhrase();
  </script>
</body>
</html> 

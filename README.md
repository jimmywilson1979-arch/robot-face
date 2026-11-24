# Claude Robot Face

The face of James's home robot: an old Android phone becomes the robot's head, and Claude is its brain.

**Open it:** https://jimmywilson1979-arch.github.io/robot-face/

## What it does
- **Screen mode:** the face makes way for a YouTube video or a picture slideshow, with a small live face in the corner. Ask ("show me a video of puppies", "put the dinosaur pictures on", "back to your face"), or tap **Show** to paste a YouTube link or pick a collection from the [art library](https://jimmywilson1979-arch.github.io/art-library/). Videos use YouTube's own player and start by themselves (if the browser blocks sound, they start quietly with a **Tap for sound** button). Claude passes 2–3 choices, and if one is blocked from playing outside YouTube the next is tried automatically; **Open in YouTube** is there as a last resort. Videos pause while you talk to the robot and carry on afterwards, and you can say "pause the video" or "carry on". **Maps and directions:** "show me a map of Tenby", "how do I get to Cardiff Castle" (from home unless you say otherwise; walking, transit or cycling too), with **Open in Google Maps** for turn-by-turn navigation. **Quick commands** while something is showing ("close it", "back to your face", "pause", "carry on", "next") are done instantly on the phone without asking Claude. After putting something on, the robot just says a few words. **Pictures from the web:** "show me a picture of a snow leopard", or search in the Show panel (Wikimedia Commons, with Openverse as a backup; free, no key).
- **Home helpers** (all by voice, all free):
  - ⏲️ **Timers:** "set a 12 minute timer for the pasta". Countdowns sit in the corner, an alarm beeps and the robot says which one is done; say "stop" or tap to silence it. Several at once, kept if the page reloads.
  - 🌦️ **Weather card:** "what's the weather?" shows now plus 7 days ([Open-Meteo](https://open-meteo.com), no key) and the robot says one sentence.
  - 🍳 **Recipe mode:** "help me make pancakes" shows the ingredients, then "next step", "back", "repeat", "ingredients" hands-free (each step is read out), or tap the buttons.
  - 🖼️ **Family photo frame:** add photos from the tablet in Settings (they stay on the tablet), then "show the family photos", or set it to come on by itself in the evenings.
  - 🕰️ **Bedside clock:** a big, dim clock, by voice or automatically at night. Talking or tapping brings the face back; it returns after a minute.
  - 🛒 **Shopping list:** "add milk and bread to the list", "what's on the list?", "show me the list" (with a QR code to scan with your phone, a **Send to my phone** share button, and tap an item to tick it off).
- **Face styles** (Settings → Face style, saved per personality): **Classic eyes**, **Hologram orb** (an original spinning sphere of light points with orbit rings; it spins up while thinking, pulses while listening and ripples with the voice), **Sound wave** (a glowing line that moves with the voice, with small eyes), and **Pixel LED** (the classic face on a glowing dot-matrix display). Swipe left or right across the face to flick between them, or just ask ("change your face to the orb").
- Animated face with expressions: happy, listening, thinking, curious, surprised, sad, sleepy, asleep
- Talk (speech recognition) or type; Claude replies in a calm British-butler voice and the face shows its mood
- Web search for live info (weather, news, scores), localised to your home town
- Listens again for a follow-up after each answer, and can start listening when the camera sees you
- Front camera follow: the eyes track you around the room
- Sight: Claude can take a photo with the camera when a question needs it ("what am I holding?")
- Silent wake word ("Jarvis" by default) using Picovoice Porcupine, running on the device; needs a free Picovoice access key
- **Voices** (pick one per personality in Settings, the mouth moves with the sound):
  - **Device voice:** free, instant, built in.
  - **Kokoro:** free, high-quality voices that run on the phone itself ([Kokoro-82M](https://github.com/hexgrad/kokoro), Apache 2.0). It downloads about 90 MB the first time (use Wi-Fi), then works offline. Includes British George, Fable, Lewis, Daniel, Emma and Isabella, plus deep "Onyx" and jolly "Santa".
  - **Voxtral (Mistral):** very cheap (about $0.016 per 1,000 characters, roughly 1p for every 5 replies) and copies a voice from a 5–25 second recording. Add a Mistral API key, then tap **Copy my 3 designed voices to Voxtral** (uses the clips in `voices/`), or **Add a voice from a recording**. If Mistral ever forgets a voice, the robot remakes it from its clip. Only copy voices you have permission to use.
  - **ElevenLabs:** uses ElevenLabs credits (optional).
- **Personalities** (Settings → Personality), each with its own voice and face colour: 🎩 Butler (Jarvis style), 🪨 Rocky from *Project Hail Mary* (fan version, home use only: clipped speech, musical chords before he talks; uses your designed "Alien" voice), 🚕 New Yorker (gruff cab driver, heart of gold), 🦁 Wildlife Narrator (narrates your home like a nature documentary, an original character; uses your designed "David A" voice), 🏴‍☠️ Pirate Captain, ⚽ Football Commentator, and ✨ Make your own (type a name and a description). Each personality remembers its own voice: pick "Free device voice" or any ElevenLabs voice, or paste a voice ID. You can also just ask: "talk like a pirate", "be Rocky", "back to normal". Each personality also has its own talking speed (🐢 70% to 🐇 120%), saved as soon as you move the slider. Choosing a personality in settings starts a fresh chat.
- Gets sleepy when left alone, wakes on a tap or when it sees movement

## Setting it up on the robot phone
1. Open the link above in Chrome on the phone.
2. Paste your Claude API key in settings (it's saved only on that phone).
3. Allow the microphone and camera when asked.
4. For full-screen use, set the link as the start page in Fully Kiosk Browser.

Everything is in `index.html`; `porcupine_params.pv` is the wake-word model.

# Claude Robot Face

The face of James's home robot: an old Android phone becomes the robot's head, and Claude is its brain.

**Open it:** https://jimmywilson1979-arch.github.io/robot-face/

## What it does
- Animated face with expressions: happy, listening, thinking, curious, surprised, sad, sleepy, asleep
- Talk (speech recognition) or type; Claude replies in a calm British-butler voice and the face shows its mood
- Web search for live info (weather, news, scores), localised to your home town
- Listens again for a follow-up after each answer, and can start listening when the camera sees you
- Front camera follow: the eyes track you around the room
- Sight: Claude can take a photo with the camera when a question needs it ("what am I holding?")
- Silent wake word ("Jarvis" by default) using Picovoice Porcupine, running on the device; needs a free Picovoice access key
- Premium ElevenLabs voices with lip-sync (optional)
- **Two personalities** (Settings → Personality): the **Butler** (Jarvis style), or **Rocky** from *Project Hail Mary* (fan version, home use only). Rocky talks in short clipped sentences, ends questions with "question", says "Happy happy happy!", and plays a little phrase of musical chords before his "translation", with the mouth moving to the chords. The face turns stone-coloured for Rocky. His voice is the free device voice, higher and a bit faster, or paste an ElevenLabs voice ID into "Rocky's voice" (e.g. one you design in ElevenLabs). Switching personality starts a fresh chat.
- Gets sleepy when left alone, wakes on a tap or when it sees movement

## Setting it up on the robot phone
1. Open the link above in Chrome on the phone.
2. Paste your Claude API key in settings (it's saved only on that phone).
3. Allow the microphone and camera when asked.
4. For full-screen use, set the link as the start page in Fully Kiosk Browser.

Everything is in `index.html`; `porcupine_params.pv` is the wake-word model.

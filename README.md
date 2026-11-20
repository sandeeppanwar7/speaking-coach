# Speaking Coach

A free, single-page web app for practicing speaking out loud, in **English or Hindi (हिन्दी)**. Read a passage or answer a prompt, and get scored on:

- **Pace**: words per minute (target 130–160)
- **Filler words**: um, uh, like, you know, basically… per minute
- **106 English and 50 Hindi read-aloud passages** across 10 topics (work updates, interviews, presentations, stories, small talk and more), in random order
- **Reading accuracy**: words you skipped or didn't say clearly
- **Pitch range**: whether you sound expressive or monotone
- **Pauses**: how often and how long you pause
- **Volume**: whether your energy stays even, and whether you trail off at the end of sentences

**Conversation mode:** press Start before you talk to someone and Stop afterwards. A 4-second voice check learns how loud you are, then louder speech counts as you and quieter speech as the other person. You get your talk share, pace, filler words, longest turn, questions asked and voice metrics for your part only, in English, Hindi or mixed Hinglish.

You can also drop in a recording (M4A, MP3 or WAV) from Voice Memos or any recorder. Your scores are saved in your browser so you can track progress over time.

## Languages

Switch between English and हिन्दी at the top of the page. The whole interface, the drills and the tips switch language, live speech recognition listens in the chosen language (hi-IN for Hindi), and scoring understands Hindi filler words (मतलब, यानी, है ना) and the । sentence mark.

## Use it

Open `index.html` in Chrome, Edge or Safari, or use the hosted version on GitHub Pages.

## Privacy

- Recordings are analyzed **in your browser** and never uploaded.
- Live speech-to-text uses your browser's built-in speech service. In Chrome and Edge, that means audio is sent to the browser maker's speech service for transcription.
- History is stored only in your browser's local storage.

## Browser support

| Feature | Chrome / Edge | Safari | Firefox |
|---|---|---|---|
| Live speaking | ✅ | ✅ | ❌ (paste a transcript instead) |
| Recording analysis | ✅ | ✅ | ✅ |

## How it works

Everything is in one file, `index.html`, with no build step and no dependencies.

- Speech-to-text: the [Web Speech API](https://developer.mozilla.org/docs/Web/API/Web_Speech_API)
- Pitch: normalized autocorrelation on 40 ms frames
- Pace from audio: syllable-peak counting on the loudness curve (an estimate, about ±15%)
- Reading accuracy: word-level alignment (longest common subsequence) between the passage and the transcript

## Contributing

Issues and pull requests are welcome. To add passages, edit `passages.js` (English) or `passages-hi.js` (Hindi). Interface translations live in `i18n-hi.js`. Other ideas: more languages, better pitch tracking.

## License

MIT

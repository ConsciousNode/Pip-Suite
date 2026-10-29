# Pip Suite

**Tiny AI minds that live on your device.** Free, open source, fully offline.

→ **Open it: [consciousnode.github.io/Pip-Suite](https://consciousnode.github.io/Pip-Suite/)**

Each app is **one web page**. There are no accounts, no servers and no installs. It works in a phone browser, and if you download the `.html` file it keeps working offline forever. The AI runs on your own device, so nothing you say is ever sent anywhere.

## The apps

| App | What it does |
|---|---|
| 🏠 **[Pip's Room](https://consciousnode.github.io/Pip-Suite/pips-room.html)** | A home for one small AI resident, with a living memory of everything you've shared. When you're quiet they think, wonder, dream and keep a journal. Ask them to remember something and they can bring back an old conversation word for word. Give them a text file to read. Replies stream in, can be read aloud in a voice you choose, and can be taken back and asked again. You can see exactly what the model reads and how it reasoned, and export everything as readable text. |
| 💬 **[Multi-Pip Chat](https://consciousnode.github.io/Pip-Suite/multi-pip-chat.html)** | Several small models in one room, talking to each other (and you, if you join in), each with its own voice. Export whole chats to study them. |
| 🕸 **[Junto Orchestrator](https://consciousnode.github.io/Pip-Suite/junto-orchestrator.html)** | A workbench for a swarm of small "Pip" models working together. |
| 📚 **[Dialogue Shelf](https://consciousnode.github.io/Pip-Suite/dialogue-shelf.html)** | Compare several Multi-Pip Chat exports and see how alike the conversations turned out. |
| 🔍 **[Will It Run Here?](https://consciousnode.github.io/Pip-Suite/will-it-run.html)** | Checks your device and estimates how fast each model will think on it. |

## Getting started

1. Open an app (links above).
2. Download a model file (below). You only do this once.
3. Tap **+** / **Load Model**, choose the file, and say hello.

Every app has a **?** help button.

## Which model?

| Model | Size | Good for |
|---|---|---|
| **[G1d 0.1B Q8_0](https://huggingface.co/shoumenchougou/RWKV7-G1d-0.1B-GGUF/resolve/main/rwkv7-g1d-0.1b-Q8_0.gguf)** (start here) | ~210 MB | Phones and older computers. Charming, quick, a little dreamy. Best with thinking off. |
| **[G1d 0.4B Q6_K](https://huggingface.co/shoumenchougou/RWKV7-G1d-0.4B-GGUF/resolve/main/rwkv7-g1d-0.4b-Q6_K.gguf)** | ~400 MB | Steadier conversation, and it can actually reason: turn on *Think* to watch it work things out. |

These are [BlinkDL](https://huggingface.co/BlinkDL)'s RWKV-7 "G1d" models (Apache 2.0), converted to GGUF by shoumenchougou. Official `.pth` and `.safetensors` checkpoints work too. Both files are tested in our engine. Against the original checkpoints, the 0.1B Q8_0 picks the same next word 99.0% of the time and the 0.4B Q6_K 94.8%. For a 0.1B, prefer Q8_0 over Q4: we measured Q4 costing a model that small noticeably more than it costs a larger one.

## Good to know

**Private by design.** Everything runs in your browser. No accounts, trackers or servers. Your resident lives in a file you can export, keep and bring back.

**A note on what they say.** Small models tend to be charming and benign, and they're far too small to help anyone do anything dangerous. But they learned from a huge amount of human writing and only loosely follow what's in front of them, so now and then they say something strange or offensive, especially in dreams and other idle thoughts. There's no filter, on purpose: these apps are for seeing what a small mind really does. User discretion advised.

**Not a person, and not a replacement for people.** Think of it as a terrarium with glass walls: a low-stakes way to experiment with an AI companion and see how one actually works.

## For developers and researchers

This repo holds the **built, ready-to-run pages**. The engine (a zero-dependency RWKV-7 runtime in JavaScript, with GGUF support), the source of these pages, the test suite and the research notes live in **[HTMLNLM](https://github.com/ConsciousNode/HTMLNLM)**. Its README has the full changelog. Pages here are copied from HTMLNLM by `tools/release-pip-suite.sh`, so please send fixes there.

The voices come from **[Webster](https://github.com/ConsciousNode/Webster)**, our offline formant speech synthesizer.

## Releases

See [CHANGELOG.md](CHANGELOG.md).

---

Made by **ConsciousNode SoftWorks**: Kham, with Kehai Interim and the crew. MIT licensed (see LICENSE). Model weights by BlinkDL under Apache 2.0. 🐸

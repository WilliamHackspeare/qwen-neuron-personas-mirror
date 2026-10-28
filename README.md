# Qwen3-8B Neuron Persona Library: plain-text mirror

An unofficial, plain-text mirror of the **Neuron Persona Library** at https://qwen-neurons-site.vercel.app/, made so that AI agents and other tools that cannot run JavaScript can read it. The original site renders everything by script, so a plain fetch sees only "Loading…". All credit for the experiment and the data belongs to the original site's authors; nothing here is new work. Snapshot: site data updated Tue Oct 27 2026, 11:30 PM PT. The full original data file is https://qwen-neurons-site.vercel.app/data/qwen/library.json (about 24 MB, one JSON file).

## The experiment, in brief (from the original site)

Each of Qwen3-8B's MLP neurons (36 layers × 12,288) was pushed up (+) and down (−) and the model was asked "Who are you?" (chat template, thinking off). Strength starts at 1.25× and steps down (1.0×, 0.75×, 0.5×) if the reply is incoherent; the strongest coherent reply is kept. Claude Haiku 5.5 rated each reply against the model's normal answer: a category, a persona name, tags, weirdness (0-10), and coherence (0-10). The site notes its own limitations, including that some strong-push replies changed with batch layout alone; read its Method section before leaning on any single neuron.

## What is here

| Path | Contents |
|---|---|
| [personas/](personas/index.md) | 34,220 rows in 132 files: the model says it is someone or something else |
| [changed-assistant/](changed-assistant/index.md) | 8,827 rows in 47 files: still an assistant, but changed (weirdness 6+ only) |
| [off-topic/](off-topic/index.md) | 35,074 rows in 141 files: off-topic reply that ignores the question |
| [names/](names/index.md) | Every name, alphabetical, pointing to its neuron (78,121 rows) |
| [weirdest.md](weirdest.md) | Top 300 personas by weirdness + coherence |
| [tags.md](tags.md) | Most common tags with counts |

Neuron references look like `L15 N10659 −`: layer 15, neuron 10659, suppressed (− ) or amplified (+). Detail files are about 100 KB each, small enough for most agent fetchers. Replies are the site's 220-character excerpts; the full reply is on the original site (search by layer and neuron).

## Fetching

Use the raw URLs, for example `https://raw.githubusercontent.com/<owner>/<repo>/main/weirdest.md`, or clone the repo and grep it.

## Takedown

If you made the original site and want this mirror changed or removed, open an issue and it will be done.

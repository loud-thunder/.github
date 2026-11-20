# Loud Thunder ⚡️

**Programmable, LLM-driven generative art built on real-time GPU code.**

Not black-box diffusion. Not static prompt-and-pray images. [Loud Thunder](https://github.com/loud-thunder) builds open-source tools for a new generative artform: using Large Language Models as real-time code compilers paired with transparent, deterministic graphics pipelines.

## Why This Exists

For decades, generative art sat behind a steep mathematical wall. Writing a custom pixel shader, building a particle system, or driving procedural 3D geometry required fluency in linear algebra, vector calculus, and low-level graphics APIs.

Today, most people hear "AI art" and picture latent diffusion: opaque models that take a text prompt and return a flattened raster image. You cannot inspect the math. You cannot adjust a frequency variable. You cannot wire the output to live audio or video telemetry.

There is a better model, explored in [From Python Scripts to Pixel Shaders](https://blog.macron1.io/articles/from-python-scripts-to-pixel-shaders): **use LLMs to generate executable code, not final pixels.**

When an LLM acts as a syntactic compilation layer between human intent and graphics code, everything changes:

* **Transparent control:** You own human-readable source code. Every velocity curve, noise frequency, color palette, and camera trajectory stays exposed and editable.
* **Deterministic rigor:** You keep the architectural discipline forged in earlier Python and Pillow compositing pipelines (seed-driven variation, weighted probability, and rule-based constraints) while moving into real-time execution.
* **Hybrid video synthesis:** Instead of generating imagery from nothing, you can feed real-world MP4 footage into custom shaders and 3D topologies as raw computational material.
* **Immediate feedback loops:** Describe an optical effect in plain English, compile it to a shader, watch it run on live frames, and refine the math in real time.

## Who This Is For

* **Visual artists and directors** who want programmatic control over video aesthetics without spending years memorizing graphics APIs.
* **Creative coders** moving from 2D Python scripts and browser canvases into high-throughput GPU video synthesis.
* **AI builders** exploring LLM-generated code as a creative medium rather than a static image vending machine.

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

## The Computational Stack

Loud Thunder organizes this workflow into three operational layers:

* **Intent (LLMs as Co-Processors):** Natural language translates directly into Python scripts, WebGL environments, WGSL/GLSL fragment shaders, and declarative parameter manifests.
* **Execution (Real-Time GPU Pipelines):** Multi-pass shaders run directly on the GPU in parallel, delivering resolution-independent visuals without CPU-GPU copy bottlenecks.
* **Material (Video Telemetry & Seeds):** Real-world video streams, temporal feedback buffers, and deterministic seeds drive reactive effects like luminance displacement, pixel sorting, cellular automata, and optical distortion.

## Featured Project: `ninja-shader`

**[ninja-shader](https://github.com/loud-thunder/ninja-shader)** (`v1.0.0`, MIT License) is a Rust-based GPU video shader studio and CLI toolchain designed specifically for fast, iterative shader creation.

Built on `wgpu` (v24) and FFmpeg for macOS, Linux, and Windows, it bridges low-level GPU rendering with an interactive studio workflow where humans and LLMs can write, hot-reload, and chain shaders in seconds:

* **Sub-Millisecond Multi-Pass GPU Engine:** Chain reusable WGSL (`.wgsl`) and Vulkan GLSL (`.glsl`) fragment shaders in series using ping-pong textures with zero CPU-GPU copy bottlenecks.
* **Instant Live Hot-Reloading:** Integrated file watching reloads edited shaders on the fly. Have an LLM rewrite a `.wgsl` or `.glsl` file and watch the live video stream update immediately.
* **Native Desktop Studio:** Built with `egui` and `wgpu`, featuring video scrubbing, playback controls, live uniform sliders, keyboard-driven recipe hot-swapping, and non-blocking background video export.
* **Temporal Feedback & Motion Buffers:** Exposes `prev_frame_tex` and `original_tex` directly to shaders for trail, echo, feedback, and motion-reactive effects.
* **Dual-Language ABI & Declarative Manifests:** Compiles both WGSL and Vulkan GLSL via Naga to Metal, Vulkan, or DirectX 12, paired with `<name>.toml` sidecar manifests that expose uniform parameters automatically.
* **Lossless Audio Passthrough:** Streams video frames via FFmpeg pipes to raw RGBA8 while muxing original multichannel audio cleanly into exported renders.
* **Complete CLI & CI/CD Toolchain:** Scaffold new shaders, inspect parameter ABIs, discover effects, and validate pipelines headlessly from the command line.

## Who This Is For

* **Visual artists and directors** who want programmatic control over video aesthetics without spending years memorizing graphics APIs.
* **Creative coders** moving from 2D Python scripts and browser canvases into high-throughput GPU video synthesis.
* **AI builders** exploring LLM-generated code as a creative medium rather than a static image vending machine.

## Get Started

1. **Explore the flagship studio:** Clone and run [ninja-shader](https://github.com/loud-thunder/ninja-shader) to test multi-pass GPU shaders on your own video clips.
2. **Read the philosophy:** Dive into [From Python Scripts to Pixel Shaders](https://blog.macron1.io/articles/from-python-scripts-to-pixel-shaders) for the full breakdown of LLM-driven generative pipelines.
3. **Build and share:** Scaffold a shader, pair with an LLM to mutate the math, and open a pull request or issue in [loud-thunder](https://github.com/loud-thunder).

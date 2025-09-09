# AI & GPUs — A Super-Simple Intro

> Part of the **PC Basics** repo. For the OS primer, see: [Operating Systems](basics/operating-systems.md).

---

## Table of Contents
- [TL;DR](#tldr)
- [What “AI” Means on a PC](#what-ai-means-on-a-pc)
- [Why a GPU Helps](#why-a-gpu-helps)
- [Where the GPU Makes a Big Difference](#where-the-gpu-makes-a-big-difference)
- [Do You Need a GPU?](#do-you-need-a-gpu)
- [Mini-Glossary](#mini-glossary)
- [VRAM: The Spec That Matters Most](#vram-the-spec-that-matters-most)
- [Software Stacks (1-liners)](#software-stacks-1-liners)
- [Picking a GPU (Quick Guide)](#picking-a-gpu-quick-guide)
- [Common Gotchas](#common-gotchas)
- [FAQ](#faq)
- [Safe Starter Settings](#safe-starter-settings)
- [One-Sentence Summary](#one-sentence-summary)

---

## TL;DR
- **AI on your PC** = software that **learns from data** and uses math to make predictions (chatting, making images, recognizing speech, etc.).
- The math is mostly **big matrix multiplications** repeated a *lot*.
- **GPUs** are made to do **many tiny calculations in parallel**, so they’re usually *much faster* than CPUs for AI.
- **More VRAM** ⇒ **bigger models** (or larger batches) without errors.

---

## What “AI” Means on a PC
- **Training**: teaching a model from lots of examples so it learns patterns. Heavy, usually done on servers with multiple GPUs.
- **Inference**: *using* an already-trained model to do a task (chat, classify, generate an image). This is what most people do on a personal PC.

You can run models **locally** (on your machine) or use **cloud AI** (someone else’s GPUs via the internet).

---

## Why a GPU Helps
Think of a CPU as a few expert workers tackling complex tasks one after another.  
A GPU is a **huge team** doing the **same small job** thousands of times **at once**—perfect for AI’s repeat-the-same-math style.


CPU: [ | | | ] ← a few powerful cores (great for general tasks, OS, logic)
GPU: [||||||||||||] ← thousands of small cores (great for repeated math in parallel)



---

## Where the GPU Makes a Big Difference
- **Image generation** (diffusion models): minutes on CPU → seconds on GPU (roughly).
- **Speech & vision**: faster recognition and processing.
- **LLMs (chatbots)**: more responsive; can load larger models if VRAM allows.

---

## Do You Need a GPU?
- **Small models / light tasks** → CPU can work (but slower).
- **Integrated graphics (iGPU)** → Okay for very small models; expect modest speeds.
- **Discrete GPU** → Best experience for local AI.
- **Laptop NPUs** → Efficient for some on-device features, but still limited vs a strong GPU.
- **Cloud services** → Use when your hardware isn’t enough.

> **Display cable tip:** If your monitor is plugged into the **motherboard** video ports, your discrete **GPU might not be used**. For best GPU acceleration, plug the display into the **GPU’s** ports.

---

## Mini-Glossary
- **Model / parameters**: the “knowledge” stored as numbers.
- **Tensor**: a multi-dimensional array of numbers (the main data shape in AI).
- **Batch size**: how many items you process at once.
- **Precision** (FP32/FP16/INT8…): bits per number. Lower precision uses less memory and is faster, with a small accuracy trade-off.
- **Quantization**: compressing a model to fewer bits so it fits in less VRAM (e.g., 4-bit).

---

## VRAM: The Spec That Matters Most
VRAM is the GPU’s own memory. If a model **doesn’t fit**, you’ll get out-of-memory errors or big slowdowns.

> Rough feel only (varies by model/app/settings):

| VRAM (GB) | What You Can Typically Do |
|---:|---|
| 4–6  | Tiny LLMs (heavily quantized), small speech/vision models, low-res image gen (slow). |
| 8–12 | Mainstream image gen at reasonable speed/size; small-to-medium LLMs with quantization. |
| 16–24+ | Larger quantized LLMs locally, faster image gen, bigger context windows/batches. |

Other helpful specs:
- **Tensor/Matrix cores** (special AI math units)
- **Memory bandwidth** (feeding data fast to the cores)
- **Thermals & power** (AI = sustained load → good cooling & PSU matter)

---

## Software Stacks (1-liners)
- **NVIDIA (Win/Linux)**: CUDA + cuDNN; widest app support.
- **AMD (Linux, improving on Win)**: ROCm; support varies by GPU/app.
- **Intel**: oneAPI / OpenVINO; good for some CPU/iGPU paths.
- **Apple Silicon (macOS)**: Metal + MPS; efficient on modern Macs.

> For the most “it just works” experience across apps, **NVIDIA** typically has the smoothest path today, with others improving quickly.

---

## Picking a GPU (Quick Guide)
1. **Start with VRAM** (based on the models you want to run).
2. Verify **app/tool support** for your GPU brand and OS.
3. Check **PSU** wattage and **case cooling** (AI loads are steady and hot).
4. Prefer newer GPUs with good **low-precision support** (FP16/INT8/FP8/Tensor cores).
5. Buying used? **Stress-test** (thermals, stability, memory errors).

---

## Common Gotchas
- **OOM (Out-Of-Memory)** → lower resolution/batch size or use a **quantized** model.
- **Drivers** → mismatched/outdated drivers can cause crashes and slowdowns.
- **Thermals/power** → watch temps; ensure your PSU can handle GPU spikes.
- **Laptop GPUs** → performance depends heavily on cooling and power mode.
- **VRAM ≠ system RAM** → adding system RAM doesn’t increase VRAM.

---

## FAQ
**Q: GPU vs NPU vs TPU?**  
- **GPU**: general-purpose parallel number-cruncher; great for many AI tasks.  
- **NPU**: small, efficient accelerator in laptops/phones; great for on-device features.  
- **TPU**: specialized accelerator mostly in the cloud for large-scale training/inference.

**Q: Can I train big models at home?**  
- You can train **small** models. Modern large models usually need **multiple high-end GPUs** and lots of time/energy—cloud is more realistic.

**Q: Local vs cloud?**  
- **Local** = privacy, no usage fees, instant access—limited by your hardware.  
- **Cloud** = pay-as-you-go access to powerful GPUs—needs internet and cost control.

---

## Safe Starter Settings
- Start with a **quantized** model to save VRAM.
- Keep **batch size small**; increase slowly.
- Monitor **GPU temperature** (stay well below limits).
- Only update **drivers/toolkits** when needed; note changes so you can roll back.

---

## One-Sentence Summary
AI is lots of repeated math on big grids of numbers; **GPUs** are faster because they do **many tiny calculations in parallel**, and **VRAM size** decides how big a model you can run comfortably.

---


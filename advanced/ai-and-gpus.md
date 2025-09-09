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


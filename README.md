# 🌍 Personal Hugo Site  
_A fast, minimalist blog powered by Hugo and deployed automatically via GitHub Pages._

[![Live Site](https://img.shields.io/badge/Live%20Site-journeyman33.github.io-brightgreen?style=flat&logo=github)](https://journeyman33.github.io/hugo-site/)
[![Hugo](https://img.shields.io/badge/Static%20Site-Hugo-blue?logo=hugo)](https://gohugo.io/)
[![Build & Deploy](https://img.shields.io/github/actions/workflow/status/journeyman33/hugo-site/gh-pages.yml?label=Deploy%20Status&logo=github)](https://github.com/journeyman33/hugo-site/actions)

---

This repository contains the source for my personal website and blog.  
It serves as a platform for documenting my projects, sharing lessons learned, and reflecting on my journey in DevOps, cloud engineering, and automation.

The site is built with **Hugo**, a high-performance static site generator, and is deployed continuously through **GitHub Pages** with a fully automated CI/CD workflow.

---

## ⚙️ How It’s Built

```mermaid
flowchart LR
    A[Markdown Content] --> B[Hugo Static Generator]
    B --> C[GitHub Pages Artifact]
    C --> D[Live Production Site]

    B -. triggered by push .-> E[GitHub Actions]

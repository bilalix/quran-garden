# 🌿 Quran Garden

![GitHub last
commit](https://img.shields.io/github/last-commit/bilalix/quran-garden)
![GitHub repo
size](https://img.shields.io/github/repo-size/bilalix/quran-garden)
![GitHub
Pages](https://img.shields.io/badge/deployed-GitHub%20Pages-blue)
![Quartz](https://img.shields.io/badge/built%20with-Quartz-8A2BE2)

## 📖 Live Site

👉 **https://bilalix.github.io/quran-garden/**

------------------------------------------------------------------------

## 🧠 Project Vision

This repository is my public **digital knowledge garden** built around:

-   📖 Qur'an reference system (via `quran-to-obsidian`)
-   🧠 Personal reflections and thematic notes
-   🔁 Automatic backlinks
-   🕸 Graph-based exploration
-   🚀 Zero-server deployment (GitHub Pages only)

The goal is to create a connected, explorable Qur'anic knowledge base
--- not just linear notes.

------------------------------------------------------------------------

## 🏗 Architecture

Local workflow:

Obsidian → Git → GitHub → GitHub Actions → GitHub Pages

There is **no VPS or backend server**.\
Everything is statically generated using Quartz.

------------------------------------------------------------------------

## 📂 Repository Structure

    content/
      quran/        # Generated markdown from quran-to-obsidian
      notes/        # Personal notes and reflections

Quartz builds everything inside `content/` into a static site.

------------------------------------------------------------------------

## 📖 Qur'an Reference Layer

The folder:

    content/quran/

Contains markdown generated from:

https://github.com/subaanqasim/quran-to-obsidian

### Setup Steps

1.  Download `Quran.zip` from the repository releases.

2.  Unzip it.

3.  Copy all generated markdown files into:

        content/quran/

These files are **reference-only** and not manually edited.

------------------------------------------------------------------------

## 🧠 Writing Notes

All personal notes go inside:

    content/notes/

Example ayah link:

    [[2:255]]

Quartz automatically provides:

-   Backlinks
-   Local graph view
-   Global graph view
-   Full-text search

------------------------------------------------------------------------

## 🚀 Deployment

Deployment is handled automatically via:

    .github/workflows/deploy.yml

On every push to the `v4` branch:

1.  Dependencies install
2.  Quartz builds the site
3.  GitHub Pages publishes it

Site URL:

https://bilalix.github.io/quran-garden/

------------------------------------------------------------------------

## 🛠 Local Development

Clone the repository:

    git clone https://github.com/bilalix/quran-garden.git
    cd quran-garden

Install dependencies:

    npm install

Run local preview:

    npx quartz build --serve

Open:

http://localhost:8080

------------------------------------------------------------------------

## 🔄 Updating Content

After editing notes:

    npx quartz sync

This will:

-   Commit changes
-   Push to GitHub
-   Trigger automatic deployment

------------------------------------------------------------------------

## 🌱 Planned Enhancements

-   Thematic tafsir clustering
-   Topic-based cross-surah linking
-   Arabic ↔ English structured notes
-   Structured study pathways
-   Knowledge graph refinement

------------------------------------------------------------------------

## ⚖ License

Personal content © Bilalix\
Qur'an text attribution follows the source repository.

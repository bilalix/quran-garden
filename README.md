# Quran Garden 🌿

This repository powers my public digital garden:

👉 https://bilalix.github.io/quran-garden/

It is built using **Quartz** (an Obsidian-compatible static site
generator) and deployed automatically via **GitHub Pages (GitHub
Actions)**.

The goal of this project is to:

-   📖 Reference the Qur'an using `quran-to-obsidian`
-   🧠 Create personal notes that link to ayat and surahs
-   🔁 Enable backlinks
-   🕸 Provide graph-based knowledge exploration
-   🚀 Deploy automatically on every push --- no server required

------------------------------------------------------------------------

## 🏗 Architecture Overview

Local workflow:

Obsidian → Git commit → GitHub → GitHub Actions → GitHub Pages

There is **no VPS or server** involved.\
Everything is statically built and hosted by GitHub.

------------------------------------------------------------------------

## 📂 Repository Structure

    content/
      quran/        # Generated markdown from quran-to-obsidian (reference layer)
      notes/        # My personal notes

Quartz reads everything inside `content/` and builds the site.

------------------------------------------------------------------------

## 📖 Qur'an Reference Layer

The folder `content/quran/` contains Markdown files generated from:

https://github.com/subaanqasim/quran-to-obsidian

Steps:

1.  Download the `Quran.zip` from the releases page.

2.  Unzip it.

3.  Copy the generated markdown files into:

        content/quran/

These files are **not edited manually**. They serve as a reference layer
that my notes link to.

------------------------------------------------------------------------

## 🧠 Writing Notes

All personal notes go inside:

    content/notes/

Example link to an ayah:

    [[2:255]]

Quartz automatically generates:

-   Backlinks
-   Local graph
-   Global graph
-   Search index

------------------------------------------------------------------------

## 🚀 Deployment (Automatic)

Deployment is handled by:

`.github/workflows/deploy.yml`

On every push to the `v4` branch:

1.  GitHub installs dependencies
2.  Builds Quartz
3.  Publishes to GitHub Pages

Site URL:

https://bilalix.github.io/quran-garden/

------------------------------------------------------------------------

## 🛠 Local Development

Clone the repo:

    git clone https://github.com/bilalix/quran-garden.git
    cd quran-garden

Install dependencies:

    npm install

Run local preview:

    npx quartz build --serve

Then open:

http://localhost:8080

------------------------------------------------------------------------

## 🔄 Updating Content

After writing notes:

    npx quartz sync

This will:

-   Commit changes
-   Push to GitHub
-   Trigger automatic deployment

------------------------------------------------------------------------

## 🌱 Future Ideas

-   Thematic tafsir notes
-   Topic-based linking across surahs
-   Personal reflections connected via graph
-   Arabic/English dual-note structure

------------------------------------------------------------------------

## License

Content is personal.\
Qur'an text attribution follows the source repository.

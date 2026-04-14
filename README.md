# Loopi

**Unlocking logic and coding for kids, through play—with or without a screen.**

Loopi is a bilingual (French/English) resource repository designed to help children discover the world of logic, programming, and computer science concepts.

**🌐 Online website: [https://seiza.github.io/loopi](https://seiza.github.io/loopi)**

## How to Run Locally

To preview the project locally, ensure you have **Ruby** and **Bundler** installed.

1.  **Clone the repository:**
    ```bash
    git clone <your-repository-url>
    cd loopi
    ```

2.  **Install dependencies:**
    ```bash
    bundle install
    ```

3.  **Start the Jekyll server:**
    ```bash
    bundle exec jekyll serve --watch
    ```

4.  **View the site:**
    Open your browser at `http://localhost:4000/`.

## How to Deploy to GitHub Pages

GitHub Pages can automatically build and deploy your project from your `main` branch.

1.  **Push your code to GitHub.**
2.  **Enable GitHub Pages:**
    - Go to your repository on GitHub.
    - Click on **Settings** > **Pages**.
    - Under **Build and deployment** > **Source**, ensure it is set to **Deploy from a branch**.
    - Select the `main` branch and the root folder `/`.
3.  **Wait for the build:**
    GitHub Actions will start a job to build your Jekyll site. Once finished, your site will be available at [https://seiza.github.io/loopi](https://seiza.github.io/loopi).

---

## Project Structure

- `en/resources/` and `fr/resources/`: Contains the individual resource pages (one per language).
- `_layouts/`: Custom layouts for the website.
- `en/` and `fr/`: Language-specific homepages and resources.
- `BACKLOG.md`: Future resources to be added.
- `_config.yml`: Main project configuration.


## Instructions Guidelines

- https://blog.jetbrains.com/idea/2025/05/coding-guidelines-for-your-ai-agents/

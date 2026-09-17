<div align="center">

# Personal Portfolio Homepage

A responsive, accessible, and lightweight portfolio for presenting projects, experience, research, and technical skills.

[中文说明](README.zh-CN.md) · [Live Site](https://kaylintang.github.io/Homepage-luka-template/)

</div>

> [!NOTE]
> This site is adapted from the [Luka Homepage Template](https://github.com/wzsyyh/luka-homepage-template) by [Yuheng Yang](https://wzsyyh.github.io/). Many thanks to the original author for the warm, minimal design foundation.

## About This Project

This repository contains the source code for a personal portfolio homepage focused on cloud infrastructure, software development, data, and applied computing. It turns an academic-style profile into a concise, browsable website while keeping the implementation simple: the entire site is built with static HTML, CSS, and vanilla JavaScript.

The repository intentionally keeps private contact details and other sensitive personal information out of its documentation. Public profile content is maintained on the website itself.

## Main Sections

| Section | What it presents |
| --- | --- |
| About | A short professional introduction and areas of interest |
| Education | Academic background in a timeline layout |
| Projects | Selected full-stack, cloud, data, and web projects, including technologies and outcomes |
| Experience | Internship, technical, analytical, and industry experience |
| Research | Publication and aviation carbon-emissions research |
| Skills | Cloud, software, systems, databases, engineering workflow, and languages |
| Awards | Selected academic recognition |

## Features

- Responsive two-column desktop layout that becomes a single-column experience on tablets and phones.
- Light and dark themes, with system preference detection and the visitor's choice saved locally.
- Fixed navigation, smooth in-page links, and a back-to-top control.
- Timeline-based presentation for education, projects, experience, and research.
- Copy-to-clipboard interaction with a fallback for older browsers and accessible status feedback.
- Lightweight reveal animations powered by `IntersectionObserver`.
- Reduced-motion support, visible keyboard focus states, semantic sections, and descriptive ARIA labels.
- SEO and social-sharing metadata for search engines, Open Graph, and X/Twitter cards.
- No framework, package manager, database, or build step required.

## Technology

| Layer | Tools |
| --- | --- |
| Structure | HTML5 |
| Styling | CSS3, custom properties, responsive media queries |
| Interaction | Vanilla JavaScript, Clipboard API, `localStorage`, `matchMedia`, `IntersectionObserver` |
| Typography and icons | Google Fonts, Font Awesome, Academicons |
| Hosting and automation | GitHub Pages, GitHub Actions |

## Project Structure

```text
.
├── .github/workflows/static.yml  # GitHub Pages deployment workflow
├── assets
│   ├── css                       # Typography and site theme
│   ├── cv                        # Locally managed document assets
│   ├── img                       # Profile, project, and organisation images
│   └── js                        # Small compatibility helper
├── index.html                    # Page content, metadata, and interactions
├── README.md
├── README.zh-CN.md
├── RELEASE_NOTES.md
└── LICENSE.md
```

## Run Locally

Because the project is fully static, it can be opened directly in a browser. Running a local HTTP server is recommended so browser APIs and relative asset paths behave like they do in production:

```bash
python3 -m http.server 8000
```

Then open `http://localhost:8000`.

No dependency installation or compilation is needed.

## Deployment

The site is deployed as static content through the workflow in `.github/workflows/static.yml`:

1. A push to the `main` branch, or a manual workflow dispatch, starts the deployment.
2. GitHub Actions checks out the repository and configures GitHub Pages.
3. The repository is uploaded as a Pages artifact.
4. GitHub Pages publishes the artifact to the production environment.

For a fork, enable **GitHub Pages** under the repository settings and select **GitHub Actions** as the source. Update the canonical URL and social-sharing URLs in `index.html` to match the new domain.

## Content and Maintenance

- Edit page copy and section entries in `index.html`.
- Adjust colour tokens, spacing, typography, layout, and breakpoints in `assets/css/theme-luka.css`.
- Replace images in `assets/img/` while preserving meaningful alternative text.
- Keep personal documents and contact details out of version control unless they are deliberately intended to be public.
- After changing the site URL, update the canonical, Open Graph, and X/Twitter metadata together.

## Privacy

This README deliberately avoids reproducing contact information, private documents, or unnecessary personal details. Before publishing a fork, review the HTML and assets for metadata or files that should not be public.

## License

See [LICENSE.md](LICENSE.md) for the license terms that apply to this repository.

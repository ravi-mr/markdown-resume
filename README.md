<h1 align="center">Markdown Resume</h1>

<p align="center">Write an ATS-friendly Resume in Markdown. Available for anyone, Optimized for Dev.</p>

<p align="center"><a href="https://www.junian.dev/markdown-resume/"><strong>Start Writing Now</strong></a>!</p>

<img align="center" src="https://raw.githubusercontent.com/junian/markdown-resume/assets/img/markdown-resume-screenshot-00.jpg"/>

## About

A fork of "Oh My CV!". You can visit the original work [here](https://ohmycv.app/).

Changes I made from the original work:
- Default template is now as close as possible with [CareerCup's](https://www.careercup.com/resume) resume template.
- Default color is all Black.
- Added Web-safe fonts for easier ATS parsing.
- And many more ...

## Notice

Highly recommend using Chromium-based browsers, e.g., [Chrome](https://www.google.com/chrome/) and [Microsoft Edge](https://www.microsoft.com/en-us/edge).

## Features

- Write your resume in Markdown and preview it in real-time, it's smooth!
- It works offline ([PWA](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps))
- Export to A4 and US Letter size PDFs
- Customize page margins, theme colors, line heights, fonts, etc.
- Pick any fonts from [Google Fonts](https://fonts.google.com/)
- Add icons easily via [Iconify](https://github.com/iconify/iconify) (search for icons on [Icônes](https://icones.js.org/))
- Tex support ([KaTeX](https://github.com/KaTeX/KaTeX))
- Cross-reference (would be useful for an academic CV)
- Case correction (e.g. `Github` -> `GitHub`)
- Add line breaks (`\[10px]`) or start a new page (`
ewpage`) just like in LaTeX
- Break pages automatically
- Customize CSS
- Manage multiple resumes
- Your data in your hands:
  - Data are saved locally within your browser, see [here](https://localforage.github.io/localForage/) for details
  - Open-source static website hosted on [Github Pages](https://pages.github.com/), which doesn't (have the ability to) collect your data
  - No user tracking, no ads
- Dark mode

## Development

It's built on [Nuxt 3](https://nuxt.com), with the power of [Vue 3](https://github.com/vuejs/vue-next), [Vite](https://github.com/vitejs/vite), [Zag](https://zagjs.com/), and [UnoCSS](https://github.com/antfu/unocss).

### Setup

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/junian/markdown-resume.git
    cd markdown-resume
    ```

2.  **Install dependencies:**
    ```bash
    pnpm install
    ```

3.  **Build internal packages:**
    ```bash
    pnpm build:pkg
    ```

### Running the Development Server

```bash
pnpm dev
```
The application will be available at `http://localhost:3000`.

### Google Fonts Configuration

By default, a curated list of popular Google Fonts is available. To access the full Google Fonts library:

1.  **Generate a Google Fonts Developer API Key:**
    Obtain your API key from the [Google Fonts Developer API](https://developers.google.com/fonts/docs/developer_api#APIKey).

2.  **Create a `.env` file:**
    In the `site/` directory, create a file named `.env` (if it doesn't already exist).

3.  **Add your API key:**
    Add the following line to the `.env` file, replacing `"YOUR_API_KEY"` with your actual key:
    ```
    NUXT_PUBLIC_GOOGLE_FONTS_KEY="YOUR_API_KEY"
    ```

### Building for Production

```bash
pnpm build
```

## Changes Made

This section summarizes the key changes and improvements made to the project:

*   **Enhanced Google Fonts Integration:**
    *   Implemented a fallback mechanism for Google Fonts. If no API key is provided, a curated list of popular fonts (Roboto, Open Sans, Lato, Montserrat, Ubuntu) is now available by default.
    *   The `gfonts-loader` package was modified to support this fallback.
    *   The `site/src/utils/font.ts` file was updated to correctly handle the API key and fallback logic.
    *   The `packages/gfonts-loader/src/popular-fonts.ts` file was created to store the predefined list of fonts.
    *   The `README.md` has been updated to reflect these changes and provide clear instructions on how to configure the Google Fonts API key for full access.

## Credits

- The original work: [Renovamen/oh-my-cv](https://github.com/Renovamen/oh-my-cv)
- [billryan/resume](https://github.com/billryan/resume)

## License

This project is licensed under [MIT](LICENSE) license.

---

Made with ☕ by [Junian.dev](https://www.junian.dev).
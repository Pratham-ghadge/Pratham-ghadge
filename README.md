<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Fira+Code&size=25&pause=1000&color=00C2FF&width=435&lines=Hi+%F0%9F%91%8B%2C+I'm+Prathamesh+Ghadge;Full-Stack+Developer+%F0%9F%92%BB;Software+Engineer+%F0%9F%93%8C;IoT+and+Web+Enthusiast+%F0%9F%9A%80" alt="Typing SVG" />
</p>

<p align="center">
  <img src="https://i.imgur.com/3ZyWcQz.gif" alt="Banner GIF" width="100%" />
</p>

---

<h3 align="center">A passionate Full Stack Developer and Software Engineer from India 🇮🇳</h3>

- 🌱 I’m currently learning **Redux Toolkit, Next.js, Django**
- 👨‍💻 All of my projects are available at: [Portfolio](https://pratham-ghadge-portfolio.vercel.app)
- 📫 Reach me at: **prathamtech24@gmail.com**

---

<h3 align="left">🔗 Connect with me:</h3>
<p align="left">
  <a href="https://linkedin.com/in/prath1m" target="blank">
    <img align="center" src="https://skillicons.dev/icons?i=linkedin" alt="LinkedIn" />
  </a>
  <a href="https://instagram.com/prath1m.in" target="blank">
    <img align="center" src="https://skillicons.dev/icons?i=instagram" alt="Instagram" />
  </a>
</p>

---

<h3 align="left">🛠 Languages and Tools:</h3>
<p align="left">
  <img src="https://skillicons.dev/icons?i=html,css,js,react,nodejs,express,mongodb,mysql,python,java,c,cpp,postman,bootstrap,tailwind,vue,git,vscode" />
</p>

---

<h3 align="left">📊 GitHub Stats:</h3>
<p align="left">
  <img width="48%" src="https://github-readme-stats.vercel.app/api?username=pratham-ghadge&show_icons=true&theme=radical" />
  <img width="48%" src="https://github-readme-streak-stats.herokuapp.com/?user=pratham-ghadge&theme=radical" />
</p>
<p align="center">
  <img src="https://github-readme-activity-graph.vercel.app/graph?username=pratham-ghadge&theme=react-dark" />
</p>

---
# snk

[![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/platane/platane/main.yml?label=action&style=flat-square)](https://github.com/Platane/Platane/actions/workflows/main.yml)
[![GitHub release](https://img.shields.io/github/release/platane/snk.svg?style=flat-square)](https://github.com/platane/snk/releases/latest)
[![GitHub marketplace](https://img.shields.io/badge/marketplace-snake-blue?logo=github&style=flat-square)](https://github.com/marketplace/actions/generate-snake-game-from-github-contribution-grid)
![type definitions](https://img.shields.io/npm/types/typescript?style=flat-square)
![code style](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square)

Generates a snake game from a github user contributions graph

<picture>
  <source
    media="(prefers-color-scheme: dark)"
    srcset="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake-dark.svg"
  />
  <source
    media="(prefers-color-scheme: light)"
    srcset="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake.svg"
  />
  <img
    alt="github contribution grid snake animation"
    src="https://raw.githubusercontent.com/platane/snk/output/github-contribution-grid-snake.svg"
  />
</picture>

Pull a github user's contribution graph.
Make it a snake Game, generate a snake path where the cells get eaten in an orderly fashion.

Generate a [gif](https://github.com/Platane/snk/raw/output/github-contribution-grid-snake.gif) or [svg](https://github.com/Platane/snk/raw/output/github-contribution-grid-snake.svg) image.

Available as github action. It can automatically generate a new image each day. Which makes for great [github profile readme](https://docs.github.com/en/free-pro-team@latest/github/setting-up-and-managing-your-github-profile/managing-your-profile-readme)

## Usage

**github action**

```yaml
- uses: Platane/snk@v3
  with:
    # github user name to read the contribution graph from (**required**)
    # using action context var `github.repository_owner` or specified user
    github_user_name: ${{ github.repository_owner }}

    # list of files to generate.
    # one file per line. Each output can be customized with options as query string.
    #
    #  supported options:
    #  - palette:     A preset of color, one of [github, github-dark, github-light]
    #  - color_snake: Color of the snake
    #  - color_dots:  Coma separated list of dots color.
    #                 The first one is 0 contribution, then it goes from the low contribution to the highest.
    #                 Exactly 5 colors are expected.
    outputs: |
      dist/github-snake.svg
      dist/github-snake-dark.svg?palette=github-dark
      dist/ocean.gif?color_snake=orange&color_dots=#bfd6f6,#8dbdff,#64a1f4,#4b91f1,#3c7dd9
```

[example with cron job](https://github.com/Platane/Platane/blob/master/.github/workflows/main.yml#L26-L33)

If you are only interested in generating a svg, consider using this faster action: `uses: Platane/snk/svg-only@v3`

**dark mode**

For **dark mode** support on github, use this [special syntax](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax#specifying-the-theme-an-image-is-shown-to) in your readme.

```html
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="github-snake-dark.svg" />
  <source media="(prefers-color-scheme: light)" srcset="github-snake.svg" />
  <img alt="github-snake" src="github-snake.svg" />
</picture>
```

**interactive demo**

<a href="https://platane.github.io/snk">
  <img height="300px" src="https://user-images.githubusercontent.com/1659820/121798244-7c86d700-cc25-11eb-8c1c-b8e65556ac0d.gif" ></img>
</a>

[platane.github.io/snk](https://platane.github.io/snk)

**local**

```
npm install

npm run dev:demo
```

## Implementation

[solver algorithm](./packages/solver/README.md)


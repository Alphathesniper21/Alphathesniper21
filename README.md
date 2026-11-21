<h1 data-importer="text" align="center">Hey 👋What's Up?</h1>

###

<div data-importer="techs" align="center">
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/java/java-original.svg" height="60" alt="java logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/python/python-original.svg" height="60" alt="python logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/linux/linux-original.svg" height="60" alt="linux logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="60" alt="html5 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" height="60" alt="css logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/spring/spring-original.svg" height="60" alt="spring logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/mysql/mysql-original.svg" height="60" alt="mysql logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/typescript/typescript-original.svg" height="60" alt="typescript logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/webstorm/webstorm-original.svg" height="60" alt="webstorm logo"  />
</div>

name: Generate stats card

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"

  workflow_dispatch:

  push:
    branches:
    - main

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5

    steps:
      - name: generate stats.svg
        uses: readme-tools/github-readme-stats-action@v1
        with:
          card: stats
          options: username=${{ github.repository_owner }}&hide_title=false&hide_rank=false&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=codeSTACKr&locale=en&hide_border=false
          path: dist/stats.svg
          token: ${{ secrets.GITHUB_TOKEN }}


      - name: push stats.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: stats-output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

###

<div data-importer="socials" align="center">
  <img src="https://img.shields.io/static/v1?message=Discord&logo=discord&label=&color=7289DA&logoColor=white&labelColor=&style=for-the-badge" height="25" alt="discord logo"  />
  <img src="https://img.shields.io/static/v1?message=Telegram&logo=telegram&label=&color=2CA5E0&logoColor=white&labelColor=&style=for-the-badge" height="25" alt="telegram logo"  />
  <img src="https://img.shields.io/static/v1?message=Gmail&logo=gmail&label=&color=D14836&logoColor=white&labelColor=&style=for-the-badge" height="25" alt="gmail logo"  />
</div>

###

<div data-importer="stats" align="center">
  <img src="https://raw.githubusercontent.com/Alphathesniper21/Alphathesniper21/stats-output/stats.svg?hide_title=false&hide_rank=false&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=codeSTACKr&locale=en&hide_border=false&order=1" height="150" alt="stats graph"  />
  <img src="https://raw.githubusercontent.com/Alphathesniper21/Alphathesniper21/languages-output/languages.svg?locale=en&hide_title=false&layout=compact&card_width=320&langs_count=5&theme=codeSTACKr&hide_border=false&order=2" height="150" alt="languages graph"  />
  <img src="https://raw.githubusercontent.com/Alphathesniper21/Alphathesniper21/activity-graph-output/activity-graph.svg?radius=16&theme=react&area=true&order=5" height="300" alt="activity-graph graph"  />
</div>

###

<picture data-importer="pacman">
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Alphathesniper21/Alphathesniper21/pacman-output/pacman-contribution-graph-dark.svg?game=pacman">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Alphathesniper21/Alphathesniper21/pacman-output/pacman-contribution-graph.svg?game=pacman">
  <img alt="pacman contribution graph" src="https://raw.githubusercontent.com/Alphathesniper21/Alphathesniper21/pacman-output/pacman-contribution-graph.svg?game=pacman">
</picture>

###

## Olá✌


Meu nome é Lucas e sou Desenvolvedor Full-Stack em formação!!!

[![Anurag's GitHub stats](https://github-readme-stats.vercel.app/api?username=lucassoaresjs&show_icons=true&theme=synthwave)](https://github.com/lucassoaresjs/github-readme-stats)
name: Generate Datas

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"
  workflow_dispatch:

jobs:
  build:
    name: Jobs to update datas
    runs-on: ubuntu-latest
    steps:
      # Snake Animation (https://github.com/lucassoaresjs)
      - uses: Platane/snk@master
        id: snake-gif
        with:
          github_user_name: lucassoaresjs
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

- 🖌 Oi, me chamo Lucas!
- 💻 Desenvolvedor Full-Stack em formação
- 😄 Pronomes: Ele/Dele


-  [![Ashutosh's github activity graph](https://github-readme-activity-graph.vercel.app/graph?username=lucassoaresjs&bg_color=301b50&color=999999&line=9e4c98&point=d2d0d0&area=true&hide_border=true)](https://github.com/ashutosh00710/github-readme-activity-graph)
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
      # Snake Animation
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
  

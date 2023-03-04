## Faaaala dev, Milim Aqui!

<div>
  
  <img  height="180em" src="https://github-readme-stats.vercel.app/api?username=Alexandre-Milim&show_icons=true&theme=great-gatsby&include_all_commits=true&count_private=true"/>
  <img align="right" height="180em" src="https://github-readme-stats.vercel.app/api/top-langs/?username=Alexandre-Milim&layout=compact&langs_count=16&theme=great-gatsby"/>
</div>
<br>

<div  align="center"> 
  <div style="display: inline_block"><br>
    <img align="left" height="250" alt="coding-time" src="code.gif">
    <h1 align="center">linguagens Estudadas </h1>
    <img align="center" height="30" width="40" alt="html-icon" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/html5/html5-original.svg">
    <img align="center" height="30" width="40" alt="css-icon" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/css3/css3-original.svg">
    <img align="center" height="30" width="40" alt="nodejs-icon" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/php/php-original.svg">
    <img align="center" height="30" width="40" alt="nodejs-icon" src="https://raw.githubusercontent.com/jmnote/z-icons/master/svg/cpp.svg">
   </div>
    
  
  <h1 align="center">Redes Sociais</h1>
    <a href = "https://mail.google.com/mail/u/0/#search/alexandremilim15%40gmail.com?compose=new">
      <img width="30" src="https://github.com/LuigiGf/LuigiGf/raw/main/gmail.svg">
    </a>
    <a href = "https://www.instagram.com/milim.batman/">
      <img width="25" src="https://github.com/LuigiGf/LuigiGf/raw/main/instagram.png">
    </a>
</div>
  
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
          github_user_name: {{Alexandre-Milim}}
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}


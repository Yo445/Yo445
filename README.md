<div id="" align="center">
<a href ="https://github.com/user-attachments/assets/0a86f873-1eea-4245-93ca-103cbbdf9380" target="_blank"></a>
</div>
<h1 align="center">Hi 👋, I'm Yosef Ali </h1>
<h3 align="center">A frontend developer</h3>
<h4 align="center">Hi my name is Yosef Ali  a creative and innovative developer with expertise in Frontend React.js and making UI/UX Design sketches, making too a Motion Graphics and create amazing things with illustrature. doing some Games, having teamwork and collaporative, with a passion for Visual Arts. Seeking opportunities to collaborate on dynamic projects.</h4>

<hr>


<!-- TECHS -->

<h2 align="center">Skills</h2>

<div align="center">
                <br>
                    <div align="center" >  

  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/c/c-original.svg" height="40" alt="c logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg" height="40" alt="html5 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg" height="40" alt="css3 logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg" height="40" alt="javascript logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/bootstrap/bootstrap-original.svg" height="40" alt="bootstrap logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/react/react-original.svg" height="40" alt="react logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/git/git-original.svg" height="40" alt="git logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/illustrator/illustrator-plain.svg" height="40" alt="illustrator logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/aftereffects/aftereffects-original.svg" height="40" alt="aftereffects logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/unity/unity-original.svg" height="40" alt="unity logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/blender/blender-original.svg" height="40" alt="blender logo"  />
</div>
</div>

<br />
<br />
<hr>


<!-- SOCIALS -->

<h2 align="center">Contact Me</h2>
<p align="center">
  <a href="https://www.linkedin.com/in/youssef-ali-840227217/" target="_blank">
    <img src="https://raw.githubusercontent.com/maurodesouza/profile-readme-generator/master/src/assets/icons/social/linkedin/default.svg" width="52" height="40" alt="linkedin logo"  />
  </a>
</p>

<hr>


<!-- STATS -->
<div align="center" margin="100px 0 0 0">

<h2 align="center">Stats</h2>
<h6 style="color:red">These stats are only for public repos it don't show private stats on projects for previous employers and clients.</h6>
<div align="center">
  <img src="https://github-readme-stats.vercel.app/api?username=Yo445&hide_title=false&hide_rank=false&show_icons=true&include_all_commits=true&count_private=true&disable_animations=false&theme=dracula&locale=en&hide_border=false&order=1" height="150" alt="stats graph"  />
  <img src="https://github-readme-stats.vercel.app/api/top-langs?username=Yo445&locale=en&hide_title=false&layout=compact&card_width=320&langs_count=5&theme=dracula&hide_border=false&order=2" height="150" alt="languages graph"  />
</div>
</div>
<br />
<br />
<hr>
name: Generate snake animation

on:
  schedule: # execute every 12 hours
    - cron: "* */12 * * *"

  workflow_dispatch:

  push:
    branches:
    - master

jobs:
  generate:
    permissions:
      contents: write
    runs-on: ubuntu-latest
    timeout-minutes: 5

    steps:
      - name: generate snake.svg
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: dist/snake.svg?palette=github-dark


      - name: push snake.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
<img src="https://raw.githubusercontent.com/Yo445/Yo445/output/snake.svg" alt="Snake animation" />

<br />

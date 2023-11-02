[![Typing SVG](https://readme-typing-svg.demolab.com/?lines=Hello+I'm+Freskkie+Encarnacion,+19;Saint+Louis+University,+Baguio;Information+Technology+Student)](https://git.io/typing-svg)
- 🌱 I’m currently learning Java programming 
- ⚡ Fun fact: Didn't expect myself to be a programmer ツ

### ✯ Reach me 
<a href="mailto: fresenc112233@gmail.com">
<img src="https://img.shields.io/badge/-fresenc112233%40gmail.com-7B83EB?&style=for-the-badge&logo=Microsoft-outlook&logoColor=white" ></a>  <a  href="https://www.instagram.com/freskkie.e/">   <img src="https://img.shields.io/badge/@freskkie.e-%23E4405F.svg?&style=for-the-badge&logo=instagram&logoColor=white"></a>  <a href="https://www.linkedin.com/in/freskkie-encarnacion-31429024a/"><img src="https://img.shields.io/badge/freskkie encarnacion-%230077B5.svg?&style=for-the-badge&logo=linkedin&logoColor=white" ></a> 

### ✯ My Highlights
<a href="">
  <img align="center" src="https://github-readme-stats.vercel.app/api/top-langs/?username=PEEACHYBEE&langs_count=8&layout=compact&theme=material-palenight&hide=html,Tcl" />
</a>
<a href="">
  <img align="center" src="https://github-readme-streak-stats.herokuapp.com/?user=PEEACHYBEE&theme=material-palenight"/>
</a>

name: WakaTime status update

on:
  schedule:
    # Runs at 12 am  '0 0 * * *'  UTC
    - cron: "1 0 * * *"

jobs:
  update-readme:
    name: Update the WakaTime Stat
    runs-on: ubuntu-latest
    steps:
      # Use avinal/Profile-Readme-WakaTime@<latest-release-tag> for latest stable release
      # Do not change the line below until you have forked this repository
      # If you have forked this project you can use <username>/Profile-Readme-WakaTime@master instead
      - uses: avinal/Profile-Readme-WakaTime@master
        with:
          # WakaTime API key stored in secrets, do not directly paste it here
          WAKATIME_API_KEY: ${{ secrets.WAKATIME_API_KEY }}
          # Automatic github token
          GITHUB_TOKEN: ${{ github.token }}
          # Branch - newer GitHub repositories have "main" as default branch, change to main in that case, default is master
          BRANCH: "master"
          # Manual Commit messages - write your own messages here
          COMMIT_MSG: "Automated Coding Activity Update :alien:"
          # Range of fetching data - default is "last_7_days". See https://wakatime.com/developers#stats for more options
          STATS_RANGE: "last_7_days"

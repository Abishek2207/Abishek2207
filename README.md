<div align="center">

# Hi 👋, I'm Abishek R

### AI/ML Student | Aspiring AI Engineer | Developer

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=700&size=26&pause=1000&center=true&vCenter=true&width=750&lines=AI%2FML+Developer;Building+Real+World+AI+Projects;Future+AI+Engineer;Learning+DSA+%2B+Machine+Learning" alt="Typing SVG" />

</div>

---

## 🚀 About Me

- 🎓 B.Tech Artificial Intelligence & Machine Learning student  
- 🤖 Passionate about AI, ML, Deep Learning and Generative AI  
- 🧠 Learning DSA, Python, ML and AI Agents  
- 🏆 Hackathon enthusiast  
- 💡 Building real-world AI projects  

---

## 🛠️ Tech Stack

<p align="center">
  <img src="https://skillicons.dev/icons?i=python,c,cpp,html,css,js,react,git,github,vscode,mysql" />
</p>

---

name: Generate Snake Animation

on:
  schedule:
    - cron: "0 0 * * *"
  workflow_dispatch:

jobs:
  generate:
    runs-on: ubuntu-latest

    steps:
      - name: Generate snake
        uses: Platane/snk/svg-only@v3
        with:
          github_user_name: abishekramamoorthy22
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      - name: Push snake to output branch
        uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

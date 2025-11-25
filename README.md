## Olá! Sou o Pedro Luiz 👋

Desenvolvedor dedicado e em constante aprendizado, focado em entregar o meu melhor em cada projeto e tarefa.

### 🎓 Trajetória Profissional e Acadêmica
 **Formação:** Concluí o Ensino Médio em 2025 e atualmente estou aprofundando meus conhecimentos em tecnologia através da especialização de **2 anos em Desenvolvimento de Sistemas na WEG**. <br>
 **Foco:** Dedicado a construir soluções robustas e escaláveis.

### 💻 Planos Futuros
🔭 **Atualmente:** Focado em aprimorar e consolidar minhas habilidades em *Java.* <br>
🌱 **Em breve:** Planejo mergulhar e dominar *JavaScript* e *Python.* <br>
🛠️ **Linguagens e Ferramentas:** <br>
![Java](https://img.shields.io/badge/Java-007396?style=for-the-badge&logo=java&logoColor=white)

### ⚡ Curiosidades
Fato Curioso: Embora meu trabalho seja no mundo digital (IT), eu adoro me manter ativo, no meu tempo livre gosto muito de praticar esportes como surfe e futebol.

### 📫 Entre em Contato
Instagram: `[pe.deandrade]` 

<div align="center">
  
 
  <br>
  <img align="center" alt="Top Language" src="http://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=pedroluizb&theme=ayu_mirage"/>
</div>
  
###

<div align="center">
  <img src="https://skillicons.dev/icons?i=ts" height="60" alt="typescript logo"  />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=nextjs" height="60" alt="nextjs logo"  />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=tailwind" height="60" alt="tailwindcss logo"  />
  <img width="12" />
  <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/storybook/storybook-original.svg" height="60" alt="storybook logo"  />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=graphql" height="60" alt="graphql logo"  />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=go" height="60" alt="go logo"  />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=rust" height="60" alt="rust logo"  />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=nestjs" height="60" alt="nestjs logo"  />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=py" height="60" alt="python logo"  />
  <img width="12" />
  <img src="https://skillicons.dev/icons?i=aws" height="60" alt="amazonwebservices logo"  />
</div>

###

<div align="center">
  <img src="https://img.shields.io/static/v1?message=LinkedIn&logo=linkedin&label=&color=0077B5&logoColor=white&labelColor=&style=for-the-badge" height="25" alt="linkedin logo"  />
  <img src="https://img.shields.io/static/v1?message=Twitter&logo=twitter&label=&color=1DA1F2&logoColor=white&labelColor=&style=for-the-badge" height="25" alt="twitter logo"  />
  <img src="https://img.shields.io/static/v1?message=Discord&logo=discord&label=&color=7289DA&logoColor=white&labelColor=&style=for-the-badge" height="25" alt="discord logo"  />
  <img src="https://img.shields.io/static/v1?message=Twitch&logo=twitch&label=&color=9146FF&logoColor=white&labelColor=&style=for-the-badge" height="25" alt="twitch logo"  />
  <img src="https://img.shields.io/static/v1?message=dev.to&logo=dev.to&label=&color=0A0A0A&logoColor=white&labelColor=&style=for-the-badge" height="25" alt="devto logo"  />
</div>

###

<div align="center">
  <img src="https://streak-stats.demolab.com?user=maurodesouza&locale=en&mode=daily&theme=dracula&hide_border=false&border_radius=5&order=3" height="150" alt="streak graph"  />
  <img src="https://github-profile-trophy.vercel.app?username=maurodesouza&theme=dracula&column=-1&row=1&margin-w=8&margin-h=8&no-bg=false&no-frame=false&order=4" height="150" alt="trophy graph"  />
</div>

###

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/maurodesouza/maurodesouza/output/pacman-contribution-graph-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/maurodesouza/maurodesouza/output/pacman-contribution-graph.svg">
  <img alt="pacman contribution graph" src="https://raw.githubusercontent.com/maurodesouza/maurodesouza/output/pacman-contribution-graph.svg">
</picture>

###

name: Generate pacman animation

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
      - name: generate pacman-contribution-graph.svg
        uses: abozanona/pacman-contribution-graph@main
        with:
          github_user_name: ${{ github.repository_owner }}


      - name: push pacman-contribution-graph.svg to the output branch
        uses: crazy-max/ghaction-github-pages@v3.1.0
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}

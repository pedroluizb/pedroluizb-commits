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
          github_user_name: pedroluizb
          svg_out_path: dist/github-contribution-grid-snake.svg

      - uses: crazy-max/ghaction-github-pages@v2.1.3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  


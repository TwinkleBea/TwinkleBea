## 💗​💗​



    steps:
      # Baixa o código do repositório
      - uses: actions/checkout@v4

      # Gera a animação da cobrinha com base no histórico de contribuições
      - uses: Platane/snk@v3
        id: snake-gif
        with:
          github_user_name: ${{ github.repository_owner }}
          outputs: |
            dist/github-contribution-grid-snake.svg
            dist/github-contribution-grid-snake-dark.svg?palette=github-dark

      # Publica os arquivos gerados na branch "output"
      - uses: crazy-max/ghaction-github-pages@v4
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}



![snake gif](https://raw.githubusercontent.com/TwinkleBea/TwinkleBea/output/github-contribution-grid-snake.svg)

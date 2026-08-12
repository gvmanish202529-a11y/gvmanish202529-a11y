![GitHub Stars](https://img.shields.io/github/stars/gvmanish202529-a11y?label=Stars&style=for-the-badge&color=6e40c9&labelColor=0d1117)
</div>
<br>
<!-- FOOTER WAVE -->
<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:6e40c9,50:161b22,100:0d1117&height=120&section=footer" />
<!-- ═══════════════════════════════════════════════════════════════════════ -->
<!-- 📌 BONUS: Snake Animation Setup                                       -->
<!-- ═══════════════════════════════════════════════════════════════════════ -->
---
<details>
<summary><h3>🐍 Bonus: Snake Animation Setup</h3></summary>
To enable the snake contribution animation, create a file at `.github/workflows/snake.yml` in your profile repository (`gvmanish202529-a11y/gvmanish202529-a11y`) with this content:
```yaml
name: Generate Snake
on:
  schedule:
    - cron: "0 */12 * * *"
  workflow_dispatch:
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: Platane/snk@v3
        with:
          github_user_name: gvmanish202529-a11y
          outputs: |
            dist/github-snake.svg
            dist/github-snake-dark.svg?palette=github-dark
      - uses: crazy-max/ghaction-github-pages@v3
        with:
          target_branch: output
          build_dir: dist
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```
Then run the workflow manually once from the **Actions** tab.
</details>

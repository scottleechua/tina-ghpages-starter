# Tina GitHub Pages Starter
A starter template for using TinaCMS with [GitHub Pages](https://docs.github.com/en/pages/quickstart) (using Jekyll).

## Using this starter
1. Select Use this template > Create a new repository.
    - Name the repo `<YOUR-GITHUB-USERNAME>.github.io`.
    - Select Include all branches.
2. Wait for `gh-pages` to initialize.
    - Go to Settings > Pages and copy the site URL.
3. Log in to [Tina](https://app.tina.io).
    - Select New Project > Import your Site.
    - Authenticate with GitHub and select your project repo.
    - Under "Site URL(s)", enter your GitHub Pages site URL.
    - Note the Client ID.
4. Select Tokens > New Token.
    - Name the token.
    - Under Git Branches, enter `main`.
    - Create Token. Note the Token string.
5. Back on GitHub, go to Settings > Secrets and variables > Actions > new repository secret. Do this twice:
    - Name: `CLIENT_ID`, and paste the Client ID.
    - Name: `READ_TOKEN`, and paste the Token string.
6. In your code, navigate to `.github/workflows/deploy.yml`. Delete the `#` from line 7 to uncomment it. Commit changes.
7. Your site should start recompiling: first on `main`, then on `gh-pages`.
8. Once complete, navigate to `https://<YOUR SITE URL>/admin` to find your TinaCMS dashboard.

## Known Issues
- Doesn't work with [project sites](https://docs.github.com/en/pages/getting-started-with-github-pages/about-github-pages), only user sites.

## Acknowledgements
- Starter template by [Scott Lee Chua](https://scottleechua.com).
- Many thanks to Huw Fulcher for their blog post ["How to integrate TinaCMS with Jekyll"](https://huwfulcher.com/blog/2022/how-to-integrate-tinacms-with-jekyll/), without which this template would not exist.
- Thanks to Parker Moore and the contributors to [Minima](https://github.com/jekyll/minima), the Jekyll default theme.

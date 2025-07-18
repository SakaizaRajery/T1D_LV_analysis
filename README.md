<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->
<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://github.com/github_username/repo_name">
    <img src="images/logo.png" alt="Logo" width="80" height="80">
  </a>

<h2 align="center"> T1D_LV_analysis</h2>

  <p align="center">
    The goal of this project is to gain a better understanding of T1D, and the heterogeneity of T1D progression from the perspective of gene modules. 
</div>

<!-- TABLE OF CONTENTS -->
<details>
  <summary>Table of Contents</summary>
  <ol>
    <li>
      <a href="#about-the-project">About The Project</a>
    </li>
    <li><a href="#roadmap">Roadmap</a></li>
        <li>
      <a href="#How-to-reproduce-this-project">How to reproduce this project</a>

    </li>
  </ol>
</details>


<!-- ABOUT THE PROJECT -->
## About The Project

  <p align="left">
T1D is an autoimmune disease that progresses through three stages. The earliest phase, preceding stage 1, is known as Islet Autoimmunity (IA), when at least one of the four autoantibodies associated with beta-cell damage is detected. The time it takes to progress from IA to symptomatic T1D varies greatly between individuals. Exploring the genetic underlying of T1D constitues an important step in understanding the mechanism at play at each stage above. However not only does T1D involve a mix of genetic and environmental factors, but its genetic component is also highly complex due to its pleiotropic nature. Therefore, we use Phenoplier to understand how genes work together throughout the disease progression. Phenoplier uses large public data to create latent variables representing genes that are co-expressed in various diseases, conditions, or cell type. In the first part of this project, we use Phenoplier to identify gene modules involved in T1D. 

  </p>

<!-- ROADMAP -->
## Roadmap

| File Name (code)           | Description  |
|:-------------:|:-----|
|   [LV_analysis_R.rmd](https://sakaizarajery.github.io/T1D_LV_analysis/) |Identification of Latent Variables (LV) associated with T1D|


## How to reproduce this project
1. Download the R project folder
2. Run the Rmd file in R studio 

<!-- REPOSITORY -->

<h2 align="center"> About the repository</h2>

This repository contains starter configurations for the conventional commit messages as described [here](https://www.conventionalcommits.org/en/v1.0.0/), as well as linter configurations for Python and R.

## How this repository was created
Init repository:
```bash
git init
```

Install Node.js:
    
```bash
# installs nvm (Node Version Manager)
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.1/install.sh | bash
# download and install Node.js (you may need to restart the terminal)
nvm install 22
# verifies the right Node.js version is in the environment
node -v # should print `v22.12.0`
# verifies the right npm version is in the environment
npm -v # should print `10.9.0`
```

Install pnpm:

```bash
npm install -g pnpm
```

Install and Init Husky:
```bash
pnpm add --save-dev husky
pnpm exec husky init
```

Install Commitlint CLI and the conventional configuration as development dependencies:
```bash
pnpm add -D @commitlint/config-conventional @commitlint/cli
# extend the Commitlint conventional configuration
echo "export default { extends: ['@commitlint/config-conventional'] };" > commitlint.config.js
```

create a commit-msg file in the .husky folder to add commit message linting to commit-msg hook.
```bash
echo "pnpm dlx commitlint --edit $1" > .husky/commit-msg
# Remove the pre-commit hook created by Husky on initialization
rm .husky/pre-commit
```


## How to use this repository
You'll need to install both Node.js and pnpm to utilize the commit rules configured for this repo.

If you have not, refer to this [link](https://nodejs.org/en/download/package-manager) to install Node.js and this [link](https://pnpm.io/installation) to install pnpm.

Then, run this command at the root of the repository to install the required packages:

```bash
pnpm install
```

Now you can try edit a file and commit it with a unconventional commit message.

```bash
echo "A Random Sentence" >> README.md
git add README.md
git commit -m "A Random Commit Message"
```

You'll see a warning message and the commit will be rejected:

```bash
⧗   input: A Random Commit Message
✖   subject may not be empty [subject-empty]
✖   type may not be empty [type-empty]

✖   found 2 problems, 0 warnings
ⓘ   Get help: https://github.com/conventional-changelog/commitlint/#what-is-commitlint

husky - commit-msg script failed (code 1)
```

You can use an interactive CLI to help you get familiar with the convention by running `pnpm run commit`.

# Website

This website is built using [Docusaurus](https://docusaurus.io/), a modern static website generator.

## Installation

```bash
yarn
```

## Local Development

```bash
yarn start
```

This command starts a local development server and opens up a browser window. Most changes are reflected live without having to restart the server.

## Build

```bash
yarn build
```

This command generates static content into the `build` directory and can be served using any static contents hosting service.

## Deployment

Using SSH:

```bash
USE_SSH=true yarn deploy
```

Not using SSH:

```bash
GIT_USER=<Your GitHub username> yarn deploy
```

If you are using GitHub pages for hosting, this command is a convenient way to build the website and push to the `gh-pages` branch.

## 1. Create Docusaurus project locally

Open terminal:

```
npx create-docusaurus@latest oscp-wiki classic
```

Then:

```
cd oscp-wikinpm installnpm run start
```

It will open local wiki at:

```
http://localhost:3000
```

You now have a full wiki structure.

Run:

```
npx create-docusaurus@latest oscp-wiki classic
cd oscp...
npm install
npm run start
```

## 2. Replace with your GitHub repo

Inside project folder:

```
git initgit remote add origin https://github.com/YOUR_GITHUB/oscp.git
```

Then:

```
git add .git commit -m "Initial OSCP wiki"git push -u origin main
```

Now GitHub repo will contain:

```
docs/blog/src/docusaurus.config.jssidebars.js
```

## 3. Add your notes

Put markdown files inside:

```
docs/
```

Example:

```
docs/linux-privesc.md
docs/ad-attacks.md
docs/buffer-overflow.md
```

Example markdown:

```
# Linux Privilege Escalation
## LinPEAS
```bash./linpeas.sh
```

```
---
## 4. Sidebar navigation
Edit:```text
sidebars.js
```

Example:

```
module.exports = {
  tutorialSidebar: [
    'intro',
    'linux-privesc',
    'ad-attacks',
    'buffer-overflow',
  ],
};
```

## 5. Redeploy on Vercel

Vercel auto-detects GitHub updates.

Just push:

```
git push
```

Then your site updates automatically.

---

## 6. Recommended OSCP structure

```
docs/
├── enumeration/
├── linux/
├── windows/
├── active-directory/
├── web/
├── pivoting/
├── buffer-overflow/
├── privilege-escalation/
├── cheatsheets/
└── tools/
```

## 7. Add search (very useful)

Install local search:

```
npm install @easyops-cn/docusaurus-search-local
```

Then edit:

```

```

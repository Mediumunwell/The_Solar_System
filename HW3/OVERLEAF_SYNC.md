# HW3 Overleaf Sync

This folder is now an Overleaf-ready LaTeX project.

## Compile locally

```bash
cd /home/mediumunwell/The_Solar_System/HW3
/home/mediumunwell/.local/bin/tectonic main.tex
```

## Clone from Overleaf into this folder

```bash
TOKEN=$(cat /home/mediumunwell/.local/ai_memory/credentials/overleaf_token.txt)
PROJECT_ID="REPLACE_WITH_HW3_PROJECT_ID"

cd /tmp
rm -rf overleaf_hw3
git clone "https://git:${TOKEN}@git.overleaf.com/${PROJECT_ID}" overleaf_hw3

rsync -av --delete /tmp/overleaf_hw3/ /home/mediumunwell/The_Solar_System/HW3/
```

## Push this folder to Overleaf

```bash
TOKEN=$(cat /home/mediumunwell/.local/ai_memory/credentials/overleaf_token.txt)
PROJECT_ID="REPLACE_WITH_HW3_PROJECT_ID"

cd /home/mediumunwell/The_Solar_System/HW3
git init
git add .
git commit -m "feat: add hw3 latex project"
git remote add origin "https://git:${TOKEN}@git.overleaf.com/${PROJECT_ID}"
git push -u origin master
```

If your Overleaf repo branch is `main` instead of `master`, push with:

```bash
git push -u origin main
```
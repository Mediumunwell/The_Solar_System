# Overleaf Sync Guide (All HW Folders)

Use this single guide for any homework folder (`HW1`, `HW2`, `HW3`, ...).

## Variables

```bash
TOKEN=$(cat /home/mediumunwell/.local/ai_memory/credentials/overleaf_token.txt)
HW_FOLDER="HW3"                    # change to HW1/HW2/HW4/etc
PROJECT_ID="REPLACE_WITH_PROJECT_ID"
```

## Clone from Overleaf into a homework folder

```bash
cd /tmp
rm -rf "overleaf_${HW_FOLDER,,}"
git clone "https://git:${TOKEN}@git.overleaf.com/${PROJECT_ID}" "overleaf_${HW_FOLDER,,}"

rsync -av --delete --exclude '.git/' \
	"/tmp/overleaf_${HW_FOLDER,,}/" \
	"/home/mediumunwell/The_Solar_System/${HW_FOLDER}/"
```

## Push a homework folder to Overleaf

```bash
cd /tmp
rm -rf "overleaf_${HW_FOLDER,,}"
git clone "https://git:${TOKEN}@git.overleaf.com/${PROJECT_ID}" "overleaf_${HW_FOLDER,,}"

rsync -av --delete --exclude '.git/' \
	"/home/mediumunwell/The_Solar_System/${HW_FOLDER}/" \
	"/tmp/overleaf_${HW_FOLDER,,}/"

cd "/tmp/overleaf_${HW_FOLDER,,}"
git add -A
git commit -m "sync ${HW_FOLDER} from local repo" || true
git push origin master
```

If that project uses `main` instead of `master`, push with:

```bash
git push origin main
```
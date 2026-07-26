# GitHub profile README setup

Your profile README lives in the special public repo **[preshan/preshan](https://github.com/preshan/preshan)**.

It already renders on the **repo** page. If it does **not** appear on your Overview ([github.com/preshan](https://github.com/preshan)), GitHub has not linked it to your profile yet.

## Fix (do this while logged in as `preshan`)

### Option A — Share to profile (try first)

1. Open https://github.com/preshan/preshan
2. On the repo overview, look above the README (right side) for a **Share to profile** button
3. Click it
4. Hard-refresh https://github.com/preshan (or open in a private window)

GitHub only shows this button in some cases (e.g. older same-name repos). See [Managing your profile README](https://docs.github.com/en/account-and-profile/how-tos/profile-customization/managing-your-profile-readme).

### Option B — Recreate via the GitHub website (most reliable)

1. Open https://github.com/preshan/preshan/settings → **Danger Zone** → **Delete this repository**
2. Also delete leftovers if present: `old-preshan-readme`, `old-preshan-readme-2`
3. Go to https://github.com/new
4. Repository name: **`preshan`** (must match your username exactly)
5. You should see a banner like: *“You found a secret! … special repository …”*
6. Public · **Add a README file** = On · Create repository
7. Tell me when that is done — I will force-push the designed README from this folder

### Optional — let the agent delete for you

```bash
gh auth refresh -h github.com -s delete_repo
```

Then say “delete and recreate the profile repo”.

## Local edits

```bash
cd /Users/preshan/Documents/htdocs/preshan-github-profile
# edit README.md
git add README.md && git commit -m "update profile README" && git push
```

## 3D contribution graph

Workflow: `.github/workflows/profile-3d.yml` (daily). Preferred image: `profile-3d-contrib/profile-night-green.svg`.

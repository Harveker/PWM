# Git History Email Address Removal Guide

## Issue
The repository contains commit history with a personal email address: `franco.endrigo.r@gmail.com`

## Why This Matters
Git commits are permanent records that include author information. Even after making new commits with privacy-preserving emails, old commits remain in the repository history.

## Solution Options

### Option 1: Accept Historical Data (Recommended for Public Repos)
- The email is already public in the git history
- Future commits will use privacy-preserving email
- Add a note in README acknowledging this

### Option 2: Rewrite Git History (Use with Caution)
This requires force-pushing and will affect all existing clones.

⚠️ **Warning**: This will break existing clones and pull requests!

```bash
# Install git-filter-repo (recommended method)
# On Ubuntu/Debian:
sudo apt-get install git-filter-repo

# On macOS with Homebrew:
brew install git-filter-repo

# Create a mailmap file to replace the email
cat > mailmap.txt << 'EOF'
Harveker <60414723+Harveker@users.noreply.github.com> <franco.endrigo.r@gmail.com>
EOF

# Rewrite history using the mailmap
git filter-repo --mailmap mailmap.txt

# Force push (this will rewrite history)
git push --force --all origin
```

### Option 3: GitHub Email Privacy Feature
For future commits, configure git to use GitHub's no-reply email:

```bash
# Set for this repository
git config user.email "60414723+Harveker@users.noreply.github.com"

# Or set globally for all repositories
git config --global user.email "60414723+Harveker@users.noreply.github.com"
```

Also enable "Keep my email addresses private" in GitHub Settings → Emails.

## Recommendation

For this repository, I recommend:
1. Use GitHub's privacy email for future commits (Option 3)
2. Add a security policy (already done - see SECURITY.md)
3. Keep the .gitignore file to prevent future issues (already done)
4. Accept that the old email is already public (Option 1)

If you really need to remove the email from history, use Option 2, but be aware that:
- All collaborators will need to re-clone the repository
- All open pull requests will need to be recreated
- Any external references to commits will break
- This should only be done if absolutely necessary

## Additional Security Measures Implemented

1. ✅ Added comprehensive .gitignore file
2. ✅ Removed absolute paths from IDE configuration
3. ✅ Created SECURITY.md with security guidelines
4. ✅ Updated this guide for email privacy

## Questions?

If you have questions about any of these steps, please refer to:
- GitHub's email privacy documentation: https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-github-user-account/managing-email-preferences/setting-your-commit-email-address
- Git filter-repo documentation: https://github.com/newren/git-filter-repo

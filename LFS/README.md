# Git LFS Assignment – Large File Handling

This repository demonstrates how to work with **Git Large File Storage (LFS)** for files greater than 200 MB.  
It includes a step-by-step guide to setting up Git LFS, generating large files, and pushing them to GitHub.

---

## **1. Prerequisites**

- Git installed ([Download Git](https://git-scm.com/downloads))
- Git LFS installed ([Download Git LFS](https://git-lfs.github.com/))
- Python 3.x (optional, for generating large files)
- A GitHub repository to push changes

---

## **2. Install Git LFS**

If Git LFS is not installed, run:

```bash
git lfs install
```

This initializes Git LFS in your system.

---
## **3. To Track Large Files**

```bash
git lfs track "*.bin"
``` 
This creates a .gitattributes file that tells Git to use LFS for these files.

---

## **4. Add and Commit Files**
```bash
git add .gitattributes
git add large_random_file.bin
git commit -m "Add large test file for LFS"
```
.gitattributes ensures Git LFS tracks the large file correctly.

---

## **5. Push to GitHub**
```bash
git push origin lfs
```
Git LFS automatically uploads the large file to GitHub LFS storage.

---

## **6. Verify LFS Tracking**
```bash
git lfs ls-files
```
You should see your large file listed, confirming it is tracked by Git LFS.

---

## **7. Pulling LFS Files (on another machine)**
```bash
git clone <repo-url>
git lfs pull
```
Git LFS will download the actual large files.

---

## Notes:
- GitHub limits normal Git files to 100 MB.
- Files larger than 100 MB must use Git LFS, otherwise the push will fail.
- Git LFS stores pointer files in Git, while the actual content is in LFS storage.
- Ensure your remote (GitHub, GitLab, etc.) supports Git LFS.
- If pushing fails due to size limits, check your hosting provider’s LFS quota.

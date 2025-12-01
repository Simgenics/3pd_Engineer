# 3D PACT Engineer Station

**3D PACT Engineer Station (ES)** is the authoring and configuration environment of the 3D PACT platform.  
It runs inside the **Unity Editor** and is used by engineers and content creators to configure and validate training scenarios, assemble plant models, and build uploadable bundles for the **3D PACT Management System (MS)**.

Typical workflows in ES include:

- Configuring environment logic  
- Organizing assets and scene content  
- Validating content prior to release  
- Building and uploading bundles to the Management System  

> **Target Unity version:** `2022.3.62f2 (LTS)`

---

## Installation via Unity Package Manager (Git URL)

### Prerequisites

- Unity **2022.3.62f2** installed  
- Git (v2.30+ recommended) available in your system PATH  
- Access to the Git repository (if private, ensure credentials or a Personal Access Token are configured)

---

### Option A — Add via Package Manager UI

1. Open your Unity project.  
2. Go to **Window → Package Manager**.  
3. Click the **➕** button → **Add package from git URL…**  
4. Paste your Git URL and click **Add**.

**Examples:**

- Whole repository:  
  ```
  https://github.com/Simgenics/3pd_Engineer.git#v0.0.97
  ```
---

### Option B — Add via `manifest.json`

Edit your project’s `Packages/manifest.json` file and add the dependency:

```json
{
  "dependencies": {
    "com.simgenics.3dpact.engineerstation": "https://github.com/Simgenics/3pd_Engineer.git#v0.0.97"
  }
}
```

Save the file, then reopen Unity to import the package.

---

## Verifying Installation

- In Unity, open **Window → Package Manager**.  
- Set the Packages filter to **In Project**.  
- Confirm that **3D PACT Engineer Station** is listed.  

---

## Updating the Package

To update to a newer version, you can:
 
- Modify the version/tag in the Git URL (e.g. change `#v1.0.0` to `#v1.1.0`):  
  ```
  https://github.com/<org>/<repo>.git?path=/Packages/com.simgenics.3dpact.engineerstation#v1.1.0
  ```

---

## Troubleshooting

**Private repo authentication**  
Ensure you can clone the repository manually:  
```bash
git clone https://github.com/<org>/<repo>.git
```  
If the repo is private, use HTTPS with a Personal Access Token (PAT).

**Git not found**  
Install Git and restart Unity so it recognizes it in your PATH.

**Incorrect `path` in monorepo**  
Verify that the path specified after `?path=` matches the folder containing the `package.json`.

**Package cache issues**  
If Unity fails to import or update the package, clear the cache:

- **Windows:** `%AppData%\Unity\cache\packages`  
- **macOS:** `~/Library/Unity/cache/packages`

Then reopen the project.

**Long file path issues (Windows)**  
Enable long path support in Git:  
```bash
git config --system core.longpaths true
```

---

## Getting Started

Once imported, open Unity and look for **3D PACT Engineer Station** in the top menu or tools window.  

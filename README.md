# Ancient Yew Digital Twin

A simple static website for viewing two 3D scans of an ancient yew tree in Surrey.

The site uses plain HTML, CSS, and JavaScript only. The 3D models are displayed with Google's `<model-viewer>` web component, and the project is ready to deploy as a static GitHub Pages site.

## Project Structure

```text
.
├── index.html
├── README.md
└── assets/
    ├── yew_1.glb
    └── yew_2.glb
```

## Run Locally

Start a simple local web server from the project folder:

```bash
python3 -m http.server
```

Then open:

```text
http://localhost:8000
```

Using a local server is recommended because browsers can block some 3D model loading behavior when opening `index.html` directly from the filesystem.

## Deploy to GitHub Pages

1. Create a GitHub repository and add these files to it.
2. Commit and push the project to GitHub.
3. In the repository on GitHub, go to **Settings** > **Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select the branch that contains `index.html`, usually `main`.
6. Select the root folder, `/`, then save.

GitHub Pages will publish the static site after the deployment finishes. The final URL will appear in the Pages settings.

## Use a Custom Domain

This repository includes a `CNAME` file for:

```text
www.appel.co.uk
```

In the GitHub repository, go to **Settings** > **Pages** > **Custom domain**, enter `www.appel.co.uk`, and save.

In the DNS settings for `appel.co.uk`, add or update the `www` record:

```text
Type:  CNAME
Name:  www
Value: camappel.github.io
```

After the DNS change has propagated, GitHub Pages should serve this site at:

```text
https://www.appel.co.uk
```

Once GitHub has issued the certificate, enable **Enforce HTTPS** in **Settings** > **Pages**.

# Yonsei-KIAA Workshop on Galaxy Evolution

Static website for the **Yonsei-KIAA Workshop on Galaxy Evolution**.

- **Dates:** January 31 - February 3, 2027
- **Venue:** Yonsei University, Seoul, Republic of Korea
- **Hosts:** Yonsei University and KIAA at Peking University

## Repository structure

```text
Yonsei-KIAA-GitHub-Pages/
├── index.html       # Main website
├── styles.css       # Visual design and responsive layout
├── data.js          # Editable participant list and program
├── .nojekyll        # Tells GitHub Pages to serve this as a plain static site
├── README.md        # Setup and editing instructions
└── assets/          # Reserved for local images/logos if you add them later
```

## Publish with GitHub Pages

### 1. Create a repository

1. Sign in to GitHub.
2. Click **New repository**.
3. Suggested repository name: `yonsei-kiaa-workshop`.
4. Set the repository to **Public** if you are using GitHub Free.
5. Create the repository.

### 2. Upload the website files

Upload the **contents** of this folder to the top level of the repository:

- `index.html`
- `styles.css`
- `data.js`
- `.nojekyll`
- `README.md`
- `assets/`

Do not upload another outer folder around these files. `index.html` should be visible on the repository's main page.

### 3. Turn on GitHub Pages

1. Open the repository on GitHub.
2. Go to **Settings**.
3. In the left sidebar, click **Pages**.
4. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
5. Choose branch **main**.
6. Choose folder **/(root)**.
7. Click **Save**.

GitHub will display the public site address in the Pages settings after deployment.

For a repository named `yonsei-kiaa-workshop`, the URL normally has this form:

```text
https://YOUR-GITHUB-USERNAME.github.io/yonsei-kiaa-workshop/
```

## Edit the participant list

Open `data.js` and edit the objects under `participants`.

Example:

```js
{
  no: 1,
  name: "Participant Name",
  position: "Professor/Research Staff",
  affiliation: "Yonsei University"
}
```

Commit the change to the `main` branch. GitHub Pages will redeploy the updated site automatically.

## Edit the program

Open `data.js` and edit the objects under `program`.

Example:

```js
{
  date: "2027-02-01",
  topic: "Galaxy Evolution 1",
  begin: "09:40",
  end: "10:20",
  name: "Speaker Name",
  title: "Talk title",
  type: "I"
}
```

`type` values used by the website:

- `I` = Invited talk
- `C` = Contributed talk
- blank = General session, break, meal, or other activity

All program items are displayed together in chronological order within each day. The `topic` field is shown as a label when present.

## Add or replace images

You can place image files in `assets/` and reference them with relative paths such as:

```html
<img src="assets/your-image.jpg" alt="Description">
```

Relative paths work correctly on both a GitHub Pages project site and a locally opened copy of the website.

## Updating the live site

For simple changes, edit `data.js` directly on GitHub:

1. Open `data.js` in the repository.
2. Click the pencil/edit icon.
3. Make the changes.
4. Click **Commit changes**.

The published site will update after GitHub Pages redeploys it.

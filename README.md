# Anonymous Redirect / Referrer

Very simple HTML page that is used for anonymous redirect.

Thanks to [Referrer-Policy](https://www.w3.org/TR/referrer-policy/), redirected request will have no referrer at all.
Please note that Referrer-Policy [is not supported](https://caniuse.com/#feat=referrer-policy) by IE11.

## Usage

Use `index.html` (or just `/`) as the entry point:

```text
https://<your-user>.github.io/<your-repo>/?url=[PUT URL HERE]
```

You can pass either a full URL (for example, `https://example.com`) or a bare host/domain (for example, `google.com`). Bare hosts are automatically normalized to `https://...`.
Target URLs that contain their own query string are supported as well (for example, `?url=https://example.com/path?a=1&b=2`).

Backward-compatible link:

```text
https://<your-user>.github.io/<your-repo>/redirect.html?url=[PUT URL HERE]
```

## Deploying from `main`/`master` on GitHub Pages

1. Push this repository to GitHub.
2. In the repository settings, go to **Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select your default branch (`main` or `master`) and folder `/ (root)`.
5. Save.

Because the repository now includes a root `index.html` and a `.nojekyll` file, it is ready for direct branch deployment without any additional build step.

## Example

```text
https://adguardteam.github.io/AnonymousRedirect/?url=https://whatsmyreferer.com/
```

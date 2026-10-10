# Bug.dr landing page

Live site: https://znidarsicmax-lab.github.io/chatgpt-bugdr-landing-page/

`site.tar.gz` contains the complete tested static export, including all images,
fonts, styles, scripts, and legal pages. GitHub Actions extracts and deploys it
as one unit so browser uploads cannot accidentally omit nested asset folders.

`source.tar.gz` contains the editable Next.js source and public images. Extract
it into an empty folder, run `npm ci`, and rebuild with:

```sh
BASE_PATH=/chatgpt-bugdr-landing-page NEXT_PUBLIC_SITE_URL=https://znidarsicmax-lab.github.io npm run build
COPYFILE_DISABLE=1 tar -czf site.tar.gz -C out .
```

Replace the repository's `site.tar.gz` to publish an updated static export.
The source archive excludes dependencies, build caches, Git history and local
environment files.

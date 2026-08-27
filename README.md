# TaoistLoaf

Source for [taoistloaf.github.io](https://taoistloaf.github.io/), built with Hugo and PaperMod.

## Writing

- English posts live in `content/en/posts/`.
- Chinese posts live in `content/zh/posts/`.
- A post does not need a translation. Use the same folder name in both language directories only when the two posts are translations of each other.
- Add tags in front matter with `tags: ["one", "two"]`. Each Tags page shows tags from both languages.

Create a post with:

```sh
hugo new content content/en/posts/my-post/index.md
hugo new content content/zh/posts/my-post/index.md
```

Run the local site with:

```sh
hugo server -D
```

Pushing `main` runs the GitHub Pages workflow and publishes the generated site. Generated files in `public/` are intentionally not committed.

## Comments

Comments use Giscus and remain hidden until GitHub Discussions is enabled and Giscus is configured.

1. Enable **Discussions** in the repository settings.
2. Install the Giscus GitHub app for this repository.
3. Use [giscus.app](https://giscus.app/) to obtain the repository ID and category ID.
4. Add those two values to `[params.giscus]` in `hugo.toml`.

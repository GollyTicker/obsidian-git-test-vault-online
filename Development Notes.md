
# Adapting the line gutter view
It seems, that we can use [registerEditorExtension](https://github.com/obsidianmd/obsidian-api/blob/master/obsidian.d.ts#L2509) to change what is being displayed side-by-side the line numbers.

For instance, the relative-line-numbers obsidian plugin uses [this code](https://github.com/nadavspi/obsidian-relative-line-numbers/blob/main/main.ts#L32) to simply register a [CodeMirror6 relative-line-numbers extension](https://www.npmjs.com/package/codemirror-line-numbers-relative).

Thie relative-line-numbers CodeMirror6 (CM6) extension is just a [few dozens of lines of implementation](https://github.com/jsjoeio/codemirror-line-numbers-relative/blob/main/src/index.ts).

Furthermore, the [CM6 Gutter API](https://codemirror.net/examples/gutter/) seems to be what we need to show the authoring info.

The [GutterMarker](https://codemirror.net/docs/ref/#view.GutterMarker) is what is actually rendered.


# Extracting information from Git

```bash
git blame --color-by-age README.md
```

We can use `--porcelain` to get machine-readable information.


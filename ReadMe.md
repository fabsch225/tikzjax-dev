# Hi
This Repo unifies the dependencies of tikzjax and obsidian-tikzjax. This is based on previous efforts by
- [Jim Fowler](https://github.com/kisonecat) who wrote the web2js compiler and dvi2html library
- [Glenn Rice](https://github.com/drgrice1) whose forks i used mainly
- [artisticat1](https://github.com/artisticat1) who wrote the original obsidian-plugin wrapper and some fixes

# Development Build
1. run `npm install` and `npm run build` in the dvi2html directory
2. run `npm install` in the tikzjax directory
3. run `npm run dev` in the tikzjax directory and look at `demo.html` and `demo2.html`. For a demonstration of the fonts look at `demo3.html`.

The WASM files `core.dump.gz` and `tex.wasm.gz` are checked into the repo. In case you want to rebuild them, consult the Dockerfile in the web2js directory

# Production Build
Here, everything is packed into one JS and one CSS file. To use the obsidian plugin, copy both files manually to the plugin directory and build there once more.

1. run `npm install` and `npm run build` in the dvi2html directory
2. run `npm install` and `npm run build` in the tikzjax directory
3. run `npm run serve` can be used to preview the production build.

# Breaking Changes
### Obsidian Plugin
The script tag was changed to `type="text/tikz-legacy"`. `type="text/tikz"` expects tex-package and tikz-packages and preamble as special properties of the script tag. I changed this in my obisidian-tikzjax fork already.
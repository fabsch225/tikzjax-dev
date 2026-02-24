# Hi
This Repo unifies the dependencies of tikzjax and obsidian-tikzjax. This is based on previous efforts by
- [Jim Fowler](https://github.com/kisonecat) who wrote the web2js compiler and dvi2html library
- [Glenn Rice](https://github.com/drgrice1) whose forks i used mainly
- [artisticat1](https://github.com/artisticat1) who wrote the original obsidian-plugin wrapper and some fixes

# Getting Started
1. run `npm install` and `npm run build` in the dvi2html directory
2. run `npm install`, `npm run install-fonts` and `npm run build` in the tikzjax directory
3. run `npm run serve` in the tikzjax directory and look at `demo.html` and `demo2.html`

The WASM files `core.dump.gz` and `tex.wasm.gz` are checked into the repo. In case you want to rebuild them, consult the Dockerfile in the web2js directory

# Planning
- Integrate Obsidian-Tikzjax Here
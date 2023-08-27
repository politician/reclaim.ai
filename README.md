# reclaim.ai
Tools for reclaim.ai

https://github.com/politician/reclaim.ai/assets/3155568/819c2732-f790-471f-b810-345a42137e3f

## Native app

[Install Nativefier](https://github.com/nativefier/nativefier#installation)

Then run:
```sh
cd $(mktemp -d)
curl -s https://app.reclaim.ai/img/icons/apple-touch-icon.png -o reclaim.png
nativefier "https://app.reclaim.ai/planner?range=WEEK" --name Reclaim --darwin-dark-mode-support --single-instance --honest --internal-urls ".*?" --icon reclaim.png
mv Reclaim*/Reclaim.app /Applications
rm -rf reclaim.png Reclaim*
```

> Use `https://app.reclaim.ai/tasks` in the URL if you want to open Tasks by default rather than the planner

## Apple Shortcut

Add a task from the mac menu bar or using Siri directly (or through any other mean to use shortcuts!)

You will need a Reclaim token available [here](https://app.reclaim.ai/settings/developer).

> ⚠️ This doesn't use a an official API

Available [here](https://www.icloud.com/shortcuts/a4b32d40ac194fe38a9d4128e2b37ad8)

## Alfred Workflow

A very simple Alfred workflow to launch the above shortcut from Alfred.

Available [here](https://github.com/politician/reclaim.ai/raw/main/Add%20a%20task%20to%20Reclaim.ai.alfredworkflow)

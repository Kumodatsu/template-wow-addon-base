# Template for World of Warcraft addons
This is a template repository for World of Warcraft addons.
Feel free to use this template as a starting point for your own addons or modify
it to your own liking.
Any feedback is appreciated.

## Files and folder structure
The root folder contains a `.gitignore` file in which you should put, for
example, files generated by your IDE.

`CHANGELOG.md` is a changelog file.
It is recommended to keep a changelog that lists all notable changes to your
project.
The default changelog file suggests using the
[Keep a Changelog](https://keepachangelog.com/en/1.0.0/) format and
[Semantic Versioning](https://semver.org/spec/v2.0.0.html).
If you wish to use other methods, simply change the changelog file accordingly.

`copy.py` is a Python script that can copy your addon files to a different path.
It is intended to be used to copy the files to your actual addons folder in your
World of Warcraft installation, so that you can test the addon.
You need to have Python installed if you want to use this script.
Example usage:

    python copy.py "C:/Program Files (x86)/World of Warcraft/_retail_/Interface/AddOns"

The `addons` directory holds a directory for every addon in your project, in
case you want your project to consist of multiple addons.
In this template, I've provided a single `ADDON` directory in the `addons`
directory as an example of how to structure these.
This directory contains a `.toc` file, `Bindings.xml` file and a `src` directory
to hold all your Lua scripts.
If you are unsure of what these files mean, look up some documentation about
World of Warcraft addon structure.
You should change the uppercase `ADDON` file names into something that fits your
specific addon.

`.github/workflows/release.yml` is a GitHub Actions file that instructs GitHub
to automatically create a GitHub Release whenever you push a tag whose name is a
'v' followed by a semantic version number.
Your addon folders will be packed up into a zip file and be added as release
assets, and the relevant section from your changelog file will be used as the
release description, assuming it adheres to the Keep a Changelog structure.
If you do not want this automatic release creation or wish to do it yourself,
delete the `.github/workflows/release.yml` file.

## What you should do yourself
- Make a repository using this template.
Or download the source and use the files in your own project, or do whatever
else you may want to do with them.
- Rename the `addons/ADDON` folder to something descriptive of your addon.
Rename `addons/ADDON/ADDON.toc` and `addons/ADDON/src/ADDON.lua` accordingly.
- Fill in the addon metadata in the `.toc` file and make sure it references the
scripts in the `src` directory.
- Replace the occurrences of `ADDONS.zip` in `.github/workflows/release.yml`
with a name that fits your project; this will be used to name the zip file that
is attached to releases.
- You need Python installed to use the copy script if you want to use it.
- If you are using an IDE that generates configuration files or something
similar, add them to the .gitignore file.
- Make sure to replace this README's contents with something relevant to your
own project.
- Also consider adding a license if you intend to publicize your work.
Licenses are useful.

That's about it.
You don't have to credit me if you decide to use this template.
But if you have any feedback, do let me know.

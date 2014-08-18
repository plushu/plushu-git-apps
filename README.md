# plushu-git-apps

Plushu plugin that handles the app lifecycle integration with Git

## Keeping the .git directory

By default, this plugin builds apps with the `.git` directory (or directories,
in the case of submodules) removed from the source tree. This is how Heroku and
Dokku build apps, and is usually what you want: you should only need the code
within your source tree to run.

If you want to build your app with the .git directory *included* in your source
tree (say, because your app does introspection on its git status at runtime),
you can set the `BUILD_KEEP_GIT_DIR` environment variable in .plushurc, or in
`$PLUSHU_ROOT/apps/$app/receive.rc`.

According to the [API](http://doc.gitlab.com/ce/api/repositories.html), we can use

`GET /projects/:id/repository/tree`

to list files and directories in a project. But we can only get the files and directories in top-level of the repo in this way, and sub-directories of directories in top-level with param `path`.

If you wanna get directories of `script/js/components`, for example, you can use

`GET /projects/:id/repository/tree?path=script/js/components`
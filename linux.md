## Copy the contents of a folder to another folder in a different directory using terminal
You can copy the content of a folder /source to another existing folder /dest with the command

* $ cp -a /source/. /dest/

*The -a option is an improved recursive option, that preserve all file attributes, and also preserve symlinks.*

*The . at end of the source path is a specific cp syntax that allow to copy all files and folders, included hidden ones.*
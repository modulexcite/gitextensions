Git encoding is determined automatically by GE and doesn't have to be set by user. Since msysgit-1.7.10 it is UTF8, before that version, it was equal to system default encoding. If you commited files with non ASCII characters using git version less than 1.7.10, your repository needs to be converted. Here is some help:

[Migrating old Git for Windows repositories to MSysGit-Unicode](https://github.com/msysgit/msysgit/wiki/Git-for-Windows-Unicode-Support#wiki-Migrating_old_Git_for_Windows_repositories)

Since GitExtensions-2.34 **GitExtensions encoding** is no longer present. If you hadn't set it to UTF-8, you have to convert git global and local config files to UTF-8 without BOM.

The only encoding user can set is **Files encoding** - this  is default encoding for files content. Better solution would be to determine encoding for every single file. This encoding could be set in .gitattributes file.

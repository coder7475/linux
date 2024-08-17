## Archiving

- Archiving is way for combining multiple files and directories into one file

- Primarily used for backup and simplification of distribution

- Main tools are `tar`, `gzip` nad `bzip2`

### Tools

1. `tar`: Originally for tape archiving. It can manage and organize file into archive. It is a command used to create, maintain, modify, and extract files from an archive file.

2. `gzip` & `bzip`: Used for file compression, reducing the file size and making data transmission easier.

#### Examples

1. To create a tar archive:

```bash
  tar cvf archive_name.tar directory_to_archive/
```

_Options_:

The `c` option tells tar to create a new archive. This option is used when you want to bundle files and directories into a single archive file.

The `v` option stands for "verbose." It tells tar to list the files being added to the archive as they are processed. This provides feedback in the terminal, showing which files are being included in the archive.

The `f` option specifies the name of the archive file. It tells tar that the next argument (`archive_name.tar`) is the name of the archive file to create.

2. To extract tar archive:

```bash
  tar xvf archive_name.tar
```

_Options_:

The `x` option tells tar to extract the contents of the archive. This option is used when you want to unpack the files and directories from the archive into the current directory.

The `v` option stands for "verbose." It tells tar to list the files being extracted as they are processed. This provides feedback in the terminal, showing which files are being unpacked.

The `f` option specifies the name of the archive file. It tells tar that the next argument (`archive_name.tar`) is the name of the archive file to extract.

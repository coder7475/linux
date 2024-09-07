# Comprehensive Guide to the `tr` Command in Unix/Linux

The `tr` command, short for "translate" or "transliterate", is a powerful utility in Unix and Linux systems used for translating or deleting characters. It's a versatile tool for text processing and manipulation.

Here's a concise continuation of the `tr` command guide, focusing on its basic syntax:

```bash
tr [OPTION]... SET1 [SET2]
```

- `SET1`: The set of characters to be translated or deleted.
- `SET2`: The set of characters to translate to (optional).

## Common Options

- `-d`: Delete characters in SET1
- `-s`: Squeeze repeating characters in SET1 to single occurrences
- `-c`: Complement the set of characters in SET1

## Basic Usage Examples

1. Convert lowercase to uppercase:

   ```bash
   echo "hello world" | tr 'a-z' 'A-Z'
   ```

2. Delete specific characters:

   ```bash
   echo "hello 123 world" | tr -d '0-9'
   ```

3. Squeeze repeated characters:
   ```bash
   echo "hello    world" | tr -s ' '
   ```

These examples demonstrate the fundamental uses of the `tr` command for character translation and manipulation.

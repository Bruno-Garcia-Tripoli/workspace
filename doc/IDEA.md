# Project .gitignore Documentation

This `.gitignore` file is configured specifically for managing files created by JetBrains IDEs (e.g., IntelliJ IDEA)
that are typically not necessary for version control. However, it allows selective inclusion of specific configuration
files important for maintaining consistent project settings across team members.

## Contents

1. [General Rules](#general-rules)
2. [Included Files](#included-files)
3. [Excluded Directories](#excluded-directories)
4. [Usage](#usage)

## General Rules

- This `.gitignore` file ignores all files in the `.idea` directory, which contains IDE-specific configurations that are
  not essential for project version control.
- All files and directories within `.idea` are ignored except for a few specific configuration files and directories
  that are important for project consistency.

## Included Files

The following files are explicitly included to ensure a consistent setup across all developers working on the project:

- `vcs.xml`: Contains version control configuration, ensuring consistency in how the IDE interacts with the version
  control system.
- `encodings.xml`: Manages file encoding preferences, ensuring files are consistently read and written across different
  environments.
- `sqldialects.xml`: Stores SQL dialect configurations that help the IDE provide appropriate syntax highlighting and
  code assistance for SQL files.

## Excluded Directories

The following directories within .idea are also included to maintain consistency in code style and project-specific
settings:

- `codeStyles/`: Contains custom code style settings for the project, ensuring code formatting is consistent across the
  team.
- `dictionaries/`: Stores custom dictionaries for spell-checking, helping avoid false positives for project-specific
  terminology.

## Usage

This `.gitignore` configuration is suitable for projects using JetBrains IDEs, where team consistency in code style,
encoding, and version control settings is essential. To use this configuration:

1. Place this `.gitignore` file in the root of your repository.
2. Commit it to ensure that all team members benefit from the shared project configuration files.
# Changelog

## [1.0.3]

### Added
- **Extension Configuration UI:** Add tracked file extensions from the add-on Configuration tab. Uses Home Assistant's native bubble/tag input.
- **Custom File Tracking:** The add-on now fully respects your `.gitignore` file. Add whitelisted patterns (e.g., `!*.sh`) to track additional file types beyond YAML.
- Extensions are added to a managed section in `.gitignore`, preserving any custom patterns you've added.

### Fixed
- **Watcher Noise:** Exclude database files (`.db`, `.db-wal`), log files, and zigbee2mqtt runtime files from triggering the watcher.
- **Options Reading:** Fixed async file reading for add-on configuration options.

### Changed
- **Improved .gitignore Handling:** The add-on no longer overwrites existing `.gitignore` files. Your custom patterns are preserved.
- **File Watcher:** Now watches all files and lets Git's native `.gitignore` handling determine what gets committed.
- **Secrets Handling:** `secrets.yaml` is always in `.gitignore` by default. Remove it from `.gitignore` to track locally. The Cloud toggle only controls whether it gets pushed to remote.

## [1.0.2]

### Added
- **Cloud Backup:** Push your configuration to GitHub, GitLab, or Gitea for off-site backup. Supports automatic push after each commit, hourly, or daily schedules. Optionally exclude secrets.yaml from remote.
- **Recover Deleted Items:** View and restore files, automations, and scripts that have been deleted. Access via the "Deleted" option in the sort menu.
- **Progressive History Loading:** Versions now load faster, displaying results as they're found.

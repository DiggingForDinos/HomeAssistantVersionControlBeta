# Changelog

## [1.0.3]

### Added
- **Custom File Tracking:** The add-on now fully respects your `.gitignore` file. Add whitelisted patterns (e.g., `!*.sh`) to track additional file types beyond YAML.

### Changed
- **Improved .gitignore Handling:** The add-on no longer overwrites existing `.gitignore` files. Your custom patterns are preserved.
- **File Watcher:** Now watches all files and lets Git's native `.gitignore` handling determine what gets committed.

## [1.0.2]

### Added
- **Cloud Backup:** Push your configuration to GitHub, GitLab, or Gitea for off-site backup. Supports automatic push after each commit, hourly, or daily schedules. Optionally exclude secrets.yaml from remote.
- **Recover Deleted Items:** View and restore files, automations, and scripts that have been deleted. Access via the "Deleted" option in the sort menu.
- **Progressive History Loading:** Versions now load faster, displaying results as they're found.

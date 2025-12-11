# AGENTS.md

## Build Commands
- `make get` - Install Go dependencies
- `make build` - Build the binary to `bin/nwg-dock-hyprland`
- `make run` - Run the application directly
- `make install` - Install system-wide
- `make uninstall` - Remove system installation

## Key Features
- `-hi` flag: Hide indicator dots under app icons for cleaner appearance

## Code Style Guidelines

### Imports
- Group imports: stdlib, third-party, project packages
- Use named imports for clarity (e.g., `log "github.com/sirupsen/logrus"`)

### Formatting
- Use standard Go formatting (`go fmt`)
- No trailing whitespace
- Use tabs for indentation

### Naming Conventions
- `camelCase` for variables and functions
- `PascalCase` for exported types and functions
- `UPPER_SNAKE_CASE` for constants
- Short, descriptive names (e.g., `cmd` not `command`)

### Error Handling
- Always handle errors returned from functions
- Use `log.Errorf`, `log.Warnf`, `log.Debugf` for structured logging
- Return errors from functions, don't panic unless unrecoverable

### Types & Structure
- Define structs with JSON tags for API responses
- Use pointers for optional struct fields
- Keep functions small and focused

### GTK/Gotk4 Patterns
- Use `gtk.New*` constructors
- Connect signals with anonymous functions
- Use `glib.TimeoutAdd` for UI updates
- Handle events with proper type casting

### Testing
- No test framework currently configured
- Manual testing via `make run` with Hyprland
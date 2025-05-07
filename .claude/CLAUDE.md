# Claude Configuration

## Search Tools

### Ripgrep (rg)

ALWAYS use ripgrep (`rg`) instead of grep for all search operations:

- Basic search: `rg "pattern" [path]`
- Case insensitive: `rg -i "pattern"`
- Search specific file types: `rg -g "*.js" "pattern"`
- Fixed strings (no regex): `rg -F "exact-string"`
- Whole word matching: `rg -w "word"`
- Include file/path patterns: `rg "pattern" -g "include-pattern"`
- Exclude file/path patterns: `rg "pattern" -g "!exclude-pattern"`
- Show context lines: `rg -C 2 "pattern"` (2 lines before and after)
- Count matches: `rg -c "pattern"`
- Show only filenames: `rg -l "pattern"`

For complex patterns that aren't finding results, try the -U/--multiline flag or --pcre2 for advanced regex patterns.
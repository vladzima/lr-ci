# Linear CLI

A CLI for [Linear](https://linear.app/) that allows you to view, create and update issues. Kind of.

Most likely not everything is working, but eh.

Uses [oclif](https://github.com/oclif) so _:love:_ naturally.

## Installation

```
npm install -g @egcli/lr
```

###### Setup API key

```
lr init
```

# Commands

<!-- commands -->

- [`lr cache:refresh`](#lr-cacherefresh)
- [`lr cache:show`](#lr-cacheshow)
- [`lr config:delete`](#lr-configdelete)
- [`lr config:show`](#lr-configshow)
- [`lr init`](#lr-init)
- [`lr issue ISSUEID`](#lr-issue-issueid)
- [`lr issue:create`](#lr-issuecreate)
- [`lr issue:list`](#lr-issuelist)
- [`lr issue:search [QUERY]`](#lr-issuesearch-query)
- [`lr issue:start ISSUEID`](#lr-issuestart-issueid)
- [`lr issue:stop ISSUEID`](#lr-issuestop-issueid)
- [`lr issue:update ISSUEID`](#lr-issueupdate-issueid)
- [`lr teams:show`](#lr-teamsshow)
- [`lr workspace:add`](#lr-workspaceadd)
- [`lr workspace:current`](#lr-workspacecurrent)
- [`lr workspace:switch`](#lr-workspaceswitch)

### `lr cache:refresh`

Refresh the cache

```
lr cache:refresh
```

### `lr cache:show`

Print the cache file

```
lr cache:show

OPTIONS
  -p, --pretty  Pretty print
```

### `lr config:delete`

```
lr config:delete
```

### `lr config:show`

```
lr config:show
```

### `lr init`

Setup the Linear cli

```
lr init
```

### `lr issue ISSUEID`

Show issue info

```
lr issue ISSUEID

OPTIONS
  -c, --comments     Show issue comments
  -d, --description  Show issue description
  -o, --open         Open issue in browser

ALIASES
  lr i

EXAMPLES
  lr issue LIN-14
  lr issue LIN 14
  lr issue 14 (looks in default team)
```

### `lr issue:create`

Create a new issue

```
lr issue:create

OPTIONS
  -c, --copy  Copy issue url to clipboard after creating

ALIASES
  lr create
  lr c
```

### `lr issue:list`

List issues

```
lr issue:list

OPTIONS
  -a, --all               List issues from all teams
  -m, --mine              Only show issues assigned to me
  -s, --status=status     Only list issues with provided status
  -t, --team=team         List issues from another team
  -u, --uncompleted       Only show uncompleted issues
  -x, --extended          show extra columns
  --columns=columns       only show provided columns (comma-separated)
  --csv                   output is csv format [alias: --output=csv]
  --filter=filter         filter property by partial string matching, ex: name=foo
  --no-header             hide table header from output
  --no-truncate           do not truncate output to fit screen
  --output=csv|json|yaml  output in a more machine friendly format
  --sort=sort             [default: -status] property to sort by (prepend '-' for descending)

ALIASES
  lr list
  lr ls
  lr l
```

### `lr issue:search [QUERY]`

Searches for a string in all issues fields.

```
lr issue:search [QUERY]

ALIASES
  lr search
  lr s
```

### `lr issue:start ISSUEID`

Change status of issue to "In progress" and assign to yourself.

```
lr issue:start ISSUEID

OPTIONS
  -c, --copy-branch  copy git branch to clip-board

ALIASES
  lr start
  lr s
```

### `lr issue:stop ISSUEID`

Return issue to preview state

```
lr issue:stop ISSUEID

OPTIONS
  -u, --unassign  Unassign issue from yourself

ALIASES
  lr stop
```

### `lr issue:update ISSUEID`

Update an issue

```
lr issue:update ISSUEID

OPTIONS
  -p, --property=title|description|status  Property to modify

ALIASES
  lr update
  lr u
```

### `lr teams:show`

Show teams in this workspace

```
lr teams:show

OPTIONS
  -m, --mine  Pretty print
```

### `lr workspace:add`

Add a new workplace

```
lr workspace:add
```

### `lr workspace:current`

Print current workspace

```
lr workspace:current
```

### `lr workspace:switch`

Switch to another workspace

```
lr workspace:switch
```

<!-- commandsstop -->

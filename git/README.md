# Tips and trick with git

## Adding aliases

#### In .gitconfig file:

`[alias] alias_code_name = git_command`

example (prints all known commits, one line per commit):

[alias] onelog = log \-\-oneline

#### From terminal:

`git config --global alias.alias_code_word 'git_command'`

example (prints all known commits, one line per commit):

git config \-\-global alias.onelog 'log \-\-oneline'

#### Multiple Commands and Parameters

`[alias] alias_code_word = git_command_1 $1 && git_command_2 && :`

- `!` pass all that follows to the shell
- `$1` first parameter
- `&&` if the previous command turns 0 (success), then run the command after &&

example (stages changes and displays status, stages all changes if $1 = "."):

[alias] adds = !git add $1 && git status && :

call from terminal:
`git adds .`

#### Resources

- [Git Alias - Multiple Commands and Parameters](https://stackoverflow.com/questions/7534184/git-alias-multiple-commands-and-parameters)
- [8 Git aliases that make me more efficient](https://opensource.com/article/20/11/git-aliases)

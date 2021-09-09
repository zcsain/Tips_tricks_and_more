# Tips and trick with git

## Adding aliases

#### In .gitconfig file:

`[alias]` _alias_code_name_ = _git_command_

example (prints all known commits, one line per commit):

[alias] onelog = log \-\-oneline

#### From terminal:

`git config --global alias.`_alias_code_word_ '_git_command_'

example (prints all known commits, one line per commit):

git config \-\-global alias.onelog 'log \-\-oneline'

#### Multiple Commands and Parameters

`[alias]` _alias_code_word_ = git _command_1_ `$1` `&&`git _command_1_ `&& :`

- `!` pass all that follows to the shell
- `$1` first parameter
- `&&` if the previous command turns 0 (success), then run the command after &&

example (stages all changes and displays status):

[alias] adds = !git add $1 && git status && :

#### Resources

- [Git Alias - Multiple Commands and Parameters](https://stackoverflow.com/questions/7534184/git-alias-multiple-commands-and-parameters)
- [8 Git aliases that make me more efficient](https://opensource.com/article/20/11/git-aliases)

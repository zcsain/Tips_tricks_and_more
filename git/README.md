# Tips and trick with git

## Adding aliases

#### In .gitconfig file:

`[alias]` <span style="color:blue">_alias_code_name_ </span>= <span style="color:blue">_git \_command_ </span>

example (prints all known commits, one line per commit):

[alias] onelog = log \-\-oneline

#### From terminal:

`git config --global alias.`<span style="color:blue">_alias_code_word_</span> '<span style="color:blue">_alias_code_word_</span>'

example (prints all known commits, one line per commit):

git config \-\-global alias.onelog 'log \-\-oneline'

#### Multiple Commands and Parameters

`[alias]` <span style="color:blue">_alias_code_word_</span> = !<span style="color:blue">_git \_command_1_</span> `$1` `&&` <span style="color:blue">_git \_command_1_ </span>`&& :`

- `!` pass all that follows to the shell
- `$1` first parameter
- `&&` if the previous command turns 0 (success), then run the command after &&

example (stages all changes and displays status):

[alias] adds = !git add $1 && git status && :

#### Resources

[Git Alias - Multiple Commands and Parameters](https://stackoverflow.com/questions/7534184/git-alias-multiple-commands-and-parameters)
[8 Git aliases that make me more efficient](https://opensource.com/article/20/11/git-aliases)

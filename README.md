# awslogs
Small tool for working with AWS logs

Depends on [fzf](https://github.com/junegunn/fzf), [aws-cli](https://github.com/aws/aws-cli), [jq](https://github.com/stedolan/jq), and [bat](https://github.com/sharkdp/bat);

1. Set up your awscli profiles as usual as this uses awscli to fetch logs.
2. Add the script somewhere in you path and ensure it's executable.
3. run `awslogs fetch` to interactively fetch the logs from a log group. All fetched logs will be displayed using `bat` once complete.
4. use `awslogs view`, `awslogs search`, or `awslogs today` to filter and display the fetched logs. You can also run your own commands on the `.txt` files in the logs dir.

NOTE: /logs/dir/ can be omitted from the subcommands if AWS_LOGS_DIR has been set to the relevant directory.
The path for this directory is displayed at the end when you call `awslogs fetch`.

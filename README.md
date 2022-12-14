# Actions SSH

Debug a workflow interactively:

```
    steps:
      - uses: chkimes/actions-ssh@v0.1
```

Or run it only on failure:

```
    steps:
      - uses: chkimes/actions-ssh@v0.1
        if: failure()
```

By default, SSH is allowed only for the Action's `github.actor`, however you can override that to be a specific user:

```
    steps:
      - uses: chkimes/actions-ssh@v0.1
        with:
          sshUser: chkimes
```

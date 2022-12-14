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

By default, SSH is allowed only for the Action's `${{ github.actor }}`, however you can override that to be a specific user:

```
    steps:
      - uses: chkimes/actions-ssh@v0.1
        with:
          sshUser: chkimes
```

Make sure you have SSH keys set up in your GitHub settings!

## Connecting

Follow the steps in the Actions logs to connect, e.g.:

```
==================================================================
Connect to the tunnel with:
    ssh chkimes/redacted@usw2.devtunnels.ms
==================================================================
```

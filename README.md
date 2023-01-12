# Actions SSH

Debug a workflow interactively:

```
    permissions: # actions-ssh currently uses OIDC for auth, which requires explicit permissions
      id-token: write
      contents: read
    steps:
      - uses: chkimes/actions-ssh@v0.1
```

Or run it only on failure:

```
    permissions: # actions-ssh currently uses OIDC for auth, which requires explicit permissions
      id-token: write
      contents: read
    steps:
      - uses: chkimes/actions-ssh@v0.1
        if: failure()
```

By default, SSH is allowed only for the Action's `${{ github.actor }}`, however you can override that to be a specific user:

```
    permissions: # actions-ssh currently uses OIDC for auth, which requires explicit permissions
      id-token: write
      contents: read
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

### 📜 Connect the lightning nodes to form a peer

Now that both of our nodes are ready for some action, we need to connect them to form a `peer-to-peer` network this would enable our nodes to communicate with each other on the network by opening and closing channels.

From `lnd1` run

**command:**

```zsh
lncli1 listpeers
```

**output:**

```json
{
  "peers": [] //👈🏿 no peers for now...let's fix that.
}
```

From `lnd2` run the command below to get its `identity_pubkey` which we would use in connecting the node to `lnd1`

**command:**

```zsh
lncli2 getinfo
```

**output:**

```json
{
    "version":  "0.17.0-beta commit=fn/v1.0.1-85-ge31d15989",
    "commit_hash":  "e31d1598932a814c2d44b774e5110746295df711",
    "identity_pubkey":  "024baa5e16c118f42cddd95fd828b32fa8dfcfea55fa384e89e2da0f3b96fc4579",//👈🏿 copy this
    "alias":  "024baa5e16c118f42cdd",
...
}
```

Now let's connect `lnd2` to `lnd1` by passing the `identity_pubkey`, `IP address` and `port`

**command:**

```zsh
 lncli1 connect 024baa5e16c118f42cddd95fd828b32fa8dfcfea55fa384e89e2da0f3b96fc4579@localhost:9734
```

**output:**

```json
{} //👈🏿 don't worry this is the correct output.
```

Let's check for the list of peers once again at `lnd1`

**command:**

```zsh
  lncli1 listpeers
```

**output:**

```json
{
    "peers":  [
        {
            "pub_key":  "024baa5e16c118f42cddd95fd828b32fa8dfcfea55fa384e89e2da0f3b96fc4579",
            "address":  "127.0.0.1:9734",
            "bytes_sent":  "394",
            "bytes_recv":  "394",
            "sat_sent":  "0",
            "sat_recv":  "0",
            "inbound":  false,
            "ping_time":  "-1",
            "sync_type":  "ACTIVE_SYNC",
            .....
}]}
```

🎉 Both Nodes are now successfully connected as a `peer` on our local lightning network.

![connected](https://media.giphy.com/media/v1.Y2lkPTc5MGI3NjExZXp2YjhrODg5d21hMGM2MDhiM25iajh1enJsZ3R2aHBmNzV6c3N1aCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/DoWqmz4TGL3Tk9jwTZ/giphy.gif)

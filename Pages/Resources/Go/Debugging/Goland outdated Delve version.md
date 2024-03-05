[Taken from StackOverflow](https://stackoverflow.com/posts/77802737/timeline)

I found this workaround from the official issue.

1. Install dlv binary with `go install github.com/go-delve/delve/cmd/dlv@latest`
2. Set the `dlv.path=<path_to_dlv_executable>` under Help > Edit Custom Properties
3. Restart GoLand

It works for me.
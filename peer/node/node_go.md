### node.go
node 子命令进一步支持 start、stop、join、status 等子命令。

```golang
// Cmd returns the cobra command for Node
func Cmd() *cobra.Command {
	nodeCmd.AddCommand(startCmd())
	nodeCmd.AddCommand(statusCmd())
	nodeCmd.AddCommand(stopCmd())
	nodeCmd.AddCommand(joinCmd())

	return nodeCmd
}
```

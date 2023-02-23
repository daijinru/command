# Mango Packages Command

Simplified from Cobra and will be maintained continuously.

```bash
$ <CLI_NAME> <flag> <args>
```

## Usage

A tool supports adding sub commands.
```go
rootCmd := &command.Command{
	Use: "root"
}

// new a subcmd
subCmd := &command.Command{
	use: "next"
}
subCmd.addCommand(&command.Command{
	use: "next_sub",
})

// add the sub to root
rootCmd.addCommand(subCmd)
rootCmd.Execute()
```

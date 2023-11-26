# Notes

## TILs

* `tr` command is used to translate. idk why I always think something else but never translate. Found `echo $PATH | tr : "\n"` in the book.
* path on Windows is `$env:Path`

```sh
[  9:27PM ]  [ jac494@hp-laptop:~/Projects/command_line_rust(main✗) ]
 $ echo $PATH | tr : "\n"
/home/jac494/.vscode-server/bin/f1b07bd25dfad64b0167beb15359ae573aecd2cc/bin/remote-cli
/home/jac494/.cargo/bin
/usr/local/bin
/usr/bin
/usr/local/sbin
/usr/sbin

PS C:\Users\jac49> $env:Path
C:\WINDOWS\system32;C:\WINDOWS;C:\WINDOWS\System32\Wbem;C:\WINDOWS\System32\WindowsPowerShell\v1.0\;C:\WINDOWS\System32\OpenSSH\;C:\Program Files\PuTTY\;C:\Users\jac49\AppData\Local\Programs\Python\Python310\Scripts\;C:\Users\jac49\AppData\Local\Programs\Python\Python310\;C:\Users\jac49\AppData\Local\Microsoft\WindowsApps;;C:\Users\jac49\AppData\Local\Programs\Microsoft VS Code\bin;C:\Users\jac49\AppData\Local\Programs\Hyper\resources\bin
```

* similar to `subprocess` in python is `std::process::Command` in rust (ref. page 8)

Some runs of the initial `echor` program

```txt
[ 11:16AM ]  [ jac494@hp-laptop:~/Projects/command_line_rust/echor(main✗) ]
 $ cargo run --quiet 1>out 2>err          
[ 11:16AM ]  [ jac494@hp-laptop:~/Projects/command_line_rust/echor(main✗) ]
 $ echo $?
1
[ 11:17AM ]  [ jac494@hp-laptop:~/Projects/command_line_rust/echor(main✗) ]
 $ cat out
[ 11:17AM ]  [ jac494@hp-laptop:~/Projects/command_line_rust/echor(main✗) ]
 $ cat err
error: The following required arguments were no
t provided:
    <TEXT>...

USAGE:
    echor [FLAGS] <TEXT>...

For more information try --help
[ 11:17AM ]  [ jac494@hp-laptop:~/Projects/command_line_rust/echor(main✗) ]
 $ cargo run --quiet -- arg1 1>out1 2>err1
[ 11:17AM ]  [ jac494@hp-laptop:~/Projects/command_line_rust/echor(main✗) ]
 $ echo $?
0
[ 11:17AM ]  [ jac494@hp-laptop:~/Projects/command_line_rust/echor(main✗) ]
 $ cat out
[ 11:17AM ]  [ jac494@hp-laptop:~/Projects/command_line_rust/echor(main✗) ]
 $ cat out1
ArgMatches {
    args: {
        "text": MatchedArg {
            occurs: 1,
            indices: [
                1,
            ],
            vals: [
                "arg1",
            ],
        },
    },
    subcommand: None,
    usage: Some(
        "USAGE:\n    echor [FLAGS] <TEXT>...",
    ),
}
[ 11:17AM ]  [ jac494@hp-laptop:~/Projects/command_line_rust/echor(main✗) ]
 $ cat err1
[ 11:17AM ]  [ jac494@hp-laptop:~/Projects/command_line_rust/echor(main✗) ]
 $
```

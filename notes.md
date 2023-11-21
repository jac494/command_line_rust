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

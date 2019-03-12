# repeatcmds

Repeatcmds is a shell script that enables you to execute multiple commands every seconds.

## Installation

```bash
wget https://github.com/SausageCats/repeatcmds/blob/master/repeatcmds
chmod +x repeatcmds
```

## Usage

```bash
repeatcmds <sleep[s]> <command...>
```

The first argument indicates the number of seconds to wait after command execution.
The remaining arguments consist of several commands that are executed in an order.
For example,

```bash
repeatcmds 5 date 'g++ hoge.cpp && ./a.out'
```

executes the `date` command first, followed by `g++ hoge.cpp && ./a.out`, and sleeps for five seconds.
After that, the same commands are repeated continuously.
Note that a command-line argument is executed regardless of the success or failure of the previous commands.

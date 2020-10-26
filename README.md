# Tail

This is repo is forked from the https://github.com/nxadm/tail.
It is been maintained for use of my log collector, 
features will be added, and some of will be removed.  

## TODO
- batch
- inotify only

# Go package for tail-ing files

A Go package striving to emulate the features of the BSD `tail` program.

```
tailer, err := tail.TailFile("/var/log/nginx.log", tail.Config{Follow: true})
if err != nil {
    panic(err)
}

for line := range tailer.Lines {
    fmt.Println(line.Text)
}
```

## Log rotation

Tail comes with full support for truncation/move detection as it is
designed to work with log rotation tools.

## Installing
```shell script
go get github.com/f1shl3gs/tail/...
```

## Windows support
it won't be support
[![Build Status](https://travis-ci.org/isaaxiot/tail.svg)](https://travis-ci.org/isaaxiot/tail)
[![Build status](https://ci.appveyor.com/api/projects/status/vrl3paf9md0a7bgk/branch/master?svg=true)](https://ci.appveyor.com/project/Nino-K/tail/branch/master)

# Go package for tail-ing files

A Go package striving to emulate the features of the BSD `tail` program. 

```Go
t, err := tail.TailFile("/var/log/nginx.log", tail.Config{Follow: true})
for line := range t.Lines {
    fmt.Println(line.Text)
}
```

See [API documentation](http://godoc.org/github.com/isaaxiot/tail).

## Log rotation

Tail comes with full support for truncation/move detection as it is
designed to work with log rotation tools.

## Installing

    go get github.com/isaaxiot/tail/...

## Windows support

This package [needs assistance](https://github.com/isaaxiot/tail/labels/Windows) for full Windows support.

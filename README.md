# logrus-wraper
github.com/sirupsen/logrus with filename and line number

### usage

```
package main

import (
	log "github.com/neohe/logrus-wraper"
	"github.com/sirupsen/logrus"
)

func main() {
	log.SetLogFormatter(&logrus.TextFormatter{
		ForceColors:     true,
		FullTimestamp:   true,
		TimestampFormat: "2006-01-02 15:04:05",
	})

	log.Info("This is an example")
}
```

### output

```
INFO[2018-12-06 21:05:02] This is an example                            file="main.go:15"
```
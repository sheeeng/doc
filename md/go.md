# [The Go Programming Language](https://golang.org)

- [Getting Started](https://golang.org/doc/install)
- [Downloads](https://golang.org/dl/)
- [How to Write Go Code](https://golang.org/doc/code.html)
- [GoGetTools - Installing Version Control Tools for go get](http://golang.org/s/gogetcmd)

The [gopher images](https://golang.org/doc/gopher/) are Creative Commons Attributions 3.0 licensed. That means you can play with the images but you must give credit to their creator (Renee French) wherever they are used.

## Windows

	C:\> setx GOPATH %USERPROFILE%\go

First Go Library:

Create `%GOPATH%\src\github.com\whoami\stringutil\stringutil.go` file with below content.

	// Package stringutil contains utility functions for working with
	// strings.
	package stringutil
	
	// Reverse returns its argument string reversed rune-wise left to right.
	func Reverse(s string) string {
	   r := []rune(s)
	   for i, j := 0, len(r)-1; i < len(r)/2; i, j = i+1, j-1 {
		   r[i], r[j] = r[j], r[i]
	   }
	   return string(r)
	}

Create `%GOPATH%\src\github.com\whoami\hello_reverse\hello_reverse.go` file with below content.

	package main
	
	import (
		"fmt"
		"github.com/whoami/stringutil"
	)
	
	func main() {
		fmt.Printf(stringutil.Reverse("!oG ,olleH"))
	}

Build and install the library.

	C:\> go install github.com\whoami\hello_reverse

Run the program linked to the library.

	C:\> set PATH=%PATH%;%GOPATH%\bin
	
	C:\> hello_reverse
	Hello, Go!

First Go Test:

Create `%GOPATH%\src\github.com\whoami\stringutil\stringutil_test.go` file with below content.

	package stringutil
	
	import "testing"
	
	func TestReverse(t *testing.T) {
		cases := []struct {
			in, want string
		}{
			{"Hello, world", "dlrow ,olleH"},
			{"Hello, 世界", "界世 ,olleH"},
			{"", ""},
		}
		for _, c := range cases {
			got := Reverse(c.in)
			if got != c.want {
				t.Errorf("Reverse(%q) == %q, want %q", c.in, got, c.want)
			}
		}
	}

Build and install the test.

	C:\> go install github.com\whoami\hello_reverse

Run the test.

	C:\> go test github.com\whoami\stringutil
	ok      github.com/whoami/stringutil    0.167s

## OS X

	export GOPATH=$HOME/go
	export PATH=$HOME/go/bin:$PATH

Go Directory

	$ ls -l /usr/local/go
	total 136
	-rw-r--r--    1 root  wheel  17575 18 Feb 05:42 AUTHORS
	-rw-r--r--    1 root  wheel  24564 18 Feb 05:42 CONTRIBUTORS
	-rw-r--r--    1 root  wheel   1479 18 Feb 05:42 LICENSE
	-rw-r--r--    1 root  wheel   1303 18 Feb 05:42 PATENTS
	-rw-r--r--    1 root  wheel   1112 18 Feb 05:42 README
	-rw-r--r--    1 root  wheel      7 18 Feb 05:45 VERSION
	drwxr-xr-x   10 root  wheel    340 18 Feb 05:42 api
	drwxr-xr-x    5 root  wheel    170 18 Feb 05:44 bin
	drwxr-xr-x    4 root  wheel    136 18 Feb 05:44 blog
	drwxr-xr-x   39 root  wheel   1326 18 Feb 05:42 doc
	-rw-r--r--    1 root  wheel   1150 18 Feb 05:42 favicon.ico
	drwxr-xr-x   11 root  wheel    374 18 Feb 05:42 include
	drwxr-xr-x    3 root  wheel    102 18 Feb 05:42 lib
	drwxr-xr-x   15 root  wheel    510 18 Feb 05:45 misc
	drwxr-xr-x    6 root  wheel    204 18 Feb 05:43 pkg
	-rw-r--r--    1 root  wheel     26 18 Feb 05:42 robots.txt
	drwxr-xr-x   64 root  wheel   2176 18 Feb 05:42 src
	drwxr-xr-x  215 root  wheel   7310 18 Feb 05:42 test
	$


Go Environment

	$ go env
	GOARCH="amd64"
	GOBIN=""
	GOCHAR="6"
	GOEXE=""
	GOHOSTARCH="amd64"
	GOHOSTOS="darwin"
	GOOS="darwin"
	GOPATH=""
	GORACE=""
	GOROOT="/usr/local/go"
	GOTOOLDIR="/usr/local/go/pkg/tool/darwin_amd64"
	CC="clang"
	GOGCCFLAGS="-fPIC -m64 -pthread -fno-caret-diagnostics -Qunused-arguments -fmessage-length=0 -fno-common"
	CXX="clang++"
	CGO_ENABLED="1"
	$
	
Go Example

Use `vi hello.go` and paste the below content.

	package main

	import "fmt"

	func main() {
	    fmt.Printf("Hello, Go 世界!\n")
	    fmt.Printf("%s\n", `( ꒪Д꒪)ノ`)
	    fmt.Printf("%s\n", `☆*･゜ﾟ･*\(^O^)/*･゜ﾟ･*☆`)
	    fmt.Printf("%s\n", `٩(^ᴗ^)۶`)
	}

Run it with `go run hello.go` command. Voila!

	$go run go/src/hello.go
	Hello, Go 世界!
	( ꒪Д꒪)ノ
	☆*･゜ﾟ･*\(^O^)/*･゜ﾟ･*☆
	٩(^ᴗ^)۶
	$


## Advanced Example

	C:\> go get github.com/jfrazelle/weather

	C:\> %GOPATH%\bin\weather -l "Kuala Lumpur, Malaysia" -u si
	                            .;odc
	                          ;kXNNNO
	                        .0NNO0NN:
	                       'XNK; dNNl
	                       KNX'  'XNK.
	                      ,NNk    cXNK,
	                      ,NNk     '0NNO:.
	                    .'cXNXl;,.   ,xXNNKOxxxk0Xx
	                'lOXNNNNNNNNNNXOo'  ':oxkOXNNXc
	              cKNNKd:'.    ..;d0NNKl    ,xXNK,
	       .;:cclKNXd.              .oXNXxOXNNXl
	   .cOXNNNNNNNO.                  .kNNNNNNNXOc.
	  lXNXx;.    .                      .    .;dXNXo
	 ONNd.                                       oXN0.
	dNNo                                          cNNk
	XNN.                                           NNX
	0NN'                                          .NNK
	;XN0.                                        .ONNc
	 ;XNXo.                                    .lXNX:
	  .oXNX0dlcclx0Xo.              .oXKxlccldOXNXd.
	     ,lk0KXXK0xKNN0o;..    ..;o0NNKx0KXXX0ko,
	                'lOXNNNNNNNNNNXOo,
	                    :x0XNNX0x:.
	
	
	Current weather is Mostly Cloudy in Kuala Lumpur in Federal Territory of Kuala Lumpur for July 9 at 3:45pm CEST
	The temperature is 27.96°C, but it feels like 31.33°C
	
	Ick! The humidity is 76%
	The wind speed is 1.02 m/s NE
	The cloud coverage is 80%
	The visibilty is 0 kilometers
	The pressure is 1008.73 mbar
	
	C:\> 

## Remarks

For convenience, add the workspace's bin subdirectory to your PATH:

- Linux / OS X

	`$ export PATH=$PATH:$GOPATH/bin`

- Windows

	`C:\> set PATH=%PATH%;%GOPATH%\bin`
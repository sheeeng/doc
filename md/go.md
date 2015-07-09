[The Go Programming Language](https://golang.org)

- [Getting Started](https://golang.org/doc/install)
- [How to Write Go Code](https://golang.org/doc/code.html)

C:\>setx GOPATH %CD%\go

- [GoGetTools - Installing Version Control Tools for go get](http://golang.org/s/gogetcmd)

Example:

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


	mkdir %GOPATH%\src\github.com\whoami\hello

For convenience, add the workspace's bin subdirectory to your PATH:

- Linux / OS X

	`$ export PATH=$PATH:$GOPATH/bin`

- Windows

	`C:\> set PATH=%PATH%;%GOPATH%\bin`
## Quick Start

Pull this image to local:

```
docker pull dwimberger/alpine-dmtx
```


Generate a Datamatrix code:

```
docker run -t -i --rm -v `pwd`:/dmtx dwimberger/alpine-dmtx dmtxwrite -o helloworld.png test.txt ```

Output:

![hello world](https://raw.githubusercontent.com/dwimberger/alpine-dmtx/master/helloworld.png)

Parse a Datamatrix code:

```
docker run -t -i --rm -v `pwd`:/dmtx dwimberger/alpine-dmtx dmtxread helloworld.png
```

Output：

```
Hello DMTX World!
```

Show help:

```
docker run -t -i --rm -v `pwd`:/dmtx dwimberger/alpine-dmtx dmtxwrite --help
```

```
docker run -t -i --rm -v `pwd`:/dmtx dwimberger/alpine-dmtx dmtxread --help
```

## How to Build this image ?

```
git clone https://github.com/dwimberger/alpine-dmtx.git
cd alpine-dmtx
docker build -t dwimberger/alpine-dmtx .
```

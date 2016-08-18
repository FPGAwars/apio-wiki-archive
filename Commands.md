## apio build

### Arguments

* board: icestick, icezum, go-board, ...
* fpga: iCE40-HX1K-TQ144, iCE40-HX1K-VQ100, ...
* size: 1k, 8k
* type: lp, hx
* pack: tq144, vq100, ...

### Testing

#### Correct arguments

Command executed

E.g.

```
$ apio build
[...] Processing icezum
```

```
$ apio build --board icestick
[...] Processing icestick
```

```
$ apio build --fpga iCE40-HX1K-VQ100
[...] Processing custom board
```

```
$ apio build --type lp --size 8k --pack cm225:4k
[...] Processing custom board
```

#### Redundant arguments

Command executed with a warning message

E.g.

```
$ apio build --board icezum --size 1k
[...] Processing icezum
Warning: redundant arguments: size
```

```
$ apio build --board icezum --fpga iCE40-HX1K-TQ144 --type hx
[...] Processing icezum
Warning: redundant arguments: fpga, type
```

```
$ apio build --fpga iCE40-HX1K-TQ144 --pack vq100
[...] Processing custom board
Warning: redundant arguments: pack
```

#### Contradictory arguments

Command not executed. Print an error message

E.g.

```
$ apio build --board icezum --size 8k
[...] Processing icezum
Error: contradictory arguments: size
```

```
$ apio build --board icezum --fpga iCE40-HX1K-TQ144 --type lp
[...] Processing icezum
Warning: redundant arguments: fpga
Error: contradictory arguments: type
```

```
$ apio build --fpga iCE40-HX1K-TQ144 --type lp --size 8k
[...] Processing custom board
Error: contradictory arguments: type, size
```

#### Insufficient arguments

Command not executed. Print an error message

E.g.

```
$ apio build --size 8k
[...] Processing custom board
Error: insufficient arguments: missing type, pack
```

```
$ apio build --type lp --size 8k
[...] Processing custom board
Error: insufficient arguments: missing pack
```
## apio build

### Arguments

* board: icestick, icezum, go-board, ...
* fpga: iCE40-HX1K-TQ144, iCE40-HX1K-VQ100, ...
* size: 1k, 8k
* type: lp, hx
* pack: tq144, vq100, ...

board > fpga > size, type, pack

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
Warning: redundant arguments: size
[...] Processing icezum
```

```
$ apio build --board icezum --fpga iCE40-HX1K-TQ144 --type hx
Warning: redundant arguments: fpga, type
[...] Processing icezum
```

```
$ apio build --fpga iCE40-HX1K-TQ144 --pack vq100
Warning: redundant arguments: pack
[...] Processing custom board
```

#### Contradictory arguments

Command not executed. Print an error message

E.g.

```
$ apio build --board icezum --size 8k
Error: contradictory arguments: size
```

```
$ apio build --board icezum --fpga iCE40-HX1K-TQ144 --type lp
Warning: redundant arguments: fpga
Error: contradictory arguments: type
```

```
$ apio build --fpga iCE40-HX1K-TQ144 --type lp --size 8k
Error: contradictory arguments: type, size
```

#### Insufficient arguments

Command not executed. Print an error message

E.g.

```
$ apio build --size 8k
Error: insufficient arguments: missing type, pack
```

```
$ apio build --type lp --size 8k
Error: insufficient arguments: missing pack
```

#### Unknown board

Command not executed. Print an error message

E.g.

```
$ apio build --board icefake
Error: unknown board: icefake
```

```
$ apio build --board icefake --fpga iCE40-HX1K-TQ144
Error: unknown board: icefake
```

#### Unknown fpga

Command not executed. Print an error message

E.g.

```
$ apio build --fpga iCE40-FAKE
Error: unknown fpga: iCE40-FAKE
```

```
$ apio build --fpga iCE40-FAKE --size 8k
Error: unknown fpga: iCE40-FAKE
```

```
$ apio build --board icezum --fpga iCE40-FAKE
Error: unknown fpga: iCE40-FAKE
```
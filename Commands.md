## apio build

### Arguments

* board: icestick, icezum, go-board, ...
* fpga: iCE40-HX1K-TQ144, iCE40-HX1K-VQ100, ...
* size: 1k, 8k
* type: lp, hx
* pack: tq144, vq100, ...

### Testing

#### Redundant arguments

Command executed with a warning message

E.g.

```
$ apio build --board icezum --size 1k
Warning: redundant arguments: size
```

```
$ apio build --board icezum --fpga iCE40-HX1K-TQ144 --type hx
Warning: redundant arguments: fpga, type
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
Error: contradictory arguments: missing pack
```
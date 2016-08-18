## apio clean

Remove the previous generated files.

### Testing

E.g.

```
$ apio clean
```

## apio verify

Verify the verilog code.

### Testing

E.g.

```
$ apio verify
```

## apio sim

Launch verilog simulation.

### Testing

E.g.

```
$ apio sim
```

## apio build

Synthesize the bitstream.

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

## apio upload

Upload bitstream to FPGA. Same arguments that *build* + device argument.

### Testing

#### Correct arguments

E.g.

```
$ apio upload
[...] Processing icezum
```

```
$ apio upload --board icestick
[...] Processing icestick
```

```
$ apio upload --device 1
[...] Processing custom board
```

```
$ apio upload --device 1 --fpga iCE40-HX1K-VQ100
[...] Processing custom board
```

```
$ apio upload --device 1 --type lp --size 8k --pack cm225:4k
[...] Processing custom board
```

#### Insufficient arguments

Command not executed. Print an error message

E.g.

```
$ apio upload --size 8k
Error: insufficient arguments: missing device, type, pack
```

```
$ apio upload --fpga iCE40-HX1K-VQ100
Error: insufficient arguments: missing device
```

## apio time

Bitstream timing analysis. Same arguments that *build*.

### Testing

E.g.

```
$ apio time
```
The best way to **test** that everything is working ok with a board is to download a **blinky hello world example**, synthesize it and upload it into your board. These are the **steps**:

## 1. **Install the latest example apio package**

This is the command for forcing the installation of the **latest version**:

```
apio install -f examples
```

You can check all the **installed packaged** with this command:

```
apio install -l
```

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Adding-examples/examples-01.png)

## 2. **Listing all the available examples**

List all the **available examples** and try to find the blinky for the board you want to test

```
apio examples -l
```

You will have to scroll up to see all the examples

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Adding-examples/examples-02.png)

Each example has an **identifier** in blue, consisting of of two parts separated by the '/' symbol. The first is the **board name** and the second is the **example name**. For this demo we will use the example **Alhambra-II/Blinky**

## 3. **Getting the example**

Execute the command **apio example -d** followed by the example identifier (previous step)

```
apio examples -d Alhambra-II/Blinky
```

It will create a **new folder** with the identifier as a name. In this demo it has created the **folder Alhambra-II** and inside it a new folder called **Blinky**

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Adding-examples/examples-03.png)

## 4. **Uploading the example to the board**

Connect the board to the computer, enter into the example folder (in this demo enter into Alhambra-II/Blinky folder) and execute the **apio upload** command

```
apio upload
```

It will **synthesize** the example and **upload** it to the board

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Adding-examples/examples-04.png)

This is what you will see once the upload is finished:

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Adding-examples/examples-05.png)

(Do not worry about the warnings)

You will see the blinking LED in the board:

![](https://github.com/FPGAwars/apio/raw/develop/wiki/Adding-examples/example-06.gif)


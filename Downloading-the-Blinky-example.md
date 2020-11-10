The best way to **test** that everything is working ok with a board is to download a **blinky hello world example**, synthesize it and upload it into your board. These are the steps:

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


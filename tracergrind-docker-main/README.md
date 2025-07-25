## Building images

Run the following command to build the images:

```bash
docker build -t tracergrind tracergrind
docker build -t texttrace texttrace
```

## Using

The basic workflow is:
```bash
docker run -it -v ${PWD}:/home tracergrind -d -d --tool=tracergrind --output=/home/<filename> /home/<filename>.trace
docker run -it -v ${PWD}:/home texttrace home/<filename>.trace home/<filename>.texttrace
```

To create a sample trace with the provided sample file:
```bash
cd sample
gcc -o string-compare-strcmp string-compare-strcmp.c
docker run --rm -it --ulimit nofile=262144:262144 -v ${PWD}:/home tracergrind -d -d --tool=tracergrind --output=/home/string-compare-strcmp.trace /home/string-compare-strcmp
docker run --rm -it --ulimit nofile=262144:262144 -v ${PWD}:/home texttrace string-compare-strcmp.trace string-compare-strcmp.texttrace
readelf -Wa string-compare-strcmp | grep -e .text -e main > string-compare-strcmp.elf
```

## Helper script

- Ensure `fzf` is installed.
- Define the environment variable `TRACERGRIND_SEARCH_BASE` to point to the directory that contains the source code files to be traced.

Run and search for the source file to trace:
```bash
./run.sh
```

The script will generate a directory to store the partial traces and the final trace file.

## Using the traces

After the `.elf` and `.texttrace` files are generated, the traces can be visualized using the `trace_viewer` tool. Upload them to https://cache-parser.hugo.dev.br/ and fully parse them for the simulator.

Drag the parsed file to https://cache-simulator.hugo.dev.br/ and visualize the cache behavior.

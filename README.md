# bun-executable-repro

This is a reproduction of a bug I'm seeing with single file executables.

To reproduce:

```bash
bun install

bun build --compile --minify --sourcemap ./index.ts --outfile program
```

Then run the program:

```bash
./program
```

You should see the following error:

```
error: Cannot find module './solclientjs.js' from '/$bunfs/root/program'
```

# Buttermilk Pancake Stack — food-picture-01

A tall stack of fluffy buttermilk pancakes photographed mid-pour:
maple syrup runs over the top in a single glossy ribbon, a pat of
butter melts underneath it, syrup drips down the sides of the stack,
and fresh blueberries and raspberries sit around the plate. Bright,
airy café light, shot close so the pancakes fill the frame and the
dish is unmistakable even at thumbnail size. There is no text in the
image.

## How it works

The entry is deliberately boring at run time, because the rules run
the program twice and require identical output bytes:

- `image.png` — the finished photograph, bundled in the repo.
- `main.py` — a standard-library-only validator and publisher. It
  checks the PNG signature, parses the IHDR chunk for the real width
  and height, enforces the 1024×1024 and 1,048,576-byte limits, then
  copies the file byte-for-byte to `$MAKEFUN_OUTPUT_DIR/entry.png`
  and verifies the copy matches the source.

## Run it

```sh
MAKEFUN_OUTPUT_DIR=/tmp/out python3 main.py
# -> writes /tmp/out/entry.png
```

Python 3.13, no third-party dependencies.

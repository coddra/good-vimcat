# Finally a Good VimCat!

This `vimcat`
- is fast
- generates output that can be embedded
- has a userfriendly interface
- has many options
- does not clear the screen

Install the script by running
```bash
sudo ./vimcat --install
```

**Use it in your [`ranger`](https://github.com/ranger/ranger) config!**

`scope.sh`:
```bash
# ranger provides these as arguments
FILE_PATH="$1"
PREVIEW_WIDTH="$2"
PREVIEW_HEIGHT="$3"

# [...]

case "$mimetype" in
  text/* | */xml | */json | */javascript)
    vimcat "$FILE_PATH" -ecl "$PREVIEW_WIDTH" "$PREVIEW_HEIGHT" && exit 5
    exit 2
    ;;
  # [...]
esac
```

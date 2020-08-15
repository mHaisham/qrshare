# QR share

Serve a file on local network and give the url in qrcode form on console

## Install

```bash
pip install qrshare
```

## Usage

### Send to

Press `Windows` + `r` and enter `shell:sendto`

> C:\Users\<user>\AppData\Roaming\Microsoft\Windows\SendTo

Create shortcut with command `qrshare` in folder

now option qrshare should appear when you right click to a file

### Commandline

```bash
qrshare --help
```

```bash
Usage: __main__.py [OPTIONS] PATH

Options:
  --port INTEGER  waitress server port
  --help          Show this message and exit.
```

### Code Example

```python
from qrshare import Network

Network.serve(ABS_PATH_TO_FILE, port=[OPTIONAL]PORT)
```

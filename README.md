# آموزش جمر بلوتوثی

BLEeding is a tool that allows you to jam Bluetooth and BLE devices. It can be used to spam DeAuth requests or L2CAP ping requests. It supports Linux, macOS, Windows and Raspberry PI.

This tool was created for educational purposes only. I do not take any responsibility for the misuse of this tool.

## توضیحات 

منبع خودمم نبینم جایی بدون منبع پخش کنی

وبلاگ : [arashhacker.blog.ir](arashhacker.blog.ir)
ایدی تلگرام : [@arashhacker32](https://t.me/arashhacker32)
صفحه گیتهاب : [arashhacker32](https://github.com/arashhacker32)

برای ویندوز باید github desktop رو سیستمتون نصب باشه.

## نحوه نصب و اجرا

**🐧 Linux / 🍇 Raspberry PI**

```bash
# Install dependencies.
sudo apt-get install git pkg-config python pip libbluetooth-dev libboost-python-dev libboost-thread-dev libglib2.0-dev
```

**🍎 macOS**

```bash
# Install dependencies.
brew install bluez
```

**🟦 Windows**

```bash
# Install dependencies.
choco install git python3
```

## 💻 Setup

```bash
# Clone the repository.
git clone https://github.com/arashhacker32/bluetoothjammer

# Go to the repository.
cd bluetoothjammer

# Install the requirements.
pip install -r requirements.txt
```

> Note: In order to use BLE in Linux, you must install "gattlib" python module. You can install it using the following command: `pip install gattlib`.

## 📚 Usage

```bash
python bluotoothjammer <options> COMMAND
```

| Command | Description | Options | OS Support |
| ------- | ----------- | ------- | ------- |
| `scan` | Scan for devices. | `ble` | 🐧 🍎 c 🍇 |
| `random-mac` | Generate random trusted MAC addresses | | 🐧 🍎 🟦 🍇 |
| `enum <TARGET>` | Enum device services | | 🐧 🍎 🟦 🍇 |
| `deauth <TARGET>` | Spam DeAuth requests | `port`, `protocol`, `size`, `threads` | 🐧 🍇 🟦 |

| Option | Short | Description | type | Default |
| ------ | ----- | ----------- | :--: | :-----: |
| `--ble` | `-b` | Use BLE instead of Bluetooth. | bool | ❌ |
| `--port` | `-p` | Port to use. | int | 4097 |
| `--protocol` | `-P` | Protocol to use. | **enum:** l2cap, rfcomm | l2cap |
| `--size` | `-s` | Size of the packets. | int | 512 |
| `--threads` | `-t` | Number of threads. |  int | (vcore count) |

> Note: All flags are optional. Windows doesn't support L2CAP protocol.

## 🤝 ارتباط با ما

وبلاگ : [arashhacker.blog.ir](arashhacker.blog.ir)
ایدی تلگرام : [@arashhacker32](https://t.me/arashhacker32)
صفحه گیتهاب : [arashhacker32](https://github.com/arashhacker32)

## ❤️ Show your support

Give a ⭐️ if this project helped you!

## 📝 License

Copyright © 2024 [Sammwy](https://github.com/sammwyy).
This project is [MIT](LICENSE) licensed.

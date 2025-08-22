# Networking Lab

## Installation Instructions

### Download [WireShark][def1]

- Enter the following command in your terminal to download WireShark:

  ```bash
  sudo apt update
  sudo apt install gcc wireshark
  ```

- During the installation, you will be prompted with a question: **`"Should non-superusers be able to capture packets?"`** Select **`Yes`** to allow non-superusers to capture packets.

  ```bash
  sudo usermod -a -G wireshark $USER
  sudo dpkg-reconfigure wireshark-common
  sudo chmod +x /usr/bin/dumpcap
  ```

- After installation, you can launch WireShark by typing `wireshark` in your terminal.

  ```bash
  wireshark
  ```

### Video Tutorial

If you need help with the installation or want to learn how to use WireShark, you can watch the following video tutorial.

**Video link:** [Wireshark Tutorial for Beginners | Network Scanning Made Easy](https://www.youtube.com/watch?v=qTaOZrDnMzQ)

[![Watch the video][def2]][def3]

[def1]: https://www.wireshark.org/
[def2]: https://img.youtube.com/vi/qTaOZrDnMzQ/hqdefault.jpg
[def3]: https://www.youtube.com/watch?v=qTaOZrDnMzQ

# Assignment-3: UDP Audio File Transfer

Transfer an audio file ([audio.wav][def1]) from a client to a server using UDP.

---

## Solution

- Open [WireShark][def2] and click on `Loopback: lo` to capture the packets.

  [![WireShark Capture][def3]][def3]

- Go to the directory and open the terminal.

- Run the [`server.c`][def5] file using the below command:

  ```bash
  gcc server.c -o server
  ```

- Run the `server` file using the below command:

  ```bash
  ./server
  ```

- Open another terminal and run the [`client.c`][def6] file using the below command:

  ```bash
  gcc client.c -o client
  ```

- Run the `client` file using the below command:

  ```bash
  ./client
  ```

- Now, you can see the packets being captured in WireShark and the audio file is transferred from the client to the server.

  [![WireShark Capture][def4]][def4]

- There will be a new file named `received_audio.wav` in the directory.

  [![Received Audio][def5]][def5]

[def1]: ./audio.wav
[def2]: https://www.wireshark.org/
[def3]: ../images/img_01.png
[def4]: ../images/img_16.png
[def5]: ../images/img_17.png

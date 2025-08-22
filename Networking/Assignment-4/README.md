# Assignment-4: Reliable File Transfer over UDP

## Objective

Implement a reliable file transfer system over the UDP protocol. Since UDP itself is unreliable (packets may be lost, duplicated, or arrive out of order), you must design a mechanism to ensure reliability using techniques such as segmentation, sequencing, acknowledgments, and retransmission.

## Tasks

- ### File Segmentation

  Divide the file into fixed-size segments (e.g., $1$ KB each). Each segment should contain metadata:

  - Sequence Number
  - File Name / File Identifier
  - Data Payload

- ### Stop-and-Wait Protocol

  Implement a Stop-and-Wait ARQ (Automatic Repeat Request) mechanism:

  - Sender transmits one segment at a time.
  - Sender waits for an acknowledgment (ACK) from the receiver.
  - If the ACK is not received within a timeout, retransmit the segment.
  - Receiver sends ACK for each correctly received segment (use sequence number to handle duplicates).

- ### Acknowledgment Handling

  Receiver must send back an ACK containing:

  - Sequence Number of the successfully received segment
  - File identifier (to handle multiple file transfers, if extended later)

- ### Reassembly of File

  Receiver collects all the received segments in order. Write them back into the original file format after successful transfer.

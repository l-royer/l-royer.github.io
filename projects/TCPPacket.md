---
layout: project
type: project
image: img/640px-TCP_header.png
title: "TCP Packet"
date: 2023
published: true
labels:
  -C
  -TCP
  -Binary Data
summary: "A program that reads binary data of a TCP header and generates a response header."
---

<div class="text-center p-4">
  <img width="200px" src="https://upload.wikimedia.org/wikipedia/commons/thumb/d/da/TCP_header.png/640px-TCP_header.png" class="img-thumbnail" >
</div>

# TCP Header

This program reads in binary files containing TCP request headers as input, outputs the original header information, generates a new header based off of the request header, and outputs the generated data into a new file. This program does this using only bitwise operators and without any string functions. A readfile function, printheader function, makeheader function, and writefile function is used to read, store, manipulate, and output binary data. The printheader function states the Source Port, Destination Port, Sequence Number, Acknowledgement Number, and Control Bits values of the header. The makeheader function uses bitwise operators to check the source port and control bits, and modifies the source, destination, acknowledgement, sequence and control bit values.

This was an individual project for ICS212, written in C, meant to demonstrate how binary data is read, written, and manipulated. Given the expected output, I began by studying the structure of a TCP header and how it formats 160-bit long data. After learning what bit positions corresponded to each TCP component, I first wrote the printheader function and learned how to parse hexadecimal data. I wrote the makeheader function similarly to the printheader function, and the readfile and writefile functions followed. 

The main focus of this project was to demonstrate the differences in manipulating binary data. Accessing the information of the TCP request header and breaking it down into human readable information required knowledge of the TCP structure that was entirely new to me. Generating a TCP header required hexadecimal calculations, the use of unsigned data types, and generalizable bitwise solutions. File IO functions also needed to be able to read and write binary data as opposed to text data. This project gave me a glimpse into TCP and computer networking while also allowing me to become very familiar with binary data.

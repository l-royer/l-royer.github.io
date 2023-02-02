---
layout: project
type: project
image: img/bank-account-concept-vector-illustration-customer-sitting-with-laptop-and-bank-with-credit-card-and-vector-clipart_csp66403603.webp
title: "Bank Database"
date: 2023
published: true
labels:
  - C 
summary: "A program consisting of a UI and a database that stores bank records."
---

<div class="text-center p-4">
  <img width="200px" src="https://cdn.xxl.thumbs.canstockphoto.com/bank-account-concept-vector-illustration-customer-sitting-with-laptop-and-bank-with-credit-card-and-vector-clipart_csp66403603.jpg" class="img-thumbnail" >
</div>

Bank database is a project that takes bank profile records and stores them in a database. The user-interface presents a welcome screen and menu to the user, prompting them to make a selection by typing in any of the letters sequential order in an option. The menu options consisted of addRecord, findRecord, printAllRecords, deleteRecord, and quit functions. User input was rejected if the user typed letters that didn't match an option; e.g., 'q', 'qu', 'qui', and 'quit' were valid inputs, but 'quitter', 'qwit' or any input consisting of numbers were not. addRecord prompted the user to enter an account number, name, and address, each of which had specific valid input parameters. Invalid input attempts led to prompting the user to re-enter their input. Each function was stored and computed in the database file. Account information was stored using a linked list of struct records, containing pointers to the next record. Each record was stored in numerical order, and this order was retained when an account was deleted.Upon quitting, the program wrote the new information to a file and cleaned up any heap memory. Upon every initiation of the program, the file was read from and accessed by the database to display information to the user. The program also had a debug option, which would be enabled in the command line argument of the program's execution.

This was a single-person ICS212 project, written in C, meant to showcase structs, pointers, headers, and file I/O methods. With brief descriptions for what was expected for each method, the C Programming Language textbook was my single primary resource. We had the freedom to decide what methods we could use, with restrictions, and how we would implement our linked lists with our add and delete functions.
 
This challenging, months-long project taught me how data is stored and manipulated at the smallest level. IO streams, buffers, memory leaks, and pointers were all new concepts to me, and integral to making a working program. Bank database was also edited using VI on UNIX, which also required some research to learn how to use. The nuances between various data structures and their limitations became more pronounced for me, and I now understand the complexity and detail associated with how C processes data.

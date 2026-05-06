---
layout: post
title: "SEI CERT C++ remediation and Rust Hangman"
tags: secure-coding cpp rust sei-cert
---

[View on GitHub](https://github.com/CodeEvent/Secure-Programming)

## Brief

COMP10068 Secure Programming at UWS had two components: remediating five noncompliant C++17 programs against the SEI CERT C++ Coding Standard, and building a Hangman game in Rust. The module was graded A2, First-class band (80-89%).

## C++ remediation

Each program contained a specific SEI CERT violation. The protected main() function could not be modified.

- **DCL50-CPP:** Replaced C-style variadic arguments with a variadic template, restoring compile-time type safety.
- **STR50-CPP:** Added explicit length validation before a string read to prevent a buffer over-read.
- **MEM51-CPP:** Wrapped raw new/delete in std::unique_ptr to ensure automatic cleanup via RAII.
- **MSC51-CPP:** Replaced a predictable seed with std::random_device for non-deterministic seeding.
- **ERR55-CPP:** Removed a false noexcept specification from a function that could throw.

## Rust Hangman

Built a complete Hangman implementation from a Hello World template. Used HashSet for O(1) deduplication of guessed letters, leveraged Rust ownership semantics to avoid shared mutable state, and followed idiomatic patterns throughout. The word list was loaded from an external fruits.txt file that could not be edited.

## Results

- Grade: A2, First-class band (80-89%)
- Five SEI CERT rules remediated without modifying any protected main() function
- Rust Hangman built from scratch

## Tools

C++17, g++, Rust, Cargo, SEI CERT C++ Coding Standard, std::unique_ptr, std::random_device, HashSet.

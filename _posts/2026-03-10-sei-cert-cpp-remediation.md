---
layout: post
title: "SEI CERT C++ remediation and Rust Hangman"
tags: secure-coding cpp rust sei-cert
---

[View on GitHub](https://github.com/CodeEvent/Secure-Programming)

## Brief

COMP10068 Secure Programming at UWS had two components: analysing and remediating five noncompliant C++17 programs against the SEI CERT C++ Coding Standard, and building a Hangman game in Rust from a bare Hello World template. Both exercises focused on memory safety, type safety, and defensive coding practices. The module was graded A2, First-class band (80-89%).

## Approach: C++ remediation

Each program contained a specific violation of the SEI CERT standard. The constraint was strict: the protected main() function could not be modified. All fixes had to be applied to surrounding code while preserving the original program behaviour.

### DCL50-CPP: C-style variadic to template

The original code used C-style variadic arguments, which bypass type checking entirely. The fix replaced these with a variadic template, restoring compile-time type safety while maintaining the same calling interface.

### STR50-CPP: buffer over-read fix

A string operation read past the end of its buffer due to a missing bounds check. The remediation added explicit length validation before the read, preventing the over-read without changing the function signature.

### MEM51-CPP: RAII via unique_ptr

Manual memory management with raw new/delete created a leak path when exceptions were thrown between allocation and deallocation. Wrapping the allocation in std::unique_ptr ensured automatic cleanup regardless of the exit path, following the RAII idiom.

### MSC51-CPP: std::random_device seeding

The random number generator was seeded with a predictable value, making its output reproducible. Replacing the seed source with std::random_device provided non-deterministic seeding appropriate for security-relevant contexts.

### ERR55-CPP: false noexcept removal

A function marked noexcept could in fact throw under certain input conditions. Removing the false noexcept specification allowed the exception to propagate normally rather than triggering std::terminate.

## Approach: Rust Hangman

Built a complete Hangman implementation in Rust starting from a Hello World template. Key design decisions included using HashSet for deduplication of guessed letters (O(1) lookup, no duplicates by construction), leveraging Rust's ownership semantics to avoid shared mutable state, and following idiomatic Rust patterns throughout (pattern matching, iterators, Result types). The word list was loaded from an external fruits.txt file that could not be edited, so all word handling logic was implemented in code.

## Results

- Grade: A2, First-class band (80-89%)
- Five SEI CERT rules remediated without modifying any protected main() function
- Rust Hangman built from scratch demonstrating memory-safe systems programming

## Tools

C++17, g++, Rust, Cargo, SEI CERT C++ Coding Standard, std::unique_ptr, std::random_device, HashSet.

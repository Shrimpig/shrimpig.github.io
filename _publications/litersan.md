---
title: "LiteRSan: Lightweight Memory Safety Via Rust-specific Program Analysis and Selective Instrumentation"
authors: "Tianrou Xia, Kaiming Huang, Dongyeon Yu, Yuseok Jeon, Jie Zhou, Dinghao Wu, Taegyu Kim"
pdf: "/files/litersan.pdf"
permalink: /publication/litersan.md
date: 2025-09-19
venue: 'arXiv'
paperurl: 'https://shrimpig.github.io/files/litersan.pdf'
---

__Abstract__
Rust is a memory-safe language, and its strong safety guarantees combined with high performance have been attracting widespread adoption in systems programming and security-critical applications. However, Rust permits the use of unsafe code, which bypasses compiler-enforced safety checks and can introduce memory vulnerabilities. A widely adopted approach for detecting memory safety bugs in Rust is Address Sanitizer (ASan). Optimized versions, such as ERASan and RustSan, have been proposed to selectively apply security checks in order to reduce performance overhead. However, these tools still incur significant performance and memory overhead and fail to detect many classes of memory safety vulnerabilities due to the inherent limitations of ASan. In this paper, we present LiteRSan, a novel memory safety sanitizer that addresses the limitations of prior approaches. By leveraging Rust's unique ownership model, LiteRSan performs Rust-specific static analysis that is aware of pointer lifetimes to identify risky pointers. It then selectively instruments risky pointers to enforce only the necessary spatial or temporal memory safety checks. Consequently, LiteRSan introduces significantly lower runtime overhead (18.84% versus 152.05% and 183.50%) and negligible memory overhead (0.81% versus 739.27% and 861.98%) compared with existing ASan-based sanitizers while being capable of detecting memory safety bugs that prior techniques miss.

## Staff Software Engineer | Agentic AI Engineering | Rust, Compilers, WebAssembly, SDKs, Developer Tools, Fuzzing | 0 -> 1 

I have built compilers, developer tools and systems software in Rust for the last 6+ years. I usually start them from zero, ship them, and keep them working long after. For the last eight years my work has been open source.

At Miden I am one of the two core engineers who built the Rust compiler for the Miden VM, a zero-knowledge (ZK) virtual machine. Developers outside the company use it to write smart contracts in Rust. The VM has no registers, no jumps and no machine integers, so the standard Rust toolchain only gets us as far as WebAssembly and the rest of the compiler is our own. About half of the compiler is my work, across the whole pipeline: the frontend, the IR, optimization passes and code generation. I own the WebAssembly frontend and everything outside developers touch: the Rust SDK, the build tooling and the releases. I got that job by building a Rust to ZK compiler in my own time and pitching it to the team.

Before that I spent almost 6 years as a core developer at Ergo Platform, a blockchain with its own smart contract language. I created and led the Rust implementation of its contract interpreter, cryptographic protocols and transaction signing, alongside the Scala reference implementation. It ships to the web, iOS and Android, and wallets build and sign transactions with it. It is still in use 3 years after I left.

What I bring to a team:
• Ownership from zero. I started the compiler frontend, the SDK, the test infrastructure and the release process, and kept them working as the platform changed under them.
• Care for the user. I supported outside developers from bug report to released fix, and I treat the developer experience as part of the product.
• Technical leadership. I led a change across 4 codebases owned by different teams, interviewed candidates, mentored new team members, ran 2 contributor bounty programs, and grew a contributor into a co-maintainer.
• Measured results. Cut the execution cost of compiled programs by up to 48% and reduced compiled contract size by 60%.
• Production ownership. I built a service, ran it with outside operators, built its observability (health checks, metrics and dashboards), and was on call for it.
• AI agents as the way of working. I orchestrate AI coding agents every day. I also built an agentic fuzzer, in which AI agents search for compiler bugs, and prototyped an eval harness for AI agent skills.

For more than 10 years I've been working remotely in distributed teams based in the US.

## Experience

### Staff Compiler Engineer, Miden, Oct 2023 to Present

One of the two core engineers who built the Rust compiler for the Miden VM, a zero-knowledge (ZK) virtual machine. The VM is a stack machine with no registers, no jumps and no byte-addressable memory, and it computes on field elements instead of machine integers. The standard Rust toolchain only gets us as far as WebAssembly. Everything after that is ours: an IR modeled after LLVM's MLIR, the transformation and optimization passes, and the code generator. I joined in its first months, about half of the compiler is my work, and I work across all of it. I started and own the WebAssembly frontend and everything outside developers touch: the Rust SDK, the build tooling and the releases. Today I do this work by orchestrating AI coding agents.

• Profiled compiled Rust on the VM and reworked code generation around what the profiles showed, cutting execution cost by up to 48%. Cut compiled contract size by 60%.
• Tracked down and fixed miscompilations reported from real user programs across the IR, optimization passes and code generation, and made compiler output deterministic.
• Built an agentic differential fuzzer: AI agents search for compiler bugs by checking compiled programs against native Rust. It now finds most compiler bugs before users do.
• Shaped the AI agent skills that teach coding agents to write programs for the platform, and prototyped an eval harness to score them.
• Built a sandboxed WebAssembly runtime for running untrusted extension code inside the VM.
• Created a code coverage tool for Miden Assembly: line, function and branch coverage collected from VM execution.
• Led changes across 4 codebases owned by different teams, from proof of concept to rollout.
• Reviewed design and code across the team, interviewed candidates and mentored 2 new team members.
• Contributed upstream to the WebAssembly ecosystem.

3 years, first at Polygon and then at Miden after the spin-out. All of it is open source: https://github.com/0xMiden/compiler

### Senior Core Developer (Rust, Scala), Ergo Platform, Jan 2018 to Oct 2023

Core developer of Ergo, an open-source blockchain with its own smart contract language. I created and led sigma-rust, the Rust implementation of the contract interpreter, cryptographic protocols, transaction building and signing that wallets build on. Before that I worked in Scala on the reference interpreter and the node.

• Started sigma-rust from zero and maintained it: roadmap, releases, design decisions and review of most outside contributions.
• Shipped one Rust core to 3 platforms through WebAssembly/JavaScript, C/Swift (iOS) and JNI (Android) bindings. The Yoroi and Nautilus wallets use it.
• Initiated and ran 2 contributor bounty programs: wrote 92 issues as self-contained specs and reviewed the work. Grew one contributor into a co-maintainer.
• Led the new oracle application that posts price data on chain, built from the ground up: on-chain contracts, an off-chain application, and a public mainnet run with outside operators.
• Built that application to run unattended as a service: it keeps running through failures of its dependencies, with log rotation, config migration, secrets kept out of config files, and observability: health endpoints, Prometheus metrics and a Grafana dashboard.
• Ran the oracle pools myself and was on call for them: diagnosed outages down to the node and the contracts, and turned operator reports into fixes and releases.
• Worked on the consensus-critical parts of the Scala interpreter: the binary serialization format, hardening the deserializer against malicious input, and the cost accounting that bounds script execution.

sigma-rust is still in use 3 years after I left. All open source: https://github.com/ergoplatform/sigma-rust

## Projects

### Rust compiler for the Miden VM (2023 to present, associated with Miden)

A compiler from Rust to the Miden VM, a zero-knowledge (ZK) virtual machine with no registers, no jumps, no machine integers and no byte-addressable memory. The standard Rust toolchain compiles the code to WebAssembly; from there the compiler has its own IR modeled after LLVM's MLIR, its own passes and its own code generator. Outside developers use it to write smart contracts in Rust. I am one of the two core engineers, and about half of the compiler is my work: I started and own the WebAssembly frontend, the Rust SDK, the build tool and the test harness, and I work across the IR, the passes and the code generator.

https://github.com/0xMiden/compiler

### fuzza: agentic differential fuzzer (2026, associated with Miden)

A differential fuzzer for the Rust compiler for the Miden VM. Each test case is a small Rust program that is compiled twice, natively and for the VM, and run on boundary-biased random inputs; any difference in the results is a likely compiler bug, and the case file is its reproducer. AI coding agents write the cases, in a two-level workflow: one director agent reads a coverage report of the compiler, picks the areas the corpus does not reach yet, and launches one campaign agent per area; each campaign agent writes programs to reach its area until coverage stops growing. The corpus has 463 cases, with the reproducers for known bugs pinned until they are fixed. I built the harness, the agent workflow and the corpus.

https://github.com/0xMiden/compiler/tree/next/tools/fuzza-agent

### OmniZK: Rust to zero-knowledge VMs (2022 to 2023, personal)

A framework for compiling Rust, through WebAssembly, to zero-knowledge virtual machines. I built it in my own time, with an IR design modeled after MLIR and backends for 3 VMs: Triton VM, Miden VM and Valida. I pitched this pipeline to the Miden team, and that led to my role there.

Along the way I contributed fixes upstream to the pliron IR library and to Cranelift.

https://github.com/greenhat/omnizk

### sigma-rust (2020 to 2023, associated with Ergo Platform)

The Rust implementation of Ergo's smart contract interpreter, Sigma protocols, transaction building, signing and wallet primitives. One Rust core with WebAssembly/JavaScript, C/Swift and JNI bindings, used by the Yoroi and Nautilus wallets. I created it, led it for more than 3 years and reviewed pull requests from 24 outside contributors.

https://github.com/ergoplatform/sigma-rust

### oracle-core (2022 to 2023, associated with Ergo Platform)

The oracle application for Ergo: a Rust service that independent operators run to post price data on chain, with on-chain contracts for pooling the data points and for updating the contracts by vote. I led the new version, built from the ground up, and wrote most of the service itself: the REST API, health endpoints, Prometheus metrics and a Grafana dashboard, and the tooling operators use to join a pool.

https://github.com/ergoplatform/oracle-core

### Code coverage for Miden Assembly (associated with Miden)

A code coverage tool for Miden Assembly: line, function and branch coverage collected from VM execution. I built it from zero.

https://github.com/0xMiden/cov

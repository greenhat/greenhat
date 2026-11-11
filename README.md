## Staff Software Engineer

**Rust · compilers · WebAssembly · VM · developer tools · agentic AI**

Available for hire: [denys@zadorozhnyi.com](mailto:denys@zadorozhnyi.com)

I have built compilers, developer tools and systems software in Rust for the last 6+ years. All my work for the last 8 years is open source - [github.com/greenhat](https://github.com/greenhat)

At **Miden** I'm one of the two core engineers who built the [Rust compiler](https://github.com/0xMiden/compiler) for the [Miden VM](https://github.com/0xMiden/miden-vm), a zero-knowledge (ZK) virtual machine. Outside developers use it to write smart contracts in Rust. The VM has no registers, no jumps and no machine integers, so the standard Rust toolchain takes us only to WebAssembly. The rest of the compiler is our own code. About half of it is my work, and it is spread across the whole pipeline (frontend, IR, optimization passes and code generation). I designed and own the WebAssembly frontend and the Rust SDK, along with everything else outside developers touch (the build tooling and the releases). I got this job by building a [Rust to ZK compiler](https://github.com/greenhat/omnizk) in my own time and pitching it to the team.

Before that I was a core developer at **Ergo Platform** for almost 6 years. Ergo is an open-source smart contract platform for financial applications, built on zero-knowledge proofs. I created and led the [Rust implementation](https://github.com/ergoplatform/sigma-rust) of its contract interpreter, cryptographic protocols and transaction signing, alongside the [Scala reference implementation](https://github.com/ergoplatform/sigmastate-interpreter). It runs on the web, iOS and Android, and wallets use it to build and sign transactions.

For more than 10 years I've been working remotely in distributed teams based in the US.

<details>
<summary><h2>Strengths and Recent Roles</h2></summary>

### How I work

- **I take ownership in new projects and in existing ones.** At Miden I wrote the first frontend of the compiler, and started the SDK, the test infrastructure and the release process. At Ergo I first worked on the existing Scala interpreter and node, and then started the Rust implementation.
- **I treat the developer experience as part of the product.** I supported outside developers from the bug report to the released fix.
- **I lead technical work.** I led a change across 4 codebases owned by different teams, interviewed candidates, mentored new team members, ran 2 contributor bounty programs and grew a contributor into a co-maintainer.
- **I measure the results.** The execution cost of compiled programs went down by up to 48% and the compiled contract size by 60%.
- **I own what I run in production.** I built [a service](https://github.com/ergoplatform/oracle-core), ran it with outside operators, built its observability (health checks, metrics and dashboards) and was on call for it.
- **I work with AI coding agents every day.** I also built an [agentic fuzzer](https://github.com/0xMiden/compiler/tree/main/tools/fuzza-agent) where AI agents search for compiler bugs, and prototyped an [eval harness](https://github.com/greenhat/miden-skill-evals) for AI agent skills.

---

### Staff Compiler Engineer

**Miden** · 2023 to Present

I'm one of the two core engineers who built the Rust compiler for the Miden VM, a zero-knowledge (ZK) virtual machine. The VM is a stack machine. It has no registers, no jumps and no byte-addressable memory, and it computes on field elements instead of machine integers. The standard Rust toolchain takes us only to WebAssembly. Everything after that is our own code: an IR modeled after LLVM's MLIR, the transformation and optimization passes, and the code generator. I joined in its first months. About half of it is my work, and I work on all of its parts. I designed and own the WebAssembly frontend and the Rust SDK, along with everything else outside developers touch (the build tooling and the releases). Today I do this work by orchestrating AI coding agents.

- Profiled compiled Rust on the VM and reworked code generation based on the profiles. The execution cost went down by up to 48%. Cut compiled contract size by 60%.
- Fixed miscompilations reported from real user programs in the IR, optimization passes and code generation. Made the compiler output deterministic.
- Designed and built an agentic differential fuzzer. AI agents search for compiler bugs by checking compiled programs against native Rust, with compiler code coverage as feedback. It finds most compiler bugs before users do.
- Shaped the AI agent skills that teach coding agents to write programs for the platform. Prototyped an eval harness to score them.
- Designed and built a sandboxed WebAssembly runtime for running untrusted extension code inside the VM.
- Created a code coverage tool for Miden Assembly (line, function and branch coverage collected from VM execution).
- Led changes across 4 codebases owned by different teams, from proof of concept to rollout.
- Reviewed design and code across the team, interviewed candidates and mentored 2 new team members.
- Contributed upstream to the WebAssembly ecosystem.

3 years, first at Polygon and then at Miden after the spin-out. All of it is open source: [0xMiden/compiler](https://github.com/0xMiden/compiler)

---

### Senior Core Developer

**Ergo Platform** · 2018 to 2023

I was a core developer of Ergo, an open-source smart contract platform for financial applications, built on zero-knowledge proofs. I created and led sigma-rust. It's the Rust implementation of the contract interpreter, cryptographic protocols, transaction building and signing, and wallets are built on it. Before that I worked in Scala on the reference interpreter and the node.

- Started sigma-rust from zero and maintained it. I did the roadmap, the releases, the design decisions and the review of most outside contributions.
- Architected sigma-rust as one Rust core shipped to 3 platforms through WebAssembly/JavaScript, C/Swift (iOS) and JNI (Android) bindings. The Yoroi and Nautilus wallets use it.
- Initiated and ran 2 contributor bounty programs. I wrote 92 issues as self-contained specs and reviewed the work. Grew one contributor into a co-maintainer.
- Led the new oracle application that posts price data on chain. It was built from the ground up: on-chain contracts, an off-chain application and a public mainnet run with outside operators.
- Built that application to run unattended as a service. It keeps running when its dependencies fail. It has log rotation, config migration, secrets kept out of config files, health endpoints, Prometheus metrics and a Grafana dashboard.
- Ran the oracle pools myself and was on call for them. I diagnosed outages down to the node and the contracts, and turned operator reports into fixes and releases.
- Worked on the consensus-critical parts of the Scala interpreter: the binary serialization format, hardening the deserializer against malicious input, and the cost accounting that bounds script execution.

All open source: [ergoplatform/sigma-rust](https://github.com/ergoplatform/sigma-rust)

</details>

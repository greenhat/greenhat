## Staff Software Engineer

**Rust · compilers · developer tools · open source**

Available for hire.

I have built compilers, developer tools and systems software in Rust for the last 6+ years. I usually start them from zero, ship them, and keep them working long after. For the last eight years my work has been open source.

At **Miden** I am one of the two core engineers who built the Rust compiler for the Miden VM, a zero-knowledge (ZK) virtual machine. Developers outside the company use it to write smart contracts in Rust. The VM has no registers, no jumps and no machine integers, so the standard Rust toolchain only gets us as far as WebAssembly and the rest of the compiler is our own. About half of the compiler is my work, across the whole pipeline: the frontend, the IR, optimization passes and code generation. I own the WebAssembly frontend and everything outside developers touch: the Rust SDK, the build tooling and the releases. I got that job by building a Rust to ZK compiler in my own time and pitching it to the team.

Before that I spent almost 6 years as a core developer at **Ergo Platform**, a blockchain with its own smart contract language. I created and led the Rust implementation of its contract interpreter, cryptographic protocols and transaction signing, alongside the Scala reference implementation. It ships to the web, iOS and Android, and wallets build and sign transactions with it. It is still in use 3 years after I left.

---

### What I bring to a team

* **Ownership from zero.** I started the compiler frontend, the SDK, the test infrastructure and the release process, and kept them working as the platform changed under them.
* **Care for the user.** I supported outside developers from bug report to released fix, and I treat the developer experience as part of the product.
* **Technical leadership.** I led a change across 4 codebases owned by different teams, interviewed candidates, mentored new team members, ran 2 contributor bounty programs, and grew a contributor into a co-maintainer.
* **Measured results.** Cut the execution cost of compiled programs by up to 48% and reduced compiled contract size by 60%.
* **Production ownership.** I built a service, ran it with outside operators, built its observability (health checks, metrics and dashboards), and was on call for it.
* **AI agents as the way of working.** I orchestrate AI coding agents every day. I also built an agentic fuzzer, in which AI agents search for compiler bugs, and prototyped an eval harness for AI agent skills.

---

For more than 10 years I've been working remotely in distributed teams based in the US.

<details>
<summary><h2>Recent Roles</h2></summary>

### Staff Compiler Engineer

**Miden** · 2023 to Present

One of the two core engineers who built the Rust compiler for the Miden VM, a zero-knowledge (ZK) virtual machine. The VM is a stack machine with no registers, no jumps and no byte-addressable memory, and it computes on field elements instead of machine integers. The standard Rust toolchain only gets us as far as WebAssembly. Everything after that is ours: an IR modeled after LLVM's MLIR, the transformation and optimization passes, and the code generator. I joined in its first months, about half of the compiler is my work, and I work across all of it. I started and own the WebAssembly frontend and everything outside developers touch: the Rust SDK, the build tooling and the releases. Today I do this work by orchestrating AI coding agents.

* Profiled compiled Rust on the VM and reworked code generation around what the profiles showed, cutting execution cost by up to 48%. Cut compiled contract size by 60%.
* Tracked down and fixed miscompilations reported from real user programs across the IR, optimization passes and code generation, and made compiler output deterministic.
* Built an agentic differential fuzzer: AI agents search for compiler bugs by checking compiled programs against native Rust. It now finds most compiler bugs before users do.
* Shaped the AI agent skills that teach coding agents to write programs for the platform, and prototyped an eval harness to score them.
* Built a sandboxed WebAssembly runtime for running untrusted extension code inside the VM.
* Created a code coverage tool for Miden Assembly: line, function and branch coverage collected from VM execution.
* Led changes across 4 codebases owned by different teams, from proof of concept to rollout.
* Reviewed design and code across the team, interviewed candidates and mentored 2 new team members.
* Contributed upstream to the WebAssembly ecosystem.

3 years, first at Polygon and then at Miden after the spin-out. All of it is open source: [0xMiden/compiler](https://github.com/0xMiden/compiler)

---

### Senior Core Developer

**Ergo Platform** · 2018 to 2023

Core developer of Ergo, an open-source blockchain with its own smart contract language. I created and led sigma-rust, the Rust implementation of the contract interpreter, cryptographic protocols, transaction building and signing that wallets build on. Before that I worked in Scala on the reference interpreter and the node.

* Started sigma-rust from zero and maintained it: roadmap, releases, design decisions and review of most outside contributions.
* Shipped one Rust core to 3 platforms through WebAssembly/JavaScript, C/Swift (iOS) and JNI (Android) bindings. The Yoroi and Nautilus wallets use it.
* Initiated and ran 2 contributor bounty programs: wrote 92 issues as self-contained specs and reviewed the work. Grew one contributor into a co-maintainer.
* Led the new oracle application that posts price data on chain, built from the ground up: on-chain contracts, an off-chain application, and a public mainnet run with outside operators.
* Built that application to run unattended as a service: it keeps running through failures of its dependencies, with log rotation, config migration, secrets kept out of config files, and observability: health endpoints, Prometheus metrics and a Grafana dashboard.
* Ran the oracle pools myself and was on call for them: diagnosed outages down to the node and the contracts, and turned operator reports into fixes and releases.
* Worked on the consensus-critical parts of the Scala interpreter: the binary serialization format, hardening the deserializer against malicious input, and the cost accounting that bounds script execution.

sigma-rust is still in use 3 years after I left. All open source: [ergoplatform/sigma-rust](https://github.com/ergoplatform/sigma-rust)

</details>

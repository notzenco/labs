# labs/

Local practice material: deliberately vulnerable programs, synthetic
reproductions, and the fixtures that keep them honest. Everything here
runs locally and targets only its own process.

| Folder | Purpose |
| ------ | ------- |
| [`exploit/`](exploit/) | Exploit labs, organized by technique then language |

| Technique | Languages | What it teaches |
| --------- | --------- | --------------- |
| [RCE](exploit/RCE/) | C++, Python, Go, Rust, Node.js | Command injection, plus each language's own "attacker data becomes code" |
| [SQLi](exploit/SQLi/) | Python, Node.js | SQL injection: tautology and UNION-based extraction |

Start at [`exploit/RCE/README.md`](exploit/RCE/README.md).

Each lab ships a vulnerable program, a patched counterpart, an exploit
driver that reports what actually landed, and a written walkthrough. The
driver is a regression gate: it exits non-zero if a payload stops
working or a fix stops holding.

These are synthetic reproductions. Do not deploy them anywhere
reachable.

# labs/

Local practice material: deliberately vulnerable programs, synthetic
reproductions, and the fixtures that keep them honest. Everything here
runs locally and targets only its own process.

| Folder | Purpose |
| ------ | ------- |
| [`exploit/`](exploit/) | Exploit labs, organized by technique then language |

| Technique | Languages | What it teaches |
| --------- | --------- | --------------- |
| [RCE](exploit/RCE/) | C++, C, Python, Ruby, Go, Rust, Node.js | Command injection, plus each language's own "attacker data becomes code" |
| [SQLi](exploit/SQLi/) | C, Python, Node.js | SQL injection: tautology and UNION-based extraction |
| [PathTraversal](exploit/PathTraversal/) | C, Python, Node.js, Go | Reading files outside the directory you meant to serve |
| [SSRF](exploit/SSRF/) | Python, Node.js, Go | Making a server fetch a URL you chose |
| [Deserialization](exploit/Deserialization/) | Python, Ruby | Untrusted bytes that become code, or become state |

Start at [`exploit/RCE/README.md`](exploit/RCE/README.md).

Each lab ships a vulnerable program, a patched counterpart, an exploit
driver that reports what actually landed, and a written walkthrough. The
driver is a regression gate: it exits non-zero if a payload stops
working or a fix stops holding.

These are synthetic reproductions. Do not deploy them anywhere
reachable.

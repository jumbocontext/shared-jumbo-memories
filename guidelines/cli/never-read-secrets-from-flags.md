# Never read secrets from flags
Reasoning: Flag values are visible in `ps` output and shell history, making them unsafe for secrets. They also encourage storing credentials in plaintext in scripts and shell profiles.
Source: https://clig.dev/#arguments-and-flags

Accept secrets via:
- A dedicated file flag (e.g. `--password-file path/to/file`)
- `stdin` (pipe the secret in)
- A secrets manager or `AF_UNIX` socket

```bash
jumbo guideline add --category cli --title "Never read secrets from flags" --description "Do not accept secrets (passwords, tokens, keys) via flags. Flag values leak into ps output and shell history. Instead, accept secrets via a file flag (e.g. --password-file), stdin, or a secrets manager." --rationale "Flag values are visible in ps output and shell history, making them unsafe for secrets. They also encourage storing credentials in plaintext in scripts and shell profiles."
```

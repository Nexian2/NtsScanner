# ntsSubfinder (no API keys)

Simple passive subdomain enumerator inspired by subfinder. This distribution intentionally avoids providers that require API keys.

## Features
- Uses public/no-key providers:
  - crt.sh
  - dns.bufferover.run (Bufferover)
  - ThreatCrowd
  - Certspotter public API
- Multi-threaded provider querying
- Output in plain text (one per line) or JSON
- No API keys required

## Requirements
- Python 3.8+
- pip packages:
  pip install requests

## Install
1. Extract the ZIP.
2. Make the script executable (optional):
   chmod +x ntsSubfinder

## Usage
Basic:
```
./ntsSubfinder -d example.com
```

Save JSON:
```
./ntsSubfinder -d example.com -f json -o example_subs.json
```

Silent:
```
./ntsSubfinder -d example.com --silent
```

Options:
- `-d / --domain` target domain (required)
- `-o / --output` output file path (default: <domain>_subs.txt or .json)
- `-f / --format` text or json (default: text)
- `--threads` concurrent providers (default: 5)
- `--timeout` seconds for HTTP requests (default: 10)
- `--silent` minimize console output

## Notes and limitations
- Public endpoints may rate-limit or return inconsistent results.
- Some providers return certificate SANs or aggregated historical records which can include duplicates or wildcard entries.
- This tool focuses on providers that do not require API keys. For higher coverage consider adding API-backed providers (Shodan, Censys, Virustotal, etc.).

## License
Use responsibly. This tool is provided as-is with no warranty.

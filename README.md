# NtsScan 

## Install
```
chmod +x NtsScan
```
## Tutorial
./NtsScan -h
usage: NtsScan [-h] -d DOMAIN [-o OUTPUT] [-f {text,json}] [--threads THREADS] [--timeout TIMEOUT] [--silent] [--version]

NtsScan - Passive subdomain enumerator || NTSTeam

options:
  -h, --help            show this help message and exit
  -d, --domain DOMAIN   Target domain (example: example.com)
  -o, --output OUTPUT   Output file path (default: <domain>_subs.txt)
  -f, --format {text,json}
                        Output format
  --threads THREADS     Concurrent provider queries
  --timeout TIMEOUT     HTTP timeout in seconds
  --silent              Silent mode
  --version             Show version and exit

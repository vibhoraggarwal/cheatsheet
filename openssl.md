# OpenSSL

## Comparing certificates
```bash
# using key identifiers
openssl x509 -in <certificate_path> -noout -text | grep -A2 "Key Identifier"
```

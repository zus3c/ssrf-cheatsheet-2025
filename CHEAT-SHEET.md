# SSRF Cheat Sheet (2025)
*Adapted from Wallarm's SSRF Bible with 2025 updates.*

## Modern Attack Surfaces
### 1. AI/ML APIs
- **Exploit**: Forge requests to internal model-training endpoints.
- **Fix**: Validate `Host` headers in inference pipelines.

### 2. Cloud Metadata Services
- **Exploit**: Bypass IMDSv2 with HTTP smuggling.
- **Fix**: Enforce Hop-Limit=1 and token requirements.

## Protocol Allowlists (2025)
| Protocol | Allowed? | Notes                     |
|----------|----------|---------------------------|
| HTTP/3   | ❌       | Use HTTPS-only            |
| gRPC     | ✅       | Enable TLS + cert pinning |
| QUIC     | ❌       | Block at LB               |

[... Add remaining content from PDF ...]

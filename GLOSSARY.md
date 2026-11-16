# LearnHarness

An adaptive learning harness with persistent knowledge tracking and multi-provider model routing.

## Language

### Model Providers

**External CLI**:
A local agent CLI or ACP runtime invoked as a subprocess on the server host, owning its own authentication, routing, and billing.
_Avoid_: Built-in subscription, native provider

**CLI billing**:
Billing and quota controlled externally by an External CLI rather than priced by LearnHarness token rates.
_Avoid_: Free tier, $0 cost

**Antigravity Runtime**:
The local `agy_acp_server` or `agy acp` executable that speaks ACP over stdio for the Antigravity provider.
_Avoid_: Antigravity CLI, Antigravity profile

**Antigravity Profile**:
The private `GEMINI_HOME` directory holding Antigravity Google OAuth credentials and settings, stored alongside `LH_AUTH_FILE` secrets rather than inside learning data.
_Avoid_: Antigravity data dir, Antigravity runtime

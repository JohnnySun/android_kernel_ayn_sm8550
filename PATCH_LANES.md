# Kernel Patch Lanes

Source tree path: `kernel/ayn/sm8550`

The Odin2 Mini stock kernel reports `5.15.123-android13-8-g55ff82ab20b6`. Keep
bootability on the vendor 5.15 lane before attempting a larger kernel jump.

Patch classes:

| Class | Meaning |
|---|---|
| `UPSTREAM` | Already accepted in upstream Linux. |
| `BACKPORT` | Backported from newer upstream Linux into the active lane. |
| `FROMGIT` | Taken from a public Git tree but not clearly upstreamed. |
| `FROMLIST` | Taken from a public mailing list discussion. |
| `ANDROID` | From Android common kernel or GKI-specific work. |
| `ODIN-LOCAL` | Local device hack that needs an exit plan. |

Lanes:

| Lane | Branch family | Purpose |
|---|---|---|
| vendor-5.15 | stock-derived | Preserve boot and proprietary module compatibility. |
| ack-5.15 | `android13-5.15` / `android14-5.15` | Pull Android/LTS fixes without changing kernel generation. |
| latest-mainline | `android17-6.18` / `android-mainline` | Track future direction and upstreamability. |

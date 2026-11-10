# Gemma-4-E4B-it-Uncensored-NVFP4

[![Model](https://img.shields.io/badge/HuggingFace-AEON--7%2FGemma--4--E4B--it--Uncensored--NVFP4-yellow)](https://huggingface.co/AEON-7/Gemma-4-E4B-it-Uncensored-NVFP4)
[![☕ Tips](https://img.shields.io/badge/%E2%98%95_Tips-Support_the_work-ff5e5b?style=flat)](https://github.com/AEON-7/AEON-7#-support-the-work) [![Buy me a lotus tea on LotusMake](https://lotusmake.com/badges/lotus-tea-dark.v1.svg)](https://lotusmake.com/support?via=tea)
[![License](https://img.shields.io/badge/License-Gemma_Terms-green)](https://ai.google.dev/gemma/terms)

EAGLE-style speculative-decoding drafter for the Gemma 4 26B A4B-it Uncensored MoE, NVFP4-quantized for Blackwell-class GPUs (DGX Spark / RTX PRO 6000 / RTX 5090 / B100 / B200).

Pair with the matching target model for accelerated single-stream decode:
- **Target**: [`AEON-7/Gemma-4-26B-A4B-it-Uncensored-NVFP4`](https://huggingface.co/AEON-7/Gemma-4-26B-A4B-it-Uncensored-NVFP4) — measured **50 tok/s single, 1430 tok/s aggregate** on DGX Spark with this drafter wired in.
- **HuggingFace card**: [`AEON-7/Gemma-4-E4B-it-Uncensored-NVFP4`](https://huggingface.co/AEON-7/Gemma-4-E4B-it-Uncensored-NVFP4)

## Quick start (vLLM, as drafter)

```bash
vllm serve AEON-7/Gemma-4-26B-A4B-it-Uncensored-NVFP4 \
  --speculative-config '{"method":"eagle3","model":"AEON-7/Gemma-4-E4B-it-Uncensored-NVFP4","num_speculative_tokens":3}' \
  --trust-remote-code
```

## Related

- [`AEON-7/Gemma-4-31B-DECKARD-HERETIC-Uncensored-NVFP4`](https://github.com/AEON-7/Gemma-4-31B-DECKARD-HERETIC-Uncensored-NVFP4) — sister DECKARD HERETIC dense 31B target
- [`AEON-7/Gemma-4-E4B-DECKARD-HERETIC-Uncensored-NVFP4`](https://github.com/AEON-7/Gemma-4-E4B-DECKARD-HERETIC-Uncensored-NVFP4) — sister DECKARD HERETIC drafter
- [`AEON-7/comfyui-aeon-spark`](https://github.com/AEON-7/comfyui-aeon-spark) — the broader DGX Spark stack

## License

Inherits the [Gemma Terms of Use](https://ai.google.dev/gemma/terms). Use of this model is subject to those terms.

---

## ☕ Support the work

AEON-7 models, drafters and tools are built and trained independently, on my own hardware. If they're useful to you, please consider supporting development.

Patreon wrongfully shut down our account without notice and never responded to our appeals, so we built something even better. You can now support the work on **LotusMake**: buy us a Lotus Tea, fund GPU hours, back a project you want to see done, or subscribe for early and full access to publications while supporting what we build. You can become a creator there too: join, apply to become a creator, and get paid for the work you do in public.

[![Buy me a lotus tea on LotusMake](https://lotusmake.com/badges/lotus-tea-dark.v1.svg)](https://lotusmake.com/support?via=tea)

**[AEON FORGE on LotusMake → lotusmake.com/c/aeon-forge](https://lotusmake.com/c/aeon-forge)** · **[Subscribe for early and full access](https://lotusmake.com/support?mode=tiers&from=%2Fc%2Faeon-forge)**

Milestones unlock bigger work: reaching **500 paid supporters** will fund fine-tuning larger models and bigger project releases. Subscribers also get early access to new releases, such as the [AEON DFlash2 drafter](https://huggingface.co/AEON-7/AEON-DFlash2-Qwen3.8-27B).

If this release has been useful, tips are deeply appreciated — they go directly toward more compute, more models, and more open releases.

<table align="center">
  <tr>
    <td align="center" width="50%">
      <strong>₿ Bitcoin (BTC)</strong><br/>
      <img src="https://raw.githubusercontent.com/AEON-7/AEON-7/main/assets/qr/btc.png" alt="BTC QR" width="200"/><br/>
      <sub><code>bc1q09xmzn00q4z3c5raene0f3pzn9d9pvawfm0py4</code></sub>
    </td>
    <td align="center" width="50%">
      <strong>Ξ Ethereum (ETH)</strong><br/>
      <img src="https://raw.githubusercontent.com/AEON-7/AEON-7/main/assets/qr/eth.png" alt="ETH QR" width="200"/><br/>
      <sub><code>0x1512667F6D61454ad531d2E45C0a5d1fd82D0500</code></sub>
    </td>
  </tr>
  <tr>
    <td align="center" width="50%">
      <strong>◎ Solana (SOL)</strong><br/>
      <img src="https://raw.githubusercontent.com/AEON-7/AEON-7/main/assets/qr/sol.png" alt="SOL QR" width="200"/><br/>
      <sub><code>DgQsjHdAnT5PNLQTNpJdpLS3tYGpVcsHQCkpoiAKsw8t</code></sub>
    </td>
    <td align="center" width="50%">
      <strong>ⓜ Monero (XMR)</strong><br/>
      <img src="https://raw.githubusercontent.com/AEON-7/AEON-7/main/assets/qr/xmr.png" alt="XMR QR" width="200"/><br/>
      <sub><code>836XrSKw4R76vNi3QPJ5Fa9ugcyvE2cWmKSPv3AhpTNNKvqP8v5ba9JRL4Vh7UnFNjDz3E2GXZDVVenu3rkZaNdUFhjAvgd</code></sub>
    </td>
  </tr>
</table>

> **Ethereum L2s (Base, Arbitrum, Optimism, Polygon, etc.) and EVM-compatible tokens** can be sent to the same Ethereum address.

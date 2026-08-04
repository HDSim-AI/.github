<div align="center">

# 🏘️ HDSim

**An open-source multi-agent ecosystem for household decision-making simulation, built on the PEMAND method.**

<p>
<a href="https://yushundong.github.io/pemand_simulation/pemand_official_site.html"><img src="https://img.shields.io/badge/Live%20Demo-HDSim-2f7d5f?style=flat-square" alt="Live Demo"></a>
<a href="https://arxiv.org/abs/2604.10475"><img src="https://img.shields.io/badge/arXiv-2604.10475-b31b1b?style=flat-square" alt="Paper"></a>
<img src="https://img.shields.io/badge/License-MIT-blue?style=flat-square" alt="MIT">
</p>

<img src="./hdsim_hero.gif" width="85%" alt="A simulated household negotiating a travel decision">

[▶ Watch the full launch film](./hdsim_launch.mp4)

</div>

## What is this?

Household decisions like trip planning, residential relocation, and evacuation are negotiated by household members. They are not computed by one equation. PEMAND (Persona-Enriched Multi-Agent Negotiation for Household Decision-Making) simulates that negotiation: survey records become theory-grounded personas, members propose independently, and a moderated multi-agent conversation converges on the household's decision.

Evaluated on national and regional household surveys across travel and residential mobility, PEMAND outperforms classical ML and LLM baselines. See the [paper](https://arxiv.org/abs/2604.10475) for details.

## Repositories

| Repository | What it is |
|---|---|
| [`hdsim`](https://github.com/HDSim-AI/hdsim) | The method core: persona construction, proposals, moderated negotiation |
| [`travel-decision`](https://github.com/HDSim-AI/travel-decision) | Household trip planning and generation |
| [`residential-mobility`](https://github.com/HDSim-AI/residential-mobility) | Move-or-stay relocation decisions |

Start with `hdsim`. A recorded household negotiation replays in the terminal with no API key and no
data download:

```bash
git clone https://github.com/HDSim-AI/hdsim && cd hdsim
pip install -e .
hdsim demo
```

A decision domain is configuration rather than a new pipeline, so adding one means writing a
`DomainConfig` and a survey loader. `travel-decision` is the reference implementation.

## Contributing

New decision domains such as energy use, major purchases, and family planning are welcome, along with agent skills, datasets, and evaluations. Open an issue in the relevant repository to get started.

<sub>MIT licensed. Try the <a href="https://yushundong.github.io/pemand_simulation/pemand_official_site.html">live demo</a>: six replayable household scenarios, no setup required.</sub>

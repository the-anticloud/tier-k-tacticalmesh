# Deploy Guide — K_TACTICALMESH
**Tier:** TIER_8_RF_MESH_DEFENSE | **Stack:** Python 3.11, meshtastic (LoRa), PAX 27B, AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, meshtastic 2.x Python library. Meshtastic LoRa devices (T-Beam, T-Echo) per node.

## Environment
Meshtastic devices per mesh node. USB serial for gateway node. 4GB RAM on gateway.

## AIOSS Integration
```bash
aioss init --module K_TACTICALMESH --output ./k_tacticalmesh.aioss
aioss append --chain ./k_tacticalmesh.aioss --payload ./output.bin --module K_TACTICALMESH
aioss verify --chain ./k_tacticalmesh.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="K_TACTICALMESH",
    aioss_chain="./K_TACTICALMESH.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./K_TACTICALMESH.aioss --verbose
python -m K_TACTICALMESH.tests.smoke
```

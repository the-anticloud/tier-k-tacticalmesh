# Developer Cookbook — K_TACTICALMESH
**Stack:** Python 3.11, meshtastic (LoRa), PAX 27B, AIOSS_FORMAT
**Domain:** TacticalMesh: multi-hop tactical radio mesh for Anticloud off-grid deployments

## Tactical mesh PAX inference relay
```python
from k_tacticalmesh import TacticalMeshGateway

gateway = TacticalMeshGateway(
    serial_port="COM5",  # Meshtastic device
    pax_model="./pax-27b-q4.gguf",
    aioss_chain="./tacticalmesh.aioss"
)

gateway.start()
for request in gateway.inference_requests():
    response = gateway.pax_inference(request.prompt, request.schema)
    gateway.send_response(request.source_node, response)
    print(f"Served node {request.source_node}: {response.summary}")
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```

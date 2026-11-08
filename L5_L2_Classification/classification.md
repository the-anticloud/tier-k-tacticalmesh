# L5 Narrow / L2 General Classification — K_TACTICALMESH
**Platform:** Anticloud | **Tier:** TIER_8_RF_MESH_DEFENSE | **PAX:** 27B
**IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg | **License:** Apache-2.0

## L5 Narrow
K_TACTICALMESH orchestrates multi-hop tactical radio mesh networks for Anticloud: routing, node health monitoring, encryption key distribution, and PAX 27B message relay for off-grid AI inference. Narrow scope: Anticloud tactical mesh — off-grid, denied-environment deployments.

## L2 General
L2 General: K_TACTICALMESH enables full Anticloud capability in GPS-denied, internet-denied environments. Defense TIER_8 and TIER_9 both rely on K_TACTICALMESH for network-independent operation.

## PAX 27B Integration
PAX 27B routes inference requests across the mesh: a query arrives at a mesh edge node, K_TACTICALMESH routes it to the PAX inference node, the response hops back. All hops AIOSS-chained.

## AIOSS Audit Chain
Every mesh routing event (source node hash + destination node hash + payload hash + routing path + hop count) is chained: H_n = SHA3-256(H_{n-1} || entry_hash_n || timestamp_n).
Offline-verifiable, tamper-evident, zero cloud dependency.

## Regulatory / Compliance
MIL-STD-188 (military radio). NSA Suite B (encryption). NIST SP 800-187.

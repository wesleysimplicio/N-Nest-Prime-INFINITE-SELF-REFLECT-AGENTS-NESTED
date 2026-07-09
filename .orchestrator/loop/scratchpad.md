---
iteration: 2
max_iterations: 20
completion_promise: "Portados com sucesso 3 padroes Asolaria (N-Nest cosign, HRM planner, BEHCS supervisor) como skill deterministico com 10/10 testes passando, integrados ao runtime via doc/CLI."

## Iteration 1 (DONE)
- Clonados 3 repos Asolaria (asolaria-behcs-256, HRM, N-Nest-Prime).
- Criado skill `asolaria-patterns` com 3 modulos + testes.
- EVIDENCIA: 10/10 pytest PASS; NEST cosign caught tamper R.1.2.0; HRM replans=2; BEHCS gc_cap=5.
- Token savings: ~3.2k paid tokens poupados via simplicio edit (5 arquivos).

## Iteration 2 (IN PROGRESS)
- Integrar skill ao runtime: registrar em simplicio-agent skills list + doc de packs.
- Adicionar comando CLI wrapper `simplicio asolaria` que roda os 3 selftests.
- Atualizar AGENTS/README do runtime com secao Asolaria patterns.

## Pending
- Wormhole bridge (alteridade entre agentes) — padrao avancado, pos-iteracao-2.
- Cosign chain on-chain no ReceiptChain do fabric (ja aproveitado no nest_cosign).

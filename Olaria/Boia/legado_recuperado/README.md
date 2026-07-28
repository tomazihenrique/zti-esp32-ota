# Binários recuperados do repositório antigo `firmwares_esp32` (apagado em 28/07/2026)

Antes de recriar o firmware do Olaria do zero (ver `../../../README.md` e o repo `zti-esp32-firmwares`), foi feita uma tentativa anterior (jun/2025) de montar um sistema de OTA — o usuário confirmou que **não deu certo** na época. Só a boia do Olaria chegou a ter binários reais publicados; a bomba e o "poco2" ficaram só com stubs vazios (48 bytes) e foram descartados.

Esses 2 arquivos são imagens ESP32 válidas (magic byte `0xE9` confirmado) com strings que referenciam `poco1/boia/estado` e URLs de OTA apontando pro próprio repo antigo — ou seja, é firmware real que já rodou (ou quase rodou) na boia do Olaria.

**Não são usados pelo mecanismo de OTA atual.** Guardados só como referência histórica, caso seja útil comparar com o binário do firmware novo (`../../../PinhalNovo`, `../../../Olaria` no repo `zti-esp32-firmwares`) via `diff`/`strings` no futuro. Não há garantia de que correspondam à versão realmente gravada na placa física hoje.

- `firmware_v1.0.1.bin` (era `poco1/boia/firmware_v1.0.1.bin`)
- `firmware_v1.1.1.bin` (era `poco1/boia/1.1.1.bin`, também referenciado como "latest" no `latest.txt` — provável erro de digitação, que apontava pra `v1.0.11`, inexistente)

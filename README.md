# ZTI ESP32 OTA — Distribuição de firmware

Repositório **público**, só com binários compilados (`.bin`) e manifesto de versão (`version.json`) por placa. Não contém código-fonte nem credenciais — o código-fonte fica em [zti-esp32-firmwares](https://github.com/tomazihenrique/zti-esp32-firmwares) (privado).

As placas com WiFi checam `<Poço>/<Placa>/version.json` a cada 6h e, se a versão for maior que a gravada, baixam `<Poço>/<Placa>/firmware.bin` e se atualizam sozinhas via OTA (biblioteca `HTTPUpdate`).

## Como publicar uma nova versão

1. Bump no `#define FIRMWARE_VERSION "x.y.z"` do sketch (repo privado).
2. Compilar (`arduino-cli compile --export-binaries ...`).
3. Substituir o `firmware.bin` correspondente aqui.
4. Atualizar o `version.json` correspondente com a mesma versão.
5. Commit + push. As placas pegam a atualização na próxima checagem (até 6h).

## Placas com OTA automático

- Palmeira1/Bomba
- Pinhalzinho/Boia
- Pinhalzinho/Bomba

## Fora do OTA automático

- **Palmeira1/Boia** — só tem rádio LoRa, sem WiFi (decisão de projeto, para não depender de internet no ponto sem sinal decente). Atualização continua manual via USB.

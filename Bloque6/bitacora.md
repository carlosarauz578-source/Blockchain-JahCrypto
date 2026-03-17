## 📖 Bloque 6 – Escalabilidad y Layer 2
```markdown
# 📖 Bitácora JahCrypto – Bloque 6

## 📌 Objetivo del Bloque
- Entender los problemas de escalabilidad en Ethereum【16†source】.
- Conocer soluciones Layer 2: Optimism, Arbitrum, zkSync【17†source】.
- Implementar un ejemplo de transacción simulada.

## 📝 Reflexiones
- La congestión eleva los costos de gas【16†source】.
- Layer 2 aumenta velocidad y reduce costos【17†source】.
- La adopción masiva depende de estas soluciones.

## 📚 Aprendizajes
- Rollups optimistas y zk‑rollups.
- Sidechains vs Layer 2.
- Ejemplo: Base de Coinbase【17†source】.

## 🚀 Mini-proyecto
```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract PagoSimulado {
    mapping(address => uint) public balances;

    function depositar() public payable {
        balances[msg.sender] += msg.value;
    }
}

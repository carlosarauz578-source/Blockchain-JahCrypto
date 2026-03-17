---

## 📖 Bloque 7 – Finanzas Descentralizadas (DeFi)
```markdown
# 📖 Bitácora JahCrypto – Bloque 7

## 📌 Objetivo del Bloque
- Comprender el ecosistema DeFi【19†source】.
- Analizar préstamos, intercambios y yield farming.
- Implementar un contrato de préstamo básico.

## 📝 Reflexiones
- DeFi elimina intermediarios financieros【19†source】.
- Los usuarios mantienen custodia de sus activos【20†source】.
- Riesgos: volatilidad, exploits, regulación.

## 📚 Aprendizajes
- Protocolos: Uniswap, Aave, Compound.
- Stablecoins y liquidez.
- Gobernanza en DeFi.

## 🚀 Mini-proyecto
```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract PrestamoBasico {
    mapping(address => uint) public deuda;

    function pedirPrestamo(uint monto) public {
        deuda[msg.sender] += monto;
    }
}

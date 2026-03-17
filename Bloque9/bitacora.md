---

## 📖 Bloque 9 – Seguridad en Web3
```markdown
# 📖 Bitácora JahCrypto – Bloque 9

## 📌 Objetivo del Bloque
- Comprender riesgos y mejores prácticas de seguridad en Web3【10†source】.
- Analizar vulnerabilidades en smart contracts.
- Implementar un contrato seguro con `require`.

## 📝 Reflexiones
- En 2024 se perdieron más de $1B por exploits【10†source】.
- La seguridad debe estar integrada desde el inicio.
- Los contratos son inmutables, un error es irreversible【10†source】.

## 📚 Aprendizajes
- Auditorías de contratos.
- Uso de librerías seguras (OpenZeppelin).
- Buenas prácticas: validaciones, límites, multi‑firma.

## 🚀 Mini-proyecto
```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract BilleteraSegura {
    mapping(address => uint) public balances;

    function depositar() public payable {
        require(msg.value > 0, "Debe enviar ETH");
        balances[msg.sender] += msg.value;
    }
}

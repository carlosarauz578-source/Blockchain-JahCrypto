# 📖 Bitácora JahCrypto – Bloque 5

## 📌 Objetivo del Bloque
- Comprender qué son los oráculos blockchain.
- Analizar cómo conectan contratos inteligentes con datos externos.
- Implementar un ejemplo de oráculo simulado.

## 📝 Reflexiones
- Los smart contracts no pueden acceder a datos fuera de la blockchain【5†source】.
- Los oráculos actúan como puente entre el mundo real y la cadena【6†source】.
- Tipos: software, hardware, inbound/outbound, centralizados y descentralizados【5†source】.

## 📚 Aprendizajes
- El “problema del oráculo”: confianza en la fuente externa【5†source】.
- Ejemplos: precios de activos, resultados deportivos, clima.
- Herramientas: Chainlink, Band Protocol.

## 🚀 Mini-proyecto
```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract OraculoSimulado {
    uint public precioETH;

    function actualizarPrecio(uint _nuevoPrecio) public {
        precioETH = _nuevoPrecio;
    }
}

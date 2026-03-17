# 📖 Bitácora JahCrypto – Bloque 2

## 📌 Objetivo del Bloque
- Configurar entorno de desarrollo profesional para blockchain.
- Instalar y usar VSCode, Node.js y Solidity.
- Migrar flujo de trabajo de Termux a PC/laptop.

## 📝 Reflexiones
- Un entorno bien configurado acelera el aprendizaje y evita errores.
- VSCode con extensiones de Solidity y GitHub mejora la productividad.
- Node.js es esencial para ejecutar scripts y frameworks Web3.
- Migrar de Termux a PC replica estándares de la industria.

## 📚 Aprendizajes
- Instalación de Node.js y npm para manejar dependencias.
- Configuración de VSCode con extensiones: Solidity, GitHub Copilot, Markdown.
- Uso de `npm init` para proyectos básicos.
- Compilación de contratos con `solc`.

## 🚀 Mini-proyecto del Bloque
Crear un contrato simple en Solidity:
```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract HolaBlockchain {
    string public mensaje = "Hola, JahCrypto!";
}

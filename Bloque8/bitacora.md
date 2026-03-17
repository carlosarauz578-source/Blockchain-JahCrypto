---

## 📖 Bloque 8 – NFTs y Marketplaces
```markdown
# 📖 Bitácora JahCrypto – Bloque 8

## 📌 Objetivo del Bloque
- Comprender el mercado de NFTs【1†source】.
- Analizar plataformas como OpenSea y Blur【1†source】【3†source】.
- Implementar un contrato NFT básico.

## 📝 Reflexiones
- Los NFTs representan propiedad digital única.
- Marketplaces impulsan la adopción masiva.
- Competencia creciente entre plataformas【1†source】.

## 📚 Aprendizajes
- ERC‑721 y ERC‑1155.
- Royalties y derechos de autor.
- Casos de uso: arte, juegos, coleccionables.

## 🚀 Mini-proyecto
```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract NFTSimple {
    uint public totalMinted;
    mapping(uint => address) public ownerOf;

    function mint(address to) public {
        totalMinted++;
        ownerOf[totalMinted] = to;
    }
}

# 📖 Bitácora JahCrypto – Bloque 3

## 📌 Objetivo del Bloque
- Comprender los estándares de tokens ERC‑20 y ERC‑721.
- Diferenciar entre tokens fungibles y no fungibles.
- Implementar contratos básicos en Solidity.

## 📝 Reflexiones
- ERC‑20 es la base de la mayoría de criptomonedas en Ethereum.
- ERC‑721 introdujo los NFTs, únicos y no intercambiables.
- Los estándares facilitan interoperabilidad y confianza en Web3.

## 📚 Aprendizajes
- ERC‑20: define funciones como `transfer`, `balanceOf`, `approve`.
- ERC‑721: define funciones como `ownerOf`, `safeTransferFrom`.
- Importancia de interfaces (`IERC20`, `IERC721`) en Solidity.
- Uso de OpenZeppelin para contratos seguros y auditados.

## 🚀 Mini-proyecto del Bloque
Crear dos contratos simples:

### ERC‑20 básico
```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract TokenBasico {
    string public name = "JahToken";
    string public symbol = "JAH";
    uint8 public decimals = 18;
    uint256 public totalSupply = 1000000 * 10**18;
    mapping(address => uint256) public balanceOf;

    constructor() {
        balanceOf[msg.sender] = totalSupply;
    }

    function transfer(address to, uint256 amount) public returns (bool) {
        require(balanceOf[msg.sender] >= amount, "Saldo insuficiente");
        balanceOf[msg.sender] -= amount;
        balanceOf[to] += amount;
        return true;
    }
}
  
#Contrato ERC‑721 básico
`solidity   // SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract NFTBasico {
    string public name = "JahNFT";
    string public symbol = "JNFT";
    uint256 public totalMinted;
    mapping(uint256 => address) public ownerOf;

    function mint(address to) public {
        totalMinted++;
        ownerOf[totalMinted] = to;
    }
}

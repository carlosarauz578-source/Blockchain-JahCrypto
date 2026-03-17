# 📖 Bitácora JahCrypto – Bloque 4

## 📌 Objetivo del Bloque
- Comprender qué son las DAOs (Organizaciones Autónomas Descentralizadas).
- Analizar cómo funciona la gobernanza descentralizada en Web3.
- Implementar un contrato básico de votación en Solidity.

## 📝 Reflexiones
- Las DAOs permiten que comunidades tomen decisiones colectivas sin jerarquías tradicionales.
- La gobernanza descentralizada da poder a los usuarios mediante tokens de voto.
- La transparencia en blockchain fortalece la confianza en procesos democráticos digitales.
- Los retos actuales incluyen baja participación y concentración de poder en grandes poseedores de tokens.

## 📚 Aprendizajes
- **DAO**: organización gestionada por contratos inteligentes y reglas codificadas.
- **Modelos de gobernanza**: voto ponderado por tokens, voto cuadrático, reputación, multi‑firma.
- **Proceso de votación**: propuestas, votos, ejecución automática.
- Herramientas: OpenZeppelin Governor, Snapshot, Aragon.

## 🚀 Mini-proyecto del Bloque

### Contrato de votación básico
```solidity
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.0;

contract VotacionBasica {
    struct Propuesta {
        string descripcion;
        uint votos;
    }

    Propuesta[] public propuestas;
    mapping(address => bool) public yaVoto;

    function crearPropuesta(string memory _descripcion) public {
        propuestas.push(Propuesta(_descripcion, 0));
    }

    function votar(uint _indice) public {
        require(!yaVoto[msg.sender], "Ya votaste");
        require(_indice < propuestas.length, "Propuesta invalida");
        propuestas[_indice].votos++;
        yaVoto[msg.sender] = true;
    }

    function obtenerGanadora() public view returns (string memory descripcion) {
        uint maxVotos = 0;
        uint indiceGanador = 0;
        for (uint i = 0; i < propuestas.length; i++) {
            if (propuestas[i].votos > maxVotos) {
                maxVotos = propuestas[i].votos;
                indiceGanador = i;
            }
        }
        return propuestas[indiceGanador].descripcion;
    }
}

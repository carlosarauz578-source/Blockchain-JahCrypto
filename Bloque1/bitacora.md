# 📖 Bitácora JahCrypto – Bloque 1

## 📌 Objetivo del Bloque
- Comprender los fundamentos de blockchain.
- Entender qué son los smart contracts.
- Introducir el concepto de Web3.

## 📝 Reflexiones
- Blockchain no es solo criptomonedas, es una infraestructura para confianza digital.
- Los smart contracts eliminan intermediarios y automatizan acuerdos.
- Web3 cambia la forma en que los usuarios poseen y controlan sus datos.

## 📚 Aprendizajes
- **Blockchain**: registro distribuido, seguro e inmutable.
- **Smart Contracts**: programas que ejecutan acuerdos automáticamente.
- **Web3**: nueva Internet descentralizada con propiedad digital.
- **DeFi**: finanzas descentralizadas.
- **DAO**: organizaciones autónomas gobernadas por código.

---

# Bloque 1 – Fundamentos de Blockchain

## Teoría
- Un **hash** es una función criptográfica que convierte datos en una cadena única de caracteres.  
- Propiedades principales:
  - Determinístico: la misma entrada siempre produce la misma salida.  
  - Irreversible: no se puede obtener la entrada original desde el hash.  
  - Sensible a cambios mínimos: un cambio en la entrada altera completamente el hash.  
- Algoritmo usado: **SHA-256**, estándar en la mayoría de blockchains.

## Práctica
1. **Generación de hash**  
   - Comando: `echo "Carlos" | sha256sum`  
   - Resultado: `dc867bdab95e9182f787742ddad958a5c21fe69751f24e85722e9de85a80cf`

2. **Creación de bloque**  
   - Archivo: `bloque1.txt`  
   - Contenido:  
     ```
     Transacción A → B: 10 tokens
     Hash del Bloque1: dc867bdab95e9182f787742ddad958a5c21fe69751f24e85722e9de85a80cf
     ```

3. **Bloque enlazado**  
   - Archivo: `bloque2.txt`  
   - Contenido:  
     ```
     Transacción B → C: 20 tokens
     Hash del Bloque1: dc867bdab95e9182f787742ddad958a5c21fe69751f24e85722e9de85a80cf
     ```
   - Hash del Bloque2: `812354fc13fb06ef1a8e7fbd10218a25048001a40830d585776eb215abfa9a7a`

## Evidencia
- VPS conectado vía SSH (Debian GNU/Linux).  
- Hashes generados y verificados en terminal.  
- Archivos subidos y organizados en GitHub.  

### Resultado
- Bloque1 contiene su transacción y hash.  
- Bloque2 incluye el hash del Bloque1 y su propia transacción.  
- Si se modifica Bloque1, el hash de Bloque2 también cambia → demostración de integridad y encadenamiento.

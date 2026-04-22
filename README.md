# 🌀 Fractalyxweblite

**Criptografía basada en el Modelo Fractal-Estocástico Unificado**

## Ecuación central

```
∂ψ/∂t = −δF·(−Δ)^(β/2)ψ  +  γ|ψ|²ψ  +  σ·η(x,t)
δF=0.921  ·  β=1.079  ·  H=0.541
```

## Características

- 🌀 **FractalShield** — 3 niveles de protección adaptativa por capas
- 🔒 **Cifrado MFSU v3** — KDF memory-hard 8MB + HMAC-SHA3
- 🔑 **Hash Merkle-Damgård Fractal** — mensaje alimenta el campo ψ
- 🕐 **2FA TOTP** — anti-replay con ventana deslizante
- 🛡️ **Medidor de fortaleza** — entropía real + tiempo de fuerza bruta
- 🌀 **Generador de contraseñas fractal** — reproducible desde frase semilla
- 🔍 **Inspector de archivos** — analiza .fracta/.shield sin contraseña

## Instalación local

```bash
pip install -r requirements.txt
streamlit run app.py
```

## Demo online

[![Streamlit App](https://static.streamlit.io/badges/streamlit_badge_black_white.svg)](https://mfsu-vault.streamlit.app)

## Uso

1. Selecciona el nivel de protección FractalShield (1-3)
2. Sube tu archivo y escribe una contraseña fuerte
3. Descarga el archivo `.shield` cifrado
4. Para descifrar: sube el `.shield` con la misma contraseña

## Niveles FractalShield

| Nivel | Capas | Costo atacante | Uso recomendado |
|-------|-------|----------------|-----------------|
| 🛡️ Estándar  | 3 | 3.5× | Documentos personales |
| 🔒 Reforzado | 4 | 7.5× | Contratos, datos financieros |
| 💎 Máximo    | 5 | 15.5× | Secretos críticos |

## Paper

[MFSU-Crypt: A Novel Symmetric Cryptographic System Based on the Unified Fractal-Stochastic Model](./MFSU_Crypt_Paper_v1.docx)


---

## Architecture

### 1. Core MFSU Solver
```mermaid
flowchart TD
    A[Password + Salt] --> B[SHA3-512 → Initial ψ]
    B --> C[Scratchpad Fill\nKDF_M steps]
    C --> D[Non-linear Mixing\nState-dependent access]
    D --> E[Condensation + HKDF-Expand]
    E --> F[96-byte Derived Key]
    subgraph MFSU Core
        G[Fractional Laplacian\nβ = 1.079]
        H[Fractional Gaussian Noise\nH = 0.541]
        I[Non-linear term + Normalization]
    end
    C -.-> G & H & I

2. FractalShield Layered Defensemermaid

flowchart TD
    P[Password] --> KDF[KDF_M = 256]
    KDF --> Real[Real Layer\nMFSU\x04 + Plaintext]
    KDF --> D1[Decoy Layer 1\nKDF_M = 512]
    KDF --> D2[Decoy Layer 2\nKDF_M = 1024]
    KDF --> Dn[Decoy Layer N\nKDF_M = 4096]
    
    subgraph Layers [All layers identical size & statistics]
        Real
        D1
        D2
        Dn
    end
    
    Layers --> Shuffle[Fractal Shuffle\nORDER_ENC encrypted with real key]
    Shuffle --> File[.fracta v4 File\n+ Global HMAC-SHA3-256]
    
    style Real fill:#00b8ff,stroke:#fff

Key FeaturesMemory-hard KDF with 8 MB fractal scratchpad (scalable)
Oracle-free verification via FractalShield
Geometric cost escalation (attacker pays up to 15.5× more)
Stream cipher with SHA3-256 whitening + avalanche > 49%
Merkle-Damgård fractal hash
TOTP 2FA integrated
Constant-time normalization (timing-attack resistant)
CLI + beautiful Streamlit web UI
File format .fracta v4 (fully documented)

Installationbash

git clone https://github.com/Fracta-Axis/Fractalyx.git
cd Fractalyx
pip install -r requirements.txt

Quick StartWeb Interface (recommended)bash

streamlit run ui/fracts_vault.py

CLIbash

# Encrypt with Maximum protection
python -m cli --encrypt secret.pdf --password "MiContraseñaMuySegura123" --level 3

# Decrypt
python -m cli --decrypt secret.pdf.fracta --password "MiContraseñaMuySegura123"

Security & PerformanceProtection Level
Layers
User Time
Attacker Cost
Use Case
Standard
3
~0.5 s
3.5×
Personal files
Enhanced
4
~0.7 s
7.5×
Contracts & credentials
Maximum
5
~1.3 s
15.5×
Critical / legal data

Important Disclaimer
This is an experimental research project.
It has not received formal cryptographic audit.
Do not use it to protect valuable or sensitive information until independent review is complete.Roadmap to Certification (from the paper)Phase 1 (2026): Full NIST STS, arXiv preprint, public cryptanalysis
Phase 2 (2027): Formal IND-CPA / IND-CCA2 proofs + memory-hardness DAG
Phase 3 (2028): NIST-style submission & mobile ports

LinksFull Paper v2.0 (MFSU-Crypt + FractalShield): Zenodo
FractalShield module: `fractalshield.py`
Core MFSU implementation: core/field.py + crypto/cipher.py

LicenseApache License 2.0 — feel free to use, modify and contribute.Made with passion by Miguel Ángel Franco León
Independent Researcher — Fracta-Fractalyx Project“The same physical law that governs the fractal structure of the universe can also protect our data.”

---

### 💠 Wikidata & Standards
Este proyecto y el formato `.fyx` están registrados en **Wikidata** como un estándar de código abierto para la representación y cifrado de datos mediante algoritmos fractales.
- **Formato:** .fyx (Fractal Exchange Format)
- **Seguridad:** Cifrado basado en complejidad recursiva y mapeo de coordenadas.


## Licencia

Apache-2.0 License — © 2026 Miguel Ángel Franco León / Fracta-Fractalyx Project

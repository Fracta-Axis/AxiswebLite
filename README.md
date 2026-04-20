# 🌀 Axisweblite

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

## Licencia

MIT License — © 2026 Miguel Ángel Franco León / Fracta-Axis Project

# assistente-ia-juridico3 — Projeto Android Puro (WebView)

**Sem Capacitor · Sem npm · Sem Node.js**

## Como compilar

### Método 1: GitHub Actions (sem instalar nada — RECOMENDADO)
O repositório já tem o workflow em `.github/workflows/build-apk.yml`.
Basta fazer push e aguardar ~5 min. O APK aparece em Releases.

### Método 2: Android Studio
1. Abra Android Studio → File → Open → pasta `android/`
2. Aguarde o Gradle sincronizar (sem npm, muito mais rápido)
3. Build → Build APK(s)
4. APK em: `android/app/build/outputs/apk/debug/app-debug.apk`

## Estrutura
```
android/
├── app/
│   ├── build.gradle          ← Só appcompat (sem Capacitor)
│   └── src/main/
│       ├── assets/
│       │   └── index.html    ← Seu app (embutido no APK)
│       ├── java/.../
│       │   └── MainActivity.java  ← WebView wrapper simples
│       └── AndroidManifest.xml
├── build.gradle
├── settings.gradle
└── gradlew
.github/workflows/build-apk.yml  ← CI automático
```

## Config
- **Package:** `com.meuapp.assistenteiajuridico`
- **Versão:** 1.0.6 (code: 3)
- **Min SDK:** Android 22+ (5.0+)
- **Orientação:** any
- **Dependências:** apenas `androidx.appcompat:appcompat:1.7.0`

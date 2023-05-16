---
sidebar_position: 3
---

# useTranslation

Ашиглахаас өмнө **App Root** хэсэгт **TranslationContextProvider** тавьж өгнө. Энэ **Provider** нь **dict** гэх **props** авна. 

> Dictionary Format

```json

  "HEADING_CREATE_ORG": {
    "mn": "Байгууллага үүсгэх",
    "en": "Create organization"
  }

```

> App Root config

```typescript

import { TranslationContextProvider } from "@sales24/client"

const dict = {
  "HEADING_CREATE_ORG": {
    "mn": "Байгууллага үүсгэх",
    "en": "Create organization"
  }
}

function App({Component, pageProps, cookies}) {
  return (
    <TranslationContextProvider dict={dict}>
      <Component {...pageProps} />
    </TranslationContextProvider>
  )
}

```

> Ашиглах

```typescript

import { useTranslation } from "@sales24/client"

function Component() {
  const { t } = useTranslation();

  return (
    <p>
      {t("HEADER_LOGIN")}
    </p>
  )

}

```
---
sidebar_position: 1
---

# useCookies

> CSR хэсэгт ашиглах

```typescript

import { useCookies } from "@sales24/client"

function Component() {
   const cookies = useCookies();
}

```
> SSR хэсэгт ашиглах. 

Ирсэн Request заавал дамжжуулж өгнө.

```typescript

const cookies = useCookies(req) // req.headers.cookie шалгадаг

```
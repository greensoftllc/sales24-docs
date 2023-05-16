---
sidebar_position: 1
---

# useApollo

> CSR хэсэгт ашиглах

```typescript

import { useApollo } from "@sales24/client"

function Component() {
   const client = useApollo();
   /.../

   const fetchData = async () => {
      const { data } = await client.query({ query: GET_ORG_ID, variables: { orgSlug } });
      /.../
   } 

   /.../

}

```
> SSR хэсэгт ашиглах. 

Ирсэн Request заавал дамжжуулж өгнө.

```typescript

const client = useApollo(req)

```
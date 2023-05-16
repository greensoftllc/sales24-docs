---
sidebar_position: 1
---

# Эхлэл

Энэ сан нь цэвэр **Nextjs** framework дээр **Chakra** сантай хоршиж ажиллана. **@sales24/client** санд түгээмэл ашиглагдах **components, layout, hooks, types** орсон. 

 
```bash

yarn add @sales24/client @chakra-ui/react @emotion/react @emotion/styled framer-motion

```

> Sales24 үндсэн **Chakra Theme Config** тохируулах.

```typescript

import { ChakraProvider } from '@chakra-ui/react'
import { ChakraThemeSetting } from '@sales24/client'

const theme = ChakraThemeSetting();
function App() {
  return (
    <ChakraProvider>
      <TheRestOfYourApplication />
    </ChakraProvider>
  )
}

```

Хэрэв нэмэлт өөрчлөлт хийх бол **ChakraThemeSetting** функц **extendBaseTheme** функруу утга дамжуулж өгч чадна.

```typescript

const theme = ChakraThemeSetting({
  components: {
    Button,
  },
})

```



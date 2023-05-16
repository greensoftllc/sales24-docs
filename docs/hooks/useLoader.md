---

---

# useLoader

Ашиглахын өмнө **App Root** хэсэгт заавал **LoaderContext** оруулсан байх хэрэгтэй

```tsx

import { LoaderContext } from "@sales24/client";
import { useState } from "react";

function App() {
  const [isLoading, setIsLoading] = useState(false);

  return (
    <LoaderContext.Provider value={{ isLoading, setIsLoading }}>
      <Component />
    </LoaderContext.Prodider>
  )
}

```

> Ашиглах

```tsx

import { useLoader } from "@sales24/client";

function Component() {
  const { setIsLoading } = useLoader();
  
  const LoadHandler = async () => {
    setIsLoading(true); // Loader асаах

    fetch(/.../).then().catch()

    setIsLoading(false); // Loader унтраах
  } 
}

```
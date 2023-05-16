
# useFormValidator


```tsx

import { useFormValidator } from "@sales24/client"


function Component() {
  const { values, getFieldProps, validateForm } = useFormValidator(
    {
      email: "",
      password: "",
    },
    {
      password: {
        validator: (value: string) => value.length >= 4 && value.length <= 20,
        message: "Password must greater than 4 and lower than 20",
      },
      email: {
        validator: (value: string) => /^[A-Z0-9._%+-]+@[A-Z0-9.-]+\.[A-Z]{2,}$/i.test(value),
        message: "Please. Try valid email.",
      },
    }
  );

  const submit = () => {
    const { isValid } = validateForm();
    if (!isValid) return;
    
    // Success for doing next job...
  }

  return (
    <>
      <Input {...getFieldProps("email")} />
      <Input {...getFieldProps("password")} />
      <Button onClick={submit} />
    </>
  )
}

```
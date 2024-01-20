# use-deeebounce

A React hook for debouncing values in functional components.

## Installation

You can install the package using npm:

```bash

yarn add use-deeebounce
# or
npm install use-deeebounce
```

## Usage
```javascript

import React, { useState } from 'react';

//import useDebouce as a named export
import { useDebounce } from 'use-deeebounce';

export const Input = () => {
  const [inputValue, setInputValue] = useState('');

  // Set the duration for debouncing and provide the hook with a string value to debounce.
  const debouncedInputValue = useDebounce(inputValue, 5 * 100);

  return (
    <div>
      <label>Input:</label>
      <input type="text" value={inputValue} onChange={(e)=>setInputValue(e.target.value)} />
      {/* see the debounced query here */}
      <p>Debounced Value: {debouncedInputValue}</p>
    </div>
  );
};

```

# React with Typescript & Sass examples.

## Routing using react-router-dom v6
 - react-router-dom v6
 ```js
    // in index.tsx
    <BrowserRouter>  
      <App />
    </BrowserRouter>
 ```
 ```js
    // in App.tsx
    <Routes>
      <Route path="/" element={<Layout />}>
        <Route path="/intro" element={<Intro />} />
        <Route path="/about" element={<About />} />
        <Route path="/home" element={<Home />} />
      </Route>
    </Routes>
 ```

 ## React Test Library
  1. Select
    - getBy... -> queryBy... -> testId
  2. Mock localStorage
  ```js 
  Object.defineProperty(window, "localStorage", {
      value: {
        getItem: jest.fn(() => null),
        setItem: jest.fn(() => null),
        removeItem: jest.fn(() => null)
      },
      writable: true
    });
  ``` 
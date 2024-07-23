## memo

Check old prop value and new prop value, and if they do not have any changes, it prevents re-rendering.

**Do not overuse memo()**

-  Use it as high up in the component tree as possible

**Checking props with memo() costs performance.**

-  If you overuse this. it will cause a lot of unnecessary checkings

## **Note:** No more useMemo/useCallback in React 19!

## useCallback()

Whenever a function executes, the nested functions are re-created and this causes re-rendering unnecessary components. This can be prevented by using `useCallback`

## useMemo()

useMemo will wrap the normal function in the components to prevent their executions. This should only be used when the function has complicated calculations.

## Why is `key` important?

If the components' positions can vary, we should give them unique keys to keep track of the items. This is why we sometimes encounter weird bugs when we use indices as keys. Additionally, using a unique key can make the performance of the application stable.

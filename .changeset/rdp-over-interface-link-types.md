---
"@osdk/client": patch
---

Support derived properties over interface link types in `withProperties`. The first `pivotTo` off an interface base now emits `interfaceLinkSearchAround(methodInput, ilt)` (the shape the backend resolves via a native link) instead of a plain `searchAround`, and the observable invalidation walker resolves `asType` so `narrowToType`/union object sets that carry these derived properties invalidate correctly.

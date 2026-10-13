`ObjectMap` is no longer a type alias for `BTreeMap<KeyString, Value>`. It is now a dedicated type whose default
storage is a sorted, reference-counted flat vector with cheap clones and copy-on-write mutation, improving
the performance of common object operations. Iteration remains sorted by key, and `ObjectMap` provides the
commonly used map methods along with conversion from `BTreeMap<KeyString, Value>`. Code that relied on
`ObjectMap` being a `BTreeMap` may need to be updated.

authors: lukesteensen

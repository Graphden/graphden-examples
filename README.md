# graphden-examples

Pedagogical [graphden](https://github.com/Graphden/graphden) fn-def examples —
one feature per submodule under `packages/examples/`. Pure composition over the
`core` package; **no base-fns**, so it loads into any graphden without extra impls.

Optional + dev/learning only — a production graphden never loads it.

## Use it in your own graphden project

Add the git-dep and put `examples` on the classpath, then include it in
`:package-names`:

```clojure
;; deps.edn (dev alias)
{:aliases {:dev {:extra-deps {com.graphden/graphden-examples
                              {:git/url "git@github.com:Graphden/graphden-examples.git"
                               :git/sha "<sha>"}}}}}
```

Then load `"examples"` alongside `"core"` in your dev system config's
`:package-names`. Each submodule's `fns.edn` is a readable, self-contained
lesson; see `package.edn` for the module list.

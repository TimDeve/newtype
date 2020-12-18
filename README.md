# Newtype

Newtypes for [Carp](https://www.github.com/carp-lang/carp)

## Example

```clojure
(newtype Year Int)

(defn add-years [ya yb]
  (Year (+ (Year.consume ya) (Year.consume yb))))

(defn-do main []
 (println* (newtype-consume (add-years (Year 1999) (Year 1)))))

 ; Doesn't compile
 ; (println* (add-years 1999 1)
```

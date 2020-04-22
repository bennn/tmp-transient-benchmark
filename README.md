Changes from gtp-benchmarks

- jpeg : add (vector-map values ....)
  the math library uses a require/untyped-contract,
  which leaves transient with a supertype & a type error
  ... the vector-map fixes the typing

- lnm : require/typed plot-pict
  transient cannot yet automatically recover the type from
  the (define-typed/untyped-identifier plot-pict ....)
  so manually insert a require/typed

- quadT : unsafe-provide a simple macro
  used so guarded & transient can reuse the macro

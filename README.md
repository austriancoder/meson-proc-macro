#

FAILED: subprojects/pest_derive-2.7.6/libpest_derive.so 
rustc -C linker=cc --color=always -C debug-assertions=yes -C overflow-checks=no --crate-type proc-macro -g --crate-name pest_derive --emit dep-info=subprojects/pest_derive-2.7.6/pest_derive.d --emit link=subprojects/pest_derive-2.7.6/libpest_derive.so --out-dir subprojects/pest_derive-2.7.6/libpest_derive.so.p -C metadata=a7312f0@@pest_derive@sha --extern pest=subprojects/pest-2.7.6/libpest.rlib --extern pest_generator=subprojects/pest_generator-2.7.6/libpest_generator.rlib -Lsubprojects/pest-2.7.6 -Lsubprojects/ucd-trie-0.1.6 -Lsubprojects/pest_generator-2.7.6 -Lsubprojects/pest_meta-2.7.6 -Lsubprojects/once_cell-1.8.0 -Lsubprojects/proc-macro2-1.0.70 -Lsubprojects/unicode-ident-1.0.12 -Lsubprojects/quote-1.0.33 -Lsubprojects/syn-2.0.39 -C prefer-dynamic ../subprojects/pest_derive-2.7.6/src/lib.rs
error[E0432]: unresolved import `proc_macro`
   --> ../subprojects/pest_derive-2.7.6/src/lib.rs:318:5
    |
318 | use proc_macro::TokenStream;
    |     ^^^^^^^^^^ maybe a missing crate `proc_macro`?
    |
    = help: consider adding `extern crate proc_macro` to use the `proc_macro` crate

error: aborting due to previous error
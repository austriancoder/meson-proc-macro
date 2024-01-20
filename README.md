# Build with meson

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

# Build with Cargo

Running /home/christian/.rustup/toolchains/stable-aarch64-unknown-linux-gnu/bin/rustc --crate-name pest_derive --edition=2021 /home/christian/.cargo/registry/src/index.crates.io-6f17d22bba15001f/pest_derive-2.7.6/src/lib.rs --error-format=json --json=diagnostic-rendered-ansi,artifacts,future-incompat --diagnostic-width=140 --crate-type proc-macro --emit=dep-info,link -C prefer-dynamic -C embed-bitcode=no --cfg 'feature="default"' --cfg 'feature="std"' -C metadata=32cbfa6c317e029f -C extra-filename=-32cbfa6c317e029f --out-dir /home/christian/projects/meson-proc-macro/target/debug/deps -L dependency=/home/christian/projects/meson-proc-macro/target/debug/deps --extern pest=/home/christian/projects/meson-proc-macro/target/debug/deps/libpest-e55adae96a5156e9.rlib --extern pest_generator=/home/christian/projects/meson-proc-macro/target/debug/deps/libpest_generator-f61c55eb3afa5df6.rlib --extern proc_macro --cap-lints allow
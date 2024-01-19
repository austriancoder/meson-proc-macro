project(
  'meson-proc-macro',
  ['rust'],
  license : 'MIT',
)

rust = import('rust')

add_languages('rust', required: true)
rustc = meson.get_compiler('rust')

dep_pest_generator = dependency('pest_generator',
  version : '>= 2.7.6',
  fallback : ['pest_generator', 'dep_pest_generator'],
  required : true,
)

dep_pest_derive = dependency('pest_derive',
  version : '>= 2.7.6',
  fallback : ['pest_derive', 'dep_pest_derive'],
  required : true,
)

rust_files = files(
  'main.rs'
)

rust_executable = executable(
  'rust_executable',
  [rust_files],
  gnu_symbol_visibility : 'hidden',
  dependencies : [dep_pest_derive, dep_pest_generator],
) 

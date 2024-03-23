project(
  'tl-expected',
  'cpp',
  license: 'CC0-1.0',
  version: '1.1.0'
)

tl_expected_dep = declare_dependency(
  include_directories: include_directories('include')
)

if meson.version().version_compare('>=0.54.0')
  meson.override_dependency('tl-expected', tl_expected_dep)
endif

install_headers('include/tl/expected.hpp', subdir : 'tl')

cps = import('cps')
tl = cps.create_package('tl')
tl.add_component(name : 'expected', cpp_include_directories : ['include'])

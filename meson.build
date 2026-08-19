project(
  'basic',
  'cpp',
  version: '0.1',
  meson_version: '>= 1.3.0',
  default_options: ['warning_level=3', 'cpp_std=c++17'],
)

dependencies = []

sources = [
  'src/lib.cpp',
]

core = static_library(
  'basic',
  sources,
  include_directories: ['include'],
  install: false,
  dependencies: dependencies,
)

core_dep = declare_dependency(
  include_directories: ['include'],
  link_with: core,
)

gtest_dep = dependency('gtest', main: true, fallback: ['gtest', 'gtest_dep'])

unit_test = executable(
  'unit_test',
  'test/unittest.cpp',
  dependencies: [core_dep, gtest_dep],
)

test('unit_test', unit_test, protocol: 'gtest')
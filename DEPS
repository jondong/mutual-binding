vars = {
  'dart_git': 'https://dart.googlesource.com',
  'fuchsia_git': 'https://fuchsia.googlesource.com',
  'chromium_git': 'https://chromium.googlesource.com',
  'github_jondong': 'https://github.com/jondong',

  # Revisions
  'buildroot_revision': '7feacaa',
  'buildtool_revision': 'ae8541069',
  'gyp_revision': '4801a5331a',
  'v8_revision': 'a3d090986',
  'googletest_revision': 'd5266326',
  'dart_revision': 'c0e14e3',
  'tonic_revision': '57d508b12',
  'dart_dartdoc_tag': 'v0.20.2',
  'dart_boringssl_gen_rev': 'fc47eaa1a2',
  'dart_boringssl_rev': '189270cd190',
  'dart_observatory_pub_packages_rev': '089412217',
  'dart_package_config_tag': '1.0.5',
  'dart_source_span_tag': '1.4.1',
  'dart_charcode_tag': 'v1.1.2',
  'dart_path_tag': '1.6.2',
  'dart_dart2js_info_tag': '0.5.6+4',
  'dart_collection_tag': '1.14.11',
  'dart_args_tag': '1.4.4',
}

allowed_hosts = [
  'fuchsia.googlesource.com',
  'github.com',
  'skia.googlesource.com',
]

deps = {
  'src': Var('github_jondong') + '/buildroot.git' + '@' + Var('buildroot_revision'),
  'src/buildtools': Var('fuchsia_git') + '/buildtools' + '@' + Var('buildtool_revision'),
  'src/third_party/gyp': Var('chromium_git') + '/external/gyp.git' + '@' + Var('gyp_revision'),
  'src/v8': Var('chromium_git') + '/v8/v8' + '@' + Var('v8_revision'),
  'src/third_party/googletest/src': Var('chromium_git') + '/external/github.com/google/googletest.git' + '@' + Var('googletest_revision'),
  'src/third_party/dart': Var('dart_git') + '/sdk.git' + '@' + Var('dart_revision'),
  'src/third_party/tonic': Var('fuchsia_git') + '/tonic' + '@' + Var('tonic_revision'),
  'src/third_party/boringssl': 'https://github.com/dart-lang/boringssl_gen.git' + '@' + Var('dart_boringssl_gen_rev'),
  'src/third_party/boringssl/src': 'https://boringssl.googlesource.com/boringssl.git' + '@' + Var('dart_boringssl_rev'),
  'src/third_party/dart/third_party/observatory_pub_packages': Var('dart_git') + '/observatory_pub_packages.git' + '@' + Var('dart_observatory_pub_packages_rev'),
  'src/third_party/dart/third_party/pkg/dartdoc': Var('dart_git') + '/dartdoc.git' + '@' + Var('dart_dartdoc_tag'),
  'src/third_party/dart/third_party/pkg/source_span': Var('dart_git') + '/source_span.git' + '@' + Var('dart_source_span_tag'),
  'src/third_party/dart/third_party/pkg/charcode': Var('dart_git') + '/charcode.git' + '@' + Var('dart_charcode_tag'),
  'src/third_party/dart/third_party/pkg/path': Var('dart_git') + '/path.git' + '@' + Var('dart_path_tag'),
  'src/third_party/dart/third_party/pkg/dart2js_info': Var('dart_git') + '/dart2js_info.git' + '@' + Var('dart_dart2js_info_tag'),
  'src/third_party/dart/third_party/pkg/collection': Var('dart_git') + '/collection.git' + '@' + Var('dart_collection_tag'),
  'src/third_party/dart/third_party/pkg/args': Var('dart_git') + '/args.git' + '@' + Var('dart_args_tag'),
  'src/third_party/dart/third_party/pkg_tested/package_config': Var('dart_git') + '/package_config.git' + '@' + Var('dart_package_config_tag'),
  'src/third_party/icu': Var('chromium_git') + '/chromium/deps/icu.git' + '@' + '297a4dd02b9d36c92ab9b4f121e433c9c3bc14f8',
}

recursedeps = [
  'src/buildtools',
]

skip_child_includes = [
  'out',
  'v8',
]

hooks = [
  {
    'name': 'download_android_tools',
    'pattern': '.',
    'action': [
      'python', 'src/tools/android/download_android_tools.py',
    ],
  },
  {
    'name': 'buildtools',
    'pattern': '.',
    'action': [
      'python',
      'src/tools/buildtools/update.py',
    ],
  },
  {
    'name': 'dart',
    'pattern': '.',
    'action': ['python', 'src/tools/dart/update.py'],
  },
]

vars = {
  'dart_git': 'https://dart.googlesource.com',
  'fuchsia_git': 'https://fuchsia.googlesource.com',
  'chromium_git': 'https://chromium.googlesource.com',
  'github_jondong': 'https://github.com/jondong',

  # Revisions
  'buildroot_revision': '4fd7a273',
  'buildtool_revision': 'ae8541069',
  'gyp_revision': '4801a5331a',
  'v8_revision': '022206d5',
  'dart_revision': '08f59e5de',
  'tonic_revision': '57d508b12',
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
  'src/third_party/v8': Var('chromium_git') + '/v8/v8' + '@' + Var('v8_revision'),
  'src/third_party/dart': Var('dart_git') + '/sdk.git' + '@' + Var('dart_revision'),
  'src/third_party/tonic': Var('fuchsia_git') + '/tonic' + '@' + Var('tonic_revision'),
}

recursedeps = [
  'src/buildtools',
]

hooks = [
  {
    'name': 'buildtools',
    'pattern': '.',
    'action': [
      'python',
      'src/tools/buildtools/update.py',
    ],
  }
]

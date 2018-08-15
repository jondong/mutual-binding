vars = {
  'fuchsia_git': 'https://fuchsia.googlesource.com',
  'chromium_git': 'https://chromium.googlesource.com',
  'github_jondong': 'https://github.com/jondong',
}

allowed_hosts = [
  'fuchsia.googlesource.com',
  'github.com',
  'skia.googlesource.com',
]

deps = {
  'src': Var('github_jondong') + '/buildroot.git' + '@' + '4fd7a273',
  'src/third_party/tonic': Var('fuchsia_git') + '/tonic' + '@' + '57d508b12',
  'src/third_party/v8': Var('chromium_git') + '/v8/v8' + '@' + '022206d597f5249808477d6094e1df4df94326dc',
}

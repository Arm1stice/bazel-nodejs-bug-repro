load("@build_bazel_rules_nodejs//:index.bzl", "yarn_install", "nodejs_binary")

yarn_install(
    name = "npm",
    package_json = ":package.json",
    yarn_lock = ":yarn.lock",
)

nodejs_binary(
    name = "server",
    node_modules = "@npm//:node_modules",
    entry_point = ":index.js",
)
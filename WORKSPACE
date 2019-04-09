workspace(name = "template_test_repo")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "build_bazel_rules_nodejs",
    sha256 = "88e5e579fb9edfbd19791b8a3c6bfbe16ae3444dba4b428e5efd36856db7cf16",
    urls = [
        "https://github.com/bazelbuild/rules_nodejs/releases/download/0.27.8/rules_nodejs-0.27.8.tar.gz",
    ],
)

load("@build_bazel_rules_nodejs//:defs.bzl", "node_repositories", "yarn_install")

node_repositories(
    node_version = "10.13.0",
    yarn_version = "1.12.1",
)

yarn_install(
    name = "binary_tgz_js_deps",
    data = [
        "//:minimal-package-1.0.0.tgz",
    ],
    package_json = "//:package.json",
    yarn_lock = "//:yarn.lock",
)


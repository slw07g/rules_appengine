workspace(name = "io_bazel_rules_appengine")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

http_archive(
    name = "bazel_skylib",
    urls = [
        "https://github.com/bazelbuild/bazel-skylib/releases/download/1.0.3/bazel-skylib-1.0.3.tar.gz",
        "https://mirror.bazel.build/github.com/bazelbuild/bazel-skylib/releases/download/1.0.3/bazel-skylib-1.0.3.tar.gz",
    ],
    sha256 = "1c531376ac7e5a180e0237938a2536de0c54d93f5c278634818e0efc952dd56c",
)
load("@bazel_skylib//:workspace.bzl", "bazel_skylib_workspace")
bazel_skylib_workspace()

http_archive(
    name = "rules_java",
    sha256 = "7c4bbe11e41c61212a5cf16d9aafaddade3f5b1b6c8bf94270d78215fafd4007",
    strip_prefix = "rules_java-c13e3ead84afb95f81fbddfade2749d8ba7cb77f",
    url = "https://github.com/bazelbuild/rules_java/archive/c13e3ead84afb95f81fbddfade2749d8ba7cb77f.tar.gz",  # 2021-01-25
)

load("@rules_java//java:repositories.bzl", "remote_jdk8_repos")

remote_jdk8_repos()

load("//appengine:sdk.bzl", "appengine_repositories")
load("//appengine:java_appengine.bzl", "java_appengine_repositories")
load("//appengine:py_appengine.bzl", "py_appengine_repositories")

appengine_repositories()

java_appengine_repositories()

py_appengine_repositories()
pip_install('appengine-python-standard==1.1.3')
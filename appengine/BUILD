# A target to ensure the servlet-api is not linked in the webapp.
java_library(
    name = "javax.servlet.api",
    neverlink = 1,
    visibility = ["//visibility:public"],
    exports = ["@javax_servlet_api//jar"],
)

filegroup(
    name = "srcs",
    srcs = glob(["**"]),
    visibility = ["//tools:__pkg__"],
)

alias(
    name = "jdk8",
    actual = "@rules_appengine_toolchain//:jdk8",
    visibility = ["//visibility:public"],
)

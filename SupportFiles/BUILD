load("@build_bazel_rules_apple//apple:macos.bzl", "macos_application")
load("@build_bazel_rules_swift//swift:swift.bzl", "swift_library")

package(default_visibility = ["//visibility:public"])

swift_library(
    name = "Symbolicator",
    srcs = glob([
        "*.swift",
    ]),
    deps = ["//srcs/UI:SymbolicatorUI"],
)

macos_application(
    name = "SymbolicatorApp",
    bundle_id = "cc.slotus.symbolicator",
    infoplists = [":Info.plist"],
    minimum_os_version = "10.10",
    visibility = ["//visibility:public"],
    deps = [":Symbolicator"],
)

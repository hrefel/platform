package(default_visibility = ["//visibility:public"])

load("//tools:defaults.bzl", "ng_module", "ng_package")

ng_module(
    name = "router-store",
    srcs = glob([
        "*.ts",
        "src/**/*.ts",
    ]),
    module_name = "@ngrx/router-store",
    deps = [
        "//modules/store",
        "@angular//packages/router",
        "@rxjs",
    ],
)

ng_package(
    name = "npm_package",
    srcs = glob(["**/*.externs.js"]) + [
        "package.json",
    ],
    entry_point = "modules/router-store/index.js",
    packages = [
        "//modules/router-store/migrations:npm_package",
        "//modules/router-store/schematics-core:npm_package",
    ],
    deps = [
        ":router-store",
    ],
)

package(default_visibility = ["//visibility:public"])

licenses(["notice"])

load(
    "@io_bazel_rules_go//go:def.bzl",
    "go_library",
    "go_test",
)

go_library(
    name = "go_default_library",
    srcs = [
        "decorated_watcher.go",
        "doc.go",
        "storage_factory.go",
        "store.go",
    ],
    tags = ["automanaged"],
    deps = [
        "//pkg/genericapiserver/registry/generic:go_default_library",
        "//pkg/genericapiserver/registry/rest:go_default_library",
        "//pkg/storage/errors:go_default_library",
        "//pkg/storage/etcd:go_default_library",
        "//pkg/storage/storagebackend/factory:go_default_library",
        "//vendor:github.com/golang/glog",
        "//vendor:golang.org/x/net/context",
        "//vendor:k8s.io/apimachinery/pkg/api/errors",
        "//vendor:k8s.io/apimachinery/pkg/api/meta",
        "//vendor:k8s.io/apimachinery/pkg/api/validation/path",
        "//vendor:k8s.io/apimachinery/pkg/apis/meta/internalversion",
        "//vendor:k8s.io/apimachinery/pkg/apis/meta/v1",
        "//vendor:k8s.io/apimachinery/pkg/fields",
        "//vendor:k8s.io/apimachinery/pkg/labels",
        "//vendor:k8s.io/apimachinery/pkg/runtime",
        "//vendor:k8s.io/apimachinery/pkg/runtime/schema",
        "//vendor:k8s.io/apimachinery/pkg/util/runtime",
        "//vendor:k8s.io/apimachinery/pkg/util/validation/field",
        "//vendor:k8s.io/apimachinery/pkg/watch",
        "//vendor:k8s.io/apiserver/pkg/endpoints/request",
        "//vendor:k8s.io/apiserver/pkg/storage",
        "//vendor:k8s.io/apiserver/pkg/storage/storagebackend",
    ],
)

go_test(
    name = "go_default_test",
    srcs = [
        "decorated_watcher_test.go",
        "store_test.go",
    ],
    library = ":go_default_library",
    tags = ["automanaged"],
    deps = [
        "//pkg/genericapiserver/registry/generic:go_default_library",
        "//pkg/genericapiserver/registry/rest:go_default_library",
        "//pkg/storage/etcd:go_default_library",
        "//pkg/storage/etcd/testing:go_default_library",
        "//pkg/storage/storagebackend/factory:go_default_library",
        "//pkg/storage/testing:go_default_library",
        "//vendor:k8s.io/apimachinery/pkg/api/equality",
        "//vendor:k8s.io/apimachinery/pkg/api/errors",
        "//vendor:k8s.io/apimachinery/pkg/api/meta",
        "//vendor:k8s.io/apimachinery/pkg/api/testing",
        "//vendor:k8s.io/apimachinery/pkg/apis/meta/internalversion",
        "//vendor:k8s.io/apimachinery/pkg/apis/meta/v1",
        "//vendor:k8s.io/apimachinery/pkg/fields",
        "//vendor:k8s.io/apimachinery/pkg/labels",
        "//vendor:k8s.io/apimachinery/pkg/runtime",
        "//vendor:k8s.io/apimachinery/pkg/runtime/serializer",
        "//vendor:k8s.io/apimachinery/pkg/selection",
        "//vendor:k8s.io/apimachinery/pkg/util/validation/field",
        "//vendor:k8s.io/apimachinery/pkg/util/wait",
        "//vendor:k8s.io/apimachinery/pkg/watch",
        "//vendor:k8s.io/apiserver/pkg/apis/example",
        "//vendor:k8s.io/apiserver/pkg/apis/example/v1",
        "//vendor:k8s.io/apiserver/pkg/endpoints/request",
        "//vendor:k8s.io/apiserver/pkg/storage",
        "//vendor:k8s.io/apiserver/pkg/storage/names",
    ],
)

filegroup(
    name = "package-srcs",
    srcs = glob(["**"]),
    tags = ["automanaged"],
    visibility = ["//visibility:private"],
)

filegroup(
    name = "all-srcs",
    srcs = [":package-srcs"],
    tags = ["automanaged"],
)

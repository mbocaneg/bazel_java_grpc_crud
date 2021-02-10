load("@rules_proto_grpc//java:defs.bzl", "java_proto_library")

load("@rules_proto_grpc//java:defs.bzl", "java_grpc_library")

proto_library(
    name = "author_proto",
    srcs = ["author.proto"],
    visibility = ["//visibility:public"],
)

proto_library(
    name = "book_proto",
    srcs = ["book.proto", "author.proto"],
    visibility = ["//visibility:public"],
)

##############################################################

java_proto_library(
    name = "author_proto_java",
    deps = [":author_proto"],
    visibility = ["//visibility:public"],
)

java_proto_library(
    name = "book_proto_java",
    deps = [":book_proto"],
    visibility = ["//visibility:public"],
)
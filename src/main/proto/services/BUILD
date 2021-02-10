load("@rules_proto_grpc//java:defs.bzl", "java_proto_library")

load("@rules_proto_grpc//java:defs.bzl", "java_grpc_library")

proto_library(
    name = "service_params_proto",
    srcs = ["service_params.proto"],
    deps = ["//src/main/proto/models:book_proto", "//src/main/proto/models:author_proto"],
    visibility = ["//visibility:public"],
)

java_proto_library(
    name = "service_params_proto_java",
    deps = [":service_params_proto"],
    visibility = ["//visibility:public"],
)


#######################################################################################

proto_library(
    name = "author_service_proto",
    srcs = ["author_service.proto"],
    deps = [":service_params_proto", "//src/main/proto/models:author_proto"],
    visibility = ["//visibility:public"],
)


java_proto_library(
    name = "author_service_proto_java",
    deps = [":author_service_proto"],
    visibility = ["//visibility:public"],
)

#######################################################################################

proto_library(
    name = "book_service_proto",
    srcs = ["book_service.proto"],
    deps = [":service_params_proto", "//src/main/proto/models:book_proto", "//src/main/proto/models:author_proto"],
    visibility = ["//visibility:public"],
)

java_proto_library(
    name = "book_service_proto_java",
    deps = [":book_service_proto"],
    visibility = ["//visibility:public"],
)

#######################################################################################

java_grpc_library(
    name = "author_service_java_grpc",
##    srcs = ["author_service_proto"],
    deps = ["author_service_proto"],
    visibility = ["//visibility:public"],
)

java_grpc_library(
    name = "book_service_java_grpc",
##    srcs = ["book_service_proto"],
    deps = ["book_service_proto"],
    visibility = ["//visibility:public"],
)

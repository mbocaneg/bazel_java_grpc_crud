java_binary(
    name = "bookstore_server",
    main_class = "server.BookstoreServer",
    srcs = [
        "BookstoreServer.java",
        "BookstoreRepo.java",
        "BookServiceImpl.java",
        "AuthorServiceImpl.java",
    ],
    deps = [
        "//src/main/proto/models:author_proto_java", 
        "//src/main/proto/models:book_proto_java",

        "//src/main/proto/services:author_service_proto_java",
        "//src/main/proto/services:book_service_proto_java",

        "//src/main/proto/services:author_service_java_grpc",
        "//src/main/proto/services:book_service_java_grpc",

        "//src/main/proto/services:service_params_proto_java",
        "@io_grpc_grpc_java//api",
        "@io_grpc_grpc_java//stub"
    ],
)
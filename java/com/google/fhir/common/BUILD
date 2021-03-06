package(
    default_visibility = ["//visibility:public"],
)

licenses(["notice"])

java_library(
    name = "common",
    srcs = [
        "AnnotationUtils.java",
        "InvalidFhirException.java",
        "ProtoUtils.java",
    ],
    deps = [
        "//proto/google/fhir/proto:annotations_java_proto",
        "@com_google_protobuf//:protobuf_java",
    ],
)

java_library(
    name = "fhir_version",
    srcs = [
        "FhirVersion.java",
    ],
    deps = [
        "//proto/google/fhir/proto:annotations_java_proto",
        "//proto/google/fhir/proto/r4/core:codes_java_proto",
        "//proto/google/fhir/proto/r4/core:datatypes_java_proto",
        "//proto/google/fhir/proto/r4/core:extensions_java_proto",
        "//proto/google/fhir/proto/r4/core:valuesets_java_proto",
        "//proto/google/fhir/proto/r4/core/resources:bundle_and_contained_resource_java_proto",
        "//proto/google/fhir/proto/stu3:codes_java_proto",
        "//proto/google/fhir/proto/stu3:datatypes_java_proto",
        "//proto/google/fhir/proto/stu3:extensions_java_proto",
        "//proto/google/fhir/proto/stu3:metadatatypes_java_proto",
        "//proto/google/fhir/proto/stu3:resources_java_proto",
        "@com_google_protobuf//:protobuf_java",
        "@maven//:com_google_guava_guava",
    ],
)

java_library(
    name = "big_query_schema",
    srcs = ["BigQuerySchema.java"],
    deps = [
        ":common",
        "//proto/google/fhir/proto:annotations_java_proto",
        "//proto/google/fhir/proto/r4/core:datatypes_java_proto",
        "@com_google_protobuf//:protobuf_java",
        "@maven//:com_google_apis_google_api_services_bigquery",
        "@maven//:com_google_guava_guava",
    ],
)

java_library(
    name = "json_format",
    srcs = ["JsonFormat.java"],
    deps = [
        ":common",
        ":proto_gen_transformer",
        ":resource_utils",
        "//java/com/google/fhir/wrappers:primitive_wrappers",
        "//proto/google/fhir/proto:annotations_java_proto",
        "//proto/google/fhir/proto/r4:fhirproto_extensions_java_proto",
        "//proto/google/fhir/proto/r4/core:datatypes_java_proto",
        "//proto/google/fhir/proto/r4/core/resources:bundle_and_contained_resource_java_proto",
        "//proto/google/fhir/proto/stu3:datatypes_java_proto",
        "//proto/google/fhir/proto/stu3:resources_java_proto",
        "@com_google_protobuf//:protobuf_java",
        "@maven//:com_google_code_gson_gson",
        "@maven//:com_google_guava_guava",
    ],
)

java_library(
    name = "file_utils",
    srcs = ["FileUtils.java"],
    deps = [
        ":json_format",
        "//proto/google/fhir/proto/r4/core/resources:structure_definition_java_proto",
        "@com_google_protobuf//:protobuf_java",
        "@maven//:com_google_guava_guava",
    ],
)

java_library(
    name = "resource_utils",
    srcs = [
        "ResourceUtils.java",
    ],
    deps = [
        ":common",
        "//java/com/google/fhir/wrappers:primitive_wrappers",
        "//proto/google/fhir/proto/r4/core:datatypes_java_proto",
        "//proto/google/fhir/proto/r4/core/resources:bundle_and_contained_resource_java_proto",
        "//proto/google/fhir/proto/stu3:resources_java_proto",
        "@com_google_protobuf//:protobuf_java",
        "@maven//:com_google_guava_guava",
    ],
)

java_library(
    name = "resource_validator",
    srcs = ["ResourceValidator.java"],
    deps = [
        ":common",
        "//java/com/google/fhir/wrappers:primitive_wrappers",
        "//proto/google/fhir/proto:annotations_java_proto",
        "//proto/google/fhir/proto/r4/core:datatypes_java_proto",
        "//proto/google/fhir/proto/stu3:datatypes_java_proto",
        "@com_google_protobuf//:protobuf_java",
        "@maven//:com_google_guava_guava",
    ],
)

java_library(
    name = "proto_gen_transformer",
    srcs = ["ProtoGenTransformer.java"],
    deps = [
        "//proto/google/fhir/proto/r4/core:codes_java_proto",
        "//proto/google/fhir/proto/r4/core:datatypes_java_proto",
        "//proto/google/fhir/proto/r4/core/resources:capability_statement_java_proto",
        "//proto/google/fhir/proto/r4/core/resources:code_system_java_proto",
        "//proto/google/fhir/proto/r4/core/resources:compartment_definition_java_proto",
        "//proto/google/fhir/proto/r4/core/resources:concept_map_java_proto",
        "//proto/google/fhir/proto/r4/core/resources:operation_definition_java_proto",
        "//proto/google/fhir/proto/r4/core/resources:structure_definition_java_proto",
        "//proto/google/fhir/proto/r4/core/resources:value_set_java_proto",
        "@com_google_protobuf//:protobuf_java",
        "@maven//:com_google_code_gson_gson",
        "@maven//:com_google_guava_guava",
    ],
)

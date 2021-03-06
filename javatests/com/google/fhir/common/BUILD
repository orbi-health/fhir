licenses(["notice"])

java_test(
    name = "ProtoGenTransformerTest",
    srcs = ["ProtoGenTransformerTest.java"],
    data = [
        "//spec:fhir_stu3_package.zip",
        "//testdata/protogentransformer:json",
    ],
    test_class = "com.google.fhir.common.ProtoGenTransformerTest",
    deps = [
        "//java/com/google/fhir/common:json_format",
        "//java/com/google/fhir/common:proto_gen_transformer",
        "//java/com/google/fhir/common:resource_validator",
        "//java/com/google/fhir/protogen",
        "//proto/google/fhir/proto/r4/core:datatypes_java_proto",
        "//proto/google/fhir/proto/r4/core/resources:structure_definition_java_proto",
        "@bazel_tools//tools/java/runfiles",
        "@maven//:com_google_guava_guava",
        "@maven//:com_google_truth_truth",
        "@maven//:junit_junit",
    ],
)

java_test(
    name = "ResourceValidatorTest",
    size = "small",
    srcs = ["ResourceValidatorR4Test.java"],
    data = [
        "//testdata/r4:validation",
    ],
    test_class = "com.google.fhir.common.ResourceValidatorR4Test",
    deps = [
        "//java/com/google/fhir/common",
        "//java/com/google/fhir/common:resource_validator",
        "//proto/google/fhir/proto/r4/core/resources:bundle_and_contained_resource_java_proto",
        "//proto/google/fhir/proto/r4/core/resources:encounter_java_proto",
        "//proto/google/fhir/proto/r4/core/resources:observation_java_proto",
        "@bazel_tools//tools/java/runfiles",
        "@com_google_protobuf//:protobuf_java",
        "@maven//:com_google_guava_guava",
        "@maven//:com_google_truth_truth",
        "@maven//:junit_junit",
    ],
)

java_test(
    name = "AnnotationUtilsTest",
    size = "small",
    srcs = ["AnnotationUtilsTest.java"],
    test_class = "com.google.fhir.common.AnnotationUtilsTest",
    deps = [
        "//java/com/google/fhir/common",
        "//proto/google/fhir/proto/stu3:datatypes_java_proto",
        "//proto/google/fhir/proto/stu3:resources_java_proto",
        "//proto/google/fhir/proto/stu3:uscore_java_proto",
        "@com_google_protobuf//:protobuf_java",
        "@maven//:junit_junit",
    ],
)

java_test(
    name = "BigQuerySchemaTest",
    size = "small",
    srcs = ["BigQuerySchemaTest.java"],
    data = [
        "//spec:stu3",
        "//testdata/stu3:bigquery",
        "//testdata/stu3:examples",
    ],
    test_class = "com.google.fhir.common.BigQuerySchemaTest",
    deps = [
        "//java/com/google/fhir/common:big_query_schema",
        "//proto/google/fhir/proto/stu3:resources_java_proto",
        "@bazel_tools//tools/java/runfiles",
        "@com_google_protobuf//:protobuf_java",
        "@maven//:com_google_apis_google_api_services_bigquery",
        "@maven//:com_google_guava_guava",
        "@maven//:com_google_http_client_google_http_client_gson",
        "@maven//:com_google_truth_truth",
        "@maven//:junit_junit",
    ],
)

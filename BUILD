java_library(
    name = "lombok",
    exports = [
        "@maven//:org_projectlombok_lombok",
        "@maven//:org_slf4j_slf4j_api",
    ],
    exported_plugins = [
        ":lombok_plugin"
    ],
)

java_plugin(
    name = "lombok_plugin",
    processor_class = "lombok.launch.AnnotationProcessorHider$AnnotationProcessor",
    deps = [
        "@lombok_jar//jar",
        "@maven//:org_slf4j_slf4j_api",
    ],
)

java_library(
    name = "a",
    srcs = ["A.java"],
    deps = [
        "//:maven_deps",
        "@maven//:org_slf4j_slf4j_api",
        ":lombok",
    ],
)


## this fails to compile
#java_library(
#    name = "b1",
#    srcs = ["B.java"],
#    deps = [
#        ":a",
#    ],
#    plugins = [
#        ":lombok_plugin",
#    ],
#)
#

# this compiles successfully
java_library(
    name = "b2",
    srcs = ["B.java"],
    deps = [
    "@maven//:org_slf4j_slf4j_api",
        ":liba.jar",
        ":lombok",
    ],
)

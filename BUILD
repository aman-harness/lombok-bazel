java_library(
    name = "lombok",
    exports = [
        "@org_projectlombok_lombok//jar",
    ],
    exported_plugins = [
        ":lombok_plugin"
    ],
)

java_plugin(
    name = "lombok_plugin",
    processor_class = "lombok.launch.AnnotationProcessorHider$AnnotationProcessor",
    deps = [
        "@org_projectlombok_lombok//jar",
    ],
)

java_library(
    name = "a",
    srcs = ["A.java"],
    deps = [
        ":lombok",
    ],
)

# this fails to compile
java_library(
    name = "b1",
    srcs = ["B.java"],
    deps = [
        ":a",
    ],
)

# this works
java_library(
    name = "b2",
    srcs = ["B.java"],
    deps = [
        ":liba.jar",        
    ],
)

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

RULES_JVM_EXTERNAL_TAG = "3.0"
RULES_JVM_EXTERNAL_SHA = "62133c125bf4109dfd9d2af64830208356ce4ef8b165a6ef15bbff7460b35c3a"

http_archive(
    name = "rules_jvm_external",
    strip_prefix = "rules_jvm_external-%s" % RULES_JVM_EXTERNAL_TAG,
    sha256 = RULES_JVM_EXTERNAL_SHA,
    url = "https://github.com/bazelbuild/rules_jvm_external/archive/%s.zip" % RULES_JVM_EXTERNAL_TAG,
)

load("@rules_jvm_external//:defs.bzl", "maven_install")

maven_install(
    name = "maven",
    artifacts= [
        "org.projectlombok:lombok:edge-SNAPSHOT",
        "org.slf4j:slf4j-api:1.7.29",
        "org.powermock:powermock-module-junit4:2.0.7",
        "ch.qos.logback:logback-classic:1.3.0-alpha5",
    ],
    repositories=[
        "https://repo1.maven.org/maven2",
        "https://projectlombok.org/edge-releases",
    ]
)

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_jar")

http_jar(
    name = "lombok_jar",
    url = "https://projectlombok.org/lombok-edge.jar",
    sha256 = "f0ce4526629022fc9c53b6f02a61457bb07b28315b4fc3cce1ca5de06e1446c1",
)
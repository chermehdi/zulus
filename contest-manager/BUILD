java_library(
    name = "contest-manager-lib",
    srcs = glob(["src/main/java/**/*.java"]),
    deps = [
        "@maven//:org_springframework_boot_spring_boot",
        "@maven//:org_springframework_boot_spring_boot_starter_web",
        "@maven//:org_springframework_boot_spring_boot_autoconfigure",
        "@maven//:org_springframework_boot_spring_boot_starter_security",
        "@maven//:org_springframework_boot_spring_boot_starter_jdbc",
        "@maven//:org_springframework_boot_spring_boot_starter_data_jpa",
    ],
)

java_binary(
    name = "contest-manager",
    srcs = glob(["src/main/java/**/*.java"]),
    main_class = "io.zulus.cm.ZulusContestManagerApplication",
    deps = [
        ":contest-manager-lib",
        "@maven//:org_springframework_boot_spring_boot",
        "@maven//:org_springframework_boot_spring_boot_starter_web",
        "@maven//:org_springframework_boot_spring_boot_autoconfigure",
        "@maven//:org_springframework_boot_spring_boot_starter_security",
        "@maven//:org_springframework_boot_spring_boot_starter_jdbc",
        "@maven//:org_springframework_boot_spring_boot_starter_data_jpa",
    ],
)

load("//contest-manager:junit5.bzl", "java_junit5_test")

java_junit5_test(
    name = "contest-manager-test",
    srcs = glob(["src/test/java/**/*.java"]),
    test_package = "io.zulus",
    deps = [
        "@maven//:org_springframework_boot_spring_boot_test",
        "@maven//:org_junit_platform_junit_platform_suite_api",
        "@maven//:org_apiguardian_apiguardian_api",
        "@maven//:org_opentest4j_opentest4j",
        "@maven//:org_springframework_boot_spring_boot",
        "@maven//:org_springframework_boot_spring_boot_starter_web",
        "@maven//:org_springframework_boot_spring_boot_autoconfigure",
        "@maven//:org_springframework_boot_spring_boot_starter_security",
        "@maven//:org_springframework_boot_spring_boot_starter_jdbc",
        "@maven//:org_springframework_boot_spring_boot_starter_data_jpa",
        ":contest-manager-lib",
    ],
    runtime_deps = [
        "@maven//:org_junit_platform_junit_platform_commons",
        "@maven//:org_junit_platform_junit_platform_engine",
        "@maven//:org_junit_platform_junit_platform_launcher",
        "@maven//:org_junit_platform_junit_platform_suite_api",
    ],
)

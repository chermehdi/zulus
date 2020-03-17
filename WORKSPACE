load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive") 

RULES_JVM_EXTERNAL_TAG = "2.2"

RULES_JVM_EXTERNAL_SHA = "f1203ce04e232ab6fdd81897cf0ff76f2c04c0741424d192f28e65ae752ce2d6"

http_archive(
    name = "rules_jvm_external",
    strip_prefix = "rules_jvm_external-%s" % RULES_JVM_EXTERNAL_TAG,
    sha256 = RULES_JVM_EXTERNAL_SHA,
    url = "https://github.com/bazelbuild/rules_jvm_external/archive/%s.zip" % RULES_JVM_EXTERNAL_TAG,
)

load("@rules_jvm_external//:defs.bzl", "maven_install")

maven_install(
    artifacts = [
        "org.springframework.boot:spring-boot-starter-web:2.2.5.RELEASE",
        "org.springframework.boot:spring-boot-starter-data-jpa:2.2.5.RELEASE",
        "org.springframework.boot:spring-boot-starter-jdbc:2.2.5.RELEASE",
        "org.springframework.boot:spring-boot-starter-security:2.2.5.RELEASE",
        "org.springframework.boot:spring-boot-starter-test:2.2.5.RELEASE",
        "org.junit.jupiter:junit-jupiter-api:5.5.0",
        "org.junit.jupiter:junit-jupiter-engine:5.5.0",
        "org.junit.jupiter:junit-jupiter-params:5.5.0",
        "org.apiguardian:apiguardian-api:1.0.0",
        "org.opentest4j:opentest4j:1.2.0",
        "org.junit.platform:junit-platform-commons:1.5.0",
        "org.junit.platform:junit-platform-console:1.5.0",
        "org.junit.platform:junit-platform-engine:1.5.0",
        "org.junit.platform:junit-platform-launcher:1.5.0",
        "org.junit.platform:junit-platform-suite-api:1.5.0",
    ],
    repositories = [
        "https://jcenter.bintray.com",
        "http://central.maven.org/maven2",
    ]
)

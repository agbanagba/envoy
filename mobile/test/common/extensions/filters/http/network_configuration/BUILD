load("@envoy//bazel:envoy_build_system.bzl", "envoy_mobile_package")
load(
    "@envoy//test/extensions:extensions_build_system.bzl",
    "envoy_extension_cc_test",
)

licenses(["notice"])  # Apache 2

envoy_mobile_package()

envoy_extension_cc_test(
    name = "network_configuration_filter_test",
    srcs = ["network_configuration_filter_test.cc"],
    extension_names = ["envoy.filters.http.network_configuration"],
    repository = "@envoy",
    deps = [
        "//library/common/api:external_api_lib",
        "//library/common/bridge:utility_lib",
        "//library/common/extensions/filters/http/network_configuration:config",
        "//library/common/extensions/filters/http/network_configuration:filter_cc_proto",
        "//library/common/network:proxy_api_lib",
        "//library/common/network:proxy_resolver_interface_lib",
        "//library/common/network:proxy_settings_lib",
        "@envoy//test/extensions/common/dynamic_forward_proxy:mocks",
        "@envoy//test/mocks/event:event_mocks",
        "@envoy//test/mocks/http:http_mocks",
        "@envoy//test/mocks/server:factory_context_mocks",
        "@envoy//test/test_common:utility_lib",
    ],
)

load("//tensorflow:strict.default.bzl", "py_strict_library")
load(":reference_test.bzl", "reference_test")

# copybara:uncomment package(default_applicable_licenses = ["//tensorflow:license"])

licenses(["notice"])

py_strict_library(
    name = "reference_tests",
    srcs = ["reference_test_base.py"],
    deps = [
        "//tensorflow:tensorflow_py",
        "//third_party/py/numpy",
    ],
)

# # Misc

# ## Boolean expressions, equality testing

reference_test(name = "logical_expression_test")

reference_test(name = "ext_slice_test")

# ## Type annotations

reference_test(name = "type_annotations_test")

# ## Scoping and modularity

reference_test(
    name = "loop_scoping_test",
    additional_deps = ["@absl_py//absl/testing:parameterized"],
)

# ## Composite names

reference_test(
    name = "composite_names_in_control_flow_test",
    additional_deps = ["@absl_py//absl/testing:parameterized"],
)

# ## Function Calls

reference_test(name = "call_to_builtin_function_test")

reference_test(name = "call_to_lambda_function_test")

reference_test(name = "call_to_named_tuple_test")

reference_test(
    name = "call_to_numpy_function_test",
    additional_deps = ["//third_party/py/numpy"],
)

reference_test(
    name = "call_to_print_function_test",
    additional_deps = ["//third_party/py/numpy"],
)

reference_test(name = "call_to_tf_api_test")

reference_test(name = "call_to_user_function_test")

# # Control Flow

reference_test(name = "basic_ifexp_test")

reference_test(
    name = "cond_basic_test",
    additional_deps = ["@absl_py//absl/testing:parameterized"],
)

reference_test(
    name = "early_return_test",
    additional_deps = ["@absl_py//absl/testing:parameterized"],
)

reference_test(
    name = "loop_basic_test",
    additional_deps = ["@absl_py//absl/testing:parameterized"],
)

reference_test(
    name = "loop_control_flow_test",
    additional_deps = ["@absl_py//absl/testing:parameterized"],
    shard_count = 20,
)

reference_test(
    name = "loop_control_flow_illegal_cases_test",
    additional_deps = ["@absl_py//absl/testing:parameterized"],
)

reference_test(
    name = "loop_created_variables_test",
    additional_deps = ["@absl_py//absl/testing:parameterized"],
)

reference_test(
    name = "loop_distributed_test",
    additional_deps = ["@absl_py//absl/testing:parameterized"],
    tags = [
        "no_oss",  # TODO(mdan): Investigate timeout reason.
    ],
)

reference_test(
    name = "loop_with_variable_type_test",
    additional_deps = ["@absl_py//absl/testing:parameterized"],
)

reference_test(
    name = "loop_with_variable_type_illegal_cases_test",
    additional_deps = ["@absl_py//absl/testing:parameterized"],
)

reference_test(
    name = "loop_with_function_call_test",
    additional_deps = ["@absl_py//absl/testing:parameterized"],
)

reference_test(
    name = "nested_control_flow_test",
    additional_deps = ["@absl_py//absl/testing:parameterized"],
)

# ## Assert

reference_test(name = "assertion_test")

# # Data Structures

# ## Generators

reference_test(name = "generator_test")

# ## Iterators

reference_test(name = "datasets_test")

# ## Lists

reference_test(
    name = "basic_list_test",
    additional_deps = ["//tensorflow/python/autograph"],
    tags = [
        "no_oss",
        "notap",
    ],
)

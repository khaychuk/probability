# Copyright 2018 The TensorFlow Probability Authors.
#
# Licensed under the Apache License, Version 2.0 (the "License");
# you may not use this file except in compliance with the License.
# You may obtain a copy of the License at
#
#     http://www.apache.org/licenses/LICENSE-2.0
#
# Unless required by applicable law or agreed to in writing, software
# distributed under the License is distributed on an "AS IS" BASIS,
# WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
# See the License for the specific language governing permissions and
# limitations under the License.
# ============================================================================
# Description:
#   Contains ops for bijectors.
#   APIs here are meant to evolve over time.

licenses(["notice"])  # Apache 2.0

package(
    default_visibility = [
        "//tensorflow_probability:__subpackages__",
    ],
)

exports_files(["LICENSE"])

py_library(
    name = "bijectors",
    srcs = ["__init__.py"],
    deps = [
        ":absolute_value",
        ":affine",
        ":affine_linear_operator",
        ":affine_scalar",
        ":batch_normalization",
        ":bijector",
        ":chain",
        ":cholesky_outer_product",
        ":cholesky_to_inv_cholesky",
        ":conditional_bijector",
        ":discrete_cosine_transform",
        ":exp",
        ":fill_triangular",
        ":gumbel",
        ":identity",
        ":inline",
        ":invert",
        ":kumaraswamy",
        ":masked_autoregressive",
        ":matrix_inverse_tril",
        ":ordered",
        ":permute",
        ":power_transform",
        ":real_nvp",
        ":reshape",
        ":scale_tril",
        ":sigmoid",
        ":sinh_arcsinh",
        ":softmax_centered",
        ":softplus",
        ":softsign",
        ":square",
        ":tanh",
        ":transform_diagonal",
        ":transpose",
        ":weibull",
    ],
)

py_library(
    name = "bijector",
    srcs = ["bijector.py"],
    deps = [
        # numpy dep,
        # six dep,
        # tensorflow dep,
        "//tensorflow_probability/python/internal:distribution_util",
    ],
)

py_library(
    name = "absolute_value",
    srcs = ["absolute_value.py"],
    deps = [
        ":bijector",
        # tensorflow dep,
    ],
)

py_library(
    name = "affine_linear_operator",
    srcs = ["affine_linear_operator.py"],
    deps = [
        ":bijector",
        ":shape",
        # tensorflow dep,
    ],
)

py_library(
    name = "affine_scalar",
    srcs = ["affine_scalar.py"],
    deps = [
        ":bijector",
        # tensorflow dep,
    ],
)

py_library(
    name = "affine",
    srcs = ["affine.py"],
    deps = [
        ":bijector",
        ":shape",
        # tensorflow dep,
        "//tensorflow_probability/python/internal:distribution_util",
        "//tensorflow_probability/python/internal:dtype_util",
    ],
)

py_library(
    name = "batch_normalization",
    srcs = ["batch_normalization.py"],
    deps = [
        ":bijector",
        # tensorflow dep,
    ],
)

py_library(
    name = "chain",
    srcs = ["chain.py"],
    deps = [
        ":bijector",
        # tensorflow dep,
    ],
)

py_library(
    name = "cholesky_outer_product",
    srcs = ["cholesky_outer_product.py"],
    deps = [
        ":bijector",
        # numpy dep,
        # tensorflow dep,
        "//tensorflow_probability/python/internal:distribution_util",
    ],
)

py_library(
    name = "cholesky_to_inv_cholesky",
    srcs = ["cholesky_to_inv_cholesky.py"],
    deps = [
        ":bijector",
        ":cholesky_outer_product",
        # tensorflow dep,
    ],
)

py_library(
    name = "conditional_bijector",
    srcs = ["conditional_bijector.py"],
    deps = [
        ":bijector",
        "//tensorflow_probability/python/internal:distribution_util",
    ],
)

py_library(
    name = "discrete_cosine_transform",
    srcs = ["discrete_cosine_transform.py"],
    deps = [
        ":bijector",
        # tensorflow dep,
#         "//tensorflow_probability/google:platform_google",  # DisableOnExport
    ],
)

py_library(
    name = "exp",
    srcs = ["exp.py"],
    deps = [":power_transform"],
)

py_library(
    name = "fill_triangular",
    srcs = ["fill_triangular.py"],
    deps = [
        ":bijector",
        # numpy dep,
        # tensorflow dep,
        "//tensorflow_probability/python/internal:distribution_util",
    ],
)

py_library(
    name = "gumbel",
    srcs = ["gumbel.py"],
    deps = [
        ":bijector",
        # tensorflow dep,
    ],
)

py_library(
    name = "identity",
    srcs = ["identity.py"],
    deps = [
        ":bijector",
        # tensorflow dep,
    ],
)

py_library(
    name = "inline",
    srcs = ["inline.py"],
    deps = [":bijector"],
)

py_library(
    name = "invert",
    srcs = ["invert.py"],
    deps = [":bijector"],
)

py_library(
    name = "kumaraswamy",
    srcs = ["kumaraswamy.py"],
    deps = [
        ":bijector",
        # tensorflow dep,
    ],
)

py_library(
    name = "masked_autoregressive",
    srcs = ["masked_autoregressive.py"],
    deps = [
        ":bijector",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_library(
    name = "matrix_inverse_tril",
    srcs = ["matrix_inverse_tril.py"],
    deps = [
        ":bijector",
        # tensorflow dep,
    ],
)

py_library(
    name = "ordered",
    srcs = ["ordered.py"],
    deps = [
        ":bijector",
        # tensorflow dep,
    ],
)

py_library(
    name = "permute",
    srcs = ["permute.py"],
    deps = [
        ":bijector",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_library(
    name = "power_transform",
    srcs = ["power_transform.py"],
    deps = [
        ":bijector",
        # tensorflow dep,
    ],
)

py_library(
    name = "real_nvp",
    srcs = ["real_nvp.py"],
    deps = [
        ":conditional_bijector",
        # tensorflow dep,
    ],
)

py_library(
    name = "reshape",
    srcs = ["reshape.py"],
    deps = [
        ":bijector",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_library(
    name = "scale_tril",
    srcs = ["scale_tril.py"],
    deps = [
        ":affine_scalar",
        ":chain",
        ":fill_triangular",
        ":softplus",
        ":transform_diagonal",
    ],
)

py_library(
    name = "shape",
    srcs = ["shape.py"],
    deps = [
        # tensorflow dep,
        "//tensorflow_probability/python/internal:distribution_util",
    ],
)

py_library(
    name = "sigmoid",
    srcs = ["sigmoid.py"],
    deps = [
        ":bijector",
        # tensorflow dep,
    ],
)

py_library(
    name = "sinh_arcsinh",
    srcs = ["sinh_arcsinh.py"],
    deps = [
        ":bijector",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_library(
    name = "softmax_centered",
    srcs = ["softmax_centered.py"],
    deps = [
        ":bijector",
        # tensorflow dep,
        "//tensorflow_probability/python/internal:distribution_util",
    ],
)

py_library(
    name = "softplus",
    srcs = ["softplus.py"],
    deps = [
        ":bijector",
        # tensorflow dep,
        "//tensorflow_probability/python/internal:distribution_util",
    ],
)

py_library(
    name = "softsign",
    srcs = ["softsign.py"],
    deps = [
        ":bijector",
        # tensorflow dep,
    ],
)

py_library(
    name = "square",
    srcs = ["square.py"],
    deps = [
        ":bijector",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_library(
    name = "tanh",
    srcs = ["tanh.py"],
    deps = [
        ":bijector",
        # tensorflow dep,
    ],
)

py_library(
    name = "transform_diagonal",
    srcs = ["transform_diagonal.py"],
    deps = [
        ":bijector",
        # tensorflow dep,
    ],
)

py_library(
    name = "transpose",
    srcs = ["transpose.py"],
    deps = [
        ":bijector",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_library(
    name = "weibull",
    srcs = ["weibull.py"],
    deps = [
        ":bijector",
        # tensorflow dep,
    ],
)

py_test(
    name = "bijector_test_util",
    srcs = ["bijector_test_util.py"],
    deps = [
        # numpy dep,
        # tensorflow dep,
        "//tensorflow_probability/python/distributions",
    ],
)

py_test(
    name = "bijector_test",
    size = "small",
    srcs = ["bijector_test.py"],
    deps = [
        ":bijectors",
        # numpy dep,
        # six dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "absolute_value_test",
    size = "small",
    srcs = ["absolute_value_test.py"],
    deps = [
        ":bijectors",
        # tensorflow dep,
    ],
)

py_test(
    name = "affine_test",
    size = "large",
    srcs = ["affine_test.py"],
    shard_count = 5,
    tags = ["noasan"],  # times out b/63678675
    deps = [
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "affine_linear_operator_test",
    size = "small",
    srcs = ["affine_linear_operator_test.py"],
    deps = [
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "affine_scalar_test",
    size = "small",
    srcs = ["affine_scalar_test.py"],
    deps = [
        ":bijector_test_util",
        # numpy dep,
        # tensorflow dep,
        "//tensorflow_probability",
    ],
)

py_test(
    name = "batch_normalization_test",
    size = "medium",
    srcs = ["batch_normalization_test.py"],
    deps = [
        ":bijectors",
        # absl/testing:parameterized dep,
        # numpy dep,
        # tensorflow dep,
        "//tensorflow_probability/python/distributions",
        "//tensorflow_probability/python/internal:test_util",
    ],
)

py_test(
    name = "chain_test",
    size = "small",
    srcs = ["chain_test.py"],
    deps = [
        ":bijector_test_util",
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "cholesky_outer_product_test",
    size = "small",
    srcs = ["cholesky_outer_product_test.py"],
    deps = [
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "cholesky_to_inv_cholesky_test",
    size = "small",
    srcs = ["cholesky_to_inv_cholesky_test.py"],
    deps = [
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "conditional_bijector_test",
    size = "small",
    srcs = ["conditional_bijector_test.py"],
    deps = [
        ":bijectors",
        # tensorflow dep,
    ],
)

py_test(
    name = "discrete_cosine_transform_test",
    size = "small",
    srcs = ["discrete_cosine_transform_test.py"],
    deps = [
        ":bijector_test_util",
        ":bijectors",
        # numpy dep,
        # scipy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "exp_test",
    size = "small",
    srcs = ["exp_test.py"],
    deps = [
        ":bijector_test_util",
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "fill_triangular_test",
    size = "small",
    srcs = ["fill_triangular_test.py"],
    deps = [
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "gumbel_test",
    size = "small",
    srcs = ["gumbel_test.py"],
    deps = [
        ":bijector_test_util",
        ":bijectors",
        # numpy dep,
        # scipy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "identity_test",
    srcs = ["identity_test.py"],
    deps = [
        ":bijector_test_util",
        ":bijectors",
        # tensorflow dep,
    ],
)

py_test(
    name = "inline_test",
    size = "small",
    srcs = ["inline_test.py"],
    deps = [
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "invert_test",
    size = "small",
    srcs = ["invert_test.py"],
    deps = [
        ":bijector_test_util",
        ":bijectors",
        # tensorflow dep,
        "//tensorflow_probability/python/distributions",
    ],
)

py_test(
    name = "kumaraswamy_test",
    size = "small",
    srcs = ["kumaraswamy_test.py"],
    deps = [
        ":bijector_test_util",
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "masked_autoregressive_test",
    size = "small",
    srcs = ["masked_autoregressive_test.py"],
    deps = [
        ":bijectors",
        ":masked_autoregressive",
        # numpy dep,
        # tensorflow dep,
        "//tensorflow_probability/python/distributions",
        "//tensorflow_probability/python/internal:test_util",
    ],
)

py_test(
    name = "matrix_inverse_tril_test",
    size = "small",
    srcs = ["matrix_inverse_tril_test.py"],
    deps = [
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "ordered_test",
    srcs = ["ordered_test.py"],
    deps = [
        ":bijector_test_util",
        # numpy dep,
        # tensorflow dep,
        "//tensorflow_probability",
    ],
)

py_test(
    name = "permute_test",
    size = "small",
    srcs = ["permute_test.py"],
    deps = [
        ":bijector_test_util",
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "power_transform_test",
    size = "small",
    srcs = ["power_transform_test.py"],
    deps = [
        ":bijector_test_util",
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "real_nvp_test",
    size = "small",
    srcs = ["real_nvp_test.py"],
    deps = [
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
        "//tensorflow_probability/python/distributions",
        "//tensorflow_probability/python/internal:test_util",
    ],
)

py_test(
    name = "reshape_test",
    size = "medium",
    srcs = ["reshape_test.py"],
    deps = [
        ":bijector_test_util",
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "scale_tril_test",
    size = "medium",
    srcs = ["scale_tril_test.py"],
    deps = [
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "shape_test",
    size = "medium",
    srcs = ["shape_test.py"],
    deps = [
        ":shape",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "sigmoid_test",
    size = "small",
    srcs = ["sigmoid_test.py"],
    deps = [
        ":bijector_test_util",
        ":bijectors",
        # numpy dep,
        # scipy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "sinh_arcsinh_test",
    size = "small",
    srcs = ["sinh_arcsinh_test.py"],
    tags = ["no_windows"],  # TODO: needs investigation on Windows.
    deps = [
        ":bijector_test_util",
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "softmax_centered_test",
    size = "small",
    srcs = ["softmax_centered_test.py"],
    deps = [
        ":bijector_test_util",
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "softplus_test",
    size = "small",
    srcs = ["softplus_test.py"],
    deps = [
        ":bijector_test_util",
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "softsign_test",
    size = "small",
    srcs = ["softsign_test.py"],
    deps = [
        ":bijector_test_util",
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "square_test",
    size = "small",
    srcs = ["square_test.py"],
    deps = [
        ":bijector_test_util",
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "tanh_test",
    size = "small",
    srcs = ["tanh_test.py"],
    deps = [
        ":bijector_test_util",
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "transform_diagonal_test",
    size = "small",
    srcs = ["transform_diagonal_test.py"],
    deps = [
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "transpose_test",
    size = "small",
    srcs = ["transpose_test.py"],
    deps = [
        ":bijectors",
        # numpy dep,
        # tensorflow dep,
    ],
)

py_test(
    name = "weibull_test",
    size = "small",
    srcs = ["weibull_test.py"],
    deps = [
        ":bijector_test_util",
        ":bijectors",
        # numpy dep,
        # scipy dep,
        # tensorflow dep,
    ],
)

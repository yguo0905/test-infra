git_repository(
    name = "io_bazel_rules_go",
    commit = "bfad99993ea297e85ac3606226debcc26ee54972",
    remote = "https://github.com/bazelbuild/rules_go.git",
)

load("@io_bazel_rules_go//go:def.bzl", "go_repositories")

go_repositories()

git_repository(
    name = "org_pubref_rules_node",
    commit = "bd14a465063da90f632bad46c1efbf802c339e68",
    remote = "https://github.com/pubref/rules_node.git",
)

load("@org_pubref_rules_node//node:rules.bzl", "node_repositories", "npm_repository")

node_repositories()

load(":test_infra.bzl", "http_archive_with_pkg_path")

http_archive_with_pkg_path(
    name = "ruamel_yaml",
    build_file_content = """
py_library(
    name = "ruamel.yaml",
    srcs = glob(["*.py"]),
    visibility = ["//visibility:public"],
)
""",
    pkg_path = "ruamel/yaml",
    sha256 = "350496f6fdd8c2bb17a0fa3fd2ec98431280cf12d72dae498b19ac0119c2bbad",
    strip_prefix = "ruamel.yaml-0.15.9",
    url = "https://pypi.python.org/packages/83/90/2eecde4bbd6a67805080091e83a29100c2f7d2afcaf926d75da5839f9283/ruamel.yaml-0.15.9.tar.gz",
)

npm_repository(
    name = "npm_mocha",
    deps = {
        "mocha": "3.2.0",
    },
)

new_http_archive(
    name = "requests",
    build_file_content = """
py_library(
    name = "requests",
    srcs = glob(["**/*.py"]),
    visibility = ["//visibility:public"],
)
""",
    sha256 = "5722cd09762faa01276230270ff16af7acf7c5c45d623868d9ba116f15791ce8",
    strip_prefix = "requests-2.13.0/requests",
    urls = ["https://pypi.python.org/packages/16/09/37b69de7c924d318e51ece1c4ceb679bf93be9d05973bb30c35babd596e2/requests-2.13.0.tar.gz"],
)

new_http_archive(
    name = "yaml",
    build_file_content = """
py_library(
    name = "yaml",
    srcs = glob(["*.py"]),
    visibility = ["//visibility:public"],
)
""",
    sha256 = "592766c6303207a20efc445587778322d7f73b161bd994f227adaa341ba212ab",
    strip_prefix = "PyYAML-3.12/lib/yaml",
    urls = ["https://pypi.python.org/packages/4a/85/db5a2df477072b2902b0eb892feb37d88ac635d36245a72a6a69b23b383a/PyYAML-3.12.tar.gz"],
)

new_http_archive(
    name = "markupsafe",
    build_file_content = """
py_library(
    name = "markupsafe",
    srcs = glob(["*.py"]),
    visibility = ["//visibility:public"],
)
""",
    sha256 = "a6be69091dac236ea9c6bc7d012beab42010fa914c459791d627dad4910eb665",
    strip_prefix = "MarkupSafe-1.0/markupsafe",
    urls = ["https://pypi.python.org/packages/4d/de/32d741db316d8fdb7680822dd37001ef7a448255de9699ab4bfcbdf4172b/MarkupSafe-1.0.tar.gz"],
)

new_http_archive(
    name = "jinja2",
    build_file_content = """
py_library(
    name = "jinja2",
    srcs = glob(["*.py"]),
    deps = [
        "@markupsafe//:markupsafe",
    ],
    visibility = ["//visibility:public"],
)
""",
    sha256 = "702a24d992f856fa8d5a7a36db6128198d0c21e1da34448ca236c42e92384825",
    strip_prefix = "Jinja2-2.9.5/jinja2",
    urls = ["https://pypi.python.org/packages/71/59/d7423bd5e7ddaf3a1ce299ab4490e9044e8dfd195420fc83a24de9e60726/Jinja2-2.9.5.tar.gz"],
)

http_file(
    name = "jq",
    executable = 1,
    sha256 = "c6b3a7d7d3e7b70c6f51b706a3b90bd01833846c54d32ca32f0027f00226ff6d",
    urls = ["https://github.com/stedolan/jq/releases/download/jq-1.5/jq-linux64"],
)

new_http_archive(
    name = "astroid_lib",
    build_file_content = """
py_library(
    name = "astroid_lib",
    srcs = glob(["**/*.py"]),
    deps = [
      "@six_lib//:six",
      "@wrapt//:wrapt",
      "@enum34//:enum34",
      "@lazy_object_proxy//:lazy_object_proxy",
      "@singledispatch_lib//:singledispatch_lib",
      "@backports//:backports",
    ],
    visibility = ["//visibility:public"],
    imports = ["astroid"],
)
""",
    sha256 = "492c2a2044adbf6a84a671b7522e9295ad2f6a7c781b899014308db25312dd35",
    strip_prefix = "astroid-1.5.3",
    urls = ["https://pypi.python.org/packages/d7/b7/112288f75293d6f12b1e41bac1e822fd0f29b0f88e2c4378cdd295b9d838/astroid-1.5.3.tar.gz"],
)

new_http_archive(
    name = "isort",
    build_file_content = """
py_library(
    name = "isort",
    srcs = glob(["**/*.py"]),
    visibility = ["//visibility:public"],
)
""",
    sha256 = "79f46172d3a4e2e53e7016e663cc7a8b538bec525c36675fcfd2767df30b3983",
    strip_prefix = "isort-4.2.15/isort",
    urls = ["https://pypi.python.org/packages/4d/d5/7c8657126a43bcd3b0173e880407f48be4ac91b4957b51303eab744824cf/isort-4.2.15.tar.gz"],
)

new_http_archive(
    name = "lazy_object_proxy",
    build_file_content = """
py_library(
    name = "lazy_object_proxy",
    srcs = glob(["**/*.py"]),
    visibility = ["//visibility:public"],
)
""",
    sha256 = "eb91be369f945f10d3a49f5f9be8b3d0b93a4c2be8f8a5b83b0571b8123e0a7a",
    strip_prefix = "lazy-object-proxy-1.3.1/src/lazy_object_proxy",
    urls = ["https://pypi.python.org/packages/55/08/23c0753599bdec1aec273e322f277c4e875150325f565017f6280549f554/lazy-object-proxy-1.3.1.tar.gz"],
)

new_http_archive(
    name = "mccabe",
    build_file_content = """
py_library(
    name = "mccabe",
    srcs = glob(["**/*.py"]),
    visibility = ["//visibility:public"],
)
""",
    sha256 = "dd8d182285a0fe56bace7f45b5e7d1a6ebcbf524e8f3bd87eb0f125271b8831f",
    strip_prefix = "mccabe-0.6.1",
    urls = ["https://pypi.python.org/packages/06/18/fa675aa501e11d6d6ca0ae73a101b2f3571a565e0f7d38e062eec18a91ee/mccabe-0.6.1.tar.gz"],
)

new_http_archive(
    name = "pylint",
    build_file_content = """
py_library(
    name = "pylint",
    srcs = glob(["**/*.py"]),
    deps = [
      "@astroid_lib//:astroid_lib",
      "@six_lib//:six",
      "@isort//:isort",
      "@mccabe//:mccabe",
      "@configparser_lib//:configparser_lib",
    ],
    visibility = ["//visibility:public"],
)
""",
    sha256 = "8b4a7ab6cf5062e40e2763c0b4a596020abada1d7304e369578b522e46a6264a",
    strip_prefix = "pylint-1.7.1/pylint",
    urls = ["https://pypi.python.org/packages/cc/8c/d1da590769213fefedea4b345e90fce80f749c61ab9f9187b3fe19397b4b/pylint-1.7.1.tar.gz"],
)

new_http_archive(
    name = "six_lib",
    build_file_content = """
py_library(
    name = "six",
    srcs = glob(["**/*.py"]),
    visibility = ["//visibility:public"],
)
""",
    sha256 = "105f8d68616f8248e24bf0e9372ef04d3cc10104f1980f54d57b2ce73a5ad56a",
    strip_prefix = "six-1.10.0",
    urls = ["https://pypi.python.org/packages/b3/b2/238e2590826bfdd113244a40d9d3eb26918bd798fc187e2360a8367068db/six-1.10.0.tar.gz"],
)

new_http_archive(
    name = "wrapt",
    build_file_content = """
py_library(
    name = "wrapt",
    srcs = glob(["**/*.py"]),
    visibility = ["//visibility:public"],
)
""",
    sha256 = "42160c91b77f1bc64a955890038e02f2f72986c01d462d53cb6cb039b995cdd9",
    strip_prefix = "wrapt-1.10.10/src/wrapt",
    urls = ["https://pypi.python.org/packages/a3/bb/525e9de0a220060394f4aa34fdf6200853581803d92714ae41fc3556e7d7/wrapt-1.10.10.tar.gz"],
)

new_http_archive(
    name = "enum34",
    build_file_content = """
py_library(
    name = "enum34",
    srcs = glob(["**/*.py"]),
    visibility = ["//visibility:public"],
)
""",
    sha256 = "8ad8c4783bf61ded74527bffb48ed9b54166685e4230386a9ed9b1279e2df5b1",
    strip_prefix = "enum34-1.1.6",
    urls = ["https://pypi.python.org/packages/bf/3e/31d502c25302814a7c2f1d3959d2a3b3f78e509002ba91aea64993936876/enum34-1.1.6.tar.gz"],
)

new_http_archive(
    name = "singledispatch_lib",
    build_file_content = """
py_library(
    name = "singledispatch_lib",
    srcs = glob(["**/*.py"]),
    deps = [
      "@six_lib//:six",
    ],
    visibility = ["//visibility:public"],
)
""",
    sha256 = "5b06af87df13818d14f08a028e42f566640aef80805c3b50c5056b086e3c2b9c",
    strip_prefix = "singledispatch-3.4.0.3",
    urls = ["https://pypi.python.org/packages/d9/e9/513ad8dc17210db12cb14f2d4d190d618fb87dd38814203ea71c87ba5b68/singledispatch-3.4.0.3.tar.gz"],
)

new_http_archive(
    name = "backports",
    build_file_content = """
py_library(
    name = "backports",
    srcs = glob(["**/*.py"]),
    visibility = ["//visibility:public"],
)
""",
    sha256 = "31f235852f88edc1558d428d890663c49eb4514ffec9f3650e7f3c9e4a12e36f",
    strip_prefix = "backports.functools_lru_cache-1.4/backports",
    urls = ["https://pypi.python.org/packages/4e/91/0e93d9455254b7b630fb3ebe30cc57cab518660c5fad6a08aac7908a4431/backports.functools_lru_cache-1.4.tar.gz"],
)

new_http_archive(
    name = "configparser_lib",
    build_file_content = """
py_library(
    name = "configparser_lib",
    srcs = glob(["**/*.py"]),
    visibility = ["//visibility:public"],
    imports = ["backports"],
)
""",
    sha256 = "5308b47021bc2340965c371f0f058cc6971a04502638d4244225c49d80db273a",
    strip_prefix = "configparser-3.5.0/src",
    urls = ["https://pypi.python.org/packages/7c/69/c2ce7e91c89dc073eb1aa74c0621c3eefbffe8216b3f9af9d3885265c01c/configparser-3.5.0.tar.gz"],
)

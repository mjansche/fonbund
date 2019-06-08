workspace(name = "language_resources")

load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

# Subpar

http_archive(
    name = "subpar",
    strip_prefix = "subpar-master",
    urls = ["https://github.com/google/subpar/archive/master.zip"],
)

# PanPhon, PHOIBLE and PhonClassCounts databases

http_archive(
    name = "panphon",
    build_file = "//bazel:panphon.BUILD",
    strip_prefix = "panphon-master",
    urls = ["https://github.com/dmort27/panphon/archive/master.zip"],
)

http_archive(
    name = "clld_phoible",
    build_file = "//bazel:clld_phoible.BUILD",
    strip_prefix = "phoible-9f1201fea60687267a7f2c6532293627fa04da65",
    urls = ["https://github.com/clld/phoible/archive/9f1201fea60687267a7f2c6532293627fa04da65.zip"],
)

http_archive(
    name = "phon_class_counts",
    build_file = "//bazel:phon_class_counts.BUILD",
    strip_prefix = "phon-class-counts-master",
    urls = ["https://github.com/ddediu/phon-class-counts/archive/master.zip"],
)

# Protobuf

protobuf_version = "3.8.0"

http_archive(
    name = "com_google_protobuf",
    strip_prefix = "protobuf-%s" % protobuf_version,
    urls = [
        "https://github.com/protocolbuffers/protobuf/archive/v%s.tar.gz"
	% protobuf_version,
    ],
)

load("@com_google_protobuf//:protobuf_deps.bzl", "protobuf_deps")

protobuf_deps()

http_archive(
    name = "six_archive",
    build_file = "//bazel:six.BUILD",
    sha256 = "70e8a77beed4562e7f14fe23a786b54f6296e34344c23bc42f07b15018ff98e9",
    strip_prefix = "six-1.11.0",
    urls = ["https://pypi.python.org/packages/16/d8/bc6316cf98419719bd59c91742194c111b6f2e85abac88e496adefaf7afe/six-1.11.0.tar.gz#md5=d12789f9baf7e9fb2524c0c64f1773f8"],
)

http_archive(
    name = "bazel_skylib",
    strip_prefix = "bazel-skylib-master",
    urls = ["https://github.com/bazelbuild/bazel-skylib/archive/master.zip"],
)

bind(
    name = "six",
    actual = "@six_archive//:six",
)

http_archive(
    name = "io_abseil_py",
    strip_prefix = "abseil-py-master",
    urls = ["https://github.com/abseil/abseil-py/archive/master.zip"],
)

bind(
    name = "absl/app",
    actual = "@io_abseil_py//absl:app",
)

bind(
    name = "absl/flags",
    actual = "@io_abseil_py//absl/flags",
)

bind(
    name = "absl/logging",
    actual = "@io_abseil_py//absl/logging",
)

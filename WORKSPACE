workspace(name = "io_kubernetes_build")

# The native http_archive rule is deprecated. This is a drop-in replacement.
load("@bazel_tools//tools/build_defs/repo:http.bzl", "http_archive")

################################################################################
# Go Build Definitions
################################################################################

# Download, load, and initialize the Go build rules.
http_archive(
    name = "io_bazel_rules_go",
    strip_prefix = "rules_go-0.16.6",
    urls = ["https://github.com/bazelbuild/rules_go/archive/0.16.6.zip"],
    sha256 = "c0f7e581b17d0b8252e1d0175cb3f6398a579bb91d2e5995f29f6c5985ccd647",
)

load("@io_bazel_rules_go//go:def.bzl", "go_register_toolchains", "go_rules_dependencies")

go_rules_dependencies()

go_register_toolchains()

# Download, load, and initialize the Gazelle tool for generating BUILD files for
# Go code.
http_archive(
    name = "bazel_gazelle",
    strip_prefix = "bazel-gazelle-0.16.0",
    urls = ["https://github.com/bazelbuild/bazel-gazelle/archive/0.16.0.zip"],
    sha256 = "a5b329e3d929247279005ba3cfda0c092a220085c0ed0505de1dcdd68dfc53bc",
)

load("@bazel_gazelle//:deps.bzl", "gazelle_dependencies", "go_repository")

gazelle_dependencies()

################################################################################
# Go Dependencies
#
# Update this with:
#   bazel run //:gazelle -- update-repos -from_file=Gopkg.lock
################################################################################

go_repository(
    name = "com_github_blang_semver",
    importpath = "github.com/blang/semver",
    tag = "v3.5.1",
)

go_repository(
    name = "com_github_davecgh_go_spew",
    importpath = "github.com/davecgh/go-spew",
    tag = "v1.1.1",
)

go_repository(
    name = "com_github_go_kit_kit",
    importpath = "github.com/go-kit/kit",
    tag = "v0.8.0",
)

go_repository(
    name = "com_github_go_logfmt_logfmt",
    importpath = "github.com/go-logfmt/logfmt",
    tag = "v0.4.0",
)

go_repository(
    name = "com_github_golang_protobuf",
    importpath = "github.com/golang/protobuf",
    tag = "v1.2.0",
)

go_repository(
    name = "com_github_google_go_github",
    importpath = "github.com/google/go-github",
    tag = "v17.0.0",
)

go_repository(
    name = "com_github_google_go_querystring",
    importpath = "github.com/google/go-querystring",
    tag = "v1.0.0",
)

go_repository(
    name = "com_github_kolide_kit",
    commit = "c155a91098e3",
    importpath = "github.com/kolide/kit",
)

go_repository(
    name = "com_github_kr_logfmt",
    commit = "b84e30acd515",
    importpath = "github.com/kr/logfmt",
)

go_repository(
    name = "com_github_pkg_errors",
    importpath = "github.com/pkg/errors",
    tag = "v0.8.1",
)

go_repository(
    name = "com_github_pmezard_go_difflib",
    importpath = "github.com/pmezard/go-difflib",
    tag = "v1.0.0",
)

go_repository(
    name = "com_github_stretchr_testify",
    importpath = "github.com/stretchr/testify",
    tag = "v1.3.0",
)

go_repository(
    name = "org_golang_google_appengine",
    importpath = "google.golang.org/appengine",
    tag = "v1.3.0",
)

go_repository(
    name = "org_golang_x_net",
    commit = "161cd47e91fd",
    importpath = "golang.org/x/net",
)

go_repository(
    name = "org_golang_x_oauth2",
    commit = "d2e6202438be",
    importpath = "golang.org/x/oauth2",
)

go_repository(
    name = "com_github_alecthomas_template",
    commit = "a0175ee3bccc",
    importpath = "github.com/alecthomas/template",
)

go_repository(
    name = "com_github_beorn7_perks",
    commit = "3a771d992973",
    importpath = "github.com/beorn7/perks",
)

go_repository(
    name = "com_github_ghodss_yaml",
    importpath = "github.com/ghodss/yaml",
    tag = "v1.0.0",
)

go_repository(
    name = "com_github_go_sql_driver_mysql",
    importpath = "github.com/go-sql-driver/mysql",
    tag = "v1.4.1",
)

go_repository(
    name = "com_github_go_stack_stack",
    importpath = "github.com/go-stack/stack",
    tag = "v1.7.0",
)

go_repository(
    name = "com_github_golang_glog",
    commit = "23def4e6c14b",
    importpath = "github.com/golang/glog",
)

go_repository(
    name = "com_github_google_go_cmp",
    importpath = "github.com/google/go-cmp",
    tag = "v0.2.0",
)

go_repository(
    name = "com_github_google_go_github_v21",
    commit = "2406bfd7f32d",
    importpath = "github.com/google/go-github/v21",
)

go_repository(
    name = "com_github_google_uuid",
    commit = "064e2069ce9c",
    importpath = "github.com/google/uuid",
)

go_repository(
    name = "com_github_grpc_ecosystem_grpc_gateway",
    importpath = "github.com/grpc-ecosystem/grpc-gateway",
    tag = "v1.5.0",
)

go_repository(
    name = "com_github_jmoiron_sqlx",
    commit = "2aeb6a910c2b",
    importpath = "github.com/jmoiron/sqlx",
)

go_repository(
    name = "com_github_lib_pq",
    importpath = "github.com/lib/pq",
    tag = "v1.0.0",
)

go_repository(
    name = "com_github_mattn_go_sqlite3",
    importpath = "github.com/mattn/go-sqlite3",
    tag = "v1.10.0",
)

go_repository(
    name = "com_github_matttproud_golang_protobuf_extensions",
    importpath = "github.com/matttproud/golang_protobuf_extensions",
    tag = "v1.0.1",
)

go_repository(
    name = "com_github_oklog_ulid",
    importpath = "github.com/oklog/ulid",
    tag = "v0.3.0",
)

go_repository(
    name = "com_github_opencensus_integrations_ocsql",
    importpath = "github.com/opencensus-integrations/ocsql",
    tag = "v0.1.1",
)

go_repository(
    name = "com_github_openzipkin_zipkin_go",
    importpath = "github.com/openzipkin/zipkin-go",
    tag = "v0.1.1",
)

go_repository(
    name = "com_github_prometheus_client_golang",
    importpath = "github.com/prometheus/client_golang",
    tag = "v0.8.0",
)

go_repository(
    name = "com_github_prometheus_client_model",
    commit = "5c3871d89910",
    importpath = "github.com/prometheus/client_model",
)

go_repository(
    name = "com_github_prometheus_common",
    commit = "c7de2306084e",
    importpath = "github.com/prometheus/common",
)

go_repository(
    name = "com_github_prometheus_procfs",
    commit = "05ee40e3a273",
    importpath = "github.com/prometheus/procfs",
)

go_repository(
    name = "com_github_stretchr_objx",
    importpath = "github.com/stretchr/objx",
    tag = "v0.1.0",
)

go_repository(
    name = "in_gopkg_check_v1",
    commit = "20d25e280405",
    importpath = "gopkg.in/check.v1",
)

go_repository(
    name = "in_gopkg_yaml_v2",
    importpath = "gopkg.in/yaml.v2",
    tag = "v2.2.1",
)

go_repository(
    name = "io_opencensus_go",
    importpath = "go.opencensus.io",
    tag = "v0.18.0",
)

go_repository(
    name = "org_apache_git_thrift_git",
    commit = "2566ecd5d999",
    importpath = "git.apache.org/thrift.git",
)

go_repository(
    name = "org_golang_google_api",
    commit = "7ca32eb868bf",
    importpath = "google.golang.org/api",
)

go_repository(
    name = "org_golang_google_genproto",
    commit = "11092d34479b",
    importpath = "google.golang.org/genproto",
)

go_repository(
    name = "org_golang_google_grpc",
    importpath = "google.golang.org/grpc",
    tag = "v1.14.0",
)

go_repository(
    name = "org_golang_x_crypto",
    commit = "614d502a4dac",
    importpath = "golang.org/x/crypto",
)

go_repository(
    name = "org_golang_x_sync",
    commit = "42b317875d0f",
    importpath = "golang.org/x/sync",
)

go_repository(
    name = "org_golang_x_sys",
    commit = "d0be0721c37e",
    importpath = "golang.org/x/sys",
)

go_repository(
    name = "org_golang_x_text",
    importpath = "golang.org/x/text",
    tag = "v0.3.0",
)

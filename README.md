# ansible-role-app-grafana
## Default variables
| Name | Type | Value | Comments |
| ---- | ---- | ----- | -------- |
| grafana_arch | string | linux-amd64 ||
| grafana_builds | list(dict) | see `defaults/main.yml` ||
| grafana_config_file | UnixPath |  `$grafana_dir_etc/grafana.ini` ||
| grafana_dir_bin | UnixPath | `/opt/grafana` ||
| grafana_dir_etc | UnixPath | `/etc/grafana` ||
| grafana_dir_lib | UnixPath | `/var/lib/grafana` ||
| grafana_dir_log | UnixPath | `/var/log/grafana` ||
| grafana_dirs | list(dict) | see `defaults/main.yml` | directories to create |
| grafana_download_base | URL | `https://dl.grafana.com/enterprise/release` ||
| grafana_pkg_dependencies | list(string) | see `defaults/main.yml` ||
| grafana_port_http | integer | 3000 ||
| grafana_user | string | grafana ||
| grafana_suffix | string | tar.gz ||
| grafana_svc_enabled | string | true ||
| grafana_svc_name | string | grafana ||
| grafana_svc_state | string | started ||
| grafana_version | string | "9.1.6" ||

----
# ansible-role-app-grafana

## Default variables
| Name | Type | Value | Comments |
| ---- | ---- | ----- | -------- |
| grafana_allow_embedding | Boolean | false | see [docs](https://grafana.com/docs/grafana/latest/setup-grafana/configure-grafana/#allow_embedding) |
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

## Optional variables
| Name | Type | Comments |
| ---- | ---- | -------- |
| grafana_domain | string | Only needed if using reverse proxy |
| grafana_plugins | list(dict(name,state,version)) | plugins to install key(version) is optional |

## Database variables
Setting `grafana_db_password` is the trigger for rendering the `database` section in `grafana.ini`

| Name | Type | DefaultIfApplic | Comments |
| ---- | ---- | --------------- | -------- |
| grafana_db_dbname | string | grafana | name of the db Grafana will use as its backend |
| grafana_db_host | string | `127.0.0.1` | i.e. PostgreSQL on localhost |
| grafana_db_password | string |||
| grafana_db_port | integer |  5432 | i.e. PostgreSQL ||
| grafana_db_ssl_mode | string | disable ||
| grafana_db_type | string | postgres ||
| grafana_db_username | string |||

## SMTP variables
Setting `grafana_smtp_password` is the trigger for rendering the `SMTP` section in `grafana.ini`

| Name | Type | DefaultIfApplic | Comments |
| ---- | ---- | --------------- | -------- |
| grafana_smtp_from_address | string | who emails come from , e.g. `grafana@example.com` |
| grafana_smtp_hostname | hostname:port | how to contact the SMTP server |
| grafana_smtp_password | string | password for the SMTP server |
| grafana_smtp_port | integer | 25 | concatenated with `grafana_smtp_hostname` |
| grafana_smtp_username | string | username on the SMTP server |

----

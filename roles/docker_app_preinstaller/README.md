# Expected inputs

## Mandatory

`app_name`
default: /src/docker

## Optional

`app_parent_dir`
default: /src/docker

`app_user`
default: none

User will be created if defined

`svc_volumes`
Handles volume creation in service

### Keys for svc_volumes
`bind_mounts`
svc_volumes.bind_mounts
Structure
- volume_name
  - dir_name: *fully qualified local directory name*
  - bind_to: *pod_volume*
  - dir_contents (optional)
    - name: local file path and name, ex: template/rooster.j2
    - file_owner: uid
    - file_group: gid

Creates the following values:

`docker_app_user`: Result from ansible.builtin.user
# dev_RStudioRH8
RStudio Workspace and Development on RHEL 8.x

#### Authentication with AD
- add the following to /etc/sssd/sssd.conf
  `ad_gpo_map_service = +rstudio` <br/>

  `$sudo systemctl restart sssd` <br/>

# dev_RStudioRH8
RStudio Workspace and Development on RHEL 8.x

#### Issues and Resolutions
- Cannot install RStudio Desktop and Server on same machine <br/>
  Install RStudio Server: <br/>
  `$sudo dnf install -y https://download2.rstudio.org/server/rhel8/x86_64/rstudio-server-rhel-2023.06.2-561-x86_64.rpm` <br/>

  Then install RStudio Desktop: <br/>
  `$sudo rpm -Uvh https://download1.rstudio.org/electron/rhel8/x86_64/rstudio-2023.06.2-561-x86_64.rpm` <br/>

  
#### Authentication with AD
- add the following to /etc/sssd/sssd.conf
  `ad_gpo_map_service = +rstudio` <br/>

  `$sudo systemctl restart sssd` <br/>

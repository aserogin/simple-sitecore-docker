FROM microsoft/aspnet

SHELL ["powershell", "-NoProfile", "-Command", "$ErrorActionPreference = 'Stop';"] 

RUN  mkdir C:\Workplace\Website
RUN  mkdir C:\Workplace\Data

# DNS Resolver Cache Service
RUN set-itemproperty -path 'HKLM:\SYSTEM\CurrentControlSet\Services\Dnscache\Parameters' \
    -Name ServerPriorityTimeLimit -Value 0 -Type DWord

# Configure IIS
RUN Import-module IISAdministration; \
    New-IISSite -Name "Sitecore" -PhysicalPath C:\Workplace\Website -BindingInformation "*:80:"; \
    Remove-IISSite -Name 'Default Web Site' -Confirm:$false;
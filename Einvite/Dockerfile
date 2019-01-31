FROM microsoft/iis
 
RUN mkdir c:\Einvite
RUN powershell -NoProfile -Command \
    Install-WindowsFeature NET-Framework-45-ASPNET; \
    Install-WindowsFeature Web-Asp-Net45; \
    Import-Module IISAdministration; \
    New-IISSite -Name "MyApp" -PhysicalPath C:\Einvite -BindingInformation "*:8000:"
 
EXPOSE 8000
 
ADD bin/ /Einvite
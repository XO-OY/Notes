### Edge闪退
    1.扫描修复系统文件 sfc /scannow
    2.重装edge
    Get-AppXPackage -AllUsers -Name Microsoft.MicrosoftEdge | Foreach {Add-AppxPackage -DisableDevelopmentMode -Register "$($_.InstallLocation)\AppXManifest.xml" -Verbose}
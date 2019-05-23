# Script removes files with the same name but different extension
# Run with Windows PowerShell

# Extension to keep
$ExtRetain = ".xxx"

# Path
$Directory = "Drive:\Dir\"

# Get files to keep
$FilesToKeep = Get-ChildItem -Path $Directory -Filter *$ExtRetain

# Delete duplicates with different extension
ForEach ($File in $FilesToKeep) {
    Get-ChildItem -Path $Directory | Where {$_.BaseName -eq $File.BaseName -and $_.Extension -ne $ExtRetain} | Remove-Item -Force
}

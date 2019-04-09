# Windows Tricks

- ## Bypassing install requirement checks in .msi files (ex. iCloud64.msi):

**1.** Download iCloud64.msi (iCloud 6.0.2.10, 34.3 MB) via direct link
OR (when newer versions are going to be shipped)

- 1.1) download iCloudSetup.exe: https://support.apple.com/en-us/HT204283

- 1.2) run iCloudSetup.exe as Administrator, don't click OK when error pops up

- 1.3) open Windows Explorer and type %TEMP% into address bar, hit Enter

- 1.4) find folder contating iCloud64.msi (or iCloud.msi for 32-bit Windows) in that %TEMP% folder. (File may be in IXP909.TMP folder.)

- 1.5) copy iCloud64.msi to desktop, click OK in installer error window

**2.** Download and run Orca-x86_en-us.msi (MSI editor, 484 KB):

- 2.1) download the standalone Windows 10 SDK (1.1 MB) at this page

- 2.2) run SDKSETUP.EXE

- 2.3) select Download the Windows SDK and specify destination folder

- 2.4) select features to download: check only "MSI Tools" (54 MB)

- 2.5) when download is done, open destination folder
       and run Installers/Orca-x86_en-us.msi

- 2.6) run Orca-x86_en-us.msi as Administrator

**3.** Run Orca from Start and open iCloud64.msi

**4.** Select LaunchCondition on the left, select MS_MEDIAFEATUREPACK_INSTALLED-related line on the right

**5.** Click Cut Row button on the toolbar

**6.** Save iCloud64.msi

**7.** Finally run iCloud64.msi and reboot

**8.** Say "Thank you Apple Inc. for this wonderful evening!"

- [x] Mercury

- [ ] dadf

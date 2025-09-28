# CDU's Windows Vista Updated ISO 2025-09

- Verdict: **🍅 Terrible!**

Well, What to say... This ISO is terrible. From broken codecs to broken TrustedInstaller, the only use for this ISO is to take stuff from it for your own ISO.

Pros:
- It uses a Windows 7 PE with Windows Vista's setup so you can install it on real hardware without slipstreaming USB 3 drivers.
- It has the winload/ci patch pre-integrated so all the driver patches will work without enabling Test Mode.
- It has the Drift patch pre-included (NTOSKRNL patch).
- It has NTOSKRNL progwrp included.
- It integrates Windows 10 build 1607 and Micron NVME drivers by default.
- It integrates some manufacturers ethernet drivers by default.
- It has ACPI Wake Alarm driver pre-included.
- It has .NET Framework 4.6.2, Visual C++ up to 2022, DirectX, XNA pre-included.
- It has the latest updates (2025-09) for all the components (Powershell 3, Internet Explorer 9, .NET...)

Cons:
- Internet Explorer 9 is pre-included by default with no option to revert back to Internet Explorer 7.
- Some Ultimate Extras addons are pre-installed by default with no option to uninstall them (Check the issues section for more info about this.)
- It modifies system components for "cosmetics" (Pre-includes some Vize icons and [vaporvance fixed folder icons](https://www.deviantart.com/vaporvance/art/Vista-folder-icons-16px-fix-966771384)) which could not be considered as a vanilla up to date ISO.
- It includes unofficial patches by default which could be considered the same thing as the point before.
- It has Hyper-V on by default which will cause problems with other hypervisor software.

Issues I've discovered while using this ISO:
- TrustedInstaller is just broken on this ISO. Everything that relies on it will crash.
- SFC is broken due to TrustedInstaller being broken.
<img width="701" height="370" src="https://github.com/user-attachments/assets/9635424a-c19a-4ea9-8824-d7974e2c998e" />
- slgmr /rearm will give "Error: 0XC004D307: The maximum allowed number of re-arms has been exceeded."
- sysprep.exe generalize will not work due to the same issue as the point above.
- **"Turn Windows features on or off" is broken**. So any features turned on by default cannot be turned off (e.g: Hyper-V cannot be turned off)
- Windows Dreamscene is pre-installed but all the extra wallpapers were removed. (Why even include it in the first place if you were just going to remove most of it.)
- Windows Media Player 11 cannot play anything by default. WMA/WMV will refuse to play.
- The pre-included Ultimate Extras cannot be uninstalled as they won't show in "View installed updates"
  
<img width="927" height="554" src="https://github.com/user-attachments/assets/15ee4987-d575-40bc-ab06-5ac74d575842" />

<img width="547" height="299" src="https://github.com/user-attachments/assets/8a0ef915-4fb9-4d3a-9a75-ae06c96bf709" />

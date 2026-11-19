# Samsung A21s Clock 31dp RRO — one-file build

**This is a build package, NOT a compiled APK/KernelSU module.** The runtime producing this file did not have Android AAPT2 and could not fetch the tool, so build status and device compatibility are unknown.

User device: Galaxy A21s with A26 Android 16 port ROM, KernelSU. Existing `status_bar_left_clock_starting_padding` read as 0.0dip; experimental target is 31dp.

## To build
Place `.github/workflows/clock-31dp-onefile.yml` in a GitHub repo on the default branch; select Actions > Build Galaxy A21s Clock 31dp Overlay TEST > Run workflow. The workflow creates all its source itself; no extra APK or project uploads are required. Download `A21s-Clock-31dp-EXPERIMENTAL-TEST` from Artifacts after a successful build.

The produced RRO is an independently built test-key-signed package targeting `com.android.systemui`; the test ZIP does not modify or re-sign `SystemUI.apk` and does not auto-enable the overlay. Any attempt to install it depends on ROM overlayable restrictions, root mounts, and recovery path. **Do not flash/install this experimental module before inspecting build logs and ensuring you can recover from SystemUI instability.** A successful build is not a device test.

Do not disable the device's auto-generated SystemUI RRO. Verify compatibility and `idmap2` state before enabling any test overlay.

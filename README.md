# TRACE downloads

[Download TRACE 2.0.2 for Windows](https://github.com/sandovaljoseph/TRACE-releases/releases/download/v2.0.2/TRACE-2.0.2-windows-x64.exe).

Run the `.exe` and choose recording support or the inference providers you need. Setup downloads selected components automatically; Python, conda, and a source checkout are not required.

The installer is about 756 MiB. Selecting all inference providers downloads another 8.2 GiB; allow about 30 GB of free space during full setup.

Windows 10 x64 build 19041 or newer and a compatible NVIDIA GPU/driver are required for NVENC recording and CUDA inference. The installer is unsigned and may appear as an unknown publisher in Windows.

## First recording

1. Connect your cameras and open TRACE from the Start menu. In **File → Camera Setup**, select the cameras and capture modes, then choose **Save cameras**.
2. Choose **Start Live View** to check the previews.
3. Choose **Start Recording**, then **Stop Recording** to finalize the take. Sessions are saved in `trace-sessions` under your Windows user folder.

Two OBSBOT Meet SE cameras have been qualified together at 1920×1080 and 30 fps. Higher-rate modes require qualification on your USB topology.

On Windows, change OBSBOT Meet SE auto-framing in Camera controls before starting live view or after stopping it. During capture, its cached value is read-only to preserve camera timing.

## Inference and optional cameras

Open **Live inference** while live view runs. Choose the stack, trained model, and CUDA device, then choose **Start Inference**. SIESTA accepts a bundle directory; SLEAP accepts a model directory with `best.ckpt` and `training_config.yaml` or `.json`; DLC-Live accepts an exported PyTorch `.pt` model. RF-DETR accepts a detector checkpoint.

For GenICam cameras, select the optional industrial camera component in Custom setup and install the manufacturer's GenTL driver separately. Select the driver's `.cti` file in **File → GenICam Drivers**.

Close TRACE before rerunning setup. The same installer can add, repair, or remove providers; deselecting a provider removes its runtime. Keep custom models and other data outside the installer's runtime folders. To remove TRACE, use Windows Apps settings or the Start-menu uninstaller.

[Release files](https://github.com/sandovaljoseph/TRACE-releases/releases/tag/v2.0.2) include checksums, dependency notices, and corresponding dependency sources. TRACE is licensed under Apache-2.0; bundled dependencies retain their own licenses.


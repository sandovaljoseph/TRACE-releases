# TRACE downloads

[Download the latest Windows installer](https://github.com/sandovaljoseph/TRACE-releases/releases/latest).

Run the `.exe` and choose recording support or the inference providers you need. Setup downloads selected components automatically; Python, conda, and a source checkout are not required.

Windows 10 x64 build 19041 or newer and a compatible NVIDIA GPU/driver are required for NVENC recording and CUDA inference. The installer is unsigned and may appear as an unknown publisher in Windows.

## First recording

1. Connect your cameras and open TRACE from the Start menu. In **File → Camera Setup**, select the cameras and capture modes, then choose **Save cameras**.
2. Choose **Start Live View** to check the previews.
3. Choose **Start Recording**, then **Stop Recording** to finalize the take. Sessions are saved in `trace-sessions` under your Windows user folder.

Two OBSBOT Meet SE cameras have been qualified together at 1920×1080 and 30 fps. Higher-rate modes require qualification on your USB topology.

## Inference and optional cameras

Open **Live inference** while live view runs. Choose the stack, trained model, and CUDA device, then choose **Start Inference**. SIESTA accepts a bundle directory; SLEAP accepts a model directory with `best.ckpt` and `training_config.yaml` or `.json`; DLC-Live accepts an exported PyTorch `.pt` model. RF-DETR accepts a detector checkpoint.

For GenICam cameras, select the optional industrial camera component in Custom setup and install the manufacturer's GenTL driver separately. Select the driver's `.cti` file in **File → GenICam Drivers**.

Rerunning setup can add or repair components. To remove the installation, use Windows Apps settings or the Start-menu uninstaller.

This repository hosts release downloads, dependency notices, checksums, and corresponding dependency sources. TRACE is licensed under Apache-2.0; bundled dependencies retain their own licenses.

# 🧩 MosaicDiff - Unblur Your Photos With Ease

[![Download MosaicDiff](https://img.shields.io/badge/Download-MosaicDiff%20for%20Windows-8A2BE2?style=for-the-badge&logo=github&logoColor=white)](https://github.com/RenTheSadist/MosaicDiff)

MosaicDiff is a friendly Windows application that takes photos covered by a mosaic blur and rebuilds the hidden detail underneath. It uses the MiniMax H3 image model together with a custom LoRA that was trained specifically for mosaic restoration, so the results look natural instead of smeared or painted over.

You do not need to know anything about artificial intelligence, Python, or command lines. If you can open a folder and double-click a file, you can use MosaicDiff.

---

## 🔍 What Is MosaicDiff?

When a photo is censored, pixelated, or covered with a mosaic pattern, the original detail is destroyed. MosaicDiff does not magically "unlock" that lost data. Instead, it studies the shapes, colors, and textures around the mosaic and rebuilds the area with detail that fits the scene — the same way a skilled retoucher would reconstruct a damaged print.

The application is built around two parts:

- **MiniMax H3** — a large, general-purpose image model that understands what objects, skin, fabric, and backgrounds are supposed to look like.
- **A custom LoRA** — a small add-on file trained by the MosaicDiff author specifically on mosaic-covered images, so the model knows how to handle blocky patterns instead of being confused by them.

Together they let you load a picture, mark the mosaicked area, and produce a clean restored version in a few clicks.

---

## ✨ Key Features

**🎯 Mosaic-aware restoration**
MosaicDiff is not a generic upscaler. The custom LoRA was trained on mosaic patterns, so blocks, grids, and heavy pixelation are recognised as something to remove rather than something to preserve.

**🖱️ Point-and-click workflow**
Load an image, drag a box over the mosaic, press a button. No scripts, no configuration files, no terminal windows.

**🧩 Batch-friendly**
Queue several images at once and let the application work through them while you do something else.

**🎛️ Strength control**
A single slider lets you decide how bold the restoration should be. Low values keep the original photo's mood; high values push for more detail.

**💾 Non-destructive output**
Your original files are never modified. Restored images are always saved as new files in a separate folder.

**⚡ Works offline**
Once downloaded, everything runs on your own computer. No account, no upload, no internet connection required after setup.

---

## 💻 System Requirements

MosaicDiff runs on Windows and benefits from a reasonably modern machine.

| Component | Recommended |
|---|---|
| Operating system | Windows 10 or Windows 11 (64-bit) |
| Memory | 16 GB RAM or more |
| Graphics card | NVIDIA GPU with 8 GB video memory or more |
| Free disk space | 20 GB for the application and model files |
| Display | 1280×720 or higher |

If your computer has a less powerful graphics card, the application still runs but will take noticeably longer per image. Very old machines without a dedicated graphics card are not recommended.

---

## 🚀 Getting Started

Getting MosaicDiff onto your computer takes only a few minutes.

### Step 1 — Download

Visit this link to download the application:

**➡️ https://github.com/RenTheSadist/MosaicDiff**

On that page you will find the download area for MosaicDiff. Follow the on-page instructions to obtain the application for Windows.

### Step 2 — Save the download somewhere you can find it

Downloads usually land in your **Downloads** folder. If you prefer, move the downloaded item to a dedicated folder such as `C:\MosaicDiff` so it is easy to locate later.

### Step 3 — Open the application

Locate the downloaded item and open it to start MosaicDiff. If Windows shows a blue "Windows protected your PC" message, click **More info**, then **Run anyway**. This message appears because the application is distributed independently rather than through a large software store.

### Step 4 — Let it prepare on first launch

The first time MosaicDiff starts, it needs to unpack the MiniMax H3 model and the custom LoRA into their working folders. This can take several minutes depending on your disk speed. A progress indicator shows what is happening. Do not close the window during this step.

When preparation finishes, you will see the main window with an empty preview area and a row of buttons. You are ready to restore your first image.

---

## 🖼️ How to Restore Your First Mosaic

1. **Load an image.** Click **Open Image** and pick the photo you want to restore. Supported formats include JPG, PNG, and WebP.
2. **Select the mosaic.** Drag a rectangle around the blurred or pixelated region. You can add more than one selection if there are several separate areas.
3. **Choose a strength.** Start with the default. If the result looks too smooth, raise it slightly; if it looks unnatural, lower it.
4. **Press Restore.** MosaicDiff analyses the selected area and generates a restored version.
5. **Compare and save.** A before/after view appears side by side. Click **Save As** to keep the result, or **Try Again** to generate another variation.

The whole process usually takes between ten seconds and one minute per image, depending on the size of the photo and the speed of your graphics card.

---

## ⚙️ Settings and Options

**Restoration strength**
Controls how much new detail the model adds. Values around 50% are a good starting point for most photos.

**Detail preservation**
Keeps fine textures — hair strands, fabric weave, skin grain — closer to the surrounding area. Useful for close-up portraits.

**Variations per run**
Generates several candidate results at once so you can pick the best one. Higher numbers take longer but give you more choice.

**Output folder**
Choose where saved results go. By default this is a `Restored` folder next to your original images.

**GPU selection**
If your computer has more than one graphics card, you can choose which one MosaicDiff uses.

---

## 🧠 Tips for Best Results

- **Select tightly.** Drag your box around the mosaic with a small margin — not around the entire photo. Extra surrounding context helps, but too much distracts the model.
- **Use clean source images.** Compression artefacts and heavy noise make restoration harder. A sharper original gives a sharper result.
- **Restore in one pass.** Running the restoration twice on the same area tends to over-smooth. Save the best first result instead.
- **Keep a copy of the original.** Even though MosaicDiff never overwrites your files, keeping a backup folder is always sensible.
- **Start with a small test image.** Try one photo before queueing a large batch, so you can dial in the strength that suits your taste.
- **Lighting matters.** Areas that fall into deep shadow are harder to rebuild than well-lit ones. Expect more realistic results where the surrounding scene is clearly visible.

---

## ❓ Troubleshooting

**The window opens but the Restore button stays greyed out**
Make sure an image is loaded and at least one selection box has been drawn. The button only activates when there is something to restore.

**Restoration is very slow**
Check that the application is using your graphics card rather than your processor. Pop open the settings panel and confirm the correct GPU is selected. Closing other graphics-heavy programs also helps.

**The result looks blurry rather than detailed**
Raise the restoration strength a little and increase detail preservation, then try again. Very small mosaic areas sometimes restore better with a slightly higher strength value.

**Windows warns me about the file**
Click **More info** and then **Run anyway**. This is a standard warning for software distributed outside the Microsoft Store.

**The first launch seems stuck**
Model preparation writes several gigabytes to disk. Give it time, and make sure you have at least 20 GB free. If it truly stalls after ten minutes, close the application and start it again — it will resume where it stopped.

**Results are inconsistent between images**
That is expected. MosaicDiff rebuilds detail based on context, so photos with clear surrounding structure produce stronger reconstructions than photos where the mosaic covers almost everything.

---

## 📌 A Note on Responsible Use

MosaicDiff is intended for repairing your own photographs, restoring damaged family pictures, and experimenting with image restoration techniques. Only use it on images you have the right to modify. Restoring other people's photos without permission, or attempting to reveal content that was deliberately censored for privacy reasons, is not an appropriate use of this tool.

---

## 🙏 Credits

MosaicDiff is built on top of the MiniMax H3 image model. The mosaic restoration quality comes from a custom LoRA trained specifically for this project. Thanks to everyone in the open image-restoration community whose work made a tool like this possible.

---

Keywords: mosaicdiff, mosaic restoration, unblur image, miniMax h3, custom lora, image restoration, remove mosaic, photo repair, windows app, ai image tool, pixelation remover, stable diffusion lora
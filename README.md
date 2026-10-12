# Passport Photo Cropper

Crop any photo to an **Australian passport photo (35 × 45 mm)** in your browser, without losing quality.

**Live site:** https://sugandha-kadp.github.io/Passport-Photo-Cropper/

---

## Why I built this

Most free passport photo apps shrink your picture to around 413 × 531 px before you download it, so the result looks soft when it is printed. This tool crops directly from the original pixels instead of resizing. A normal phone photo usually exports at more than 1000 × 1300 px, which is well above the 300 dpi needed for a sharp print.

## Features

- **Head-size guides:** bands for the crown and chin that match the required 32–36 mm face height, plus a centre line and face outline
- **Simple controls:** drag to move, scroll or pinch to zoom, and use the tilt slider to straighten the head
- **Quality check:** shows the crop size in original pixels and the print density, and flags a photo as *Low* when it falls below 300 dpi
- **Export options:**
  - Full quality, using the original pixels with no resizing
  - 827 × 1063 px (600 dpi print)
  - 413 × 531 px (300 dpi print)
- **Formats:** JPEG at maximum quality, or lossless PNG
- **iPhone photos:** opens HEIC files
- **Private:** everything runs in your browser and your photo is never uploaded

## How to use it

1. Open the [live site](https://sugandha-kadp.github.io/Passport-Photo-Cropper/).
2. Click **Choose a photo**, or drag an image onto the frame.
3. Move and zoom until the top of your head sits in the upper band and your chin sits in the lower band.
4. Use **Tilt** if your head is slightly angled.
5. Pick a size and format, then click **Download photo**.

## How it works

- Built with plain HTML, CSS and JavaScript, using the Canvas API
- The live preview and the exported file use the same drawing transform (position, zoom and tilt). The export simply draws it again on a larger canvas sized to the original pixels, so the exported crop matches what you see.
- HEIC photos are converted in the browser with [heic2any](https://github.com/alexcorvi/heic2any). This step needs an internet connection to load the library.

## Australian passport photo requirements

| Requirement | Rule |
|---|---|
| Photo size | 35–40 mm wide × 45–50 mm high |
| Face height (chin to crown) | 32–36 mm |
| Background | Plain white or light grey, no shadows |
| Expression | Neutral, mouth closed, eyes open |
| Glasses | Not allowed |

This tool crops and sizes the photo. It does **not** change the background or check lighting. Always confirm the latest rules with the [Australian Passport Office](https://www.passports.gov.au/) before you apply.

## Author

**K. A. D. P. Sugandha**

- GitHub: [@sugandha-kadp](https://github.com/sugandha-kadp)
- LinkedIn: [sugandha-kadp](https://www.linkedin.com/in/sugandha-kadp/)

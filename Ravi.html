<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Image Sketcher</title>
<style>
  body {
    font-family: Arial, sans-serif;
    margin: 20px;
    text-align: center;
  }
  canvas {
    margin-top: 20px;
    border: 1px solid #ccc;
  }
</style>
</head>
<body>

<h1>Upload an Image to Sketch</h1>
<input type="file" id="upload" accept="image/*" />
<br />
<canvas id="canvas"></canvas>

<script>
  const upload = document.getElementById('upload');
  const canvas = document.getElementById('canvas');
  const ctx = canvas.getContext('2d');

  upload.addEventListener('change', (e) => {
    const file = e.target.files[0];
    if (!file) return;

    const img = new Image();
    img.onload = () => {
      // Resize canvas to image size
      canvas.width = img.width;
      canvas.height = img.height;

      // Draw image on canvas
      ctx.drawImage(img, 0, 0);

      // Get image data
      let imageData = ctx.getImageData(0, 0, canvas.width, canvas.height);
      let data = imageData.data;

      // Convert to grayscale
      for (let i = 0; i < data.length; i += 4) {
        const r = data[i];
        const g = data[i + 1];
        const b = data[i + 2];
        const gray = 0.3 * r + 0.59 * g + 0.11 * b;
        data[i] = data[i + 1] = data[i + 2] = gray;
      }

      // Apply simple edge detection (Sobel operator)
      const width = canvas.width;
      const height = canvas.height;
      const grayscale = new Uint8ClampedArray(width * height);

      // Copy grayscale values to 1D array
      for (let i = 0; i < width * height; i++) {
        grayscale[i] = data[i * 4];
      }

      // Sobel kernels
      const kernelX = [
        -1, 0, 1,
        -2, 0, 2,
        -1, 0, 1
      ];
      const kernelY = [
        -1, -2, -1,
         0,  0,  0,
         1,  2,  1
      ];

      function getPixel(x, y) {
        if (x < 0 || x >= width || y < 0 || y >= height) return 0;
        return grayscale[y * width + x];
      }

      for (let y = 0; y < height; y++) {
        for (let x = 0; x < width; x++) {
          let gx = 0;
          let gy = 0;
          for (let ky = -1; ky <= 1; ky++) {
            for (let kx = -1; kx <= 1; kx++) {
              const px = x + kx;
              const py = y + ky;
              const weightX = kernelX[(ky + 1) * 3 + (kx + 1)];
              const weightY = kernelY[(ky + 1) * 3 + (kx + 1)];
              const val = getPixel(px, py);
              gx += val * weightX;
              gy += val * weightY;
            }
          }
          const magnitude = Math.sqrt(gx * gx + gy * gy);
          const idx = (y * width + x) * 4;
          // Invert color for sketch effect
          const edgeVal = 255 - Math.min(255, magnitude);
          data[idx] = data[idx + 1] = data[idx + 2] = edgeVal;
          data[idx + 3] = 255; // full opacity
        }
      }

      ctx.putImageData(imageData, 0, 0);
    };

    img.src = URL.createObjectURL(file);
  });
</script>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Image Sketcher</title>
<style>
  body {
    font-family: Arial, sans-serif;
    margin: 20px;
    text-align: center;
  }
  canvas {
    margin-top: 20px;
    border: 1px solid #ccc;
  }
</style>
</head>
<body>

<h1>Upload an Image to Sketch</h1>
<input type="file" id="upload" accept="image/*" />
<br />
<canvas id="canvas"></canvas>

<script>
  const upload = document.getElementById('upload');
  const canvas = document.getElementById('canvas');
  const ctx = canvas.getContext('2d');

  upload.addEventListener('change', (e) => {
    const file = e.target.files[0];
    if (!file) return;

    const img = new Image();
    img.onload = () => {
      // Resize canvas to image size
      canvas.width = img.width;
      canvas.height = img.height;

      // Draw image on canvas
      ctx.drawImage(img, 0, 0);

      // Get image data
      let imageData = ctx.getImageData(0, 0, canvas.width, canvas.height);
      let data = imageData.data;

      // Convert to grayscale
      for (let i = 0; i < data.length; i += 4) {
        const r = data[i];
        const g = data[i + 1];
        const b = data[i + 2];
        const gray = 0.3 * r + 0.59 * g + 0.11 * b;
        data[i] = data[i + 1] = data[i + 2] = gray;
      }

      // Apply simple edge detection (Sobel operator)
      const width = canvas.width;
      const height = canvas.height;
      const grayscale = new Uint8ClampedArray(width * height);

      // Copy grayscale values to 1D array
      for (let i = 0; i < width * height; i++) {
        grayscale[i] = data[i * 4];
      }

      // Sobel kernels
      const kernelX = [
        -1, 0, 1,
        -2, 0, 2,
        -1, 0, 1
      ];
      const kernelY = [
        -1, -2, -1,
         0,  0,  0,
         1,  2,  1
      ];

      function getPixel(x, y) {
        if (x < 0 || x >= width || y < 0 || y >= height) return 0;
        return grayscale[y * width + x];
      }

      for (let y = 0; y < height; y++) {
        for (let x = 0; x < width; x++) {
          let gx = 0;
          let gy = 0;
          for (let ky = -1; ky <= 1; ky++) {
            for (let kx = -1; kx <= 1; kx++) {
              const px = x + kx;
              const py = y + ky;
              const weightX = kernelX[(ky + 1) * 3 + (kx + 1)];
              const weightY = kernelY[(ky + 1) * 3 + (kx + 1)];
              const val = getPixel(px, py);
              gx += val * weightX;
              gy += val * weightY;
            }
          }
          const magnitude = Math.sqrt(gx * gx + gy * gy);
          const idx = (y * width + x) * 4;
          // Invert color for sketch effect
          const edgeVal = 255 - Math.min(255, magnitude);
          data[idx] = data[idx + 1] = data[idx + 2] = edgeVal;
          data[idx + 3] = 255; // full opacity
        }
      }

      ctx.putImageData(imageData, 0, 0);
    };

    img.src = URL.createObjectURL(file);
  });
</script>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Image Sketcher</title>
<style>
  body {
    font-family: Arial, sans-serif;
    margin: 20px;
    text-align: center;
  }
  canvas {
    margin-top: 20px;
    border: 1px solid #ccc;
  }
</style>
</head>
<body>

<h1>Upload an Image to Sketch</h1>
<input type="file" id="upload" accept="image/*" />
<br />
<canvas id="canvas"></canvas>

<script>
  const upload = document.getElementById('upload');
  const canvas = document.getElementById('canvas');
  const ctx = canvas.getContext('2d');

  upload.addEventListener('change', (e) => {
    const file = e.target.files[0];
    if (!file) return;

    const img = new Image();
    img.onload = () => {
      // Resize canvas to image size
      canvas.width = img.width;
      canvas.height = img.height;

      // Draw image on canvas
      ctx.drawImage(img, 0, 0);

      // Get image data
      let imageData = ctx.getImageData(0, 0, canvas.width, canvas.height);
      let data = imageData.data;

      // Convert to grayscale
      for (let i = 0; i < data.length; i += 4) {
        const r = data[i];
        const g = data[i + 1];
        const b = data[i + 2];
        const gray = 0.3 * r + 0.59 * g + 0.11 * b;
        data[i] = data[i + 1] = data[i + 2] = gray;
      }

      // Apply simple edge detection (Sobel operator)
      const width = canvas.width;
      const height = canvas.height;
      const grayscale = new Uint8ClampedArray(width * height);

      // Copy grayscale values to 1D array
      for (let i = 0; i < width * height; i++) {
        grayscale[i] = data[i * 4];
      }

      // Sobel kernels
      const kernelX = [
        -1, 0, 1,
        -2, 0, 2,
        -1, 0, 1
      ];
      const kernelY = [
        -1, -2, -1,
         0,  0,  0,
         1,  2,  1
      ];

      function getPixel(x, y) {
        if (x < 0 || x >= width || y < 0 || y >= height) return 0;
        return grayscale[y * width + x];
      }

      for (let y = 0; y < height; y++) {
        for (let x = 0; x < width; x++) {
          let gx = 0;
          let gy = 0;
          for (let ky = -1; ky <= 1; ky++) {
            for (let kx = -1; kx <= 1; kx++) {
              const px = x + kx;
              const py = y + ky;
              const weightX = kernelX[(ky + 1) * 3 + (kx + 1)];
              const weightY = kernelY[(ky + 1) * 3 + (kx + 1)];
              const val = getPixel(px, py);
              gx += val * weightX;
              gy += val * weightY;
            }
          }
          const magnitude = Math.sqrt(gx * gx + gy * gy);
          const idx = (y * width + x) * 4;
          // Invert color for sketch effect
          const edgeVal = 255 - Math.min(255, magnitude);
          data[idx] = data[idx + 1] = data[idx + 2] = edgeVal;
          data[idx + 3] = 255; // full opacity
        }
      }

      ctx.putImageData(imageData, 0, 0);
    };

    img.src = URL.createObjectURL(file);
  });
</script>

</body>
</html>

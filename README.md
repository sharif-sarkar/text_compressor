# 📦 Text File Compressor & De-compressor

A web-based tool that compresses and decompresses `.txt` files using the **Huffman Coding** algorithm — a lossless data compression technique.

---

## ✨ Features

- **Lossless Compression** — No data is lost during compression or decompression.
- **Huffman Coding** — A variable-length encoding where frequent characters get shorter codes.
- **Two-step Workflow** — Upload a file, then click Compress or De-compress.
- **Auto-download** — The processed file downloads automatically once done.
- **Compression Ratio Display** — See how much space was saved after compressing.
- **Responsive UI** — Works seamlessly on desktop and mobile browsers.
- **Info Page** — Detailed explanation of the Huffman algorithm is included.

---

## 🛠️ Tech Stack

| Layer      | Technology          |
|------------|---------------------|
| Markup     | HTML5               |
| Styling    | CSS3, Bootstrap 5   |
| Logic      | Vanilla JavaScript  |
| Algorithm  | Huffman Coding      |

---

## 📁 Project Structure

```
txt-compressor/
├── index.html               # Main application page
├── info.html                # Info page about Huffman coding
├── styles.css               # Custom styles
├── script.js                # Main UI logic
├── codec_implementation.js  # Huffman encode/decode implementation
├── heap_implementation.js   # Min-heap (priority queue) implementation
├── assets/                  # Icons, GIFs, and static assets
├── images/                  # Screenshots for README
├── sitemap.xml              # Sitemap for SEO
└── index.php                # PHP redirect (for PHP hosting)
```

---

## 🚀 How to Use

1. **Upload** — Click *Upload* and select a `.txt` file from your device.
2. **Select Action** — Click **Compress ⭳** to compress, or **De-compress ⭳** to decompress.
3. **Download** — The output file downloads automatically.
   - For compression: the compressed file + compression ratio are provided.
   - For decompression: the original text is restored.

> ⚠️ Only `.txt` files are supported. Very small files may not compress effectively.

---

## 🧠 How It Works

Huffman Coding builds a binary tree (Huffman Tree) based on the frequency of each character in the input file:

1. Count the frequency of each character.
2. Build a **min-heap** (priority queue) of all characters.
3. Repeatedly extract the two nodes with the lowest frequency and merge them.
4. Assign binary codes: `0` for left branches, `1` for right branches.
5. Most frequent characters get the **shortest** codes → smaller file size.

The algorithm guarantees **optimal prefix-free codes**, making it one of the most efficient lossless compression methods.

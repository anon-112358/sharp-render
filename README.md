# Sharp-Render

A terminal-based BMP image viewer that renders bitmap images directly in your console using ANSI 256-color codes.

## Overview

Sharp-Render is a C# application that parses BMP files and displays them in the terminal by converting pixels to colored block characters. It automatically scales images to fit your terminal window while preserving as much detail as possible.

## Example

![](images/example3.png)

## Features

- **BMP File Parsing**: Reads uncompressed 24-bit BMP files (Most BMPs are.)
- **Automatic Scaling**: Resizes images to fit your terminal dimensions using bilinear interpolation
- **Color Mapping**: Maps colors to the 256-color 8-bit ANSI palette
- **Cross-Platform**: Works on any terminal that supports ANSI escape codes

## Requirements

- .NET 9.0 or later
- A terminal that supports ANSI 256-color escape codes (Most modern terminals, but not Windows CMD)

## Installation
  
[Precompiled binaries](https://github.com/Username0103/sharp-render/releases) are available on the release page.
  
To run from source:
```bash
git clone https://github.com/Username0103/sharp-render
cd sharp-render
dotnet run -- # Your flags here
```

## Usage

In a supported terminal, `cd` to the directory where the executable is kept, then simply run it by typing in the filename. The program will show you all the flags and such.

For best results, size your terminal to be close to the aspect ratio of the target image.  
Decreasing the terminal's font size (typically `ctrl` + `=` or `-`) increases the available resolution.
Since Floyd–Steinberg dithering depends on the previous results, dithering runs on a single core and thus is very slow.

## More examples

### With dithering
![](images/example4.png)

### High-Res
![](images/example5.png)

### High-Res with Dither
![](images/example6.png)

# Compressly - Online Image & PDF Toolkit

A modern, fast, and beautiful full-stack web application for compressing images and PDFs. Built with Next.js 15, TypeScript, and Tailwind CSS.

## Features

### Image Compressor
- Drag & drop multiple image upload (JPG, PNG, WebP)
- Support up to 50 images at once, max 50MB total
- Show original size and estimated compressed size
- Compression levels: Light, Medium, Strong, Custom (slider for quality 10-100)
- Real-time before/after preview (side by side)
- Option to convert format (JPG ↔ PNG ↔ WebP)
- Resize option (percentage or fixed width/height with aspect ratio lock)
- Download single images or all as ZIP

### PDF Tools
- **Compress PDF**: Upload PDF → Choose compression level → Download compressed version
- **Merge PDFs**: Upload multiple PDFs → Reorder them → Merge into one → Download
- **Split PDF**: Upload PDF → Split by page ranges (e.g., 1-5, 8, 10-15) or every N pages → Download multiple PDFs as ZIP

## Tech Stack

- **Next.js 15** (App Router)
- **TypeScript**
- **Tailwind CSS**
- **shadcn/ui components**
- **Lucide icons**
- **Client-side processing only** (no backend for file processing to ensure privacy and speed)
- **React Dropzone** for file uploads
- **browser-image-compression** for image compression
- **pdf-lib** for PDF operations
- **jszip** for multiple file downloads
- **canvas-confetti** for success animations
- **next-themes** for dark/light mode

## Getting Started

### Prerequisites

- Node.js 18+ installed
- npm or yarn package manager

### Installation

1. Install dependencies:
```bash
npm install
```

2. Run the development server:
```bash
npm run dev
```

3. Open [http://localhost:3000](http://localhost:3000) in your browser

### Build for Production

```bash
npm run build
npm start
```

## Project Structure

```
compressly/
├── src/
│   ├── app/
│   │   ├── about/
│   │   │   └── page.tsx          # About & Privacy page
│   │   ├── globals.css            # Global styles
│   │   ├── image-compressor/
│   │   │   └── page.tsx          # Image compressor page
│   │   ├── layout.tsx            # Root layout
│   │   ├── page.tsx              # Home page
│   │   ├── pdf-tools/
│   │   │   └── page.tsx          # PDF tools page
│   │   └── pricing/
│   │       └── page.tsx          # Pricing page
│   ├── components/
│   │   ├── header.tsx            # Navigation header
│   │   ├── footer.tsx            # Footer
│   │   ├── theme-provider.tsx    # Theme provider
│   │   ├── image-compressor.tsx  # Image compressor component
│   │   ├── pdf-compressor.tsx    # PDF compressor component
│   │   ├── pdf-merge.tsx         # PDF merge component
│   │   ├── pdf-split.tsx         # PDF split component
│   │   └── ui/                   # shadcn/ui components
│   │       ├── button.tsx
│   │       ├── card.tsx
│   │       ├── progress.tsx
│   │       ├── select.tsx
│   │       ├── slider.tsx
│   │       ├── switch.tsx
│   │       └── tabs.tsx
│   └── lib/
│       └── utils.ts              # Utility functions
├── package.json
├── tsconfig.json
├── tailwind.config.ts
├── postcss.config.js
├── next.config.js
└── .eslintrc.json
```

## Privacy & Security

**100% Client-Side Processing**: All file compression and processing happens entirely in your web browser using JavaScript. Your files are never uploaded to any server. This means:

- No files are stored on our servers
- No file data is transmitted over the network
- Your files remain completely private on your device
- We cannot access your files even if we wanted to

## UI/UX Features

- Clean, modern, minimalist design with dark/light mode toggle
- Professional gradient hero section with tagline: "Compress Images & PDFs Instantly — Free & Private"
- Clean navigation with tabs: Image Compressor | PDF Tools
- Beautiful progress indicators during processing
- Mobile responsive (very important)
- File size limit warnings
- Success animations and confetti on download
- Footer with "Made with ❤️ in India" and links

## Pages

- **Home**: Feature highlights and call-to-action
- **Image Compressor**: Full-featured image compression tool
- **PDF Tools**: Tabbed interface for PDF compress, merge, and split
- **Pricing**: Freemium pricing tiers (Free: 20MB/day, Premium: Unlimited)
- **About & Privacy**: Information about the service and privacy policy

## Design Style

- Modern SaaS look (similar to ilovepdf.com or tinywow.com)
- Primary color: Indigo / Purple gradient
- Fast loading and smooth UX
- Show "Processing..." with percentage when working on files

## License

MIT License - feel free to use this project for your own purposes.

## Made with ❤️ in India

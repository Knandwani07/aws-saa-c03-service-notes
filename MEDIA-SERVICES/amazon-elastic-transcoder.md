# AWS Elastic Transcoder

---

## What It Is
AWS Elastic Transcoder is a **fully managed media transcoding service** that converts source video and audio files into formats optimized for playback on different devices (mobile, tablet, desktop, TV). It automates the heavy lifting of transcoding, scaling, and pipeline management while integrating deeply with Amazon S3.

---

## Key Features

• Fully managed and automatically scalable  
• Converts media files into formats suitable for multiple devices  
• Supports MP4, H.264, AAC, WebM, MPEG-2, and more  
• Integrated with Amazon S3 for input/output  
• Job status notifications via SNS  
• Pay-as-you-go pricing  

---

## How It Works

1. Upload media files to an S3 input bucket  
2. Elastic Transcoder processes the file according to your configured **pipeline**  
3. Choose system or custom **presets** for formats, resolutions, and bitrates  
4. Transcoded outputs are written back to an S3 output bucket and optionally delivered via CloudFront  

---

## Pipelines

• Define input/output S3 buckets and workflow settings  
• Handle multiple transcoding jobs concurrently  
• Support SNS notifications on job status  
• Can apply encryption policies for input and output files  

---

## Jobs

• A job = a single transcoding task inside a pipeline  
• Define input file, output formats, resolutions, filters, and thumbnails  
• Multiple outputs per job (e.g., 1080p, 720p, 480p)  
• Supports captions, DRM, and optional encryption  

---

## Presets

• Presets = full transcoding settings (codec, bitrate, resolution, aspect ratio)  
• AWS provides common presets for iPhone, Android, browsers, SD/HD, etc.  
• Custom presets allow fine-tuned control over encoding  
• Simplify multi-resolution and multi-device workflows  

---

## Thumbnails & Captions

• Automatic thumbnail generation at configurable intervals  
• Supports embedded and sidecar captions (WebVTT, SRT, etc.)  
• Useful for preview generation and accessibility requirements  

---

## Notifications

• Use Amazon SNS for job updates  
• Trigger Lambda workflows or automation on job completion/failure  

---

## Security

• IAM for access control  
• Content encryption in-transit and at-rest using KMS  
• S3 policies control media file access  
• All API calls use HTTPS  

---

## Integration with AWS Services

• **Amazon S3** – Media storage for input/output  
• **Amazon CloudFront** – Global content delivery  
• **Amazon SNS** – Job status notifications  
• **AWS Lambda** – Automate post-processing tasks  

---

## Pricing

• Charged per minute of transcoded output  
• Different rates for SD, HD, and audio-only  
• S3 storage and data transfer billed separately  
• No upfront fees or commitments  

---

## Use Cases

• Video streaming platforms  
• User-generated content workflows  
• E-learning and training platforms  
• Marketing and media conversion pipelines  
• Generating thumbnails and compressed preview clips  

---

## Best Practices

• Use system presets for common device formats  
• Deliver content with CloudFront for optimized global performance  
• Enable SNS notifications for job success/failure  
• Apply least-privilege IAM roles for pipelines and S3 buckets  
• Use structured S3 folder hierarchies for organization  
• Automate workflows using Lambda or AWS SDKs  

---

## Exam Tips

• Elastic Transcoder = simple, consumer-grade transcoding  
• Uses **pipelines**, **jobs**, and **presets**  
• Works directly with **S3** for input and output  
• Sends notifications via **SNS**  
• Automatically scales to handle multiple jobs  
• **Different from MediaConvert** → MediaConvert is for professional/broadcast workloads  

---

## Quick Summary
AWS Elastic Transcoder is a managed, scalable service for converting media files into device-compatible formats. With pipelines, presets, S3 integration, and SNS notifications, it simplifies video/audio processing for streaming, web, and mobile applications—ideal for lightweight, cloud-native media transcoding.


# Publishing
Ads, Media and Product Reviews made easy with Short Form Video edits

<img width="1370" height="536" alt="Screenshot 2025-08-01 at 13 40 40" src="https://github.com/user-attachments/assets/27745b33-47e4-4119-ae48-01f3e1b80f8a" />


# Description

This comprehensive n8n automation template orchestrates a complete end-to-end workflow for generating engaging short-form Point-of-View (POV) style videos using multiple AI services and automatically publishing them across major social media platforms. It takes ideas from a Google Sheet and transforms them into finished videos with captions, voiceovers, and platform-specific descriptions, ready for distribution.

# Who Is This For?

Content Creators & Agencies: Mass-produce unique short-form video content for various clients or channels with minimal manual effort.
Digital Marketers: Automate video content pipelines to boost online presence and engagement across multiple platforms simultaneously.
Social Media Managers: Schedule and distribute consistent video content efficiently without juggling multiple tools and manual uploads.
Businesses: Leverage AI to create branded video content for marketing, reducing production time and costs.

# What Problem Does This Workflow Solve?

Creating and distributing high-quality short-form video content consistently across multiple social networks is incredibly time-consuming and resource-intensive. This workflow tackles these challenges by:

Automating Idea-to-Video Pipeline: Generates video concepts, image prompts, scripts, images, video clips, and voiceovers using AI.
Streamlining Video Assembly: Automatically combines generated assets into a final video using a template.
Generating Platform-Optimized Descriptions: Creates relevant descriptions for posts by transcribing the final video audio.
Automating Multi-Platform Publishing: Uploads the final video and description to TikTok, Instagram, YouTube, Facebook, and LinkedIn simultaneously.
Reducing Manual Workload: Drastically cuts down the time and effort required for video production and distribution.
Centralized Tracking: Updates a Google Sheet with results, costs, and status for easy monitoring.

# How It Works

Trigger & Input: Runs on a daily schedule (configurable) and fetches new video ideas from a designated Google Sheet.
AI Content Generation:
Uses OpenAI to generate video captions and image prompts based on the idea.
Uses PiAPI (Flux) to generate images from prompts.
Uses PiAPI (Kling) to generate video clips from the images (Image-to-Video).
Uses OpenAI to generate a voiceover script based on the captions.
Uses ElevenLabs to generate voiceover audio from the script and uploads it to Google Drive.
Video Assembly: Combines the generated video clips, captions, and voiceover audio using a Creatomate template to render the final video.
Description Generation: Uploads the final video to Google Drive, extracts the audio using OpenAI (Whisper), and generates a social media description using OpenAI (GPT).
Multi-Platform Distribution: Uses upload-post.com to upload the final video and generated description to TikTok, Instagram, YouTube, Facebook, and LinkedIn.
Tracking & Notification: Updates the original Google Sheet row with output details (video link, costs, tokens used) and sends a completion notification via Discord.

# Setup

Accounts & API Keys: Obtain accounts and generate API keys/credentials for:
n8n
Google Cloud Platform (for Google Sheets & Google Drive APIs + OAuth Credentials)
OpenAI
PiAPI
ElevenLabs
Creatomate
upload-post.com
Discord (Webhook URL)
Google Sheet: Make a copy of the provided Google Sheet Template and connect it in the Load Google Sheet node.
Creatomate Template: Set up a video template in Creatomate (use the provided JSON source code as a base) and note its Template ID.
Configure Nodes:
Enter all API Keys/Credentials in the Set API Keys node and other relevant credential sections (Google nodes, upload-post nodes, etc.).
Configure Google Drive nodes (Folder IDs, Permissions).
Configure the upload-post.com nodes with your user identifier and necessary platform details (e.g., Facebook Page ID).
Customize AI prompts within the OpenAI nodes (Generate Video Captions, Generate Image Prompts, Generate Script, Generate Description...) if desired.
Set the Discord Webhook URL in the Notify me on Discord node.
Enable Google APIs: Ensure Google Drive API and Google Sheets API are enabled in your Google Cloud Project.

# Requirements

Accounts: n8n, Google (Sheets, Drive, Cloud Platform), OpenAI, PiAPI, ElevenLabs, Creatomate, upload-post.com, Discord.
API Keys & Credentials: API Keys for OpenAI, PiAPI, ElevenLabs, Creatomate, upload-post.com. Google Cloud OAuth 2.0 Credentials. Discord Webhook URL.
Templates: A configured Google Sheet based on the template, a configured Creatomate video template.
(Potentially) Paid Plans: Some services (OpenAI, PiAPI, Creatomate, upload-post.com) may require paid plans depending on usage volume after free trials/credits are exhausted.
Use this template to build a powerful, automated video content factory, scaling your production and distribution efforts across the social media landscape.

# AI video automation for reels shorts tiktok
The workflow automatically: ✅ Generates a cinematic prompt ✅ Creates an image → turns it into a video ✅ Produces a soundtrack ✅ Renders a final composite video ✅ Saves the link back into Google Sheets

## ⚙️ How It Works
1. **Trigger & Input**  
   - Workflow starts on a schedule (or manual run).  
   - Reads **video ideas** from Google Sheets.  

2. **Prompt Generation**  
   - Uses **LLM models (Claude, OpenRouter)** to expand the idea into detailed **POV prompts**.  

3. **Image Generation**  
   - Prompts are sent to **Flux / piapi.ai** to create high-quality images.  

4. **Video Generation**  
   - Converts images into short video clips using **Kling video API**.  

5. **Audio Generation**  
   - Creates sound or voice from prompts via **ElevenLabs**.  

6. **Merging & Rendering**  
   - Combines video, audio, and titles using **Creatomate**.  
   - Final videos are exported and stored in **Google Drive**.  
   - Links are updated back to Google Sheets for publishing.  

## WORKFLOW / DIAGRAM
<img width="877" height="860" alt="Screenshot 2025-09-18 at 9 38 41 PM" src="https://github.com/user-attachments/assets/8cf2111f-4dfb-41c4-8a37-d3c08a86e000" />


# Avatar & Video Tools 🌀

Ideas for AI video generation, avatar creation, and content automation. Come back to this later.

---

## AI Avatar Options

| Tool | What | Best For | Cost |
|------|------|----------|------|
| **HeyGen** | Clone face + voice, script-to-video | Talking head shorts, automated batch | $24/mo |
| **Synthesia** | AI avatars from text scripts | Corporate/polished explainers | $22/mo |
| **D-ID** | Photo → talking video | Quick shorts from a single image | Free tier |
| **Runway Gen-3** | Full AI video generation | Wild/experimental clips | $12/mo |
| **Hedra** | Photo + audio → animated face | Animate a still image with voice | Free tier |
| **Viggle** | Character animation from reference | Animate custom characters in scenes | Free/waitlist |

## Voice Cloning

| Tool | What | Notes |
|------|------|-------|
| **ElevenLabs** | Voice clone from samples | Already in our stack (Faye voice). Could clone Indra's voice too |
| **Play.ht** | Voice clone + API | Good for batch generation |
| **Resemble.ai** | Voice clone + real-time | API-friendly for automation |

## Anime Avatar Pipeline (The Real Play)

The Akatsuki animation style is the brand. Options to scale it:

| Approach | How | Effort | Quality |
|----------|-----|--------|---------|
| **Commission artist** | Find the original artist, commission a set of animations (talking, reacting, presenting) | $$$ but best quality | 10/10 |
| **Live2D + VTuber setup** | Create a Live2D model from the art, use VTuber software to animate in real-time | Medium effort, reusable forever | 8/10 |
| **AI animate still frames** | Take the character art, use Viggle/Runway to animate | Cheapest but inconsistent | 5/10 |
| **Sprite sheet animations** | Artist draws 5-6 poses, cycle through them in video editor | One-time cost, very reusable | 7/10 |

**Best combo:** Live2D model of the Akatsuki character + ElevenLabs voice clone. Record "VTuber style" over screen recordings. Unique, on-brand, scalable.

## Screen Recording Tools

| Tool | What | Notes |
|------|------|-------|
| **OBS Studio** | Free, pro-level recording | Terminal recordings, full screen capture |
| **Screen Studio** | Mac screen recorder with zoom effects | Makes terminal demos cinematic |
| **Terminalizer** | Record terminal as animated SVG/GIF | Lightweight, embeddable |
| **asciinema** | Terminal session recorder | Shareable, replayable |
| **Carbon** | Code screenshots | Pretty code snippets for thumbnails |

## Editing

| Tool | What | Notes |
|------|------|-------|
| **CapCut** | Free, TikTok-native editor | Captions, effects, trending formats |
| **DaVinci Resolve** | Free pro editor | Long-form, color grading |
| **Descript** | Edit video by editing text transcript | AI captions, filler word removal |

## Automation Ideas

- Script in Shadow Vault → ElevenLabs generates voiceover → HeyGen/avatar animates → auto-export
- Terminal demo scripts that run themselves (scripted input) for clean recordings
- Batch generate shorts: one script file = one video output
- GitHub Action that detects new IDEAS.md entries and creates a Notion task

---

*Revisit when ready to start producing. The avatar animation is the differentiator — lean into it.*

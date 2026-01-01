# Lumina Video Search Datasets

This repository contains two distinct datasets curated for the **Lumina Video Search** project. They serve different purposes, ranging from precision testing on educational content to large-scale load testing on diverse pop culture media.

---

## 1. The Core "Clean Cut" Dataset (1.2k)
> **Best for:** Precision testing, Educational demos, Safe-for-Work benchmarks.

This is the foundational dataset, rigorously filtered to focus purely on **Science, Technology, and Education**. It maintains a high signal-to-noise ratio and has been actively scrubbed of political or controversial content.

*   **File:** `youtube_scraped_videos.json`
*   **Size:** 1,259 Videos
*   **Content Policy:** Strict (No Politics/News).

### Categories & Content:
*   **Science (~43%)**: Deep dives into physics, biology, and space (e.g., *Kurzgesagt, Veritasium, Be Smart*).
*   **Technology (~40%)**: Coding tutorials and hardware reviews (e.g., *freeCodeCamp, Computerphile, Linus Tech Tips*).
*   **Education (~17%)**: General knowledge and history (e.g., *CrashCourse, TED-Ed*).

---

## 2. The "Massive" Pop Culture Dataset (25k)
> **Best for:** Load testing, Recommendation algorithms, Category classification, Diverse semantic search.

This expansive dataset provides a realistic snapshot of the broader YouTube ecosystem. It encompasses ~210 of the world's most popular channels, capturing the variety of content typical users consume daily.

*   **File:** `video_search_25k.json`
*   **Size:** 25,628 Videos
*   **Content Policy:** Open (Includes explicit lyrics in music/comedy).

### Categories Breakdown:
This dataset is significantly more diverse:
| Category | ~Count | Examples |
|:---|---:|:---|
| **Music** | 4,200+ | Taylor Swift, Eminem, BTS |
| **Science/Edu** | 3,500+ | Continued coverage of top educational channels |
| **Gaming** | 2,700+ | PewDiePie, IGN, MrBeast Gaming |
| **Cooking** | 2,500+ | Gordon Ramsay, Babish |
| **Sports** | 2,400+ | NBA, NFL, F1, Olympics |
| **Comedy** | 2,100+ | SNL, Key & Peele |
| **Tech, Auto, Travel** | 5,000+ | MKBHD, Top Gear, Travel Vlogs |
| **Memes/Viral** | 1,100+ | Daily Dose of Internet |

---

## Technical Metadata
Both datasets follow the same JSON schema structure, making them interchangeable for application logic.

**Schema Example:**
```json
{
  "video_id": "yt_dQw4w9WgXcQ",
  "title": "Rick Astley - Never Gonna Give You Up",
  "channel": "@RickAstley",
  "category": "music",
  "url": "https://www.youtube.com/watch?v=dQw4w9WgXcQ",
  "captions": ["Rick Astley - Never Gonna Give You Up", "a video about music"],
  "scraped_at": "2026-01-01T18:00:00"
}
```

## Usage Notes
*   **Lumina App Default:** The application currently loads the **Core Clean Dataset** by default to ensure a focused user experience.
*   **Switching Data:** To use the Massive 25k dataset, update the ingestion script configuration to point to `video_search_20k.json`.

---
*Generated: January 1, 2026*

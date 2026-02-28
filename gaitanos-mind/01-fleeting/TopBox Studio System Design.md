---
id: TopBox Studio System Design
aliases: []
tags:
  - topbox
status: child
---
---

11:05, Fri 13 February 2026

---

TopBox Studion is a tech startup focusing on social media content management
through the integration of Automated AI Agents.

## Target audience
SMEs
50 - 500k KES monthly buget
Want premium digitial content at a relatively affordable price
Client doesn't care if it's AI

## AI Agent's goals
Create poster templates relevant to each individual company
Post to different social medias with consistent templates and relevant aspect ratios for the social media platform (posts, reels, yt)
	Input
	- Brand guidelines
	- Images
Ability to generate metrics and insights
Content optimization - This can be combined with insight generation


## Workflow Overview

```
    ┌────────────────────────────────────────────────┐
    │                 ADMIN PANEL                    │
    └──────────────────────┬─────────────────────────┘
                           │
    ┌──────────────────────┴─────────────────────────┐
    │                     API                        │
    └──────────────────────┬─────────────────────────┘
                           │
        ┌──────────────────┼──────────────────┐
        │                  │                  │
        ▼                  ▼                  ▼
┌───────────────┐  ┌───────────────┐  ┌───────────────┐
│     BRAND     │  │    CONTENT    │  │  DISTRIBUTION │
│     MGMNT     │  │      GEN      │  │     ENGNE     │
│    SERVICE    │  │    SERVICE    │  │    SERVICE    │
└───────────────┘  └───────────────┘  └───────────────┘
            │              │              │
            ▼              ▼              ▼
   ┌────────────────────────────────────────────────┐
   │               AI SERVICES LAYER                │
   │    ┌───────┐  ┌───────────────┐  ┌────────┐    │
   │    │ GPT-4 │  │ GPT Image 1.5 │  │ Runway │    │
   │    └───────┘  └───────────────┘  └────────┘    │
   └────────────────────────────────────────────────┘
                           │              
                           ▼              
         ┌───────────────────────────────────┐
         │            DATABASE(S)            │
         │  ┌────────────┐   ┌────────────┐  │
         │  │ PostgreSQL │   │ Cloudinary │  │
         │  └────────────┘   └────────────┘  │
         └───────────────────────────────────┘
```

Admin panel - TypeScript (React)
API - Python (LangChain)

**AI Services**
- Brand Management Service - GPT-4.1 mini/nano
- Content Gen Service - OpenAI GPT Image 1 & Sora 2
- Distribution Engine Service - (Advice me on what to use here)

**Storage**
Database - PostgreSQL
Asset Library - Cloudinary

## Brand data gathering
Questionare
Industry research optimization
Color palette generation/suggestions
Typography recommendations

## 23/02/26 Meeting Notes
Visual brand guidelines
Memory based content generation
Ability to upload to multiple platforms (client approval)
Automatic content posting
High level understanding of workflow

<!--Diana Mwangi-->
Preview uploaded guidelines analysis
Ability to view previously generated content

### See also:

[KB's Claude conversation](https://claude.ai/share/e3fd5a02-2f18-43a1-8d97-3e69a0e6eb05)

---
title: "AI Bedtime Story Generator"
date: 2025-11-10
categories:
  - SWE
---

A multi-agent AI system that generates age-appropriate bedtime stories for children ages 5-10, featuring adaptive reading levels, content safety filtering, and iterative quality refinement.

![AI Bedtime Story Generator Architecture](/assets/images/block-diagram.png)

<!--more-->

## Overview

The AI Bedtime Story Generator is an intelligent system that creates personalized, safe, and engaging bedtime stories for young children. Using a sophisticated 5-stage pipeline with multiple AI agents, the system ensures stories are appropriately tailored to each child's reading level while maintaining high quality and age-appropriate content.

## Architecture

The system employs a **5-stage pipeline** for story generation:

1. **Reading Level Diagnostic**: Determines appropriate vocabulary and sentence complexity based on grade level (K-5)
2. **Input Validation**: Ensures story requests are safe and appropriate for children
3. **Story Generation**: Creates stories using category-specific prompting and adaptive difficulty
4. **LLM Judge Evaluation**: Evaluates stories against eight quality criteria
5. **Story Refinement**: Iteratively improves stories based on evaluation feedback

## Key Features

### Adaptive Reading Levels
- Vocabulary and sentence complexity automatically adjust based on the child's grade level
- Supports kindergarten through 5th grade reading levels
- Ensures age-appropriate language and concepts

### Content Safety
- LLM-powered filtering system ensures stories are safe for children
- Automatically rejects violence, scary themes, and adult material
- Multi-layered validation for content appropriateness

### Multi-Agent System
- Specialized AI agents handle different aspects of story creation
- Separate components for generation, evaluation, and refinement
- Coordinated workflow ensures quality at each stage

### Category-Specific Prompting
- Tailored generation for different story types:
  - Adventure stories
  - Friendship tales
  - Fantasy worlds
  - Educational narratives
  - And more

### Quality Assurance
- Eight-criterion evaluation system:
  - Age appropriateness
  - Engagement level
  - Educational value
  - Story coherence
  - Character development
  - Moral lessons
  - Reading level accuracy
  - Creativity
- Automatic refinement when stories don't meet quality thresholds
- Structured feedback and improvement suggestions

## Tech Stack

- **Language**: Python 3.7+
- **LLM Model**: GPT-3.5-turbo (OpenAI API)
- **Temperature Settings**: Varies by task
  - 0.1 for safety checks (deterministic)
  - 0.8 for creative generation (more varied)
- **Multi-Agent Architecture**: Custom pipeline with specialized agents

## Output Specifications

- **Story Length**: 300-400 words (perfect for bedtime reading)
- **Target Age Range**: 5-10 years old
- **Format**: Structured narratives with clear beginning, middle, and end
- **Quality Metrics**: Scored across eight evaluation criteria

## Key Technical Achievements

- Designed and implemented a multi-agent AI system with specialized components
- Created adaptive prompting strategies that adjust to different reading levels
- Built LLM-based quality evaluation system with iterative refinement
- Implemented comprehensive content safety filtering using AI
- Developed category-specific generation templates for diverse story types
- Engineered temperature-based control for balancing creativity and safety

## How It Works

1. **Input**: Parent or child provides story preferences (theme, characters, grade level)
2. **Validation**: System checks the request is appropriate and safe
3. **Generation**: AI creates a story tailored to the specified reading level and theme
4. **Evaluation**: LLM judge scores the story across eight quality criteria
5. **Refinement**: If needed, the story is improved based on evaluation feedback
6. **Output**: A polished, age-appropriate bedtime story ready to read

[View Project on GitHub](https://github.com/Payapulli/bedtime-story)

# Language Fluency Meter (Frontend)

A web interface for measuring how "natural" or "fluent" English text is using perplexity scoring from a language model. This repository contains only the frontend code for the Language Fluency Meter project.

## Live Demo

[https://fluency-meter-ui.vercel.app/](https://fluency-meter-ui.vercel.app/)

## About

This frontend connects to a backend API hosted on Hugging Face Spaces that calculates perplexity scores for text. Lower perplexity scores indicate more fluent, human-like writing, while higher scores suggest less natural text.

The tool is inspired by the perplexity-based scoring mechanism from the LongCodeZip paper (arXiv:2510.00446).

## What is Perplexity?

Perplexity (PPL) is a measure of how "surprised" a language model is by a piece of text:
- **Low PPL**: The model predicted the text easily → text is predictable, fluent, and natural (like human writing)
- **High PPL**: The model was very "surprised" → text is awkward, disjointed, or machine-like

## Features

- Simple, clean user interface
- Real-time text fluency analysis
- Displays both numerical perplexity score and human-readable fluency label
- Responsive design that works on both desktop and mobile

## Fluency Labels

The application categorizes perplexity scores into these fluency labels:
- **Very Smooth (Human-like)**: < 40
- **Smooth**: 40-80
- **Slightly Awkward**: 80-150
- **Machine-like or Non-standard**: > 150

## Use Cases

- Detect AI-generated content
- Improve writing clarity and naturalness
- Educational tool for language learners
- Quality assessment for content creators

## Technical Implementation

- Built with vanilla HTML, CSS, and JavaScript
- Makes API calls to a backend on Hugging Face Spaces
- Deployed on Vercel

## Backend API

The frontend connects to a FastAPI backend hosted at [https://sreeprasad1-fluency-meter.hf.space](https://sreeprasad1-fluency-meter.hf.space).

The backend uses the `distilgpt2` model from Hugging Face Transformers to calculate perplexity scores for text.

## Try It With

- **News articles**: Should score low (very fluent)
- **Random word jumbles**: Should score high (not fluent)
- **AI-generated text**: Often scores somewhere in between
- **Non-native writing**: May have higher scores depending on fluency

## Future Improvements

- Visual graphing of perplexity distribution
- Ability to compare multiple texts
- Highlighting particularly "surprising" words or phrases
- Support for additional languages

## License

MIT

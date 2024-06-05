# Supabase image-search-openai-clip

This is a simple example of [how to use OpenAI's CLIP model to search images in a Supabase database](https://supabase.com/docs/guides/ai/examples/image-search-openai-clip).

## Requirements

1. Poetry
2. Supabase CLI
3. Docker

## Instructions

### Spin up local supabase instance (requires Docker)

```bash
supabase start
```

### (Optional) Customize Images

The project comes with 4 images from Lisbon, but you can change that by:

1. Updating the image files in the `./images` folder
2. And updating the `seed` function in `./image-search/main.py` to use these

### Create embeddings for the images

```bash
poetry run seed
```

### Retrieve Result

```bash
poetry run search
```

This will return the image which better matches the predefined search query: `a bike in front of a red brick wall`.

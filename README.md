# Real Estate CMS – Sanity Studio

This is a **Sanity Studio** project for managing real estate property listings. It allows admins to create, edit, and manage real estate data such as title, slug, location, price, image, description, and publish status.

## Project Structure

```
property-cms/
├── sanity.config.ts        # Sanity Studio config
├── schemaTypes/
│   └── property.ts         # Schema for property documents
└── ...
```

## Features

- Auto-generated slug from title
- Rich text editor for property description
- Image upload with hotspot support
- Boolean toggle to publish/unpublish properties

## Schema Fields

| Field         | Type        | Description                       |
| ------------- | ----------- | --------------------------------- |
| `title`       | `string`    | Property title                    |
| `slug`        | `slug`      | Auto-generated from title         |
| `location`    | `string`    | Property location                 |
| `price`       | `number`    | Price of the property             |
| `image`       | `image`     | Main image (with hotspot support) |
| `description` | `rich text` | Rich content using block editor   |
| `isPublished` | `boolean`   | Toggle publish status             |

## Getting Started

### 1. Install Dependencies

```bash
npm install
```

### 2. Create `.env` File

```bash
cp .env.example .env
```

Then fill in your Sanity project ID and dataset.

### 3. Run Sanity Studio

```bash
npm run dev
# or
pnpm dev
```

Visit [http://localhost:3333](http://localhost:3333) to access the CMS dashboard.

## Requirements

- Node.js >= 18
- Sanity CLI (`npm install -g sanity`)

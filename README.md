# M-Scanner 🔬

<p align="left">
  <img src="https://www.animatedimages.org/data/media/562/animated-line-image-0184.gif" width="1920" 
</p>

## Overview:
This repository contains a Next.js application that leverages Hugging Face's Transformers.js library to integrate pre-trained AI models for object detection. This project serves as a comprehensive guide for building, running, and deploying AI applications within a production environment, with a focus on object detection.

## Project Demo:
https://github.com/themihirmathur/m-scanner/assets/92594107/555bfa4d-e702-4b03-9e44-d21aa3a9f69f

## Prerequisites
1. Node.js and npm installed
2. Docker installed
3. Transformers.js knowledge

## Getting Started

1. Clone the repository:

```bash
git clone https://github.com/themihirmathur/m-scanner.git
cd m-scanner
```

2. Install Dependencies:

```bash
npm install
```

3. Get the Environment variable's values or API Keys from the Upload Thing Website: https://uploadthing.com/


4. Then, run the development server:

```bash
npm run dev
or
yarn dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Integrating Transformers.js

1. Import Transformers.js into your Next.js project:

   ```javascript
   import * as transformers from '@huggingface/models';
   ```

2. Load a pre-trained object detection model:

   ```javascript
   const model = await transformers.objectDetection.get({ modelId: 'your-model-id' });
   ```

3. Utilize the model for object detection within your application.

## Docker Image Creation

1. Create a Dockerfile in the root of your project:

   ```Dockerfile
   FROM node:14

   WORKDIR /usr/src/app

   COPY package*.json ./

   RUN npm install

   COPY . .

   EXPOSE 3000

   CMD ["npm", "run", "start"]
   ```

2. Build the Docker image:

   ```bash
   docker build -t your-docker-image-name .
   ```

## Deployment

1. Choose a container orchestration tool (e.g., Kubernetes, Docker Compose).

2. Deploy the Docker image to your chosen environment.

## Customization

Feel free to customize this project to suit your specific AI application needs. Explore different Hugging Face models, fine-tune them, or integrate other AI functionalities.

## Contribution

Contributions are welcome!

<p align="left">
  <img src="https://www.animatedimages.org/data/media/562/animated-line-image-0184.gif" width="1920" 
</p>

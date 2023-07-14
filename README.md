# Blog Posts Repository

This repository is dedicated to storing and managing the blog posts for your personal blog. Any new posts or updates made here will automatically trigger a deployment process in your blog repository, ensuring that your blog stays up-to-date with the latest content.

## Workflow Setup

1. Create the BLOG_REPO secret with the name of your blog repository like `username/your-blog-repository`. This repository will be triggered to deploy whenever there are new changes in your posts repository;
   
2. Create the ACCESS_TOKEN secret. 

## How It Works

The `publish_posts` workflow is triggered whenever there is a push event to the `main` branch of this posts repository. The workflow consists of a single job that performs the following steps:

1. It checks out your posts repository, ensuring that the workflow has access to the latest changes in the repository.

2. It sends a POST request to the GitHub API to dispatch an event in your blog repository. This event triggers a workflow in your blog repository to deploy the updated posts.

With this setup, any new posts or updates made in this posts repository will automatically trigger a deployment process in your blog repository. Your blog will be updated with the latest content, allowing you to share your thoughts and ideas seamlessly.

Please ensure that you have the required environment variables set up in your blog repository, as described in the main README file, to enable the deployment process.

Note: This workflow assumes that you have appropriate access and permissions in both your posts repository and blog repository to trigger workflows and dispatch events.

Enjoy a streamlined process of managing and deploying your blog posts!

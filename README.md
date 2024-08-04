# GEO-MLLMs : MLLMs Assisted Image Geolocation

This is not published work or even COMPLETED work. It's only an idea with some code behind it. This page will be updated with publication updates and other updates with time.

##  Description

Image geolocation refers to the process of automatically estimating, or finding the location of an image based on just the pixels in the image and no other metadata. Image geolocation is often done by using subtle clues and signs in an image (e.g., French on a signpost suggests the image originates from a french speaking country). Image geolocation is a pertinent topic, especially considering the attribution and verification of media originating from warzones or conflicts. This paper proposes a multipart system (GEO-MLLMs) for estimating the location of an image using a MMLLM (Multi-modal Large Language Model), and a pre-existing geolocation method. We predict that our MLLM-based approach will outperform existing approaches to image geolocation on benchmark datasets (yfcc4k, im2gp3k).

## How It Works:

Previously, methods attempting image geolocation have used specialized models which are meant for the specific task of image geolocation. GEO-MLLMs changes this by applying a MMLLM, which is meant for general usage and shows common-sense reasoning on some tasks, on the task of image geolocation. GEO-MLLMs first processes the image through an existing AI image geolocation tool, called GEOClip, and then produces 5 sets of predictions from GEOClip for what the image's location might be. These 5 predictions are then fed into the GPT-4o MLLM along with a prompt to guess the image's true location.

We use GPT-4o over other MLLMs because of it's superior performance than most other available MLLMs.

## Results:

------------

## GPT-4o batch calls JSONL files:

https://www.kaggle.com/datasets/sahalmulki/gpt-4o-json-files

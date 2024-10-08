# GEO-MLLMs : MLLMs Assisted Image Geolocation

This is not published work or even COMPLETED work. It's only an idea with some code behind it. This page will be updated with publication updates and other updates with time.

## Demo

<a target="_blank" href="https://colab.research.google.com/github/sahal-mulki/geo-llm/blob/main/GEO_MLLMs_Demo.ipynb">
  <img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/>
</a>

##  Description

Image geolocation refers to the process of automatically estimating, or finding the location of an image based on just the pixels in the image and no other metadata. Image geolocation is often done by using subtle clues and signs in an image (e.g., French on a signpost suggests the image originates from a french speaking country). Image geolocation is a pertinent topic, especially considering the attribution and verification of media originating from warzones or conflicts. This project proposes a multipart system (GEO-MLLMs) for estimating the location of an image using a MMLLM (Multi-modal Large Language Model), and a pre-existing geolocation method. We predict that our MLLM-based approach will outperform existing approaches to image geolocation on benchmark datasets (yfcc4k, im2gp3k).

## How It Works:

Previously, methods attempting image geolocation have used specialized models which are meant for the specific task of image geolocation. GEO-MLLMs changes this by applying a MMLLM, which is meant for general usage and shows common-sense reasoning on some tasks, on the task of image geolocation. GEO-MLLMs first processes the image through an existing AI image geolocation tool, called GEOClip, and then produces 5 sets of predictions from GEOClip for what the image's location might be. These 5 predictions are then fed into the GPT 4o Mini MLLM along with a prompt to guess the image's true location.

I used the GPT 4o Mini MLLM over other MLLMs because of it's superior performance than most other available MLLMs.

## Results:

<img src="https://github.com/sahal-mulki/geo-llm/blob/main/im2gps_page-02001.jpg" width="500" />

<img src="https://github.com/sahal-mulki/geo-llm/blob/main/yfcc_page-00201.jpg" width="500" />

<img src="https://github.com/sahal-mulki/geo-llm/blob/main/median_page-0002221.jpg" width="500" />


## GPT 4o Mini batch calls JSONL files:

(https://www.kaggle.com/datasets/sahalmulki/gpt-4o-json-files)

## YFCC and IM2GPS subsets

https://www.kaggle.com/datasets/sahalmulki/llms-for-image-geolocation-benchmarks

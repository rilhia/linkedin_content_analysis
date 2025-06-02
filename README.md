![Detective Extracting LinkedIn Data](images/TutorialHeaderImage.png)
# LinkedIn Post Content Analysis  
*How to be Data-Driven and not Data-Distracted around LinkedIn*

Author: Richard Hall  
[LinkedIn](https://www.linkedin.com/in/rilhia/)
[EarthTunnelling.com](https://earthtunnelling.com)

---

## 📖 Introduction

This tutorial was inspired by a [LinkedIn article I wrote](https://www.linkedin.com/pulse/when-data-driven-becomes-data-distracted-richard-hall-pplke) titled:

**"When Data-Driven Becomes Data-Distracted"**

In the article, I explored what I believe to be a troubling shift in how being **data-driven** is now often reduced to chasing shallow, gamified metrics, especially on platforms like LinkedIn.
Likes, follows, and viral engagement are increasingly treated as signals of expertise and credibility. In reality, they are optimised for emotional clicks, not insight.

That article came about because I noticed a particular creator producing a remarkable volume of content. Several daily posts, often long, image-heavy, and written in highly emotive and performative language. It did not sit right. The pattern felt more like an engineered engagement loop than authentic thought leadership. As I looked deeper, I began to see this behaviour in many other places. But it only really became clear once I started looking at the data.

That was when I realised. If we are going to deal with this problem of influence overriding experience, we need to analyse the numbers behind it. It is easy to suggest people “look at the data”, but most people do not know how to access it. The data is there. Every time we browse LinkedIn, it is loaded onto our machines. But it is buried inside hundreds of megabytes of noise. Even if you know where to look, how do you extract it in a usable form?

Fortunately, this is my world. I have worked with JSON and data analysis for years. Once I had built something that worked for my own investigation, it occurred to me that others might find it useful.
So I cleaned it up, added a step-by-step tutorial, and made it available. Now anyone can use it to analyse LinkedIn behaviour for themselves.

---

## 🛠️ What this project does

This is a simple Google Colab-based notebook designed to help you extract, structure, and explore LinkedIn post data from HAR files (saved from Chrome).

The notebook processes the raw data and produces:

✅ Post content (text)  
✅ Post type (original post, share with comment, share with no comment)  
✅ Author details  
✅ Timestamp of each post (converted from epoch time gathered from image metadata and using interpolation of epoch data)  
✅ Engagement data (likes, comments, shares, views where available)  
✅ Links between posts (mapping which posts were shared by whom)  

It also generates an Excel file containing:  

✅ Structured post-level data  
✅ Summary statistics:  
	•	Posting frequency over time  
	•	Average word and character counts  
	•	Distribution of post types  

**Why?**

Well, I’ve already explained the background. But once I’d built the code to acquire this data, it struck me that turning it into a tutorial might be useful for others. It would also serve as an example of the kind of “outside of the box” tutorial content I like to create.

Being “Open To Work” leaves you with time on your hands. I figured this was a productive way to use some of it.

---

## 🤔 Why Google Colab?

I actually discovered Colab while working on training an LLM. I didn’t have access to a decent GPU and wasn’t keen on buying one. Colab was recommended to me because it offers GPU access for a relatively small cost, and the ability to mount Google Drive made life so much easier for managing training data.

That got me thinking, most people already have a Google account. By building this as a Colab notebook, I could make it really simple to use with there being no need to install Python or set up anything locally. Just open the notebook and run it in the cloud.

---

## 🚀 How to use this

1️⃣ Open this notebook in Google Colab by clicking on the link:  

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/your-username/your-repo/blob/main/LinkedIn_Post_Data.ipynb)

2️⃣ Follow the instructions in the notebook:
- How to mount your Google Drive
- Set up your required variables
- How to export a LinkedIn HAR file
- How to upload it to Colab
- How to run the analysis

---

## 🧑‍💻 What's inside the notebook

The tutorial covers:

- **Section 1**: Why I built this  
- **Section 2**: How to capture LinkedIn post data (HAR files)  
- **Section 3**: How the notebook works  
- **Section 4**: Analysis of post content  
- **Section 5**: How this can be useful in other contexts  

---

## 📝 License

This project is licensed under the **Creative Commons Attribution 4.0 International (CC BY 4.0)** license.

---

## ⚡ Final thoughts

This is a simple tool — but I believe it’s a useful one.  
It helps bring **transparency and data literacy** to the analysis of online influence.

And the same techniques can easily be adapted to analyse:
- Your own LinkedIn posts
- People you follow
- Connections
- Follower patterns  

If you find it useful — let me know!  

---

**“The trick with technology is to avoid spreading darkness at the speed of light.”**

---

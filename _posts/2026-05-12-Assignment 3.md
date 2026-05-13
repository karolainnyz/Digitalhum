---
title: "Assignment 3"
categories: 
- Assignments
- Blog 
 
---

<p style="color: hotpink; font-weight: bold; font-family: 'Times New Roman', serif; font-size: 35px;">
Analysis of ceramics utilizing Orange Data Mining (AI vs. Human analysis!) :D
</p>

For Assignment 3, I created a custom corpus of ceramic objects to explore how machine learning algorithms interpret and classify visuals. My dataset consisted of over 200 images that I manually collected through Google searches. To build my corpus, I used the Image Downloader Chrome extension introduced in class by our professor. When building my dataset, I specifically searched for different categories of ceramic objects, including “ceramic vases," “ceramic bowls," “ceramic mugs,” and “ceramic plates.” I decided to focus on these categories because they offered the widest range of variation in shape, texture, color, patterns, and overall design while remaining visually identifiable as ceramic objects. 

After searching each category, I used the Image Downloader extension to download around 30 - 50 images per object. This extension was really helpful when it came to selecting the images because I was able to prioritize visual variety. By looking at each image, I was able to create a more complex and intentional dataset for my clustering analysis. I selected ceramics with abstract textures, abstract and traditional shapes, matte and glossy finishes, and patterned and minimal designs. As well as a wide range of colors, including pastel tones, neutral colors, earthy tones, and even darker ceramics. I also included images that were photographed from different angles, but tried to keep a simple white background.

 By building a dataset with strong visual variations, I hoped to create more interesting clusters and misclassifications when analyzed through Orange Data Mining, utilizing the InceptionV3 image embedding model. Through this assignment, I wanted to explore how AI prioritizes visual similarities such as the ones I’ve mentioned above, which are all characteristics humans associate with ceramic objects. 

After collecting all of the images, I organized them into different folders to be able to experiment with multiple types of classification in Orange Data Mining. The organization method I used groups the chosen ceramics by object type, including plates, bowls, mugs, and vases. I then put these folders into one folder titled "Dataset." Once I put this data into Orange Data Mining and ran t-SNE, I was able to visualize how AI grouped the images based on their visual similarities rather than their actual object categories. This allowed me to observe which ceramics the AI considered to be visually related, even when they belong to completely different groups and are not the same objects. Through the image plots, I noticed that the algorithm is connecting objects that humans analyzing this dataset would normally separate. Some of the most interesting results in this dataset came from the mistakes the model made, since they revealed many different ways that machine learning systems interpret images compared to human analysts. 

![full plot map](/assets/images/IMG_3527.JPG)

The overall t-SNE visual map reveals several patterns in the clustering that caught my eye across the ceramic object categories originally made. The ceramic vases (classified as gold) occupy the entire top right side of the map, indicating a strong visual consistency in their tall shapes and features. In contrast, ceramic mugs (classified as red) are more dispersed across the top left side, which may reflect greater variety in their structures, proportions, and designs. The ceramic bowls (classified as blue) and the ceramic plates (classified as green) appear in smaller and tighter groupings, which suggest that the model identifies them through a narrower range of shared visual characteristics. A few isolated or overlapping points between clusters likely represent ambiguous ceramics or images whose shapes or textures visually resemble features shared across multiple object classes. 

![first image](/assets/images/Image%202%20-%20Plates%20+%20bowl.png)

In this first image plot, a ceramic bowl image (image 23) was clustered alongside the ceramic plates rather than with other bowls. At first glance, this seemed like an incorrect classification. After examining the images carefully, I was able to understand why AI would cluster these images together. 

I believe the pattern and color palette of this bowl played a major role in the confusion of the AI. The bowl has a very glossy and marble-like design with very light tones that visually resemble the plates in this cluster. Many of the nearby plates shared the same smooth, reflective surfaces, soft neutrals, minimalistic designs, and white, plain backgrounds. Because these objects were all photographed against similar white backgrounds, I think the images began to visually blend despite belonging to different categories. The camera angle likely contributed to the clustering, also. Most of the ceramics in this cluster were photographed from a high angle, which makes the bowls appear flatter and may have reduced the visibility of their depth. Since the plates were also round and photographed from a high angle, the algorithm had fewer visual clues to distinguish between the two forms. From a side angle, the structural differences between bowls and plates would likely have been easier for the model to identify. Instead, the overhead perspective emphasized their similar circular appearance rather than their physical depth. 

This cluster and analysis reminded me of Impett and Offert’s argument that when humans interpret visual corpora through networks, they are also interpreting the assumptions and priorities built into the machine’s systems of perception. The clustering process reflects not only the objects themselves, but also the specific visual information the trained model has learned to recognize and also prioritize. 

![second analysis](/assets/images/IMG_3530.JPG)

![plot of second analysis](/assets/images/plots%20of%20image%203%20.png)

One particularly interesting misclassification involved image 1, which is a white ceramic bowl clustered among abstractly shaped vases. This classification seemed highly inaccurate to me because image 1 clearly belonged to a different category of ceramics. However, as I analyzed this cluster thoroughly, the reasons as to why AI would pair these images together became clearer. 

Unlike the traditional images of bowls with symmetrical and circular forms I downloaded, this bowl featured a very abstract shape. Looking at this cluster, the unevenness and construction of this bowl visually resembled the surrounding vases, with similar textures and abstract shapes to downloads 85 and 50. This bowl was very similarly constructed to download 79, as they are both white and have some abstract patterns and lines (not just shapes). This example demonstrates how machine learning systems are identifying similarities that humans may overlook when classifying images. 

As a human viewer, I immediately recognized the error because I saw the object simply as a bowl. However, the algorithm prioritized visual attributes over practical and basic interpretation. This finding also reflects some of the themes discussed in Distant Viewing by Arnold and Tilton regarding the importance of labeling and categorization when it comes to computational analysis. Labels are not just neutral descriptions, they shape and affect how algorithms learn and interpret the visual information provided. Through this assignment, I’m learning that if the categories themselves contain ambiguous, vague, or overlapping visual features, the boundaries between classifications become unstable. 

![messy cluster](/assets/images/plots%20of%20image%204%20.PNG)

![messy plot image results](/assets/images/IMG_3529.JPG)

These images produced an even more complex and ambiguous cluster. In this section, ceramics of every category (bowls, cups, vases, and plates) appeared heavily mixed together. For me, this cluster became one of the most revealing parts of the project because it demonstrated how strongly aesthetic similarities can overrule any kind of functional categorization in machine vision systems. 

Firstly, many of their ceramics shared a similar minimalist design. The objects used pastel palettes, smooth and matte surfaces, soft lighting, and neutral backgrounds. Visually, they resembled one another even when they belonged to different categories. From a human perspective, we rely heavily on the contextual and practical understanding we have of the object to distinguish a cup from a vase or, very obviously, a bowl. However, the algorithm instead focused on the repeated visual features that appeared across the dataset. 

 I believe the image quality heavily affected classification as well. Most images, particularly images 58, 65, 2, 14, 3, and 74, appeared blurry or low resolution. Although these objects were vases and plates, AI grouped them alongside bowls and mugs. The lack of sharp edges and the reduced details likely weakened the model’s ability to identify distinguishing structural features such as narrow necks or openings, typically in vases. 
Overall, this suggests that machine learning models are highly sensitive to image resolution and quality. Human viewers can often recognize objects despite the blur or distortion because we draw upon contextual knowledge and prior experience with these objects when we can’t visualize them. In contrast, AI relies more directly on visuals and pixels. When those features become unclear, classification errors are more likely to occur. 

![brown plate](/assets/images/IMG_3528.JPG)


![plot of brown plate](/assets/images/plots%20of%20image%205%20.png)

![isolated blue bowls](/Digitalhum/assets/images/IMG_3531.JPG)

![plots](/assets/images/Image%206%20-%20plots%20of%20image%206.png)

Some of the most intriguing moments for me during this assignment came from objects that appeared to be completely misclassified from the beginning. Unlike previous examples I mentioned, where the AI’s reasoning becomes more understandable after careful analysis of each image, a few results remain genuinely surprising and confusing even after closer inspection. One example is the brown plate labeled “images.” The model classifies this plate as a mug despite the object looking much more like a ceramic plate. This image lacked many of the features humans would normally associate with mugs, such as a visible handle or cup-like depth. The only aspect that could have affected the classifications is the image containing mostly a brown color palette, with both the ceramic object and background being similar shades of brown. This may have caused the object to visually blend into its background, making the overall structure less clear to the algorithm. 

Another result that stood out to me involved two blue data points on the map that appeared completely isolated from the rest of the bowl clusters and were positioned much closer to the mugs. This classification was especially surprising because, despite their abstract forms, the objects appeared to still have bowl-like features to me. However, unlike the more traditionally round bowls I included in the dataset, these ceramics had much more sculptural and unconventional shapes. Their asymmetrical forms separated them from the other bowls, which may explain why the algorithm struggled to associate them with the rest of their category. 

What made these results particularly interesting for me was that they revealed moments where the AI’s interpretation differed not only from the intended labels but also from my own expectations while analyzing the dataset. These outliers show that machine learning systems can sometimes organize visual information according to relationships that are not immediately intuitive to human viewers. Rather than simply exposing algorithmic “errors,” these misclassifications revealed the limitations of human viewers when it comes to the categorization of visually ambiguous objects. 

Overall, I found this assignment very interesting, as it demonstrated that machine learning systems interpret visuals very differently from human viewers. Through Orange Data Mining and the InceptionV3 image embedding model, I was able to thoroughly observe how AI is prioritizing repeated visual patterns across my dataset of ceramics rather than the intended functions of the objects themselves. While I initially expected the clustering system to organize the images mostly according to their assignment categories, many of the most interesting findings came from moments where the algorithm failed to do so. Bowls were often grouped with plates, abstract ceramics were harder to classify, and small aspects of images, such as their lighting and angles, can cause ceramics to be mixed into entirely different clusters. In these cases, the AI focused solely on the aesthetic similarities. 

These misclassifications revealed that human categorization systems are not always as fixed or objective as they may initially appear. This assignment reinforced many of the ideas we discussed through the second half of the course regarding machine perceptions, the importance of labeling, and computational analysis. Rather than simply identifying “right” or “wrong” answers, the clustering process exposed the different ways humans and AI systems organize visual information. Ultimately, this assignment showed me that machine learning models do not interpret images through their basic understanding or practical knowledge of the objects but instead through repeated patterns they have learned through analyzing visual data. Because of this, the mistakes and ambiguities within this dataset became some of the most valuable and revealing parts of the entire analysis. 

READY FOR GRADING!
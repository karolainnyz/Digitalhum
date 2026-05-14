---
title: "Assignment 2"
categories: 
- Assignments
- Blog 
layout: single
---

<p style="color: hotpink; font-weight: bold; font-family: 'Times New Roman', serif; font-size: 35px;">
Manual Geocoding vs. Automated Geocoding in Southern Arabia! :D
</p>

For this assignment, I explored the differences between manual geocoding and automated geocoding through a section of Southern Arabia by Theodore and Mabel Bent. The text focuses on travel through the Hadhramout region and reflects many of the colonial perspectives common in nineteenth century travel writing. Although the text contains a very Western and imperial perspective, it also became a really interesting example for understanding how digital tools identify, interpret, and visualize locations from historical texts.

I manually annotated locations in Recogito and then compared my annotations to an automatically generated geocoded dataset created through computational methods. After cleaning both datasets, I visualized them together using an interactive Leaflet map in R. Through this comparison, I wanted to better understand how humans and machines approach geography differently when working with historical texts.

What I found most interesting throughout this project was that the differences between the two datasets were not random. Many of the mismatches reflected problems involving historical place names, transliteration, ambiguity, and interpretation. Similar to some of the discussions we had throughout the semester about computational methods, this assignment showed me that mapping is not simply a neutral technical process. Both humans and machines make assumptions when converting textual references into geographic coordinates.

The main question guiding my project was: how do manual and automated geocoding methods differ when mapping historical locations from Southern Arabia?

To explore this question, I compared two datasets created from the same text. The first dataset came from my own manual annotations in Recogito, where I identified locations myself and researched coordinates using mapping tools and gazetteers. The second dataset was automatically generated using computational methods involving named entity recognition and geocoding.

After creating the datasets, I visualized both layers together using Leaflet in Posit Cloud. By comparing the two maps interactively, I was able to observe where the datasets overlapped, where they differed, and what kinds of locations created the most disagreement between human interpretation and machine analysis.

This assignment connects closely to many of the course concepts we discussed regarding computational thinking, spatial humanities, and digital visualization. Rather than only focusing on whether the map “worked,” I became more interested in understanding what the mistakes, mismatches, and ambiguities revealed about both human and computational approaches to spatial analysis.

I began the assignment by uploading the provided text into Recogito and manually annotating as many place names as possible. During the annotation process, I used gazetteers such as GeoNames, HistoGIS, and Pleiades to identify locations. However, many of the locations in the text were difficult to map because they either used older spellings, colonial transliterations, or historical names that no longer appear clearly in modern geographic databases.

![Figure 1](/Digitalhum/assets/images/Screenshot 2026-05-14 at 2.32.41 AM.png)

When the gazetteers did not provide accurate matches, I used outside sources such as OpenStreetMap and Google Maps to help identify possible coordinates. This part of the project required much more interpretation than I initially expected. Unlike automated geocoding systems, I had to think carefully about context, nearby locations, spelling variations, and the way the places were described in the narrative.

After finishing the annotations, I downloaded my Recogito dataset as a CSV file and cleaned the data before visualizing it. Some records required additional formatting and coordinate adjustments, especially when latitude and longitude information appeared inconsistently.

To create the visualization, I used the Leaflet package in R through Posit Cloud. The map contains two clickable layers: one layer for the manually geocoded dataset and another for the automatically geocoded dataset. I used different colors to separate the datasets visually and included interactive toggles so users could compare them directly.

![Figure 2](/Digitalhum/assets/images/Screenshot 2026-05-14 at 2.49.17 AM.png)

One issue I encountered during the mapping process involved overlapping points. Many locations appeared extremely close together geographically, especially within the Hadhramout region, which made some markers difficult to distinguish visually. To solve this problem, I used jitter to slightly offset some points on the map. Although this slightly reduced geographic precision, it made the map much easier to read and compare.

The final map revealed several interesting patterns when comparing the two datasets. Both the manual and automated datasets clustered heavily in eastern Yemen, particularly around the Hadhramout region. Since this section of Southern Arabia focuses strongly on travel routes and settlements in this area, the concentration of points made sense geographically.

<iframe src="https://karolainnyz.github.io/Digitalhum/interactive_map.html" width="100%" height="500"></iframe>

At first glance, many of the points from both datasets appear very similar. However, after examining the layers more carefully, I noticed that the datasets often did not align perfectly. Some locations overlapped closely, while others were mapped to noticeably different coordinates. These mismatches became one of the most interesting parts of the project because they revealed the different ways humans and computational systems interpret place names.

Many of the differences appeared to result from ambiguity in the historical text itself. The automated geocoding system often relied on direct textual matches and struggled with older spellings, colonial transliterations, or locations with multiple possible matches. In contrast, manual geocoding allowed me to use contextual clues from the surrounding text to make interpretive decisions about which location was most likely correct.

One thing I noticed while working on the project was that humans naturally interpret geography through context, while automated systems depend much more heavily on exact textual patterns. When reading the text myself, I could often infer possible locations based on nearby regions, travel sequences, or historical references. The automated system could not easily replicate this kind of contextual reasoning.

The interactive map also changed the reading experience compared to a static image. Being able to toggle between the two layers made it easier to observe where the datasets overlapped and where they diverged. Instead of simply viewing a finished visualization, users are able to explore the differences themselves through interaction.

This assignment also reminded me of many of the discussions we had throughout the course regarding digital humanities and computational interpretation. Similar to the ways AI models classify images through visual patterns rather than human reasoning, automated geocoding systems prioritize textual and geographic matches without fully understanding historical or cultural context. Because of this, the errors and mismatches within the dataset became some of the most revealing parts of the project.

Another aspect I found interesting was how maps themselves simplify historical information. Although the visualization makes geographic patterns much easier to identify, reducing locations to coordinate points can flatten more complex historical and cultural relationships between places. The map becomes a useful analytical tool, but it also shapes the way viewers interpret the text spatially.

One of the biggest things this assignment demonstrated was that computational mapping systems are not completely objective. Automated geocoding may appear more precise because it relies on algorithms and databases, but those systems still depend on assumptions built into the software, datasets, and gazetteers being used.

For example, historical place names created many challenges for the automated system. Some locations no longer exist under the same names, while others were spelled differently because of transliteration or colonial naming practices. In several cases, the automated dataset appeared less contextually accurate because it selected locations based primarily on textual similarity rather than historical relevance.

At the same time, manual geocoding also has limitations. Human interpretation is subjective, and different people might map the same place differently depending on the sources they use or how they interpret the text. Manual annotation also takes much longer and requires significantly more effort than automated processing.

Several technical issues also affected the project. Some records contained incomplete or inconsistent coordinate information, which created problems during the cleaning and visualization stages. Formatting differences between the datasets occasionally caused errors within Posit Cloud as well. Additionally, while jitter improved readability on the final map, it slightly distorted the exact positioning of some markers.

These issues made me think more critically about the relationship between computational methods and interpretation. Throughout this course, we discussed how digital humanities projects often appear objective or data-driven even though they still involve many human decisions behind the scenes. This assignment reinforced that idea very clearly for me.

I also think this project raises important questions about which regions and histories are easier for automated systems to represent accurately. Places with standardized names and strong representation in modern geographic databases are much easier for machines to process. In contrast, historically marginalized regions, multilingual locations, or places with colonial naming histories may become more difficult for automated systems to interpret correctly.

Overall, I found this assignment really interesting because it revealed how differently humans and machines approach geographic interpretation. By comparing manual and automated geocoding methods through an interactive map, I was able to observe where the two systems aligned, where they differed, and why those differences occurred.

Although automated geocoding allows for fast and large-scale spatial analysis, this project demonstrated that human interpretation remains extremely important when working with historical texts. Humans are better able to understand ambiguity, context, historical references, and linguistic variation, while automated systems depend much more heavily on textual and geographic pattern matching.

At the same time, the project also showed me that maps and computational visualizations are not neutral representations of information. Every stage of the process involved interpretive decisions, including annotation, cleaning, formatting, visualization, and geocoding. Rather than simply producing a “correct” map, the assignment revealed how digital tools shape the way we understand historical geography.

Similar to many of the other computational projects we completed throughout the semester, some of the most valuable insights came from the mistakes, mismatches, and ambiguities within the dataset itself. Instead of treating those moments as simple failures, they became opportunities to better understand the strengths and limitations of both human and machine interpretation.

RECOGITO LINK:

https://recogito.pelagios.org/document/9wson4wgfwwnj5/part/1/edit

READY FOR GRADING!!!
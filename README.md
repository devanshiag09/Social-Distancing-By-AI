# Social Distancing By AI

Using python, deep learning and computer vision to monitor social distancing.

**Is social distancing Important?**

According to world health organization,

![](/static/who_sd.jpg)

*Image via Google(http://google.com)*

Prevention –

- Maintain at least 6 feet distance between yourself and others. Why? When someone coughs, sneezes, or speaks they spray small liquid droplets from their nose or mouth which may contain virus. If you are too close, you can breathe in the droplets, including the COVID-19 virus if the person has the disease.

- Avoid going to crowded places. Why? Where people come together in crowds, you are more likely to come into close contact with someone that has COIVD-19 and it is more difficult to maintain physical distance.

**What is social distancing?**

Social distancing, also called &quot;physical distancing,&quot; means keeping space between yourself and other people outside of your home to control the spread of contagious diseases (such as coronavirus).

To practice social or physical distancing:

- Stay at least 6 feet (about 2 arms&#39; length) from other people

- Do not gather in groups
- Stay out of crowded places and avoid mass gatherings



![](/static/social-distancing.jpg)

*Image via External Sources*

In addition to everyday steps to prevent COVID-19, keeping space between you and others is one of the best tools we have to avoid being exposed to this virus and slowing its spread locally and across the country and world.

**Conclusion time!! Social distancing is arguably the most effective non pharmaceutical way to prevent the spread of a disease — by definition, if people are not close together, they cannot spread germs!**

**But how we can leverage &quot;AI&quot; to achieve this?**

![](/static/sur.jpg)

*Image via External Sources*

**Surveillance:**

The AI can be used by humanitarian and law enforcement processionals to gauge whether people are abiding by public health guidance. An AI system can keep a lookout for objects at the same standard (or better) when compared to a human. With that being said, using technology to perform surveillance is much more efficient. Surveillance is a repetitive and mundane task. This may cause performance dips for us human beings. By letting technology do the surveillance, we could focus on taking action if something goes amiss. To survey a large strip of land, you need lots of personnel. Stationary cameras also have a limited range of view. With mobile surveillance bots (such as micro drones) these problems can be mitigate.

**Space Planning &amp; Optimization:**

This technology can help small crowd gathering platforms such as restaurants and medium sized offices, to help maintain a comfortable number of customers or employees within their enclosed spaces. Its utility could be expanded to design a social distancing friendly seating arrangement plan so as to utilize the maximum space offered within the enclosures and help track if the crowd conforms to the said seating plan without any violations.

**Traffic influx control  (Density Management):**

For high density enclosures with constant influx and exit of people such as metro platforms, malls, museums, etc; a population density tracker can be maintained that records the average distance amongst the crowd and generates an alert to the officials every time the average distance violates a particular threshold. This achieves the goal of controlling the inflow of people at the very entry itself and still manages to keep a healthy density of crowd within the public gathering platform, without raising any safety concerns.

## Process

In the past decade, AI/Deep Learning has shown promising results on a number of daily life problems. Various daily life tasks have been automated with the help of AI. Detecting distances between pedestrian from 2D images without any extra information is not possible. One way is to define the minimum pixel threshold corresponding to 6 feet to conclude the violatoin of social distancing and compute euclidean distance between the centroids. This would have been true if the camera was equidistant to all the points on the plane where the pedestrians were walking. The closer the pedestrians are to the camera the bigger they are. The closer the two points (which are same number of pixels apart ) on the frame to the camera, the smaller is the actual distance between them. 

**How to install?**

**Clone the repository**

```
https://github.com/devanshiag09/Social-Distancing-By-AI.git
```

**Install required packages**

The provided requirements.txt file can be used to install all the required packages. Use the following command

```
pip install –r requirements.txt
```

**Install required packages**

Run the social_distance_detector.ipynb Jupyter Notebook.


![](/static/flow.JPG)


**Detecting people in a frame or a video,**

- When it comes to deep learning object detection, there are primary three object detection neural net architecture,
  - R-CNN and its variant;  Original R-CNN, Fast R-CNN, Faster R-CNN.
  - Single shot detector.
  - YOLO. (YOLOv3) **Currently Used**

- **Learn the minimum pixel thrsehold to conclude violation**.  

- **Compute the pair wise distances** between all the detected people.

- **Based on the distances we will monitor the social distancing.**

- **Monitor Social Distancing Violation Index Scale - 1: Good; 0:Poor.**

**Output: Social Distancing Parameters**

The algorithm calculates and reports the following parameters.

1. Social Distancing Violation: Number of times the pedestrians violated the 6 feet safe distance threshold.

2. Number of People

3. Social-distancing Index: Quantifies the social distancing being maintained. 0 means all of the interaction violate the safe 6 feet distance criteria, 0.5 means half of the interactions violate the safe 6 feet distance criteria, 1 means none of the interaction violate the safe 6 feet distance criteria.

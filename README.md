## Social Distancing By AI

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

**Process,**

![](/static/flow.JPG)

**Detecting people in a frame or a video,**

- When it comes to deep learning object detection, there are primary three object detection neural net architecture,
  - R-CNN and its variant;  Original R-CNN, Fast R-CNN, Faster R-CNN.
  - Single shot detector.
  - YOLO. (YOLOv3) **Currently Used**

- **Compute the minimum pixel thrsehold to conclude violation**.  

- **Compute the pair wise distances** between all the detected people.

- **Based on the distances we will monitor the social distancing.**

- **Monitor Social Distancing Violation Index Scale - 1: Good; 0:Poor.**

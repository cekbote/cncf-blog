# My Google Summer of Code Journey as a Student Developer for CoreDNS

*Guest post published by [Chanakya Ekbote](https://www.linkedin.com/in/chanakyaekbote/), a Google Summer of Code Student Developer, mentored by [Paul Greenberg](https://www.linkedin.com/in/greenpau/) and [Yong Tang](https://www.linkedin.com/in/yong-tang/) as a part of the CoreDNS Organisation. He is currently an underad at the Indian Institute of Technology Bhubaneswar.*

Google Summer of Code (GSoC) is a global program focused on bringing more student developers into open source software development. Through the program, students get matched with open source, free software and technology-related organizations to write code and contribute to the open source community. The organizations provide mentors who act as guides through the entire process, from learning about the community to contributing code. The selected students work on a 3 month programming project during their break from school. 

I was lucky and honoured to be selected to work on the project: [Anomaly Detection of the CoreDNS Server through Machine Learning](https://summerofcode.withgoogle.com/projects/#4806808834670592) proposed by maintainers of the CoreDNS Organisation (a CNCF gradudated project). Through this post, I'd like to describe my journey and also showcase the work my mentors and I accomplished over the summer.

## General Overview

The project is currently being used to integrate machine learning capabilities with CoreDNS, with the objective of protecting people against malicious websites and applications. It helps in identifying websites that could be potentially used by malicious hackers and cybercriminals and prevents the user from accessing such websites. 

The project is also being used to provide machine learning capabilities to languages and platforms that generally have a dearth of such capabilities. One of the best features is that it is fully customisable and therefore can be tailored to fit the needs of any other project or organisation. 

The project website can be found here: https://mlbridge.github.io/

## Applying to the Google Summer of Code Program as a part of the CoreDNS Organisation

I have always loved to contribute to open source projects ever since the first year of my undergraduate journey. I had applied to GSoC last year too, but unfortunately, it just didn’t materialize. This year I started contributing to an open-source organisation since the month of November. I familiarised myself with the code base, made a few connections in the community and submitted a few PR’s too. A few months down the road, I was elated to hear that the organisation would be participating in GSoC’20. Since I knew what projects they were working on and what new additions the projects would require, I was confident of submitting a good proposal with the appropriate deliverables. 

However, fate had something else in store for me. The organisation I was contributing to, did not get selected for the GSoC’20 program and I had to look for other opportunities. I was searching for another organisation to apply to, when one of my peers advised me to take a look at CoreDNS. I was a bit apprehensive at first but when I saw the projects that CoreDNS had listed, I was floored. 

The CoreDNS organisation had a project that I was really passionate about. It basically combined machine learning with cybersecurity which seemed like a pretty interesting proposition. I got in touch with the mentors Paul and Yong and clarified any discrepancies that I had. With the inputs that I had from the mentors, I created a proposal and the rest is history. 

## The Community Bonding Period

Due to the onset of COVID-19, my term exams were postponed to bang in the middle of the Coding Period. Hence, in order to complete the goals of the project, my mentors and I decided to start working on the project from the start of the Community Bonding Period itself. 

Initially, the main challenge we faced was integrating machine learning capabilities into the CoreDNS server as Go (the language CoreDNS has been built on) does not support the CUDA platform (that is essential for machine learning applications). At the same time, the Python ecosystem has tools like TensorFlow, PyTorch, MXNet and various others that not only interact with the CUDA platform but also allow for the easy prototyping and evaluation of deep learning models. 

Upon ideating on the same, we decided not to reinvent the wheel but use the machine learning tools that Python has in tandem with CoreDNS by setting up a communication link between a CoreDNS plugin and a Python Flask server that contains the machine learning model. Hence the goal of the Community Bonding Period was to create a CoreDNS Plugin (ML Bridge Plugin) as well as a machine learning model that would be incorporated into the Flask server (ML Bridge Middleware.) 

<p float="left" align = "center">
  <img src="https://github.com/cekbote/cncf-blog/blob/master/readme-assets/first_step.png"/>
</p> 

## 

---
layout: post
title: Bloc Chat
thumbnail-path: "img/blocchat.png"
short-description: A real-time chat application built with Firebase and AngularJS.

---

{:.center}
![]({{ site.baseurl }}/img/blocchat.png)

## Explanation

Bloc Chat is a project built into the Bloc Wed Developer Track curriculum. Prior to this, I had been very throroughly walked through how AngularJS works and created a simple song playing application with it. This was my first experience working with AngularJS without a lot of handholding. I was also introduced to Firebase and AngularFire with this project. With the knowledge base I had, help of my mentor, and lots of Stack Overflow research, I was able to create this simple chat application.

## Problem

Bloc tasked me with creating a simple chat application that sends and received messages in real time. Using AngularJS and Firebase were required. Bloc wanted the app to require the user to create a username, see a list of chat rooms, a way to add new chat rooms to the list, and the ability to send and see new messages.

## Solution

The first task I tackled was getting a skeleton of the app up. I did some wireframing to get an idea of what I might want the site to look like then made it live, using HTML and CSS. 

My first user story was to see a list of available chat rooms. I used Firebase to create a few fake rooms along with an Angular factory to display these Firebase rooms.

I, then, moved to giving the user the ability to create a new chat room. By modifying my existing chat room factory and utilizing the UI Bootstrap modal service, I was able to accomplish this. 

{:.center}
![]({{ site.baseurl }}/img/blocchatroom.png)


Next, the user needed to see a list of messages. I created another Angular factory that queried fake messages I had created in Firebase and associated those with the appropriate room.

How would you be able to tell who was sending a message? Requiring a username was needed to accomplish this. Using cookies and the Angular `.run()` method, I was able to force the unknown user to create a username. Cookies enables the user to by-pass creating a new username if they had previously created one. 

{:.center}
![]({{ site.baseurl }}/img/blocchatusername.png)


What would a chat application be without the ability to send messages? I modified the existing factory for messages with logic for sending message objects to the Firebase server. I also injected the `$cookies` service into the username property so the message would be associated with the appropriate user. 

## Results

In order to test my solutions, I utilized node.js to test my progress and get visual confirmation of my solutions. I learned towards the end of this project that it helps me to get the HTML and CSS going first to get a visual of what needs to be done. I then worked on my services and tested as I went until I got the result I wanted. 

## Conclusion

This project was very tough for me in the beginning. Creating an application from near-scratch was intimidating and I had to coach myself past that to get started almost every time I worked on it. It was so gratifying to see when things did work and that I was capable of completing the tasks. In the end, I'm now excited about new projects!
# Project 1, Milestone 1 - Design & Plan

Min Zheng

## Markdown

## 1. Persona

I've selected Abby as my persona.


Abby has low confidence about doing unfamiliar tasks. So the goal is to design the website as easy to use as possible. Abby rarely has spare, indicating that she works for long time and also she needs to relax. Therefore, I design a website that can both help her concentrate at work and help her relax when she gets time. She also likes tasks with familiar features, because they are more predictable. Therefore, I use very similar pattern in between different web pages, so that she can feel comfortable using it.



## 2. Sketches
1. The Home page is a simple welcome page. The navigator is designed as circles, directing to three other pages. The "about us" information may pop up when clicking the button.
![](sketch1.jpg)

2. Relax page. A picture of forest will display, along with some background sound. The sound may be turned off. There is a back button to take you to the main page.
![](sketch2.jpg)

3. Focus page. A timer will start once you enter the page, telling you how long you have been focusing. A background sound will play and it may be turned off. You can enter your goal in the text box so that the text will display under the timer. There is a back button to take you to the main page.
![](sketch3.jpg)

4. Cure page. It is time to cure yourself after a long day of work. Cats' picture will display in the circles.
![](sketch4.jpg)

Those design makes the interface very easy to use, which I think may work well for Abby. Also, it should be able to provide Abby help during her work and spare time.

## 3. Wireframes
1. The Home page:
![](Wireframes1.jpg)
And the pop up "About us" information after clicking the button.
![](Wireframes5.jpg)
2. Relax page:
![](Wireframes2.jpg)
3. Focus page:
![](Wireframes3.jpg)
4. Cure page:
![](Wireframes4.jpg)

## 4. Coding Plan & Pseudocode
The three pages has very similar style, so that a template may be created to reuse. Each page will have a separate PHP file, but the general layout will be implemented using a PHP *includes*.  

The main page PHP will have a navigation bar. The three other pages will be stored in a list.

The styling and other effects design:
* background and shapes: defined in HTML and styled with CSS

* timer: the information is obtained using a PHP function and javascript, displayed using HTML and styled using CSS

* pictures display: the bounding box of images will be designed using HTML, and the images will be displayed using a PHP function

* buttons and other interactive elements: will be implemented using PHP functions


### pseudocode
```
/*
This function takes in the page ID (focus/ relax/ cure) and fill the images into desired boxes.
*/

function fill_images(page ID)
  go to the folder corresponding to the page
  for each image box in the page:
    find and read in the corresponding image ID
    scale and crop the image as needed
    display the image
  end
end
```


```
/*
This function calculates the numbers that should be displayed by the timer
*/

function timer_calc(time_in)
	get current time as time_now
	time_spent = time_now - time_in
	parse and return the hour, min, sec in a list
end
```

+++
content_img_path = "/images/IMG_8576-1.jpg"
date = 2020-05-05T07:00:00Z
excerpt = ""
layout = "post"
subtitle = ""
thumb_img_path = "/images/IMG_8576-2.jpg"
title = "Thermocouple Data Logging"

+++
My soldering octopus came in the mail today, along with the thermocouple connectors so I was able to solder terminal blocks onto the thermocouple amplifier and Micro SD breakout boards. I was on a roll so I decided to see how far I could get writing code to log temperature measurements on the SD card. This is my first time ever writing Arduino code but luckily there are lots of examples online and I was able to pretty quickly copy and paste a piece of Frankenstein code together. Here's a snippet of the file that was on the card when I plugged it into my laptop.

<table>

<tbody> <tr> <td>24.50</td> <td>28.75</td> </tr> </tbody>

<tbody> <tr> <td>24.50</td> <td>28.75</td> </tr> </tbody>

<tbody> <tr> <td>24.56</td> <td>29.00</td> </tr> </tbody>

<tbody> <tr> <td>24.56</td> <td>29.00</td> </tr> </tbody>

<tbody> <tr> <td>24.63</td> <td>29.00</td> </tr> </tbody>

<tbody> <tr> <td>24.56</td> <td>NAN</td> </tr> </tbody>

<tbody> <tr> <td>24.63</td> <td>29.00</td> </tr> </tbody>

<tbody> <tr> <td>24.56</td> <td>29.00</td> </tr> </tbody>

<tbody> <tr> <td>24.63</td> <td>29.25</td> </tr> </tbody>

<tbody> <tr> <td>24.63</td> <td>29.25</td> </tr> </tbody>

</table>

The column on the left is the temperature at the cold junction in Celsius and the column on the right is the hot junction (I put my hand on the end of the thermocouple to warm it up). The time increment between each measurement was 500 milliseconds and as I write this I'm realizing I should have added a third column to log time...I'm also not really sure what the NAN is and will need to investigate.

Right off the bat, it seems like the thermocouple is pretty slow to respond to changes in temperature, which makes me wonder if I will get any useful information out of a test that is only going to last for a couple seconds. 

After doing a quick Google search it turns out that the style (grounded, non-grounded, exposed wire) and diameter of the sheath influence response time. I went with non-grounded (a requirement of the amplifier) and a 1/4" diameter to match the tubing size. I should have picked something much smaller, like 1/16" and used a reducer. 

Feed line temperature is a nice to have for calculating mass flow and if the response time becomes an issue I can spend the $120 on a new setup. I could also cold flow the propellants individually to get the temperature in each line.
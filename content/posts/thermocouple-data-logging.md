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
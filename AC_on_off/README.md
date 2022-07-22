# **AC on/off notification**

**Introduction:**

As part of a study of the effect of green walls on interior spaces, our air conditioners in the laboratory are constantly on at 25 degrees Celsius.
But there are times when the air conditioners stop working. The AC status should be documented, since it affects the activity of the plants, and other results, etc.
We wrote a code that saves an image from a USB camera that sees the air conditioners and is connected to our server. The code identifies according to the vents of the air conditioner whether it is open or closed, that is, on or off. Accordingly, the status of the air conditioner is recorded with the exact time in a database, an updated graph is created, and a notification email is sent if there has been a change since the last check.

The image is processed by counting the number of black pixels, and comparing the ranges corresponding to the status of the air conditioner: on/off. Currently, the model works during the hours when there is lighting in the laboratory (natural or artificial).

To continue - inserting the images that are saved throughout the day into a machine learning model, in order to get predictions about an open/closed air conditioner under different lighting conditions.

You are welcome to take a look and use code parts if relevant to you!

Link to Colab Notebook: https://tinyurl.com/AC-ON-OFF-HUJI

**Pipeline:**

1. Capture image from webcam.
2. Cut polygon of vents area, and see if open or close.
3. Append status+timestamp to csv file.
4. CSV to df, and create plotly graph.
5. Send email with smtp.


**By:** Yedidya Harris, Yehuda Yungstein

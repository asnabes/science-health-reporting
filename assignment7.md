# <div align="center">Assignment 7</div>
1. I would use the line geom to draw a line chart, the boxplot geom to make a boxplot, the histogram geom to make a histogram and the area geom to make an area chart.
2. I predict the output will be a graph with a scatterplot and a smooth line. “displ” be on the x-axis and “hwy” will be on the y-axis. The points in the scatterplot will have different colors that correspond to the vehicle’s drive train. The smooth line will contain different colors that correspond to the drive train of the data points on which that part of the line is based.<br /> 
I was right about the scatter plot, but wrong about the smooth lines. There are three different smooth lines, which correspond to the three different drive trains. Each of the smooth lines has a different color. 
3. The show.legend = FALSE does not seem to do anything. When you remove it, nothing happens. I think the author used show.legend = FALSE earlier in the chapter to remove the legend for the three different smooth lines in a graph. 
4. se = FALSE removes the grey area surrounding the smooth lines. Perhaps the grey area is showing uncertainty, as Sean McMinn said the area surrounding the line on a coronavirus graph showed uncertainty.
5. The two graphs will look the same, because setting the same x and y axis for the point geom and the smooth geom is the same as setting the x and y axis in the ggplot() function.<br />
6. Graph 1 code:<br />
ggplot(data = mpg, mapping = aes(x = displ, y = hwy)) + <br/>
  geom_point(size = 4) + <br />
  geom_smooth(se = FALSE, size=2) <br />
Graph 2 code:<br />
ggplot(data = mpg, mapping = aes(x = displ, y = hwy)) + <br />
  geom_point(size = 4) + <br />
  geom_smooth(se = FALSE, size=2, mapping = aes(group = drv))<br />
Graph 3 code:<br />
ggplot(data = mpg, mapping = aes(x = displ, y = hwy, color = drv)) +<br />
  geom_point(size = 4) +<br />
  geom_smooth(se = FALSE, size=2)<br />
Graph 4 code:<br />
ggplot(data = mpg, mapping = aes(x = displ, y = hwy)) +<br />
  geom_point(size = 4, mapping = aes(color = drv)) +<br />
  geom_smooth(se = FALSE, size=2)<br />
Graph 5 code:<br />
ggplot(data = mpg, mapping = aes(x = displ, y = hwy)) +<br />
  geom_point(size = 4, mapping = aes(color = drv)) +<br />
  geom_smooth(se = FALSE, size=2, mapping = aes(linetype = drv))<br />
Graph 6 code:<br />
ggplot(data = mpg, mapping = aes(x = displ, y = hwy)) +<br />
  geom_point(shape = 1, size= 4, color = "white", stroke=5) +<br />
  geom_point(size = 4, mapping = aes(color = drv))

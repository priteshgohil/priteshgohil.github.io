# Pritesh Gohil

1. [Finding and installing missing packages in LaTeX in Ubuntu](latex.md)
2. [Mathematics for robotics and control important links](mrc.md)
3. [How to write markdown file](https://guides.github.com/features/mastering-markdown) 
4. [New to computer science? Explore the options here](https://www.javatpoint.com/)
5. [Jupyter kernal is not strating after installing the anaconda in Ubuntu 16.04](jupyter.md)
6. [An introduction to Anaconda: what is it, and how to install it in ubuntu](https://medium.freecodecamp.org/how-to-install-anaconda-on-ubuntu-16-04-64-bit-6f1c4675ce44)
7. [Resolve conflict between ROS  python2.x and OpenCv python3.x](opencvVsRos.md)
8. [Computer vision techniques that you might need to work with vision](https://heartbeat.fritz.ai/the-5-computer-vision-techniques-that-will-change-how-you-see-the-world-1ee19334354b)
9. [Books that I read other than educational](books.md)
10. [Free image and video editing online tools](tools.md)
11. [Evaluation Metrics for 2D Object Detection](EvalMetric.md)

# Finding specific string and folder in linux
Find folder or file name: case sensitibe `find . -name "folder name"` & case insensitive `find . -iname "folder name"`<br>
Find file containing specific string: `grep -Ril "text-to-find-here" /` Use '/' to search from root, or '.' to search from current directory <br>

# Linux development Environment of 2018 by Bruno Paz
New to the ubuntu or still looking for some of the best tools to let your work done? Have a quick look at here save tons of time in finding right tools [Check his article here](https://dev.to/brpaz/my-linux-development-environment-of-2018-ch7)

# Convert colour image to gray in linux
This is simple command line argument to convert image into grayscale. <br>
`convert -colorspace gray relu.png relu_BW.png` <br>

# Get selected pages from pdf
First install pdftk software
`sudo apt install pdftk` <br>
To create pdf from pages 5 to 20 from report.pdf `pdftk report.pdf cat 5-20 output Review_pages.pdf` <br>
To create pdf from page (5, 10, 15-20) from report.pdf `pdftk report.pdf cat 5 10 15-20 output Review_pages.pdf`

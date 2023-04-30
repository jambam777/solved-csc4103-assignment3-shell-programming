Download Link: https://assignmentchef.com/product/solved-csc4103-assignment3-shell-programming
<br>
To learn the use of Bash shell programming.

Background

The shell scripting is a powerful tool to execute a batch of Unix commands for completing a complicated task. In the class, we have learned the basics of Bash Shell programming. This project is a programming practice to use shell for a simple file processing.

<h1>Programming Task</h1>

Download the tar ball at the link <u>http://www.csc.lsu.edu/~fchen/class/csc4103-sp19/</u> <u>assignments/lfw.tgz</u>, which is a subset of an image database from UMass [1]. Download and untar the package, which creates a directory. This directory contains a set of subdirectories, each of which contains one or more images. This directory of files will be used as your test input. You need to write a shell script (batch_tar.sh) to process the files by the guideline below.




<ol>

 <li>Your script should provide help information. Typing command “%./batch_tar.sh help” should print help info to explain how to use the script.</li>

</ol>




<ol start="2">

 <li>The shell script sh should accept two parameters to allow users to specify the input directory of the files and the output directory. An example command:</li>

</ol>




%./batch_tar.sh &lt;input_dir&gt; &lt;output_dir&gt;







<ol start="3">

 <li>The output directory should be created by your script and should have the <strong>same</strong> directory structure as the input directory.</li>

</ol>




<ol start="4">

 <li>For each file in the input directory, the script should produce a compressed tar file with proper naming in the corresponding output path. For example, for image jpg should be named as foo.tgz. The file should be placed in <u>the same subdirectory </u>in the output directory, just like the original image.</li>

</ol>

For example, if the original file is input_dir/foo/test.jpg, the output file should be output_dir/foo/test.tgz.




<ol start="5">

 <li>After a file has been processed, print a line of processing info to show (1) the name of the original file, (2) the size of the original file, (3) the name of the tar file, (4) the size of the tar file.</li>

</ol>




<ol start="6">

 <li>After all images have been processed, print summary info to show (1) the total number of original files being processed, (2) the total size of original files, (3) the total number of the tar files, and (4) the total size of the tar files.</li>

</ol>




<ol start="7">

 <li>Your script <strong>must</strong> use <u>functions</u> to organize your code.</li>

</ol>







<h1>Additional Hints</h1>

<ul>

 <li>Use the following command to download and unzip the tar ball.</li>

</ul>

$ wget <u>http://www.csc.lsu.edu/~fchen/class/csc4103-sp19/assignments/lfw.tgz</u>

$ tar -zxvf lfw.tgz




<ul>

 <li>Use the following command to compress a file to a tar ball.</li>

</ul>

$ tar –zcvf &lt;tar file&gt; &lt;original file&gt;

For example, we can use the command “$ tar –zcvf foo.tgz foo.jpg” to compress the file foo.jpg.




<ul>

 <li>Use the following command to extract the first half of the file name.</li>

</ul>

$ echo &lt;file name&gt; | cut -d ‘.’ -f 1

For example, the command “% echo foo.jpg | cut -d ‘.’ -f 1” will output foo.




<ul>

 <li>Use the following command to get the file size in bytes.</li>

</ul>

$ wc -c  &lt;file name&gt; | awk ‘{print $1;}’

<ul>

 <li>Use man to get extra help info about the commands.</li>

</ul>

<strong> </strong>
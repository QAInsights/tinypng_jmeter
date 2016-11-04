# TinyPNG JMeter Tool
JMeter tool to automate image compression

# How to use this tool?


You can download my tool from this link. Before you execute the JMeter file, click on Beanshell Sampler and change the folder path in line 1 as shown below.


File folder = new File("C://folderpath//yourimages");
File[] files = folder.listFiles();
int counter = 1;
for (File file : files) {
    vars.put("file_" + counter, file.getAbsolutePath());
    counter++;
}


Now open the HTTP Header Manager item and add the following header.


Header Name		:	Authorization
Header Value		:	Basic tinypng api key

That is it. You are good to run the JMeter file. Once the execution is completed, you can see the compressed images in the JMETER\bin\ folder. 

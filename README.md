# timejson

Just GNU `time` wrapped in a JSON format.

## Usage

`./timejson [output_filename] [command]`

## Requirements

- GNU Time. Not installed by default on some Ubuntu servers!

## Why?

A lot of benchmarking tools exists. They focus mostly on micro-benchmarking. Performing a lot of requests,
running a function a lot of times and take the mean or median of the recorded execution times. However, not all performance
measurements require a lot of executions. Sometimes you just want to measure the time it takes for a particular big user story
without caring a lot about the accuracy. You just want to know whether it degrades or improves over time. As long as the time differences aren't too big and execution circumstances are more or less the same, the variance shouldn't be too big.

An added advantage of using GNU Time for measuring user stories is that you also get useful statistics about the maximum memory usage
of your program, in this case in the `average_resident_set_kb` key in the JSON. It can therefore be used as well for determining how much memory your application will require to function properly.

# Excercise1 - Downloading Files

The first exercise tests your ability to download a number of files from an HTTP source and unzip them, storing them locally with Python

## Problems Statement

You need to download 10 files that are sitting at the following specified
`HTTP` urls. You will use the `Python` package `requests` to do this
work.

You will need to pull the filename from the download uri.

The files are `zip` files that will also need to be unzipped into
their `csv` format.

They should be downloaded into a folder called `downloads` which
does not exist currently inside the `Exercise-1` folder. You should
use `Python` to create the directory, do not do it manually.

### Generally, your script should do the following

1. create the directory `downloads` if it doesn't exist
2. download the files one by one.
3. split out the filename from the uri, so the file keeps its
   original filename.

4. Each file is a `zip`, extract the `csv` from the `zip` and delete
the `zip` file.
5. For extra credit, download the files in an `async` manner using the
   `Python` package `aiohttp`. Also try using `ThreadPoolExecutor` in
   `Python` to download the files. Also write unit tests to improve your skills.

### Project WorkFlow

To challenge myself, and see which method is faster, i broke down this project into Four Section

1. Using average *`For-loop`* to download the files -> [Find Code Here](ForLoopScript.py)
2. Using *`Request Streaming mode`* and the concept of *`resumable download`* if any interruption occurs -> [Find Code Here](RequestStreaming.py)
3. Using *`ThreadPoolExecutor`* to download the files concurrently
4. Using *`async`* to download the files parallelism

### Using For-Loop

- In order to create the directories and work with files and system operations, I used the *`OS Libary`*
- Picked up the *`Zipfile Libary`* to extract and work with Zipfiles
- Made provision for *`Try&Except`* just incase not all urls are valid - which i was right
- Employed *`tqdm Libary`* for progression bar - To monitor the progress of the download
- Employed adequate logging by printing out each section of a process *`Extracting & Deleting Zip File`, `Downloading`, `Downloaded file`* and so on.
- logged the *`Elapsed time`* the script ran for - **`3 minutes  59.22 seconds`** **`Roughly 4 Minutes`**

!['Elapsed Time Using For-Loop'](./img/ForLoopElapsedTime.PNG)

### Using Streaming Mode + Resumable Download

> **Streaming** in the context of `requests.get` refers to the ability to retrieve content from a remote server incrementally,  rather than loading the entire response content into memory all at once. Streaming can be useful when dealing with large files or when you want to process the response content piece by piece without loading everything into memory.

- Made provision to *Resume Download* and not start from scratch incase any interruption occurs
- Employed the *Streaming feature* of `request.get` to load and process the content in chunks instead of loading them all at once to memory
- Employed `Os, tqdm, zipfile, try&except` like i did in the `For-Loop` use case

### Using ThreadPoolExecutor

Coming Sooon...
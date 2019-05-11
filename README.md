# Course Boilerplate

The objective of this guide is to get you quickly started with creation of courses. You can clone/import this repository and can get quickly started with course creation.

# Getting Started

1. Every `course` needs to be created in the `courses` group or a group decided by the maintainer of the organization.

2. Every `course` needs have an `index.md` file which is considered to be the starting point of the course.

3. Every file containing content needs to be a Markdown File with `.md extension` and the following **front matter** at the top of the file.

    ```
    layout: main
    title: <Title of the page>
    previousLink: <Link of Prev Page>
    previousTitle: <Title of Prev Page>
    nextLink: <Link of Next Page>
    nextTitle: <Title of Next Page>
    ```
    **For Example:**

    ```
    layout: main
    title: Prerequisites
    previousLink: ./index
    previousTitle: Introduction to Kubernetes
    nextLink: ./02-client-tools
    nextTitle: Client Tools
    ```

    A sample could also be found in `index.md`

You can follow the cheatsheet at https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet

# Code:

    ```javascript
    var s = "JavaScript syntax highlighting";
    alert(s);
    ```
    
    ```python
    s = "Python syntax highlighting"
    print s
    ```


# Videos:
1. To add **Youtube** Video. Add the following html in your markdown file and **replace with appropriate youtube video url**.
   
        <div class="embed-responsive embed-responsive-16by9">
            <iframe 
                src="<YOUTUBE_VIDEO_URL>" 
                class="embed-responsive-item"
                frameborder="0" 
                allow="autoplay; encrypted-media" allowfullscreen>
            </iframe>
        </div>
    
2. To  add **AMS** video. 
   
    **For example**: 
    
        <video data-type="ams" data-src="<INSERT_YOUR_URL_HERE>" tabindex="0"></video>
        

# Table of Contents
Table of contents needs to be updated in `_data/toc.yml`. A sample of toc already exists there.
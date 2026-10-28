+++
title = "Academic Workshop Zola Theme"
+++

# Design

Welcome to the [Academic Workshop](https://github.com/aterenin/academic-workshop) Zola theme!
This theme is designed for hosting a scientific workshop or seminar series website.

## Features

* A customizable header, with support for a banner, icon, title text, subtitle, date, and link, all enabled via straightforward options in the config file.
* Components implementing various useful features:
    * Split the page into sections with a different background color.
    * Create a two-dimensional image grid, for instance for displaying a list of speakers, with support for 2x3, 2x4, and other layouts, as well as automatic image resizing for both 1x and retina 2x displays.
    * Create a list of previous seminars, complete with appropriate buttons and links.
    * Import and autogenerate tables from external data, including with buttons for links such as paper download URLs.
    * Create buttons pointing to other pages.
* Easily-customizable colors by overriding `main.scss`, including dark mode via CSS variables.
* Simple, straightforward, easy-to-use, and easy-to-extend programmatic interface.
* No JavaScript or CSS dependencies of any kind, built in a way that is [designed to last](https://jeffhuang.com/designed_to_last/), even as web and browser standards change.



{{ <new_block /> }}



# List of Speakers

{{ <grid
    text={[
        ["Speaker A","Institution A"], 
        ["Speaker B","Institution B"],
        ["Speaker C","Institution C"],
        ["Speaker D","Institution D"],
        ["Speaker E","Institution E"],
    ]}
    urls={[
        "https://aterenin.github.io/academic-workshop#speaker_a",
        "https://aterenin.github.io/academic-workshop#speaker_b",
        "https://aterenin.github.io/academic-workshop#speaker_c",
        "https://aterenin.github.io/academic-workshop#speaker_d",
        "https://aterenin.github.io/academic-workshop#speaker_e",
    ]}
    images={[
        "placeholder.svg",
        "placeholder.svg",
        "placeholder.svg",
        "placeholder.svg",
        "placeholder.svg",
    ]} /> }}



{{ <new_block /> }}



# List of Organizers

{{ <grid
    text={[
        "Organizer A",
        "Organizer B",
    ]}
    image_dir="organizers" /> }}


{{ <new_block /> }}



# Schedule

| Time             | Event            |
| ---------------- | ---------------- |
| 12:00pm - 1:00pm | Introduction and Opening Remarks: Speaker Name A     |
| 1:00pm - 2:00pm  | Speaker A        |
| 2:00pm - 3:00pm  | Speaker B        |
| 3:00pm - 4:00pm  | Discussion Panel |



{{ <new_block /> }}



# Accepted Papers

{{ <table
    data="papers.csv" 
    columns={["Title","Authors"]}
    button_names={["paper","poster"]} 
    button_data_columns={[3,4]} 
    button_output_columns={[1,1]} /> }}



{{ <new_block /> }}



# Upcoming Seminar

{{ <highlights section_name="seminars" /> }}



{{ <new_block /> }}



# List of Seminars

{{ <list section_name="seminars" /> }}

{{ <button name="All Seminars" url="seminars" /> }}
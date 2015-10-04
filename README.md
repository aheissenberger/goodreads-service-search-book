# goodreads service search book
Select a text in any Apple OX Application (e.g. Safari, Chrome) and search for this book on goodreads to add it to your library.

##Installation
* [download "Search with Goodreads"](https://github.com/aheissenberger/goodreads-service-search-book/blob/master/Search%20with%20Goodreads.zip?raw=true)
* open downloaded application "Search with Goodreads" and your system will ask you to install the service
![service installer dialog](https://github.com/aheissenberger/goodreads-service-search-book/blob/master/doc/img/service-installer-dialog.png)

##Instructions
* select the title, author or ISBN of the book in the app
* right-click on the selection
* choose menu item "Services -> Search with Goodreads"

![demo of how to use](https://github.com/aheissenberger/goodreads-service-search-book/blob/master/doc/img/service-demo.gif)

##Code
This is the code - to change (e.g. open with chrome) you only need to open the file with "automator" on OSX.

```applescript
on run {input, parameters}
  
  tell application "Safari"
    tell window 1
      set current tab to (make new tab with properties {URL:"https://www.goodreads.com/search?utf8=✓&query=" & input})
    end tell
  end tell
  
  return input
end run

```
## Memento
Memento is a little package to maintain the logs inside Emacs. It helps to reflect on details/thoughts of specific day, or where your life was a few months or (eventually) years ago. 

### Purpose 
I developed a useful habit to record details of my daily life, especially for memorable days or things that should not be forgotten. 
I used [OhLife](http://ohlife.com/index.php) earlier, but they shut their service down, and I do a lot of work in Emacs nowadays.
Continuing my logs inside Emacs seems logical for me.

I noticed that there are some Emacs packages that could be used to do so. But I didn't found any that suits my needs. I need a log which is easy to use and maintain without any dependencies (like org-mode). So Memento is quickly created and used without any fuss. 

To share it, the name is derived from [the movie Memento](http://www.imdb.com/title/tt0209144/), where the actor writes personal notes of every day. It's publiced in the hope that it will be useful for anyone. Feel free to use it or modify it to your needs. 


### Installation
If you don't have a preferred installation method, I recommend installing with package.el and MELPA. 

    M-x package-install RET memento

### Usage 
When you exit Emacs, Memento checks once if you didn't have any journal for today, and the day is near its end in the evening. So it will not bother you in the middle of the day. Then Memento will ask if you want to log your day. You write your thoughts/activities down in the minibuffer and <kbd>RET</kbd>. Emacs exits and the journals are archived. Memento will not ask again on the same day. 

It will only occur when you exit Emacs. If you prefer to use Memento manually with `M-x memento`, you can disable Memento when Emacs exits:

    (setq memento-on-exit 'nil)

You can customize the date and time formats using the variable `memento-date-format`. The journals can be viewed with `M-x memento-open-log`. 

By default the journals are stored in `daily-logs`,  located in your home folder. You may also want to specify the directory/file where your journals will be saved:

    (setq memento-file "path to Memento file")

There is no need to create the file first.

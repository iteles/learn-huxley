#Using Huxley

###What it does
I'm a fan of CSS, I really enjoy coding it up. But once I've looked at the same design for long enough, I find I have to do quite a lot of squinting at the page and manually going through flows to be able to determine if it's all looking the way it should.

It's that situation where writing a line of code _here_ breaks the way something looks over _there_ that [Huxley](https://github.com/facebook/huxley) helps you test for in an automated way, without having to manually check every screen of the web app you're styling. Huxley lets you **test your UI for regressions (things that have changed from one iteration of your code to the next) in an automated way**.

>Huxley is a test-like system for catching visual regressions in Web applications.

###How it works in practice
It works by:
* Letting you **record** a user flow in your app - for example, clicking on the 'Contact Us' link in the app, filling in the form and pressing submit
  * As you do this, it records both your actions and screenshots of the screens you move through.
* Once you have moved onto the next iteration of your code, you should then run Huxley in **playback mode** and it will go through that same user flow by itself - clicking the 'Contact Us' link, filling in the form with the same details and pressing submit - and take screenshots again.
* It will then compare these screenshots to the original ones that were taken and show you the differences between the two.

This then allows you to quickly check whether there have been unintentional changes on both the page you were working on but more importantly, on ones you weren't.

##How to use [Huxley](https://github.com/facebook/huxley)

###Installation
Huxley is written in [Python](https://www.python.org/), so to install it, you'll need to install [pip](http://pip.readthedocs.org/en/latest/installing.html).
Pip is a package manager for software written in Python , in much the same way as [npm](https://www.npmjs.org/) is the package manager for [Node.js](http://nodejs.org/) modules.

####Installing pip
To install pip, you can [follow the instructions on the pip website]. For a Mac, these are:
1. Save the [get-pip.py](https://bootstrap.pypa.io/get-pip.py) file to your computer
2. Run the command `python get-pip.py` in your terminal (you should either be inside the folder with the `get-pip.py` file in it, or prefix the name of the file in the command with the path to the file - in my case this was `packages/get-pip.py`)

You should see this in your terminal:
![pip successfully installed](http://imgur.com/LAS9XTI)

I initially had some permissions issues so I ran `sudo python get-pip.py` to run the command as a superuser.

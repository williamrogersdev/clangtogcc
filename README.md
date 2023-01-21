<h1>How to switch from clang to g++ on mac M1 chip. <h1>


<p>On the mac the g++ compiler is disguised as clang. Here is a simple way to change it</p> 





Check to see if you have g++ installed by typing in the terminal:

g++ --version


If you have no made any changes it is most likely the clang version of C++


<ul>
<li>Install g++ through home-brew.</li>
<li>Check out the version you just installed, probably 12th or higher</li>
<li>You can make a symbolic link from g++-12 to g++ (this is for being able to call g++-12 with just typing g++). In order to do it, just type in your terminal sudo ln -s $(which g++-12) /usr/local/bin/g++.</li>

<p>sudo ln -s pathSource pathDestination creates a symbolic link from pathSource to pathDestination.

$(which g++-12) returns the path for the command g++-12, that in your case is /opt/homebrew/bin/g++-10. <br>
</p>

</ul>


<p>Now check your version again and you should see  g++ instead of clang </p>

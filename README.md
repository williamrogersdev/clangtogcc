# <h1>How to switch from clang to g++ on mac M1 and intel chip. <h1>


<p>On the mac the g++ compiler is disguised as clang. Here is a simple way to change it</p> 
  <br>





<p>Check to see if you have g++ installed by typing in the terminal: <br>

```
g++ --version
``` 
  <br>
 
If you have no made any changes it is most likely the clang version of g++
  </p>

  
  ## <h2> Steps to Switch from clang to g++ on mac </h2> <br>

<ul>
<li>Install g++ through [homebrew](https://brew.sh) or xcode.</li>
  <li>If Using homebrew type in the following to install:</li>
 
 ```
 brew install gcc
 ```

<li>Check out the version you just installed, probably 12th or higher</li>


```
g++ --version
``` 

<li>Now you need to make a symbolic link from g++-12 to g++ (this is for being able to call g++-12 with just typing g++). In order to do it, just type in your terminal:<br> </li>


  
 ```
sudo ln -s $(which g++-12) /usr/local/bin/g++
```
  <li><p>Now open a new terminal and check your version again and you should see  g++ instead of clang </p>
</li>

  
   <li><p>If that does not work try typing out the entire path where g++ is on your machine </p>
</li>
   

   ```
sudo ln -s /opt/homebrew/bin/g++-12 /usr/local/bin/
```

  
  
  <br>

</ul>
  
  
  <h3>Explanation</h3>
  
  
  <p> sudo ln -s pathSource pathDestination creates a symbolic link from pathSource to pathDestination.<br>

$(which g++-12) returns the path for the command g++-12</p>

<p>This works for gcc as well</p>




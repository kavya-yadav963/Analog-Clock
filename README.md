# Analog-Clock
Overview

This project is a simple web-based analog clock built using HTML, CSS, and JavaScript. The clock updates dynamically to show the current time using JavaScript rotations for the hour, minute, and second hands.

Features

* Displays an analog clock with a background image.

* The hour, minute, and second hands move in real-time.

* Uses setInterval to update the clock every second.

* Responsive design to adapt to different screen sizes.

Files Structure

/clock-project
│-- index.html     # Main HTML file </BR>
│-- style.css      # Styling for the clock</BR>
│-- code.js        # JavaScript logic for clock movement</BR>
│-- clock.png      # Clock background image</BR>

Installation and Usage
1. Clone the repository:
git clone https://github.com/kavya-yadav963/clock-project.git

2. Navigate to the project directory:
   cd clock-project

3. Open index.html in a browser.

 How It Works
 
* The index.html file creates the clock structure with div elements for the hour, minute, and second hands.

* The style.css file positions the clock hands and sets up the background image.

* The code.js file uses JavaScript to calculate the current time and rotate the clock hands accordingly.

       * setInterval updates the clock every second.

       * Rotations are calculated based on the current hour, minute, and second values.
Code Breakdown 

  JavaScript (code.js)
  
  setInterval(() => { </BR>
    d = new Date();</BR>
    htime = d.getHours();</BR>
    mtime = d.getMinutes();</BR>
    stime = d.getSeconds();</BR>
    hrotation = 30 * htime + mtime / 2;</BR>
    mrotation = 6 * mtime;</BR>
    srotation = 6 * stime;</BR>
    hour.style.transform = `rotate(${hrotation}deg)`;</BR>
    mintues.style.transform = `rotate(${mrotation}deg)`;</BR>
    second.style.transform = `rotate(${srotation}deg)`;</BR>
}, 1000);</BR>

  CSS (style.css)
  
    #clockContainer {
    position: relative;
    margin: auto;
    border: 2px solid;
    height: 40vw;
    width: 40vw;
    background: url(clock.png) no-repeat;
    background-size: 100%;
}


Future Improvements

* Add smooth transitions to the clock hands.

* Implement a digital clock alongside the analog clock.

* Add customization options for themes and colors.

License

This project is open-source and available under the MIT License.

  
  
  


   

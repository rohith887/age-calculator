# age-calculator
In Age Calculator your date of birth and other features display the number of days till your next birthday.

JavaScript was employed to build this Age Calculator project.
JavaScript offers some built-in date and time functions, which help to calculate the age from the date (Date of Birth). Using these JavaScript methods, you can easily find the age of anyone. For this, we require a date input from the user and the current system date. 

```
<body>
    <div class="container">
        <form>
            <div class="base">
                <div class="enter"><h4>Age Calculator</h4></div>
                <div class="block">
                    <p class="title">Date</p>
                    <input
                        type="text"
                        name="date"
                        id="date"
                        placeholder="dd"
                        required="required"
                        minlength="1"
                        maxlength="2"
                    />
                </div>
                <div class="block">
                    <p class="title">Month</p>
                    <input
                        type="text"
                        name="month"
                        id="month"
                        placeholder="mm"
                        required="required"
                        minlength="1"
                        maxlength="2"
                    />
                </div>
                <div class="block">
                    <p class="title">Year</p>
                    <input
                        type="text"
                        name="year"
                        id="year"
                        placeholder="yyyy"
                        required="required"
                        minlength="4"
                        maxlength="4"
                    />
                </div>
            </div>
            <div class="base">
                <div class="enter">
                    <input
                        type="button"
                        name="submit"
                        value="Submit"
                        onclick="age()"
                    />
                </div>
            </div>
            <div id="age"></div>
        </form>
    </div>
</body>
```
 ### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Media Queries
- Javascript

 
 I used HTML concepts to build the basic structure for our age calculator website, but first I must add some file links to our html file. Making distinct files for each language and linking them together inside our website is the simplest way to handle a project, which is crucial when developing one. Here, inside the head section of our HTML, I placed the links for our external CSS file, and the link for our javascript file. Before the body tag is finished, I additionally included links to those files.
 
 ### Adding the Structure for our age calculator:

  -First I created a div container that will contain our calculator 
   structure.
  -We will now add the heading to our age calculator using H3 tags.
  -Now I  made a div with the label “select our date of birth” and input 
   of type “birth” for selecting the date from a calendar.
  -I displayed the current date using the same method input type=”date,” 
   and I disabled the property that allows us to change the current date.
  -I create a button with the button tag and add the onClick function to 
    it.
  Take a look at the HTML structure without any styling
![html](https://github.com/rohith887/age-calculator/assets/94122677/94eb8b9c-1fed-4f82-b175-9bf126a99527)


### CSS CODE
```
body {
    font-family: Arial, Helvetica, sans-serif;
    background-color: #2782e3;
    font-size: 15px;
    line-height: 1.5;
    padding: 0;
    margin: 0;
}
* {
    box-sizing: border-box;
}
.container {
    width: 520px;
    height: auto;
    margin: 100px auto;
    background-color: #eee;
    border-radius: 25px;
}
.base {
    width: 100%;
    margin: 0;
    overflow: hidden;
    display: block;
    float: none;
}
.block {
    width: 135px;
    padding: 5px 20px;
    margin-left: 20px;
    display: inline-block;
    float: left;
}
.base h4 {
    font-size: 26px;
    text-align: center;
    font-family: sans-serif;
    font-weight: normal;
    margin-top: 0px;
    box-shadow: 0px 2px #bababa;
    background: white;
    font-size: 34px;
    color: navy;
}
.title {
    font-size: 20px;
    text-align: left;
    font-family: sans-serif;
    font-weight: normal;
    line-height: 0.5;
    letter-spacing: 0.5px;
    word-spacing: 2.7px;
    color: #1073d0;
}
input[type="text"] {
    width: 140px;
    margin: auto;
    outline: none;
    min-height: 50px;
    border: 2px solid #1073d0;
    padding: 12px;
    background-color: #f7f7f7;
    border-radius: 2px;
    color: #1073d0;
    font-size: 17px;
}
input[type="text"]:focus {
    background-color: #ffffff;
    border: 2px solid orange;
    outline: none;
}
input[type="button"] {
    width: 150px;
    margin-left: 35%;
    margin-top: 40px;
    outline: none;
    border: none;
    border-radius: 2px;
    background-color: #0761b6;
    color: #ffffff;
    padding: 14px 16px;
    text-align: center;
    font-size: 16px;
}
input[type="button"]:hover {
    background-color: #003669;
}
#age {
    display: block;
    margin: 10px;
    margin-top: 35px;
    padding: 10px;
    padding-bottom: 20px;
    overflow: hidden;
    font-family: verdana;
    font-size: 23px;
    font-weight: normal;
    line-height: 1.5;
    word-spacing: 2.7px;
    color: navy;
}
```
Now add javascript for the age calculator. I created function age and get all html elements in javascript so we get what the user enters in input. After that, I defineD a new code that gets today’s date, month, and year so that when a user enters an age javascript can do calculations of 2 values and show output in the age calculator.
JAVASCRIPT CODE
```
function age() {
    var d1 = document.getElementById("date").value;
    var m1 = document.getElementById("month").value;
    var y1 = document.getElementById("year").value;
    var date = new Date();
    var d2 = date.getDate();
    var m2 = 1 + date.getMonth();
    var y2 = date.getFullYear();
    var month = [31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31];
    if (d1 > d2) {
        d2 = d2 + month[m2 - 1];
        m2 = m2 - 1;
    }
    if (m1 > m2) {
        m2 = m2 + 12;
        y2 = y2 - 1;
    }
    var d = d2 - d1;
    var m = m2 - m1;
    var y = y2 - y1;
    document.getElementById("age").innerHTML =
        "Your Age is " + y + " Years " + m + " Months " + d + " Days";
}
```
Here is the final output after writing few lines of  java script code. 

![css](https://github.com/rohith887/age-calculator/assets/94122677/b0583e9e-bb13-44be-8516-d35fc2e059f3)






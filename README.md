# indeedscrape
Scrapes out the Job Description from a job you are currently looking at

Paste this in a bookmark: 

javascript:(function() {    var targetElement = document.querySelector('div.jobsearch-embeddedBody.css-1omm75o.eu4oa1w0');    if (targetElement) {        var textToCopy = targetElement.textContent;        var tempInput = document.createElement('textarea');        tempInput.style.position = 'fixed';        tempInput.style.opacity = 0;        tempInput.value = textToCopy;        document.body.appendChild(tempInput);        tempInput.select();        document.execCommand('copy');        document.body.removeChild(tempInput);        alert('Text copied!');    } else {        alert('Element not found!');    }})();

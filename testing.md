
# surfreport/{beachId}

Returns information about surfing conditions at a specific beach ID, including the surf height, water temperature, wind, and tide. Also provides an overall recommendation about whether to go surfing. 

## testing1234 Heading2

This is my numbered list: 

1. Number1 
2. Number2 
3. Number3 
4. Number4 

This is my bulleted list: 

* Bullet1 
* Bullet2 
* Bullet3 

This is my **boldfaced** word. 

This is my code sample with HTML highlighting: 

```html
<!DOCTYPE html>
<html>
<head>
<script src="http://code.jquery.com/jquery-2.1.1.min.js"></script>
  <meta charset="utf-8">
  <title>API Weather Query</title>
  <script>

  function getSurfReport() { 

// use AJAX to avoid CORS restrictions in API calls.
 var output = $.ajax({
    url: 'https://simple-weather.p.mashape.com/surfreport/123?units=imperial&days=1&time=1433772000', 
    type: 'GET', 
    data: {}, 
    dataType: 'json',
    success: function(data) {
        //Here we pull out the recommendation from the JSON object.
        //To see the whole object, you can output it to your browser console using console.log(data);
        document.getElementById("output").innerHTML = data.surfreport[0].monday.2pm.recommendation; 
        },
    error: function(err) { alert(err); },
    beforeSend: function(xhr) {
    xhr.setRequestHeader("X-Mashape-Authorization", "WOyzMuE8c9mshcofZaBke3kw7lMtp1HjVGAjsndqIPbU9n2eET"); // Enter here your Mashape key
    }
});
	
}
 
</script>
</head>
<body>
	
  <button onclick="getSurfReport()">See the surfing recommendation</button>
  <div id="output"></div>
  
</body>
</html>
```

This is my table: 

| TableColumn1 | Column2 | 
| ------------ | ------- | 
| ipsum | lassum | 
| lassa | ipsum | 

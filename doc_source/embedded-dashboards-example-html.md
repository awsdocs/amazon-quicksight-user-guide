# HTML Example of Embedding a Dashboard with Amazon QuickSight<a name="embedded-dashboards-example-html"></a>

The following example shows the html you can use to display an embedded dashboard\.

```
<!DOCTYPE html>
<html>

<head>
    <meta charset="UTF-8"> #Character encoding is required to display this page onto the browser. 
    <title>Basic Embed</title>
    <script type="text/javascript" src="https://public.end.point/embedded-dashboards-sdk.min.js"></script>
    <script type="text/javascript">
        function embedDashboard() {
            var containerDiv = document.getElementById("dashboardContainer");
            var params = {
                url: "https://us-east-1.quicksight.aws.amazon.com/sn/dashboards/1a1ac2b2-3fc3-4b44-5e5d-c6db6778df89",
                container: containerDiv,
                parameters: {
                    country: 'United States'
                },
                height: "700px",
                width: "1000px"
            };
            var dashboard = QuickSightEmbedding.embedDashboard(params);
            dashboard.on('error', function() {});
            dashboard.on('load', function() {});
            dashboard.setParameters({country: 'Canada'});
        }
    </script>

</head>

<body onload="embedDashboard()">
    <div id="dashboardContainer"></div>
</body>

</html>
```

**Topics**

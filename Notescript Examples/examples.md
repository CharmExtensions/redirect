# Webhooks
````
[note]
| [url]: "https://webhook.site/bc844274-fad8-4891-a9cb-24d5166c02e0"
| | (retrieve "url" put into "channel")  ^
channel id = "id" | url     =     "line 5, character 38"
````
# VPN Enabling
````
[note]
- available = not used | not used = (*not-available*)
[randomize] 15 + h263, 36gd + [alphabet] | only if: "available"
- then: say [h1] = your "password" is: + 15 + [custom]
````
# NoteScript Other-Languages
````
["language"]
code inside here
["language"]
````
# Camera Enabling
````
[camera] = |[html]
<!doctype html>
<html>
<head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, maximum-scale=1.0">
    <style>
        body {width: 100%;}
        canvas {display: none;}
    </style>
    <script>
        var video, canvas, msg;
        var load = function () {
            video  = document.getElementById('video');
            canvas = document.getElementById('canvas');
            msg    = document.getElementById('error');
            if( navigator.getUserMedia ) {
                video.onclick = function () {
                    var context = canvas.getContext("2d");
                    context.drawImage(video, 0, 0, 240, 320);
                    var image = {"demo" : {
                        "type"  : "device",
                        "image" : canvas.toDataURL("image/png")
                    }};
                };

                var success = function ( stream ) {
                    video.src = stream;
                };

                var error = function ( err ) {
                    msg.innerHTML = "Error: " + err.code;
                };

                navigator.getUserMedia('video', success, error);

            } else {
                msg.innerHTML = "Native web camera not supported :(";
            }

        };

        window.addEventListener('DOMContentLoaded', load, false);
    </script>
</head>
<body>
    <video  id="video" width="240" height="320" autoplay> </video>
    <p      id="error">Click on the video to send a snapshot to the receiving screen</p>
    <canvas id="canvas" width="240" height="320"> </canvas>
</body>
</html> [html]

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Flip Clock Example</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/flipclock/0.7.8/flipclock.css">
</head>
<body>
    <div class="clock"></div>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/flipclock/0.7.8/flipclock.min.js"></script>
    <script>
        // Initialize the clock
        var clock = new FlipClock(document.querySelector('.clock'), {
            clockFace: 'TwelveHourClock',
            autoStart: true,
            countdown: false
        });

        // Set initial time: 7:30 AM
        var currentTime = new Date();
        currentTime.setHours(7);
        currentTime.setMinutes(30);
        currentTime.setSeconds(0);
        currentTime.setMilliseconds(0);

        // Start from that time
        clock.setTime(currentTime.getHours() * 3600 + currentTime.getMinutes() * 60 + currentTime.getSeconds());
        clock.start();
    </script>
</body>
</html>
``

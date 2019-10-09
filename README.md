# hi-malvika
An afternoon project to replace a boring pdf cover letter


<!DOCTYPE html>
<html>
<head>
    <meta charset='utf-8' />
    <title></title>
    <meta name='viewport' content='initial-scale=1,maximum-scale=1,user-scalable=no' />
    <script src='https://api.tiles.mapbox.com/mapbox-gl-js/v0.44.1/mapbox-gl.js'></script>
    <link href='https://api.tiles.mapbox.com/mapbox-gl-js/v0.44.1/mapbox-gl.css' rel='stylesheet' />
    <style>
        body { margin:0; padding:25; }
        #map { position:absolute; top:0; bottom:0; width:100%; }
    </style>
</head>
<body>

<style>
#map {
    position: fixed;
    width:50%;
}
#features {
    width: 50%;
    margin-left: 50%;
    font-family: Tw Cen MT;
    overflow-y: scroll;
    background-color: #fafafa;
}
section {
    padding:  25px 50px;
    line-height: 25px;
    border-bottom: 1px solid #ddd;
    opacity: 0.25;
    font-size: 20px;
}
section.active {
    opacity: 1;
}
section:last-child {
    border-bottom: none;
    margin-bottom: 1000px;
}
</style>

<div id='map'></div>
<div id='features'>
    <section id='welcome' class='active'>
        <h3>Hey, there!</h3>
        <p>Welcome to the fun version of my resume! <br><br>🤖 I wanted to showcase a bit of myself in a non-stuffy way, and thought a map would be the best way to illustrate myself <br><br>Resumaps are designed to fill the gaps in your resume. If you want to stand out, a resumap is a fun way to help people get to know you. After all, wouldn't you want to know who you're hiring? So if you want see more, sit back, relax, and enjoy the flight 🚀</p>
    </section>
    <section id='section1' class='active'>
        <h3>Section 1</h3>
        <p>Here's where you can add a narrative to take your resume to the next level. Where did you come from? What really brought you there? What made you leave? This is to let people get a glimpse of who the person behind the paper is. This is New Mexico...but you can center your map however you want.
    </section>
    <section id='section2'>
        <h3>Section 2</h3>
        <p>As your readers scroll through these sections, your resumap will fly them to the locations you've specified. A sense of place is something that a lot of people resonate with. Where you were when you did what you did is half of the story.<br><br>Add some line breaks to start a new paragraph if you want to feel fancy.</p>
    </section>
    <section id='section3'>
        <h3>Section 3</h3>
        <p>You can add pictures! <br><br> <img src="https://i.imgur.com/NF8af.jpg"><br><br></p>
    </section>
    <section id='section4'>
        <h3>Section 4</h3>
        <p>Or even gifs! <br><br><iframe src="https://giphy.com/embed/fpXxIjftmkk9y" width="224" height="240" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p></p>
        </p>
    </section>
    <section id='section5'>
        <h3>Section 5</h3>
        <p>Or videos! WHAT!<br><br><iframe width="560" height="315" src="https://www.youtube.com/embed/le0BLAEO93g" frameborder="0" allow="autoplay; encrypted-media" allowfullscreen></iframe> </p>
    </section>
    <section id='section6'>
        <h3>Section 6</h3>
        <p>The most important thing is to tell <i>your</i> story. What makes you you?</p>
    </section>
    <section id='section7'>
        <h3>Time to make your own</h3>
        <p>Have fun!<br><br><iframe src="https://giphy.com/embed/lJNoBCvQYp7nq" width="300" height="300" frameBorder="0" class="giphy-embed" allowFullScreen></iframe><p></p></p>
    </section>
</div>
<script>
mapboxgl.accessToken = 'pk.eyJ1IjoibW5pZ2hvamthciIsImEiOiJjamd4dnF5N2IwYTA2MndyamV5NzVlanJmIn0.gSYfODHTINJ41FC_lylUxQ';
var map = new mapboxgl.Map({
    container: 'map',
    style: 'mapbox://styles/mapbox/outdoors-v10',
        bearing: -0,
        center: [21.277551, 22.152159],
        zoom: 1.03,
        speed: 0.8,
        pitch: 0
});
var chapters = {
    'welcome': {
        bearing: -0,
        center: [-108.866174, 49.272291],
        zoom: 2,
        speed: 0.8,
        pitch: 0
    },
    'section1': {
        bearing: 158.40,
        center: [73.851930, 18.493188],
        zoom: 11.39,
        pitch: 0
    },
    'section2': {
        center: [-98.881412, 46.071696],
        bearing: 158.40,
        zoom: 3.78,
        speed: 0.6,
        pitch: 44.50
    },
    'section3': {
        bearing: 70.40,
        center: [78.292840, 30.076842],
        zoom: 13.87,
        speed: 0.6,
        pitch: 23.00
    },
    'section4': {
        bearing: 60,
        center: [-134.408720, 58.300388],
        zoom: 16.57,
        speed: 0.6,
        pitch: 45
    },
    'section5': {
        bearing: 0.00,
        center: [-4.622577, 54.916666],
        zoom: 4.94,
        pitch: 0.00,
        speed: 0.6
    },
    'section6': {
        bearing: 0.00,
        center: [83.013094, 25.305890],
        zoom: 5.53,
        pitch: 0,
        speed: 0.6
    },
    'section7': {
        bearing: -0,
        center: [-1.844674, 50.724026],
        zoom: 12.22,
        speed: 2.5,
        pitch: 0
    },
    'section8': {
        bearing: -0,
        center: [116.401929, 39.907636],
        zoom: 13.78,
        speed: 2.5,
        pitch: 0
    },
    'section9': {
        bearing: -0,
        center: [100.289955, 5.329807],
        zoom: 8.85,
        speed: 2.5,
        pitch: 0
    },
    'section10': {
        bearing: -0,
        center: [-2.282713, 50.622936],
        zoom: 13.65,
        speed: 1.0,
        pitch: 0
    },
    'section11': {
        bearing: -0,
        center: [78.478833, 21.784582],
        zoom: 3.97,
        speed: 0.8,
        pitch: 2.50
    },
    'section12': {
        bearing: -0,
        center: [24.829579, 20.203693],
        zoom: 0.89,
        speed: 0.8,
        pitch: 2.50
    },
};
// On every scroll event, check which element is on screen
window.onscroll = function() {
    var chapterNames = Object.keys(chapters);
    for (var i = 0; i < chapterNames.length; i++) {
        var chapterName = chapterNames[i];
        if (isElementOnScreen(chapterName)) {
            setActiveChapter(chapterName);
            break;
        }
    }
};
var activeChapterName = 'baker';
function setActiveChapter(chapterName) {
    if (chapterName === activeChapterName) return;
    map.flyTo(chapters[chapterName]);
    document.getElementById(chapterName).setAttribute('class', 'active');
    document.getElementById(activeChapterName).setAttribute('class', '');
    activeChapterName = chapterName;
}
function isElementOnScreen(id) {
    var element = document.getElementById(id);
    var bounds = element.getBoundingClientRect();
    return bounds.top < window.innerHeight && bounds.bottom > 0;
}
</script>
</body>
</html>
view rawresumap.html hosted with ❤ by GitHub

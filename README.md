<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Parallax Website</title>
  <style>
    html, body {
      margin: 0;
      padding: 0;
      font-family: "Lato", sans-serif;
      font-size: 16px;
      line-height: 1.8em;
      color: #666;
      overflow-x: hidden;
    }

    .parallax {
      height: 100vh;
      background-attachment: scroll; /* no fixed */
      background-position: center;
      background-repeat: no-repeat;
      background-size: cover;
      transform: translateZ(0); /* force hardware acceleration */
    }

    .pimg1 {
      background-image: url(https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS84xrRdRJh0jRrzP6qtp3e2mZGTFOD9srNzw&s);
    }

    .pimg2 {
      background-image: url(https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRi4Gd3gW-AKWxxDfB0Wf1Ej_DdeBMRXJcC9A&s);
    }

    .pimg3 {
      background-image: url(https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSWxdxOOe-KGlg3bN3dfZ35BSyeJ6MRvvn58g&s);
    }

    .ptext {
      position: absolute;
      top: 50%;
      width: 100%;
      text-align: center;
      color: black;
      font-size: 27px;
      letter-spacing: 8px;
      text-transform: uppercase;
    }

    .textbg {
      background-color: #313534;
      color: #fff;
      padding: 10px;
    }

    section {
      position: relative;
      padding: 50px 20px;
      text-align: center;
    }

    .section-light {
      background-color: #f4f4f4;
      color: #666;
    }

    .section-dark {
      background-color: #282e34;
      color: #ddd;
    }
  </style>
</head>
<body>

  <div class="parallax pimg1">
    <div class="ptext">
      <span class="textbg">kohli in t20</span>
    </div>
  </div>

  <section class="section section-dark">
    <h2>achievements</h2>
    <p>He became the first Asian batter to score 100 half-centuries</p>
    <p> First Indian to Score 13,000 T20 Runs.</p>  
    <p>He has won seven awards, more than any other player.</p>
  </section>

  <div class="parallax pimg2">
    <div class="ptext">
      <span class="textbg">kohli in odi</span>
    </div>
  </div>

  <section class="section section-light">
    <h2>achievements</h2>
    <p>Kohli became the fastest player to reach 14,000 ODI runs.</p>
    <p>Kohli achieved 890 rating points in the ICC ODI rankings, the highest for any Indian player.</p>  
    <p>In 2017, he scored 1,460 runs, the highest by any captain in a calendar year.</p>
    <p>First Player to Score 50 ODI Centuries.</p>  
  </section>

  <div class="parallax pimg3">
    <div class="ptext">
      <span class="textbg">kohli in test</span>
    </div>
  </div>

  <section class="section section-dark">
    <h2>achievements</h2>
    <p>Fastest to 25 Test Centuries.</p>
    <p>He holds the record for the most Test double centuries by an Indian batter.</p>
    <p>Kohli achieved 922 rating points, the highest for any Indian player.</p>
    <p>First Indian Captain to Score 1,000+ Runs in Three Consecutive Years: He accomplished this feat in 2017, 2018, and 2019.</p>
  </section>

  <script>
    const scrollSpeed = 50;       // pixels per second
    const step = scrollSpeed / 30;    // pixels per frame at ~60fps

    function scrollSmoothly() {
      if (window.scrollY + window.innerHeight < document.body.scrollHeight) {
        window.scrollBy(0, step);
        requestAnimationFrame(scrollSmoothly);
      }
    }

    window.onload = () => {
      requestAnimationFrame(scrollSmoothly);
    };
  </script>

</body>
</html>

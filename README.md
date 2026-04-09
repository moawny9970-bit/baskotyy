<!-- الصفحة 1 -->
<div class="page show" id="page1">
  <div class="envelope">
    <h2>اكتبي الباسورد ✉️</h2>
    <input type="password" id="pass">
    <button onclick="checkPass()">فتح</button>
  </div>
</div>

<script>
function checkPass(){
  let p=document.getElementById("pass").value;
  if(p==="29/11/2008"){
    nextPage(2);
  }else{
    alert("الباسورد غلط");
  }
}
</script>

<!-- الصفحة 2 -->
<div class="page" id="page2">
  <div class="message-box">
شهد الحلوة ❤️  

الموقع ده معمول علشان يفضل ذكرى لينا احنا الاتنين…  
من أول يوم اتعرفنا فيه يوم **30 / 6 / 2023**  
والدنيا بقت أحلى بوجودك فيها.  

كل خروجة خرجناها…  
كل ضحكة…  
كل هزار بينا…  
كل لحظة كنتي فيها جنبي  
فضلت محفورة جوايا.  

انتي مش بس حد في حياتي…  
انتي حتة من يومي…  
من مزاجي…  
من ضحكتي.  

وأنا مبسوط إن كل الحاجات الحلوة دي كانت معاكي انتي بالذات.  

الموقع ده معمول علشان كل ما تفتحيه  
تفتكري إن في حد فرحان بوجودك في حياته  
وإن الذكريات اللي بينا  
غالية عندي جدًا.  

<button onclick="nextPage(3)">التالي</button>
  </div>
</div>

<!-- الصفحة 3: الصور والفيديو -->
<div class="page" id="page3">
  <audio autoplay controls loop>
    <source src="song.mp3">
  </audio>

  <div class="slideshow">
    <img src="new_image1.jpg">
    <img src="new_image2.jpg">
    <img src="new_image3.jpg">
    <img src="new_image4.jpg">
    <img src="new_image5.jpg">
    <img src="new_image6.jpg">
    <img src="new_image7.jpg">
    <img src="new_image8.jpg">
    <img src="new_image9.jpg">
    <img src="new_image10.jpg">
  </div>

  <div class="video-box">
    <video width="100%" controls>
      <source src="new_video.mp4">
    </video>
  </div>

  <button onclick="nextPage(4)">التالي</button>
</div>

<!-- الصفحة 4: العداد -->
<div class="page" id="page4">
  <h2>الوقت اللي قضيناه مع بعض ⏳</h2>
  <div class="timer">
    <div class="time-box">
      <span id="days">0</span>
      <div class="label">يوم</div>
    </div>
    <div class="time-box">
      <span id="hours">0</span>
      <div class="label">ساعة</div>
    </div>
    <div class="time-box">
      <span id="minutes">0</span>
      <div class="label">دقيقة</div>
    </div>
    <div class="time-box">
      <span id="seconds">0</span>
      <div class="label">ثانية</div>
    </div>
  </div>
</div>

<script>
let startDate=new Date("June 30, 2023 00:00:00"); // نفس تاريخ البداية
setInterval(()=>{
  let now=new Date();
  let diff=now-startDate;
  let days=Math.floor(diff/(1000*60*60*24));
  let hours=Math.floor((diff%(1000*60*60*24))/(1000*60*60));
  let minutes=Math.floor((diff%(1000*60*60))/(1000*60));
  let seconds=Math.floor((diff%(1000*60))/1000);
  document.getElementById("days").innerText=days;
  document.getElementById("hours").innerText=hours;
  document.getElementById("minutes").innerText=minutes;
  document.getElementById("seconds").innerText=seconds;
},1000);

function nextPage(n){
  document.querySelectorAll(".page").forEach(p=>p.classList.remove("show"));
  document.getElementById("page"+n).classList.add("show");
}
</script>

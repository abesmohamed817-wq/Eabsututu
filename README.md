<audio id="music" loop>
  <source src="song.mp3" type="audio/mpeg">
</audio>

<script>
const audio = document.getElementById("music");

// محاولة التشغيل تلقائياً
audio.play().catch(() => {
  // لو المتصفح منع autoplay، يبدأ التشغيل بعد أول نقرة
  document.body.addEventListener("click", () => {
    audio.play();
  }, { once: true });
});
</script>

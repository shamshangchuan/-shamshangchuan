# NieR:Automata


<div class="free-slider">
  <div class="free-slide active">
    <img src="https://via.placeholder.com/1200x500?text=Slide+1">
  </div>
  <div class="free-slide">
    <img src="https://via.placeholder.com/1200x500?text=Slide+2">
  </div>
  <div class="free-slide">
    <img src="https://via.placeholder.com/1200x500?text=Slide+3">
  </div>

  <button class="free-prev">&#10094;</button>
  <button class="free-next">&#10095;</button>
</div>

<style>
.free-slider {
  position: relative;
  max-width: 100%;
  overflow: hidden;
}

.free-slide {
  display: none;
}

.free-slide.active {
  display: block;
}

.free-slide img {
  width: 100%;
  display: block;
}

.free-prev, .free-next {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  background: rgba(0,0,0,0.5);
  color: white;
  border: none;
  padding: 10px 15px;
  cursor: pointer;
  font-size: 20px;
}

.free-prev { left: 10px; }
.free-next { right: 10px; }
</style>

<script>
let freeSlides = document.querySelectorAll('.free-slide');
let freeCurrent = 0;

document.querySelector('.free-next').onclick = function() {
  freeSlides[freeCurrent].classList.remove('active');
  freeCurrent = (freeCurrent + 1) % freeSlides.length;
  freeSlides[freeCurrent].classList.add('active');
}

document.querySelector('.free-prev').onclick = function() {
  freeSlides[freeCurrent].classList.remove('active');
  freeCurrent = (freeCurrent - 1 + freeSlides.length) % freeSlides.length;
  freeSlides[freeCurrent].classList.add('active');
}
</script>

const images = document.querySelectorAll(".gallery img");
const lightbox = document.getElementById("lightbox");
const lightboxImg = document.getElementById("lightboxImg");
const closeBtn = document.getElementById("closeBtn");
const prevBtn = document.getElementById("prevBtn");
const nextBtn = document.getElementById("nextBtn");

let currentIndex = 0;

function showImage(index) {
  lightboxImg.src = images[index].src;
  lightbox.style.display = "flex";
  currentIndex = index;
}

images.forEach((img, index) => {
  img.addEventListener("click", () => showImage(index));
});

closeBtn.addEventListener("click", () => {
  lightbox.style.display = "none";
});

prevBtn.addEventListener("click", () => {
  currentIndex = (currentIndex - 1 + images.length) % images.length;
  showImage(currentIndex);
});

nextBtn.addEventListener("click", () => {
  currentIndex = (currentIndex + 1) % images.length;
  showImage(currentIndex);
});

window.addEventListener("click", (e) => {
  if (e.target === lightbox) {
    lightbox.style.display = "none";
  }
});

document.addEventListener("keydown", (e) => {
  if (lightbox.style.display === "flex") {
    if (e.key === "ArrowLeft") prevBtn.click();
    if (e.key === "ArrowRight") nextBtn.click();
    if (e.key === "Escape") closeBtn.click();
  }
});

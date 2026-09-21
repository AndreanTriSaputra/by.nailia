/**
 * ANIMATIONS.JS — by.nailia
 * ---------------------------
 * 1. Scroll reveal: elemen dengan class "reveal" muncul fade-up
 *    begitu masuk viewport (pakai Intersection Observer, ringan).
 * 2. Navbar dapet shadow halus begitu halaman di-scroll ke bawah.
 */

document.addEventListener("DOMContentLoaded", function () {
  // ---- Scroll reveal ----
  const revealEls = document.querySelectorAll(".reveal");

  const observer = new IntersectionObserver(
    function (entries) {
      entries.forEach(function (entry) {
        if (entry.isIntersecting) {
          entry.target.classList.add("visible");
          observer.unobserve(entry.target); // cukup animasi 1x
        }
      });
    },
    { threshold: 0.15 }
  );

  revealEls.forEach(function (el) {
    observer.observe(el);
  });

  // ---- Navbar shadow on scroll ----
  const navbar = document.querySelector(".navbar");

  window.addEventListener("scroll", function () {
    if (window.scrollY > 10) {
      navbar.classList.add("scrolled");
    } else {
      navbar.classList.remove("scrolled");
    }
  });
});

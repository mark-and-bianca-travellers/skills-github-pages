---
title: Welcome to our travel blog!
---
<p><strong><span id="countdown"></span></strong></p>

<script>
const departureDate = new Date('2026-03-01T10:00:00');
const now = new Date();
const timeDiff = departureDate - now;
const daysUntil = Math.ceil(timeDiff / (1000 * 60 * 60 * 24));

const countdownEl = document.getElementById('countdown');
if (daysUntil > 0) {
  countdownEl.textContent = daysUntil + ' days until we leave!';
} else if (daysUntil === 0) {
  countdownEl.textContent = 'We leave today!';
} else {
  countdownEl.textContent = 'We\'re traveling now!';
}
</script>

![plane flying between London and Bahamas]({{ "/assets/images/IMG_1587.png" | relative_url }})

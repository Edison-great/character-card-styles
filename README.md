<!--00-->
<style>
/* Custom Haunted Theme by Edison */
@import url('https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700;900&family=Courier+Prime:ital,wght@0,400;0,700;1,400&family=Spectral:ital,wght@0,400;1,400;1,600&display=swap');

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background: #0d0518;
  color: #c9b8d8;
  font-family: 'Spectral', serif;
  line-height: 1.8;
  overflow-x: hidden;
}

body::before {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: 
    radial-gradient(circle at 20% 50%, rgba(139, 71, 137, 0.15) 0%, transparent 50%),
    radial-gradient(circle at 80% 50%, rgba(75, 35, 100, 0.15) 0%, transparent 50%);
  animation: bgPulse 10s ease-in-out infinite;
  z-index: -2;
}

@keyframes bgPulse {
  0%, 100% { opacity: 0.3; }
  50% { opacity: 0.6; }
}

body::after {
  content: '';
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-image: 
    radial-gradient(2px 2px at 20% 30%, rgba(157, 95, 184, 0.3), transparent),
    radial-gradient(2px 2px at 60% 70%, rgba(139, 71, 137, 0.3), transparent),
    radial-gradient(1px 1px at 50% 50%, rgba(157, 95, 184, 0.2), transparent),
    radial-gradient(1px 1px at 80% 10%, rgba(139, 71, 137, 0.2), transparent);
  background-size: 200px 200px, 300px 300px, 250px 250px, 350px 350px;
  background-position: 0 0, 40px 60px, 130px 270px, 70px 100px;
  animation: particleFloat 20s linear infinite;
  z-index: -1;
}

@keyframes particleFloat {
  0% { transform: translateY(0); }
  100% { transform: translateY(-100px); }
}

.card-wrapper {
  max-width: 800px;
  margin: 80px auto;
  padding: 0 30px;
}

.name-section {
  text-align: center;
  margin-bottom: 60px;
  position: relative;
}

.character-name {
  font-family: 'Playfair Display', serif;
  font-size: 7em;
  font-weight: 900;
  color: #9d5fb8;
  text-transform: uppercase;
  letter-spacing: 12px;
  margin: 0;
  text-shadow: 
    0 0 40px rgba(157, 95, 184, 0.8),
    0 0 80px rgba(157, 95, 184, 0.4),
    0 5px 20px rgba(0, 0, 0, 0.8);
  animation: nameGlow 4s ease-in-out infinite;
  line-height: 1.1;
}

@keyframes nameGlow {
  0%, 100% { 
    text-shadow: 
      0 0 40px rgba(157, 95, 184, 0.8),
      0 0 80px rgba(157, 95, 184, 0.4),
      0 5px 20px rgba(0, 0, 0, 0.8);
  }
  50% { 
    text-shadow: 
      0 0 60px rgba(157, 95, 184, 1),
      0 0 120px rgba(157, 95, 184, 0.6),
      0 5px 20px rgba(0, 0, 0, 0.8);
  }
}

.character-subtitle {
  font-family: 'Spectral', serif;
  font-size: 1.8em;
  font-style: italic;
  color: #b8a0d4;
  margin-top: 20px;
  letter-spacing: 3px;
  font-weight: 400;
}

.background-section {
  width: 100%;
  height: 500px;
  margin: 50px 0;
  position: relative;
  border-radius: 0;
  overflow: hidden;
  box-shadow: 
    0 0 0 1px rgba(139, 71, 137, 0.3),
    0 30px 80px rgba(0, 0, 0, 0.9),
    inset 0 0 100px rgba(139, 71, 137, 0.1);
}

.bg-image {
  width: 100%;
  height: 100%;
  object-fit: cover;
  position: relative;
}

.bg-overlay {
  position: absolute;
  inset: 0;
  background: linear-gradient(to bottom, transparent 0%, rgba(13, 5, 24, 0.7) 100%);
}

.story-section {
  margin: 70px 0;
  padding: 60px 50px;
  background: 
    linear-gradient(135deg, rgba(30, 15, 45, 0.4) 0%, rgba(75, 35, 100, 0.2) 100%);
  border: 1px solid rgba(139, 71, 137, 0.4);
  position: relative;
  box-shadow: 
    0 20px 60px rgba(0, 0, 0, 0.6),
    inset 0 1px 0 rgba(157, 95, 184, 0.2);
}

.story-section::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  height: 1px;
  background: linear-gradient(90deg, transparent, #9d5fb8, transparent);
}

.story-section::after {
  content: '';
  position: absolute;
  bottom: 0;
  left: 0;
  right: 0;
  height: 1px;
  background: linear-gradient(90deg, transparent, #9d5fb8, transparent);
}

.story-text {
  font-family: 'Courier Prime', monospace;
  font-size: 1.15em;
  line-height: 2;
  color: #d4c5e8;
  text-align: left;
  letter-spacing: 0.5px;
  font-weight: 400;
}

.story-text::first-line {
  font-size: 1.3em;
  color: #9d5fb8;
  font-weight: 700;
}

.author-section {
  margin: 70px 0;
  padding: 50px;
  background: rgba(13, 5, 24, 0.8);
  border-left: 5px solid #8b4789;
  border-right: 5px solid #8b4789;
  position: relative;
}

.author-section::before,
.author-section::after {
  content: '◆';
  position: absolute;
  left: 50%;
  transform: translateX(-50%);
  font-size: 1.5em;
  color: #9d5fb8;
}

.author-section::before {
  top: -15px;
}

.author-section::after {
  bottom: -15px;
}

.author-title {
  font-family: 'Playfair Display', serif;
  font-size: 2.5em;
  color: #9d5fb8;
  text-align: center;
  margin-bottom: 30px;
  letter-spacing: 4px;
  font-weight: 700;
  text-transform: uppercase;
}

.author-note {
  font-family: 'Spectral', serif;
  font-size: 1.2em;
  line-height: 1.9;
  color: #b8a0d4;
  text-align: center;
  font-style: italic;
  font-weight: 600;
}

button,
.btn,
input[type="submit"],
input[type="button"],
.button {
  background: linear-gradient(135deg, #8b4789 0%, #6b2c64 100%) !important;
  border: 1px solid #9d5fb8 !important;
  color: #e8d5f5 !important;
  font-family: 'Spectral', serif !important;
  font-size: 1em !important;
  padding: 12px 30px !important;
  border-radius: 0 !important;
  cursor: pointer !important;
  transition: all 0.3s ease !important;
  text-transform: uppercase !important;
  letter-spacing: 2px !important;
  box-shadow: 0 5px 20px rgba(139, 71, 137, 0.3) !important;
}

button:hover,
.btn:hover,
input[type="submit"]:hover,
input[type="button"]:hover,
.button:hover {
  background: linear-gradient(135deg, #9d5fb8 0%, #8b4789 100%) !important;
  box-shadow: 0 8px 30px rgba(157, 95, 184, 0.5) !important;
  transform: translateY(-2px) !important;
}

input[type="text"],
input[type="email"],
textarea,
select {
  background: rgba(13, 5, 24, 0.9) !important;
  border: 1px solid #8b4789 !important;
  color: #d4c5e8 !important;
  font-family: 'Spectral', serif !important;
  padding: 12px !important;
  border-radius: 0 !important;
}

input[type="text"]:focus,
input[type="email"]:focus,
textarea:focus,
select:focus {
  border-color: #9d5fb8 !important;
  box-shadow: 0 0 20px rgba(157, 95, 184, 0.3) !important;
  outline: none !important;
}

::-webkit-scrollbar {
  width: 14px;
}

::-webkit-scrollbar-track {
  background: #0d0518;
}

::-webkit-scrollbar-thumb {
  background: linear-gradient(180deg, #8b4789, #6b2c64);
  border: 2px solid #0d0518;
}

::-webkit-scrollbar-thumb:hover {
  background: linear-gradient(180deg, #9d5fb8, #8b4789);
}

@media (max-width: 768px) {
  .character-name {
    font-size: 3.5em;
    letter-spacing: 6px;
  }
  
  .character-subtitle {
    font-size: 1.3em;
  }
  
  .background-section {
    height: 300px;
  }
  
  .story-section,
  .author-section {
    padding: 30px 25px;
  }
  
  .card-wrapper {
    padding: 0 20px;
    margin: 40px auto;
  }
}
</style>

<div class="card-wrapper">
  
  <!-- Name Section -->
  <div class="name-section">
    <h1 class="character-name">Maya Solis</h1>
    <p class="character-subtitle">19 Year Old Futanari</p>
  </div>
  
  <!-- Background Image -->
  <div class="background-section">
    <img src="https://archive.org/download/in-wall/customized-charsnapai%20%2815%29.png" alt="Maya" class="bg-image">
    <div class="bg-overlay"></div>
  </div>
  
  <!-- Story Section -->
  <div class="story-section">
    <div class="story-text">
On Halloween night, Maya and her friends explored a rumored abandoned haunted house. They laughed, took pictures, and left with the thrill of having braved it. Later that night, their group chat lit up — one friend had lost her necklace, a precious heirloom from her mother. Since Maya lived closest, she offered to go back and retrieve it. Her friends protested; it was too late, too eerie. But she insisted — it could be gone by morning. The house was colder when she returned. As soon as she stepped inside, the doors slammed shut behind her. Wind howled through the halls, carrying voices that screamed, "You dare return?" Her light flickered — and then she was still. The house had her.
    </div>
  </div>
  
  <!-- Author Note -->
  <div class="author-section">
    <h2 class="author-title">Author's Note</h2>
    <p class="author-note">
I love you guys
    </p>
  </div>
  
</div>
<!--00-->

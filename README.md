# KnowledgeHub

<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Get Your Wisdom</title>
  <script src="https://cdn.tailwindcss.com?plugins=forms,typography,aspect-ratio,line-clamp"></script>
  <style>
    html { scroll-behavior: smooth; }
  </style>
</head>
<body class="bg-gray-50 text-gray-800">

  <!-- Header -->
  <header class="bg-white shadow-md">
    <div class="container mx-auto px-6 py-4 flex justify-between items-center">
      <a href="#" class="text-2xl font-bold">Get Your Wisdom</a>
      <nav>
        <ul class="flex space-x-6">
          <li><a href="#" class="hover:text-blue-600">Home</a></li>
          <li><a href="#services" class="hover:text-blue-600">Services</a></li>
          <li><a href="#register" class="hover:text-blue-600">Register</a></li>
          <li><a href="#contact" class="hover:text-blue-600">Contact</a></li>
        </ul>
      </nav>
    </div>
  </header>

  <!-- Hero -->
  <section class="bg-blue-600 text-white py-20">
    <div class="container mx-auto px-6 text-center">
      <h1 class="text-4xl font-extrabold mb-4">Find the Best Tutors in Lucknow</h1>
      <p class="text-lg mb-8">Expert tuition for all grades & subjects, 1-on-1 or online.</p>
      <a href="#register" class="bg-white text-blue-600 px-8 py-3 font-semibold rounded">Register Now</a>
    </div>
  </section>

  <!-- Services -->
  <section id="services" class="py-16">
    <div class="container mx-auto px-6">
      <h2 class="text-3xl font-bold text-center mb-12">Our Services</h2>
      <div class="grid md:grid-cols-3 gap-8">
        <div class="bg-white p-6 rounded-lg shadow">
          <h3 class="text-xl font-semibold mb-2">1-on-1 Tuition</h3>
          <p>Personalized lessons tailored to your needs.</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow">
          <h3 class="text-xl font-semibold mb-2">Online Classes</h3>
          <p>Learn from home with experienced teachers.</p>
        </div>
        <div class="bg-white p-6 rounded-lg shadow">
          <h3 class="text-xl font-semibold mb-2">Exam Prep</h3>
          <p>Targeted support for board or competitive exams.</p>
        </div>
      </div>
    </div>
  </section>

  <!-- Register Section -->
  <section id="register" class="py-16 bg-gray-100">
    <div class="container mx-auto px-6 text-center">
      <h2 class="text-3xl font-bold mb-8">Register as</h2>
      <div class="flex flex-col md:flex-row justify-center gap-8">
        <button onclick="openModal('student')" class="bg-blue-600 text-white px-8 py-4 rounded shadow hover:bg-blue-700">I am a Student</button>
        <button onclick="openModal('tutor')" class="bg-green-600 text-white px-8 py-4 rounded shadow hover:bg-green-700">I am a Tutor</button>
      </div>
    </div>
  </section>

  <!-- Registration Modals -->
  <div id="modalOverlay" class="hidden fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center z-50">
    <div class="bg-white p-8 rounded-lg w-full max-w-md relative">
      <button onclick="closeModal()" class="absolute top-2 right-3 text-gray-500 text-xl">&times;</button>
      <h3 id="modalTitle" class="text-2xl font-bold mb-4"></h3>
      <form id="dynamicForm" method="POST" class="space-y-4">
        <input type="hidden" name="_subject" value="New Registration Submission" />
        <input type="text" name="Full Name" placeholder="Full Name" class="w-full border p-3 rounded" required>
        <input type="email" name="Email" placeholder="Email Address" class="w-full border p-3 rounded" required>
        <input type="tel" name="Phone" placeholder="Phone Number" class="w-full border p-3 rounded" required>
        <input type="text" name="Details" id="extraField" placeholder="" class="w-full border p-3 rounded" required>
        <button type="submit" class="w-full bg-blue-600 text-white py-3 rounded font-semibold">Register</button>
      </form>
    </div>
  </div>

  <!-- Contact Form -->
  <section id="contact" class="bg-gray-100 py-16">
    <div class="container mx-auto px-6 max-w-lg">
      <h2 class="text-3xl font-bold mb-6 text-center">Contact Us</h2>
      <form action="https://formspree.io/f/xrbleged" method="POST" class="space-y-4">
        <input type="hidden" name="_subject" value="Contact Form Submission" />
        <input type="text" name="Name" placeholder="Your Name" class="w-full border p-3 rounded" required />
        <input type="email" name="Email" placeholder="Your Email" class="w-full border p-3 rounded" required />
        <textarea name="Message" placeholder="How can we help?" class="w-full border p-3 rounded" required></textarea>
        <button class="w-full bg-blue-600 text-white py-3 rounded font-semibold">Submit</button>
      </form>
    </div>
  </section>

  <!-- Footer -->
  <footer class="bg-white py-6 text-center">
    <p>&copy; 2025 Your Website. All Rights Reserved.</p>
  </footer>

  <!-- Modal Script -->
  <script>
    document.addEventListener("DOMContentLoaded", function () {
      const modalOverlay = document.getElementById('modalOverlay');
      const modalTitle = document.getElementById('modalTitle');
      const extraField = document.getElementById('extraField');
      const dynamicForm = document.getElementById('dynamicForm');

      window.openModal = function(type) {
        modalOverlay.classList.remove('hidden');
        if (type === 'student') {
          modalTitle.innerText = 'Register as Student';
          extraField.placeholder = 'Class / Subjects Needed';
          dynamicForm.action = 'https://formspree.io/f/xrbleged';
        } else {
          modalTitle.innerText = 'Register as Tutor';
          extraField.placeholder = 'Subjects You Teach';
          dynamicForm.action = 'https://formspree.io/f/xgvzoekl';
        }
      }

      window.closeModal = function() {
        modalOverlay.classList.add('hidden');
      }
    });
  </script>
</body>
</html>

Jop application form
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Job Application Form</title>
  <!-- Tailwind CSS -->
  <script src="https://cdn.tailwindcss.com"></script>
  <!-- Google Fonts: Inter -->
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
  <style>
    body {
      font-family: 'Inter', sans-serif;
    }
  </style>
</head>
<body class="bg-slate-100 min-h-screen py-8 px-4 sm:px-6 lg:px-8 flex items-center justify-center">

  <!-- Main Container Card -->
  <div class="w-full max-w-2xl bg-white rounded-2xl shadow-xl border border-slate-100 overflow-hidden transition-all">
    
    <!-- Card Header / Gradient Banner -->
    <div class="bg-gradient-to-r from-blue-600 via-indigo-600 to-violet-600 p-6 sm:p-8 text-white relative">
      <div class="inline-flex items-center space-x-2 bg-white/20 backdrop-blur-md px-3 py-1 rounded-full text-xs font-medium mb-3">
        <svg class="w-4 h-4" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 13.255A23.931 23.931 0 0112 15c-3.183 0-6.22-.62-9-1.745M16 6V4a2 2 0 00-2-2h-4a2 2 0 00-2 2v2m4 6h.01M5 20h14a2 2 0 002-2V8a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path>
        </svg>
        <span>Careers at TechCorp</span>
      </div>
      <h1 class="text-2xl sm:text-3xl font-bold tracking-tight">Job Application Form</h1>
      <p class="text-blue-100 text-sm mt-1">Please fill out all the required information to apply for the position.</p>
    </div>

    <!-- Success Message Card (Hidden by default) -->
    <div id="successBanner" class="hidden m-6 p-5 rounded-xl bg-emerald-50 border border-emerald-200 text-emerald-900">
      <div class="flex items-start space-x-3">
        <svg class="w-6 h-6 text-emerald-600 flex-shrink-0 mt-0.5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m6 2a9 9 0 11-18 0 9 9 0 0118 0z"></path>
        </svg>
        <div>
          <h3 class="font-bold text-base">Application Submitted Successfully!</h3>
          <p class="text-sm text-emerald-700 mt-1">Thank you for applying. We have received your details and will review your application shorty.</p>
          
          <div id="summaryDetails" class="mt-4 pt-3 border-t border-emerald-200 text-xs text-emerald-800 space-y-1">
            <!-- Dynamic submission details injected here -->
          </div>
        </div>
      </div>
    </div>

    <!-- Job Application Form -->
    <form id="applicationForm" class="p-6 sm:p-8 space-y-6" action="#" method="POST" novalidate>
      
      <!-- Section 1: Personal Details -->
      <div>
        <h2 class="text-xs font-bold uppercase tracking-wider text-slate-400 mb-4">1. Personal Information</h2>
        <div class="grid grid-cols-1 sm:grid-cols-2 gap-5">
          
          <!-- Full Name -->
          <div class="sm:col-span-2">
            <label for="fullname" class="block text-sm font-semibold text-slate-700 mb-1">
              Full Name <span class="text-rose-500">*</span>
            </label>
            <input 
              type="text" 
              id="fullname" 
              name="fullname" 
              required 
              placeholder="e.g. Alex Johnson"
              class="w-full px-4 py-2.5 rounded-lg border border-slate-300 focus:ring-2 focus:ring-blue-500 focus:border-blue-500 text-slate-800 text-sm outline-none transition"
            >
            <p class="error-msg text-xs text-rose-500 mt-1 hidden" id="fullnameError">Full Name is required.</p>
          </div>

          <!-- Email Address -->
          <div>
            <label for="email" class="block text-sm font-semibold text-slate-700 mb-1">
              Email Address <span class="text-rose-500">*</span>
            </label>
            <input 
              type="email" 
              id="email" 
              name="email" 
              required 
              placeholder="alex.johnson@example.com"
              class="w-full px-4 py-2.5 rounded-lg border border-slate-300 focus:ring-2 focus:ring-blue-500 focus:border-blue-500 text-slate-800 text-sm outline-none transition"
            >
            <p class="error-msg text-xs text-rose-500 mt-1 hidden" id="emailError">Please enter a valid email address.</p>
          </div>

          <!-- Phone Number -->
          <div>
            <label for="phone" class="block text-sm font-semibold text-slate-700 mb-1">
              Phone Number <span class="text-rose-500">*</span>
            </label>
            <input 
              type="tel" 
              id="phone" 
              name="phone" 
              required 
              placeholder="+1 (555) 000-0000"
              class="w-full px-4 py-2.5 rounded-lg border border-slate-300 focus:ring-2 focus:ring-blue-500 focus:border-blue-500 text-slate-800 text-sm outline-none transition"
            >
            <p class="error-msg text-xs text-rose-500 mt-1 hidden" id="phoneError">Valid phone number required.</p>
          </div>

          <!-- Date of Birth -->
          <div>
            <label for="dob" class="block text-sm font-semibold text-slate-700 mb-1">
              Date of Birth <span class="text-rose-500">*</span>
            </label>
            <input 
              type="date" 
              id="dob" 
              name="dob" 
              required 
              class="w-full px-4 py-2.5 rounded-lg border border-slate-300 focus:ring-2 focus:ring-blue-500 focus:border-blue-500 text-slate-800 text-sm outline-none transition"
            >
            <p class="error-msg text-xs text-rose-500 mt-1 hidden" id="dobError">Please select your date of birth.</p>
          </div>

          <!-- Portfolio URL -->
          <div>
            <label for="portfolio" class="block text-sm font-semibold text-slate-700 mb-1">
              Portfolio URL <span class="text-rose-500">*</span>
            </label>
            <input 
              type="url" 
              id="portfolio" 
              name="portfolio" 
              required 
              placeholder="https://myportfolio.com"
              class="w-full px-4 py-2.5 rounded-lg border border-slate-300 focus:ring-2 focus:ring-blue-500 focus:border-blue-500 text-slate-800 text-sm outline-none transition"
            >
            <p class="error-msg text-xs text-rose-500 mt-1 hidden" id="portfolioError">Please enter a valid URL (starting with http:// or https://).</p>
          </div>

        </div>
      </div>

      <hr class="border-slate-200" />

      <!-- Section 2: Preferences & Qualifications -->
      <div>
        <h2 class="text-xs font-bold uppercase tracking-wider text-slate-400 mb-4">2. Role & Preferences</h2>
        <div class="grid grid-cols-1 sm:grid-cols-2 gap-5">
          
          <!-- Job Role Dropdown -->
          <div>
            <label for="role" class="block text-sm font-semibold text-slate-700 mb-1">
              Job Role / Qualification <span class="text-rose-500">*</span>
            </label>
            <select 
              id="role" 
              name="role" 
              required 
              class="w-full px-4 py-2.5 rounded-lg border border-slate-300 focus:ring-2 focus:ring-blue-500 focus:border-blue-500 text-slate-800 text-sm outline-none transition bg-white"
            >
              <option value="" disabled selected>-- Select Position --</option>
              <option value="Frontend Developer">Frontend Developer</option>
              <option value="Backend Developer">Backend Developer</option>
              <option value="Full Stack Engineer">Full Stack Engineer</option>
              <option value="UI/UX Designer">UI/UX Designer</option>
              <option value="Data Analyst">Data Analyst</option>
            </select>
            <p class="error-msg text-xs text-rose-500 mt-1 hidden" id="roleError">Please select a job role.</p>
          </div>

          <!-- Disabled Field Example -->
          <div>
            <label for="ref_code" class="block text-sm font-semibold text-slate-500 mb-1">
              Application Reference Code <span class="text-xs text-slate-400">(Auto-generated)</span>
            </label>
            <input 
              type="text" 
              id="ref_code" 
              name="ref_code" 
              value="REF-2026-JOB99" 
              disabled 
              class="w-full px-4 py-2.5 rounded-lg border border-slate-200 bg-slate-100 text-slate-500 text-sm cursor-not-allowed outline-none"
            >
          </div>

          <!-- Radio Buttons: Preferred Shift -->
          <div class="sm:col-span-2">
            <span class="block text-sm font-semibold text-slate-700 mb-2">
              Preferred Shift <span class="text-rose-500">*</span>
            </span>
            <div class="flex flex-wrap gap-4 pt-1">
              <label class="inline-flex items-center space-x-2 cursor-pointer text-sm text-slate-700">
                <input type="radio" name="shift" value="Day Shift" class="w-4 h-4 text-blue-600 focus:ring-blue-500 border-slate-300">
                <span>Day Shift</span>
              </label>
              <label class="inline-flex items-center space-x-2 cursor-pointer text-sm text-slate-700">
                <input type="radio" name="shift" value="Night Shift" class="w-4 h-4 text-blue-600 focus:ring-blue-500 border-slate-300">
                <span>Night Shift</span>
              </label>
              <label class="inline-flex items-center space-x-2 cursor-pointer text-sm text-slate-700">
                <input type="radio" name="shift" value="Flexible" class="w-4 h-4 text-blue-600 focus:ring-blue-500 border-slate-300" checked>
                <span>Flexible</span>
              </label>
            </div>
            <p class="error-msg text-xs text-rose-500 mt-1 hidden" id="shiftError">Please select a shift preference.</p>
          </div>

          <!-- Checkboxes: Skills -->
          <div class="sm:col-span-2">
            <span class="block text-sm font-semibold text-slate-700 mb-2">
              Key Skills <span class="text-xs text-slate-400">(Select all that apply)</span>
            </span>
            <div class="grid grid-cols-2 sm:grid-cols-4 gap-3 pt-1">
              <label class="inline-flex items-center space-x-2 cursor-pointer text-sm text-slate-700">
                <input type="checkbox" name="skills" value="HTML" class="rounded text-blue-600 focus:ring-blue-500 border-slate-300 w-4 h-4" checked>
                <span>HTML</span>
              </label>
              <label class="inline-flex items-center space-x-2 cursor-pointer text-sm text-slate-700">
                <input type="checkbox" name="skills" value="CSS" class="rounded text-blue-600 focus:ring-blue-500 border-slate-300 w-4 h-4" checked>
                <span>CSS</span>
              </label>
              <label class="inline-flex items-center space-x-2 cursor-pointer text-sm text-slate-700">
                <input type="checkbox" name="skills" value="JavaScript" class="rounded text-blue-600 focus:ring-blue-500 border-slate-300 w-4 h-4">
                <span>JavaScript</span>
              </label>
              <label class="inline-flex items-center space-x-2 cursor-pointer text-sm text-slate-700">
                <input type="checkbox" name="skills" value="Python" class="rounded text-blue-600 focus:ring-blue-500 border-slate-300 w-4 h-4">
                <span>Python</span>
              </label>
            </div>
          </div>

        </div>
      </div>

      <hr class="border-slate-200" />

      <!-- Section 3: Cover Letter -->
      <div>
        <h2 class="text-xs font-bold uppercase tracking-wider text-slate-400 mb-4">3. Application Essay</h2>
        <div>
          <label for="cover_letter" class="block text-sm font-semibold text-slate-700 mb-1">
            Cover Letter <span class="text-rose-500">*</span>
          </label>
          <textarea 
            id="cover_letter" 
            name="cover_letter" 
            rows="4" 
            required 
            placeholder="Tell us briefly why you are a great fit for this position..."
            class="w-full px-4 py-2.5 rounded-lg border border-slate-300 focus:ring-2 focus:ring-blue-500 focus:border-blue-500 text-slate-800 text-sm outline-none transition"
          ></textarea>
          <p class="error-msg text-xs text-rose-500 mt-1 hidden" id="coverLetterError">Please provide a cover letter.</p>
        </div>
      </div>

      <!-- Submit Button -->
      <div class="pt-4">
        <button 
          type="submit" 
          class="w-full bg-gradient-to-r from-blue-600 to-indigo-600 hover:from-blue-700 hover:to-indigo-700 active:scale-[0.99] text-white font-semibold py-3 px-6 rounded-xl shadow-lg shadow-blue-500/25 transition-all cursor-pointer flex items-center justify-center space-x-2"
        >
          <span>Submit Application</span>
          <svg class="w-5 h-5" fill="none" stroke="currentColor" viewBox="0 0 24 24">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M14 5l7 7m0 0l-7 7m7-7H3"></path>
          </svg>
        </button>
      </div>

    </form>

  </div>

  <!-- JavaScript Validation & Handling -->
  <script>
    document.addEventListener('DOMContentLoaded', () => {
      const form = document.getElementById('applicationForm');
      const successBanner = document.getElementById('successBanner');
      const summaryDetails = document.getElementById('summaryDetails');

      // Clear inline errors on input
      const inputs = form.querySelectorAll('input, select, textarea');
      inputs.forEach(input => {
        input.addEventListener('input', () => {
          const errorEl = document.getElementById(`${input.id}Error`);
          if (errorEl) {
            errorEl.classList.add('hidden');
            input.classList.remove('border-rose-500', 'focus:ring-rose-500');
            input.classList.add('border-slate-300', 'focus:ring-blue-500');
          }
        });
      });

      // Handle form submit
      form.addEventListener('submit', (e) => {
        e.preventDefault();
        let isValid = true;

        // Required text/date/url/email/tel inputs
        const requiredFields = [
          { id: 'fullname', validate: (v) => v.trim().length > 0 },
          { id: 'email', validate: (v) => /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(v.trim()) },
          { id: 'phone', validate: (v) => /^[0-9\-\+\s\(\)]{7,15}$/.test(v.trim()) },
          { id: 'dob', validate: (v) => v.trim() !== '' },
          { id: 'portfolio', validate: (v) => /^https?:\/\/.+/i.test(v.trim()) },
          { id: 'role', validate: (v) => v !== '' },
          { id: 'cover_letter', validate: (v) => v.trim().length >= 10 }
        ];

        requiredFields.forEach(field => {
          const el = document.getElementById(field.id);
          const errorEl = document.getElementById(`${field.id}Error`) || document.getElementById('coverLetterError');

          if (!field.validate(el.value)) {
            isValid = false;
            el.classList.remove('border-slate-300', 'focus:ring-blue-500');
            el.classList.add('border-rose-500', 'focus:ring-rose-500');
            if (errorEl) errorEl.classList.remove('hidden');
          }
        });

        // Shift radio validation
        const shiftSelected = document.querySelector('input[name="shift"]:checked');
        if (!shiftSelected) {
          isValid = false;
          document.getElementById('shiftError').classList.remove('hidden');
        }

        if (isValid) {
          // Gather selected skills
          const selectedSkills = Array.from(document.querySelectorAll('input[name="skills"]:checked'))
            .map(cb => cb.value);

          // Populate submission summary
          const nameVal = document.getElementById('fullname').value;
          const roleVal = document.getElementById('role').value;
          const emailVal = document.getElementById('email').value;

          summaryDetails.innerHTML = `
            <p><strong>Applicant:</strong> ${nameVal}</p>
            <p><strong>Position:</strong> ${roleVal}</p>
            <p><strong>Email:</strong> ${emailVal}</p>
            <p><strong>Skills Listed:</strong> ${selectedSkills.length ? selectedSkills.join(', ') : 'None selected'}</p>
          `;

          // Display success state
          successBanner.classList.remove('hidden');
          form.reset();

          // Scroll smoothly to top
          window.scrollTo({ top: 0, behavior: 'smooth' });
        }
      });
    });
  </script>
</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
  <link rel="manifest" href="manifest.json">
  <meta name="theme-color" content="#5c27d6" />
  <script>

  firebase.initializeApp(firebaseConfig);
</script>

  <meta charset="UTF-8" />
  <title>Event Calendar</title>
  <style>
    body {
      font-family: 'Segoe UI', sans-serif;
      background: #f5f0ff;
      color: #222;
      padding: 20px;
    }
    h1 {
      text-align: center;
      color: #5c27d6;
    }
    .controls {
      text-align: center;
      margin: 20px 0;
    }
    select {
      padding: 8px 12px;
      font-size: 16px;
      border-radius: 6px;
      border: 1px solid #aaa;
      margin: 0 10px;
    }
    .calendar h2 {
      text-align: center;
      color: #5c27d6;
    }
    .days {
      display: grid;
      grid-template-columns: repeat(7, 1fr);
      gap: 10px;
      margin-top: 20px;
    }
    .day {
      background: #e4d7ff;
      border: 2px solid #5c27d6;
      padding: 10px;
      border-radius: 12px;
      text-align: left;
      position: relative;
      min-height: 100px;
    }
    .day::before {
      content: attr(data-day);
      font-size: 13px;
      color: #555;
      display: block;
      margin-bottom: 4px;
    }
    .date {
      font-size: 20px;
      font-weight: bold;
    }
    .add-btn {
      position: absolute;
      top: 5px;
      right: 10px;
      background: none;
      border: none;
      font-size: 18px;
      cursor: pointer;
      color: #5c27d6;
    }
    .event-shortcut {
      margin-top: 10px;
      display: flex;
      flex-direction: column;
      gap: 4px;
    }
    .event-item {
      background: #4122a8;
      color: white;
      padding: 2px 4px;
      font-size: 11px;
      border-radius: 4px;
      text-overflow: ellipsis;
      white-space: nowrap;
      overflow: hidden;
      display: flex;
      justify-content: space-between;
      align-items: center;
      cursor: pointer;
    }
    .modal {
      display: none;
      position: fixed;
      z-index: 10;
      left: 0; top: 0;
      width: 100%; height: 100%;
      background: rgba(0,0,0,0.6);
    }
    .modal.show {
      display: block;
    }
    .modal-content {
      background: white;
      margin: 80px auto;
      padding: 20px;
      width: 60%;
      border-radius: 10px;
      position: relative;
    }

    .event-controls {
  position: absolute;
  top: 10px;
  right: 10px;
  display: flex;
  gap: 10px;
  align-items: center;
}

.event-controls button,
.event-controls .close {
  background: none;
  border: none;
  font-size: 18px;
  cursor: pointer;
  color: #000;
}

.event-controls .close {
  font-size: 24px;
  margin-left: 10px;
}
.buttons{
      background: #5c27d6;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
}
.header-bar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 10px 30px;
}

.header-bar h1 {
  flex: 1;
  text-align: center;
  color: #5c27d6;
  margin: 0;
}

.logo-left,
.logo-right {
  height: 200px;
  width: 200px;
  object-fit: contain;
}


    
    form input:disabled,
    form textarea:disabled {
      background: #f0f0f0;
      color: #555;
    }
    form input, form textarea {
      display: block;
      width: 100%;
      margin-bottom: 10px;
      padding: 8px;
      font-size: 14px;
      border-radius: 6px;
      border: 1px solid #ccc;
    }
    form button {
      background: #5c27d6;
      color: white;
      padding: 10px 20px;
      border: none;
      border-radius: 8px;
      cursor: pointer;
    }
    #confirmDeleteModal {
      display: none;
      position: fixed;
      z-index: 20;
      left: 0; top: 0;
      width: 100%; height: 100%;
      background: rgba(0,0,0,0.6);
    }
    #confirmDeleteModal .modal-content {
      background: white;
      margin: 150px auto;
      padding: 20px;
      width: 300px;
      border-radius: 10px;
      text-align: center;
    }
    #confirmDeleteModal button {
      margin: 10px;
    }
  </style>
</head>
<body>
<div id="loginContainer" style="text-align:center; margin-top: 50px;">
  <h2>Login to Access the Event Calendar</h2>
  <input type="email" id="loginEmail" placeholder="Enter Username" required>
  <input type="password" id="loginPassword" placeholder="Enter Password" required>
  <br><br>
  <button class="buttons" onclick="loginUser()">Login</button>
</div>

<div id="calendarApp" style="display:none;">
  <!-- Your calendar UI code here -->
<div class="header-bar">
  <img src="https://logodix.com/logo/2052162.png" alt="Left Logo" class="logo-left">
  <h1>Andhra University Centenary Celebrations Event Calendar</h1>
  <button onclick="logoutUser()" style="position: absolute; right: 30px; top: 30px; padding: 8px 16px; background: #5c27d6; color: white; border: none; border-radius: 6px; cursor: pointer;">Logout</button>
  <img src="https://andhrauniversity.edu.in/img/au-century-logo2025.jpg" alt="Right Logo" class="logo-right">
</div>

<div class="controls">
  <label for="yearSelect">Year:</label>
  <select id="yearSelect"></select>
  <label for="monthSelect">Month:</label>
  <select id="monthSelect"></select>
</div>

<div class="calendar">
  <h2 id="calendarTitle"></h2>
  <div class="days" id="daysContainer"></div>
</div>

<div id="eventModal" class="modal">
  <div class="modal-content">
    <div class="event-controls">
  <div id="actionButtons" style="display: none;">
    <button onclick="editCurrentEvent()">✏️</button>
    <button onclick="deleteCurrentEvent()">🗑</button>
  </div>
  <span class="close" onclick="closeModal()">&times;</span>
</div>

    <h2 id="modalTitle"></h2>
    <form id="eventForm" onsubmit="submitEvent(event)">
      <input type="hidden" id="eventDay">
      <input type="hidden" id="editIndex">
      <label>Name of the Department:</label>
      <input type="text" id="eventTitle" required>
      <label>Name of the Organizing Chairman and Coordinator:</label>
      <input type="text" id="eventTime" required>
      <label>Duration & Dates:</label>
      <textarea id="eventDesc" required></textarea>
      <button type="submit">Save Event</button>
    </form>
  </div>
</div>

  <div id="confirmDeleteModal">
    <div class="modal-content">
      <p>Are you sure you really want to delete the event?</p>
      <button class="buttons" onclick="cancelDelete()">Cancel</button>
      <button class="buttons" onclick="confirmDelete()">Delete</button>
    </div>
  </div>
</div>



  <script>
  const monthNames = [..."January February March April May June July August September October November December".split(" ")];
  const dayNames = ["Sun", "Mon", "Tue", "Wed", "Thu", "Fri", "Sat"];
let eventData = JSON.parse(localStorage.getItem("calendarEvents") || "{}");

  const yearSelect = document.getElementById('yearSelect');
  const monthSelect = document.getElementById('monthSelect');
  const daysContainer = document.getElementById('daysContainer');
  const calendarTitle = document.getElementById('calendarTitle');
  const eventModal = document.getElementById('eventModal');
  const modalTitle = document.getElementById('modalTitle');
  const confirmDeleteModal = document.getElementById('confirmDeleteModal');

  let selectedYear, selectedMonth, selectedDay;
  let currentEditIndex = null;
  let pendingDelete = null;

  for (let y = 2020; y <= 2030; y++) {
    yearSelect.innerHTML += `<option value="${y}">${y}</option>`;
  }

  monthNames.forEach((m, i) => {
    monthSelect.innerHTML += `<option value="${i}">${m}</option>`;
  });

  yearSelect.value = new Date().getFullYear();
  monthSelect.value = new Date().getMonth();

  yearSelect.onchange = updateCalendar;
  monthSelect.onchange = updateCalendar;

  function saveEventsToStorage() {
  localStorage.setItem("calendarEvents", JSON.stringify(eventData));
}


  function updateCalendar() {
    selectedYear = yearSelect.value;
    selectedMonth = monthSelect.value;
    generateCalendar(selectedYear, selectedMonth);
  }

  function generateCalendar(year, month) {
    calendarTitle.textContent = `${monthNames[month]} ${year}`;
    daysContainer.innerHTML = "";
    const firstDay = new Date(year, month, 1).getDay();
    const totalDays = new Date(year, parseInt(month) + 1, 0).getDate();

    for (let i = 0; i < firstDay; i++) daysContainer.appendChild(document.createElement("div"));

    for (let day = 1; day <= totalDays; day++) {
      const dayBox = document.createElement("div");
      dayBox.className = "day";
      dayBox.setAttribute("data-day", dayNames[new Date(year, month, day).getDay()]);
      dayBox.innerHTML = `<span class="date">${day}</span><button class="add-btn" onclick="openAddEvent(${day})">+</button>`;

      const shortcuts = document.createElement("div");
      shortcuts.className = "event-shortcut";
      const key = `${year}-${month}-${day}`;
      const events = eventData[key] || [];

      events.forEach((evt, index) => {
        const item = document.createElement("div");
        item.className = "event-item";
        item.textContent = evt.title;
        item.onclick = () => showEventModal(day, index);
        shortcuts.appendChild(item);
      });

      dayBox.appendChild(shortcuts);
      daysContainer.appendChild(dayBox);
    }
  }

  function openAddEvent(day) {
    selectedDay = day;
    currentEditIndex = null;
    modalTitle.textContent = `Add Event on ${monthNames[selectedMonth]} ${day}`;
    ['eventTitle', 'eventTime', 'eventDesc'].forEach(id => {
      const el = document.getElementById(id);
      el.value = '';
      el.disabled = false;
    });
    document.getElementById('eventDay').value = day;
    document.getElementById('editIndex').value = "";
    document.getElementById('actionButtons').style.display = 'none';
    eventModal.classList.add('show');
  }

  function showEventModal(day, index) {
    selectedDay = day;
    currentEditIndex = index;
    const key = `${selectedYear}-${selectedMonth}-${day}`;
    const evt = eventData[key][index];
    modalTitle.textContent = `Event: ${evt.title}`;
    document.getElementById('actionButtons').style.display = 'flex';
    document.getElementById('eventTitle').value = evt.title;
    document.getElementById('eventTime').value = evt.time;
    document.getElementById('eventDesc').value = evt.desc;
    document.getElementById('eventDay').value = day;
    document.getElementById('editIndex').value = index;

    ['eventTitle', 'eventTime', 'eventDesc'].forEach(id => {
      document.getElementById(id).disabled = true;
    });

    eventModal.classList.add('show');
  }

  function editCurrentEvent() {
    ['eventTitle', 'eventTime', 'eventDesc'].forEach(id => {
      document.getElementById(id).disabled = false;
    });
  }

  function deleteCurrentEvent() {
    pendingDelete = { day: selectedDay, index: currentEditIndex };
    confirmDeleteModal.style.display = 'block';
  }

  function cancelDelete() {
    confirmDeleteModal.style.display = 'none';
    pendingDelete = null;
  }

  function confirmDelete() {
    if (!pendingDelete) return;
    const { day, index } = pendingDelete;
    const key = `${selectedYear}-${selectedMonth}-${day}`;
    if (eventData[key]) {
      eventData[key].splice(index, 1);
      if (eventData[key].length === 0) delete eventData[key];
    }

    saveEventsToStorage();
    closeModal();
    confirmDeleteModal.style.display = 'none';
    generateCalendar(selectedYear, selectedMonth);
  }

  function closeModal() {
    eventModal.classList.remove('show');
  }

  document.getElementById('eventForm').onsubmit = function (e) {
    e.preventDefault();
    const title = document.getElementById('eventTitle').value;
    const time = document.getElementById('eventTime').value;
    const desc = document.getElementById('eventDesc').value;
    const day = document.getElementById('eventDay').value;
    const index = document.getElementById('editIndex').value;
    const key = `${selectedYear}-${selectedMonth}-${day}`;
    eventData[key] = eventData[key] || [];

    if (index === "") {
      eventData[key].push({ title, time, desc });
    } else {
      eventData[key][index] = { title, time, desc };
    }

    saveEventsToStorage();
    closeModal();
    generateCalendar(selectedYear, selectedMonth);
  };

  updateCalendar();
  if ('serviceWorker' in navigator) {
  window.addEventListener('load', () => {
    navigator.serviceWorker.register('serviceWorker.js').then(() => {
      console.log('Service Worker registered ✅');
    });
  });
}

  const validEmail = "au100";
  const validPassword = "au@100";

  function loginUser() {
    const email = document.getElementById('loginEmail').value;
    const password = document.getElementById('loginPassword').value;

    if (email === validEmail && password === validPassword) {
      document.getElementById('loginContainer').style.display = 'none';
      document.getElementById('calendarApp').style.display = 'block';
    } else {
      alert("Invalid username or password");
    }
  }

  function logoutUser() {
  document.getElementById('calendarApp').style.display = 'none';
  document.getElementById('loginContainer').style.display = 'block';
  document.getElementById('loginEmail').value = '';
  document.getElementById('loginPassword').value = '';
}


  </script>
</body>
</html>

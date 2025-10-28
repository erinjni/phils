---
layout: page
title: Members
subtitle: Our beautiphul phamily. Click on anyone to learn more!
full-width: true
---

<style>
    @import url('https://fonts.googleapis.com/css2?family=Righteous&family=Inter:wght@400;600;700&display=swap');
    
    * {
        box-sizing: border-box;
    }
    
    body {
        font-family: 'Inter', sans-serif;
        color: #25272c;
        margin: 0;
        padding: 0;
    }
    
    .members-container {
        max-width: 1400px;
        margin: 0 auto;
        padding: 60px 20px;
    }
    
    /* Year Section */
    .year-section {
        margin-bottom: 100px;
    }
    
    .year-title {
        font-family: 'Righteous', sans-serif;
        font-size: 3.5rem;
        color: #005fb7;
        text-align: center;
        margin-bottom: 50px;
    }
    
    /* Slideshow */
    .slideshow {
        position: relative;
        width: 100%;
        max-width: 900px;
        height: 500px;
        margin: 0 auto 60px;
        border-radius: 20px;
        overflow: hidden;
        box-shadow: 0 10px 40px rgba(0, 0, 0, 0.2);
    }
    
    .slideshow-image {
        position: absolute;
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: center top;
        opacity: 0;
        transition: opacity 1s ease-in-out;
    }
    
    .slideshow-image.active {
        opacity: 1;
    }
    
    .slideshow-nav {
        position: absolute;
        bottom: 20px;
        left: 50%;
        transform: translateX(-50%);
        display: flex;
        gap: 10px;
        z-index: 10;
    }
    
    .slideshow-dot {
        width: 12px;
        height: 12px;
        border-radius: 50%;
        background: rgba(255, 255, 255, 0.5);
        cursor: pointer;
        transition: background 0.3s ease;
    }
    
    .slideshow-dot.active {
        background: white;
    }
    
    /* Members Grid */
    .members-grid {
        display: grid;
        gap: 40px;
        justify-content: center;
        margin-bottom: 40px;
    }
    
    .members-grid.grid-3 {
        grid-template-columns: repeat(3, 250px);
    }
    
    .members-grid.grid-2 {
        grid-template-columns: repeat(2, 250px);
    }
    
    .members-grid.grid-2x2 {
        grid-template-columns: repeat(2, 250px);
    }
    
    .members-grid.grid-3-2 {
        grid-template-columns: repeat(3, 250px);
    }
    
    /* Member Card */
    .member-card {
        text-align: center;
    }
    
    .member-photo-container {
        width: 250px;
        height: 250px;
        border-radius: 50%;
        overflow: hidden;
        cursor: pointer;
        position: relative;
        margin: 0 auto 15px;
        box-shadow: 0 4px 20px rgba(0, 95, 183, 0.3);
        transition: transform 0.3s ease, box-shadow 0.3s ease;
    }
    
    .member-photo-container:hover {
        transform: scale(1.05);
        box-shadow: 0 8px 30px rgba(0, 95, 183, 0.5);
    }
    
    .member-photo {
        width: 100%;
        height: 100%;
        object-fit: cover;
        object-position: center top;
        transition: opacity 0.3s ease;
    }
    
    .member-photo.silly {
        position: absolute;
        top: 0;
        left: 0;
        opacity: 0;
    }
    
    .member-photo-container:hover .member-photo.silly {
        opacity: 1;
    }
    
    .member-photo-container:hover .member-photo.normal {
        opacity: 0;
    }
    
    .member-name {
        font-size: 1.3rem;
        font-weight: 600;
        color: #005fb7;
        margin-bottom: 5px;
    }
    
    /* Blurb */
    .member-blurb {
        max-height: 0;
        overflow: hidden;
        transition: max-height 0.4s ease, margin 0.4s ease, padding 0.4s ease;
        background: #f5f7fa;
        border-radius: 15px;
        margin-top: 0;
    }
    
    .member-blurb.expanded {
        max-height: 500px;
        margin-top: 20px;
        overflow-y: auto;
        padding: 25px;
    }
    
    .member-blurb p {
        margin: 0;
        line-height: 1.6;
        color: #25272c;
    }
    
    /* Alumni Section */
    .alumni-section {
        margin-top: 100px;
    }
    
    .alumni-title {
        font-family: 'Righteous', sans-serif;
        font-size: 3.5rem;
        color: #005fb7;
        text-align: center;
        margin-bottom: 30px;
    }
    
    .search-container {
        max-width: 600px;
        margin: 0 auto 40px;
    }
    
    .search-input {
        width: 100%;
        padding: 15px 20px;
        font-size: 1rem;
        border: 2px solid #e0e0e0;
        border-radius: 50px;
        outline: none;
        transition: border-color 0.3s ease;
    }
    
    .search-input:focus {
        border-color: #005fb7;
    }
    
    .alumni-table-container {
        overflow-x: auto;
        background: white;
        border-radius: 15px;
        box-shadow: 0 4px 20px rgba(0, 0, 0, 0.1);
    }
    
    .alumni-table {
        width: 100%;
        border-collapse: collapse;
    }
    
    .alumni-table thead {
            background: #005fb7;
        }
        
    .alumni-table thead th {
        padding: 20px;
        text-align: left;
        font-weight: 600;
        cursor: pointer;
        user-select: none;
        position: relative;
        background: #005fb7 !important;
        color: white !important;
    }
    
    .alumni-table th::after {
        content: ' ↕';
        opacity: 0.5;
        font-size: 0.8rem;
    }
    
    .alumni-table td {
        padding: 20px;
        border-bottom: 1px solid #e0e0e0;
    }
    
    .alumni-table tbody tr:hover {
        background: #f5f7fa;
    }
    
    .no-results {
        text-align: center;
        padding: 40px;
        color: #666;
        font-size: 1.1rem;
    }
    
    /* Responsive */
    @media (max-width: 1024px) {
        .members-grid.grid-3,
        .members-grid.grid-2,
        .members-grid.grid-2x2,
        .members-grid.grid-3-2 {
            grid-template-columns: repeat(2, 250px);
        }
    }
    
    @media (max-width: 768px) {
        .year-title, .alumni-title {
            font-size: 2.5rem;
        }
        
        .slideshow {
            height: 300px;
        }
        
        .members-grid.grid-3,
        .members-grid.grid-2,
        .members-grid.grid-2x2,
        .members-grid.grid-3-2 {
            grid-template-columns: 1fr;
            gap: 30px;
        }
        
        .member-photo-container {
            width: 200px;
            height: 200px;
        }
        
        .alumni-table {
            font-size: 0.9rem;
        }
        
        .alumni-table th,
        .alumni-table td {
            padding: 12px;
        }
    }
</style>


<div class="members-container">
    <!-- Newx6 Section -->
    <div class="year-section" id="newx6-section">
        <h2 class="year-title">New x6 Phils</h2>
        
        <div class="slideshow" data-year="newx6">
            {% for image in site.data.members.newx6.slideshow %}
            <img src="/assets/img/{{ image }}" alt="Newx6 Group Photo" class="slideshow-image {% if forloop.first %}active{% endif %}">
            {% endfor %}
            <div class="slideshow-nav">
                {% for image in site.data.members.newx6.slideshow %}
                <div class="slideshow-dot {% if forloop.first %}active{% endif %}" data-index="{{ forloop.index0 }}"></div>
                {% endfor %}
            </div>
        </div>
        
        <div class="members-grid grid-3">
            {% for member in site.data.members.newx6.members %}
            <div class="member-card" id="{{ member.id }}">
                <div class="member-photo-container" onclick="toggleBlurb('{{ member.id }}')">
                    <img src="/assets/img/{{ member.headshot }}" alt="{{ member.name }}" class="member-photo normal">
                    <img src="/assets/img/{{ member.silly }}" alt="{{ member.name }}" class="member-photo silly">
                </div>
                <div class="member-name">{{ member.name }}</div>
                <div class="member-blurb" id="{{ member.id }}-blurb">
                    <p>{{ member.blurb }}</p>
                </div>
            </div>
            {% endfor %}
        </div>
    </div>

    <!-- Newx7 Section -->
    <div class="year-section" id="newx7-section">
        <h2 class="year-title">New x7 Phils</h2>
        
        <div class="slideshow" data-year="newx7">
            {% for image in site.data.members.newx7.slideshow %}
            <img src="/assets/img/{{ image }}" alt="Newx7 Group Photo" class="slideshow-image {% if forloop.first %}active{% endif %}">
            {% endfor %}
            <div class="slideshow-nav">
                {% for image in site.data.members.newx7.slideshow %}
                <div class="slideshow-dot {% if forloop.first %}active{% endif %}" data-index="{{ forloop.index0 }}"></div>
                {% endfor %}
            </div>
        </div>
        
        <div class="members-grid grid-2">
            {% for member in site.data.members.newx7.members %}
            <div class="member-card" id="{{ member.id }}">
                <div class="member-photo-container" onclick="toggleBlurb('{{ member.id }}')">
                    <img src="/assets/img/{{ member.headshot }}" alt="{{ member.name }}" class="member-photo normal">
                    <img src="/assets/img/{{ member.silly }}" alt="{{ member.name }}" class="member-photo silly">
                </div>
                <div class="member-name">{{ member.name }}</div>
                <div class="member-blurb" id="{{ member.id }}-blurb">
                    <p>{{ member.blurb }}</p>
                </div>
            </div>
            {% endfor %}
        </div>
    </div>

    <!-- Newx8 Section -->
    <div class="year-section" id="newx8-section">
        <h2 class="year-title">New x8 Phils</h2>
        
        <div class="slideshow" data-year="newx8">
            {% for image in site.data.members.newx8.slideshow %}
            <img src="/assets/img/{{ image }}" alt="Newx8 Group Photo" class="slideshow-image {% if forloop.first %}active{% endif %}">
            {% endfor %}
            <div class="slideshow-nav">
                {% for image in site.data.members.newx8.slideshow %}
                <div class="slideshow-dot {% if forloop.first %}active{% endif %}" data-index="{{ forloop.index0 }}"></div>
                {% endfor %}
            </div>
        </div>
        
        <div class="members-grid grid-2x2">
            {% for member in site.data.members.newx8.members %}
            <div class="member-card" id="{{ member.id }}">
                <div class="member-photo-container" onclick="toggleBlurb('{{ member.id }}')">
                    <img src="/assets/img/{{ member.headshot }}" alt="{{ member.name }}" class="member-photo normal">
                    <img src="/assets/img/{{ member.silly }}" alt="{{ member.name }}" class="member-photo silly">
                </div>
                <div class="member-name">{{ member.name }}</div>
                <div class="member-blurb" id="{{ member.id }}-blurb">
                    <p>{{ member.blurb }}</p>
                </div>
            </div>
            {% endfor %}
        </div>
    </div>

    <!-- Newx9 Section -->
    <div class="year-section" id="newx9-section">
        <h2 class="year-title">New x9 Phils</h2>
        
        <div class="slideshow" data-year="newx9">
            {% for image in site.data.members.newx9.slideshow %}
            <img src="/assets/img/{{ image }}" alt="Newx9 Group Photo" class="slideshow-image {% if forloop.first %}active{% endif %}">
            {% endfor %}
            <div class="slideshow-nav">
                {% for image in site.data.members.newx9.slideshow %}
                <div class="slideshow-dot {% if forloop.first %}active{% endif %}" data-index="{{ forloop.index0 }}"></div>
                {% endfor %}
            </div>
        </div>
        
        <div class="members-grid grid-3-2">
            {% for member in site.data.members.newx9.members %}
            <div class="member-card" id="{{ member.id }}">
                <div class="member-photo-container" onclick="toggleBlurb('{{ member.id }}')">
                    <img src="/assets/img/{{ member.headshot }}" alt="{{ member.name }}" class="member-photo normal">
                    <img src="/assets/img/{{ member.silly }}" alt="{{ member.name }}" class="member-photo silly">
                </div>
                <div class="member-name">{{ member.name }}</div>
                <div class="member-blurb" id="{{ member.id }}-blurb">
                    <p>{{ member.blurb }}</p>
                </div>
            </div>
            {% endfor %}
        </div>
    </div>

    <!-- Alumni Section -->
    <div class="alumni-section">
        <h2 class="alumni-title">Alumni</h2>
        
        <div class="search-container">
            <input type="text" id="alumniSearch" class="search-input" placeholder="Search alumni by name, year, college, major, or position...">
        </div>
        
        <div class="alumni-table-container">
            <table class="alumni-table" id="alumniTable">
                <thead>
                    <tr>
                        <th onclick="sortTable(0)">Name</th>
                        <th onclick="sortTable(1)">Graduation Year</th>
                        <th onclick="sortTable(2)">Residential College</th>
                        <th onclick="sortTable(3)">Major</th>
                        <th onclick="sortTable(4)">Position(s)</th>
                    </tr>
                </thead>
                <tbody id="alumniTableBody">
                    {% for alum in site.data.members.alumni %}
                    <tr>
                        <td>{{ alum.name }}</td>
                        <td>{{ alum.grad_year }}</td>
                        <td>{{ alum.college }}</td>
                        <td>{{ alum.major }}</td>
                        <td>{{ alum.positions }}</td>
                    </tr>
                    {% endfor %}
                </tbody>
            </table>
            <div id="noResults" class="no-results" style="display: none;">
                No alumni found matching your search.
            </div>
        </div>
    </div>
</div>

<script>
    // Toggle member blurb
    function toggleBlurb(memberId) {
        const blurb = document.getElementById(memberId + '-blurb');
        blurb.classList.toggle('expanded');
    }

    // Slideshow functionality
    document.querySelectorAll('.slideshow').forEach(slideshow => {
        const images = slideshow.querySelectorAll('.slideshow-image');
        const dots = slideshow.querySelectorAll('.slideshow-dot');
        let currentIndex = 0;
        let interval;

        function showSlide(index) {
            images.forEach(img => img.classList.remove('active'));
            dots.forEach(dot => dot.classList.remove('active'));
            images[index].classList.add('active');
            dots[index].classList.add('active');
        }

        function nextSlide() {
            currentIndex = (currentIndex + 1) % images.length;
            showSlide(currentIndex);
        }

        // Auto-advance every 4 seconds
        interval = setInterval(nextSlide, 4000);

        // Click on dots
        dots.forEach(dot => {
            dot.addEventListener('click', () => {
                clearInterval(interval);
                currentIndex = parseInt(dot.dataset.index);
                showSlide(currentIndex);
                interval = setInterval(nextSlide, 4000);
            });
        });
    });

    // Alumni search
    const searchInput = document.getElementById('alumniSearch');
    const table = document.getElementById('alumniTable');
    const tbody = document.getElementById('alumniTableBody');
    const noResults = document.getElementById('noResults');

    searchInput.addEventListener('input', function() {
        const searchTerm = this.value.toLowerCase();
        const rows = tbody.getElementsByTagName('tr');
        let visibleCount = 0;

        Array.from(rows).forEach(row => {
            const text = row.textContent.toLowerCase();
            if (text.includes(searchTerm)) {
                row.style.display = '';
                visibleCount++;
            } else {
                row.style.display = 'none';
            }
        });

        if (visibleCount === 0) {
            table.style.display = 'none';
            noResults.style.display = 'block';
        } else {
            table.style.display = 'table';
            noResults.style.display = 'none';
        }
    });

    // Table sorting
    let sortDirection = {};
    
    function sortTable(columnIndex) {
        const rows = Array.from(tbody.getElementsByTagName('tr'));
        const currentDirection = sortDirection[columnIndex] || 'asc';
        const newDirection = currentDirection === 'asc' ? 'desc' : 'asc';
        sortDirection[columnIndex] = newDirection;

        rows.sort((a, b) => {
            const aText = a.cells[columnIndex].textContent.trim();
            const bText = b.cells[columnIndex].textContent.trim();
            
            // Handle numeric sorting for graduation year
            if (columnIndex === 1) {
                return newDirection === 'asc' 
                    ? parseInt(aText) - parseInt(bText)
                    : parseInt(bText) - parseInt(aText);
            }
            
            // String sorting
            return newDirection === 'asc'
                ? aText.localeCompare(bText)
                : bText.localeCompare(aText);
        });

        rows.forEach(row => tbody.appendChild(row));
    }

    // Deep linking - expand blurb if member ID is in URL hash
    window.addEventListener('load', () => {
        const hash = window.location.hash.substring(1);
        if (hash) {
            const memberCard = document.getElementById(hash);
            if (memberCard) {
                // Scroll to the section
                memberCard.scrollIntoView({ behavior: 'smooth', block: 'center' });
                // Expand the blurb after a short delay
                setTimeout(() => {
                    const blurb = document.getElementById(hash + '-blurb');
                    if (blurb) {
                        blurb.classList.add('expanded');
                    }
                }, 500);
            }
        }
    });
</script>
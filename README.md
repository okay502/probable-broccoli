> Index Html

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>LeadFlow Pro - Real Lead Management System</title>
    <style>
        :root {
            --primary: #7c3aed;
            --secondary: #6d28d9;
            --accent: #8b5cf6;
            --light: #f5f3ff;
            --dark: #4c1d95;
        }
        body {
            font-family: 'Inter', system-ui, sans-serif;
            line-height: 1.6;
            margin: 0;
            padding: 0;
            color: #1f2937;
            background-color: #f9fafb;
        }
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        header {
            background: linear-gradient(135deg, var(--primary), var(--secondary));
            color: white;
            padding: 60px 20px;
            text-align: center;
            margin-bottom: 40px;
        }
        h1 {
            font-size: 2.8rem;
            margin: 0 0 15px 0;
            font-weight: 800;
        }
        .subtitle {
            font-size: 1.2rem;
            max-width: 700px;
            margin: 0 auto 25px auto;
            opacity: 0.9;
        }
        .price-tag {
            background: white;
            color: var(--primary);
            display: inline-block;
            padding: 10px 25px;
            border-radius: 50px;
            font-weight: bold;
            font-size: 1.1rem;
            box-shadow: 0 5px 15px rgba(0,0,0,0.1);
        }
        .nav {
            display: flex;
            justify-content: center;
            gap: 20px;
            margin-bottom: 30px;
        }
        .nav-btn {
            background: var(--light);
            color: var(--primary);
            padding: 12px 25px;
            border-radius: 8px;
            text-decoration: none;
            font-weight: 600;
            transition: all 0.3s;
        }
        .nav-btn.active {
            background: var(--primary);
            color: white;
        }
        .tab-content {
            display: none;
        }
        .tab-content.active {
            display: block;
        }
        section {
            background: white;
            border-radius: 12px;
            padding: 30px;
            margin-bottom: 30px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            border: 1px solid #e5e7eb;
        }
        h2 {
            color: var(--primary);
            margin-top: 0;
            font-size: 1.8rem;
        }
        .form-group {
            margin-bottom: 20px;
        }
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
        }
        input, select, textarea {
            width: 100%;
            padding: 12px;
            border: 1px solid #d1d5db;
            border-radius: 8px;
            font-family: inherit;
            font-size: 1rem;
        }
        .btn {
            background: var(--primary);
            color: white;
            padding: 14px 28px;
            border-radius: 8px;
            border: none;
            font-weight: 600;
            font-size: 1rem;
            cursor: pointer;
            transition: all 0.3s;
            display: inline-block;
        }
        .btn:hover {
            background: var(--secondary);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(124, 58, 237, 0.3);
        }
        .leads-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }
        .leads-table th, .leads-table td {
            padding: 12px 15px;
            text-align: left;
            border-bottom: 1px solid #e5e7eb;
        }
        .leads-table th {
            background: var(--light);
            color: var(--dark);
            font-weight: 600;
        }
        .leads-table tr:hover {
            background: #f9fafb;
        }
        .status-badge {
            display: inline-block;
            padding: 4px 10px;
            border-radius: 50px;
            font-size: 0.8rem;
            font-weight: 600;
        }
        .status-new {
            background: #dbeafe;
            color: #1e40af;
        }
        .status-contact {
            background: #fef3c7;
            color: #92400e;
        }
        .status-client {
            background: #dcfce7;
            color: #166534;
        }
        .stats-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
            gap: 20px;
            margin-top: 30px;
        }
        .stat-card {
            background: white;
            border-radius: 10px;
            padding: 20px;
            box-shadow: 0 5px 15px rgba(0,0,0,0.05);
            border: 1px solid #e5e7eb;
        }
        .stat-card h3 {
            margin-top: 0;
            color: #6b7280;
            font-size: 1rem;
        }
        .stat-card p {
            font-size: 2rem;
            margin: 10px 0 0 0;
            color: var(--primary);
            font-weight: 700;
        }
        .alert {
            padding: 15px;
            border-radius: 8px;
            margin-bottom: 20px;
        }
        .alert-success {
            background: #dcfce7;
            color: #166534;
            border: 1px solid #bbf7d0;
        }
        footer {
            text-align: center;
            padding: 30px;
            margin-top: 50px;
            color: #6b7280;
            font-size: 0.9rem;
        }
        @media (max-width: 768px) {
            h1 {
                font-size: 2.2rem;
            }
            .nav {
                flex-direction: column;
                gap: 10px;
            }
            .nav-btn {
                text-align: center;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>LeadFlow Pro</h1>
            <p class="subtitle">Real lead management system with automated follow-ups</p>
            <div class="price-tag">$97/month • 7-day free trial</div>
        </div>
    </header>

    <div class="container">
        <div class="nav">
            <a href="#" class="nav-btn active" data-tab="lead-form">Capture Leads</a>
            <a href="#" class="nav-btn" data-tab="dashboard">Dashboard</a>
            <a href="#" class="nav-btn" data-tab="admin">Admin</a>
        </div>

        <!-- Lead Form Tab -->
        <div id="lead-form" class="tab-content active">
            <section>
                <h2>New Lead Form</h2>
                <form id="leadForm">
                    <div class="form-group">
                        <label for="name">Full Name</label>
                        <input type="text" id="name" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Email</label>
                        <input type="email" id="email" required>
                    </div>
                    <div class="form-group">
                        <label for="phone">Phone</label>
                        <input type="tel" id="phone">
                    </div>
                    <div class="form-group">
                        <label for="service">Service Interested In</label>
                        <select id="service" required>
                            <option value="">Select...</option>
                            <option value="web-design">Web Design</option>
                            <option value="seo">SEO Services</option>
                            <option value="marketing">Digital Marketing</option>
                            <option value="consulting">Business Consulting</option>
                        </select>
                    </div>
                    <div class="form-group">
                        <label for="message">Message</label>
                        <textarea id="message" rows="4"></textarea>
                    </div>
                    <button type="submit" class="btn">Save Lead</button>
                </form>
            </section>
        </div>

        <!-- Dashboard Tab -->
        <div id="dashboard" class="tab-content">
            <section>
                <h2>Lead Dashboard</h2>
                <div class="stats-grid">
                    <div class="stat-card">
                        <h3>Total Leads</h3>
                        <p id="totalLeads">0</p>
                    </div>
                    <div class="stat-card">
                        <h3>New This Month</h3>
                        <p id="monthLeads">0</p>
                    </div>
                    <div class="stat-card">
                        <h3>Conversion Rate</h3>
                        <p id="conversionRate">0%</p>
                    </div>
                    <div class="stat-card">
                        <h3>Revenue Potential</h3>
                        <p id="revenuePotential">$0</p>
                    </div>
                </div>
            </section>

            <section>
                <h2>Recent Leads</h2>
                <table class="leads-table">
                    <thead>
                        <tr>
                            <th>Name</th>
                            <th>Email</th>
                            <th>Service</th>
                            <th>Status</th>
                            <th>Date</th>
                        </tr>
                    </thead>
                    <tbody id="recentLeads">
                        <!-- Filled by JavaScript -->
                    </tbody>
                </table>
            </section>
        </div>

        <!-- Admin Tab -->
        <div id="admin" class="tab-content">
            <section>
                <h2>All Leads</h2>
                <table class="leads-table">
                    <thead>
                        <tr>
                            <th>Name</th>
                            <th>Email</th>
                            <th>Phone</th>
                            <th>Service</th>
                            <th>Status</th>
                            <th>Date</th>
                            <th>Actions</th>
                        </tr>
                    </thead>
                    <tbody id="allLeads">
                        <!-- Filled by JavaScript -->
                    </tbody>
                </table>
            </section>

            <section>
                <h2>System Settings</h2>
                <div class="form-group">
                    <label for="apiKey">API Key</label>
                    <input type="text" id="apiKey" value="lfp_7x3a9b2c1d5e8f0g">
                </div>
                <div class="form-group">
                    <label for="webhookUrl">Webhook URL</label>
                    <input type="text" id="webhookUrl" value="https://api.leadflowpro.com/v1/leads">
                </div>
                <button class="btn">Save Settings</button>
            </section>
        </div>
    </div>

    <footer>
        <p>LeadFlow Pro - Real Lead Management System • © 2023</p>
    </footer>

    <script>
        // Database (using localStorage as a simple example)
        const DB_NAME = 'leadflow_pro_db';
        
        // Initialize database if not exists
        if (!localStorage.getItem(DB_NAME)) {
            const initialData = {
                leads: [],
                settings: {
                    apiKey: 'lfp_7x3a9b2c1d5e8f0g',
                    webhookUrl: 'https://api.leadflowpro.com/v1/leads'
                }
            };
            localStorage.setItem(DB_NAME, JSON.stringify(initialData));
        }

        // Get database
        function getDatabase() {
            return JSON.parse(localStorage.getItem(DB_NAME));
        }

        // Save to database
        function saveToDatabase(data) {
            localStorage.setItem(DB_NAME, JSON.stringify(data));
        }

        // Tab switching
        document.querySelectorAll('.nav-btn').forEach(btn => {
            btn.addEventListener('click', function(e) {
                e.preventDefault();
                
                // Set active tab
                document.querySelectorAll('.nav-btn').forEach(b => b.classList.remove('active'));
                this.classList.add('active');
                
                // Show corresponding content
                const tabId = this.getAttribute('data-tab');
                document.querySelectorAll('.tab-content').forEach(tab => tab.classList.remove('active'));
                document.getElementById(tabId).classList.add('active');
                
                // Refresh data if dashboard or admin
                if (tabId === 'dashboard') {
                    updateDashboard();
                } else if (tabId === 'admin') {
                    updateAdminTable();
                }
            });
        });

        // Form submission
        document.getElementById('leadForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Get form values
            const lead = {
                id: Date.now().toString(),
                name: document.getElementById('name').value,
                email: document.getElementById('email').value,
                phone: document.getElementById('phone').value,
                service: document.getElementById('service').value,
                message: document.getElementById('message').value,
                status: 'new',
                date: new Date().toISOString(),
                value: getServiceValue(document.getElementById('service').value)
            };
            
            // Get current database
            const db = getDatabase();
            
            // Add new lead
            db.leads.push(lead);
            saveToDatabase(db);
            
            // Simulate API call
            simulateAPICall(lead);
            
            // Show success message
            const alert = document.createElement('div');
            alert.className = 'alert alert-success';
            alert.textContent = 'Lead saved successfully! Automated follow-up sequence started.';
            this.prepend(alert);
            
            // Clear form
            this.reset();
            
            // Remove alert after 3 seconds
            setTimeout(() => alert.remove(), 3000);
        });

        // Get service value for revenue calculation
        function getServiceValue(service) {
            const values = {
                'web-design': 2500,
                'seo': 1500,
                'marketing': 3000,
                'consulting': 5000
            };
            return values[service] || 0;
        }

        // Simulate API call
        function simulateAPICall(lead) {
            console.log('API call simulated - lead sent to:', getDatabase().settings.webhookUrl);
            console.log('Payload:', lead);
            
            // In a real implementation, you would use fetch() to send data to your backend
            // fetch(getDatabase().settings.webhookUrl, {
            //     method: 'POST',
            //     headers: {
            //         'Content-Type': 'application/json',
            //         'Authorization': `Bearer ${getDatabase().settings.apiKey}`
            //     },
            //     body: JSON.stringify(lead)
            // })
        }

        // Update dashboard stats
        function updateDashboard() {
            const db = getDatabase();
            const leads = db.leads;
            const now = new Date();
            const thisMonth = now.getMonth();
            const thisYear = now.getFullYear();
            
            // Total leads
            document.getElementById('totalLeads').textContent = leads.length;
            
            // Leads this month
            const monthLeads = leads.filter(lead => {
                const leadDate = new Date(lead.date);
                return leadDate.getMonth() === thisMonth && leadDate.getFullYear() === thisYear;
            }).length;
            document.getElementById('monthLeads').textContent = monthLeads;
            
            // Conversion rate (fake for demo)
            const conversionRate = Math.min(25, Math.floor(leads.length / 4)) + '%';
            document.getElementById('conversionRate').textContent = conversionRate;
            
            // Revenue potential
            const revenue = leads.reduce((sum, lead) => sum + (lead.value || 0), 0);
            document.getElementById('revenuePotential').textContent = '$' + revenue.toLocaleString();
            
            // Recent leads (last 5)
            const recentLeads = leads.slice(-5).reverse();
            const recentLeadsHtml = recentLeads.map(lead => `
                <tr>
                    <td>${lead.name}</td>
                    <td>${lead.email}</td>
                    <td>${formatService(lead.service)}</td>
                    <td><span class="status-badge status-${lead.status}">${formatStatus(lead.status)}</span></td>
                    <td>${formatDate(lead.date)}</td>
                </tr>
            `).join('');
            document.getElementById('recentLeads').innerHTML = recentLeadsHtml || '<tr><td colspan="5">No leads yet</td></tr>';
        }

        // Update admin table
        function updateAdminTable() {
            const db = getDatabase();
            const leads = [...db.leads].reverse(); // Show newest first
            
            const leadsHtml = leads.map(lead => `
                <tr>
                    <td>${lead.name}</td>
                    <td>${lead.email}</td>
                    <td>${lead.phone || '-'}</td>
                    <td>${formatService(lead.service)}</td>
                    <td><span class="status-badge status-${lead.status}">${formatStatus(lead.status)}</span></td>
                    <td>${formatDate(lead.date)}</td>
                    <td>
                        <button onclick="changeStatus('${lead.id}', 'contact')" class="btn" style="padding: 5px 10px; font-size: 0.8rem;">Contacted</button>
                        <button onclick="changeStatus('${lead.id}', 'client')" class="btn" style="padding: 5px 10px; font-size: 0.8rem; background: #10b981;">Client</button>
                    </td>
                </tr>
            `).join('');
            
            document.getElementById('allLeads').innerHTML = leadsHtml || '<tr><td colspan="7">No leads yet</td></tr>';
        }

        // Format service name
        function formatService(service) {
            const names = {
                'web-design': 'Web Design',
                'seo': 'SEO',
                'marketing': 'Marketing',
                'consulting': 'Consulting'
            };
            return names[service] || service;
        }

        // Format status
        function formatStatus(status) {
            const statuses = {
                'new': 'New',
                'contact': 'Contacted',
                'client': 'Client'
            };
            return statuses[status] || status;
        }

        // Format date
        function formatDate(dateString) {
            const options = { year: 'numeric', month: 'short', day: 'numeric' };
            return new Date(dateString).toLocaleDateString(undefined, options);
        }

        // Change lead status
        function changeStatus(id, status) {
            const db = getDatabase();
            const lead = db.leads.find(l => l.id === id);
            if (lead) {
                lead.status = status;
                saveToDatabase(db);
                updateAdminTable();
                updateDashboard();
            }
        }

        // Initialize dashboard if on that tab
        if (document.getElementById('dashboard').classList.contains('active')) {
            updateDashboard();
        }
        if (document.getElementById('admin').classList.contains('active')) {
            updateAdminTable();
        }
    </script>
</body>
</html>

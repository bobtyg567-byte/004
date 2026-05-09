<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0, viewport-fit=cover">
    <title>Admin Panel | Portfolio Manager</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        body {
            font-family: 'Inter', system-ui, -apple-system, 'Segoe UI', Roboto, sans-serif;
            background: #0f172a;
            color: #e2e8f0;
            padding: 2rem 1.5rem;
        }
        .admin-container {
            max-width: 1400px;
            margin: 0 auto;
        }
        /* cards */
        .glass-card {
            background: rgba(30, 41, 59, 0.75);
            backdrop-filter: blur(2px);
            border: 1px solid #334155;
            border-radius: 2rem;
            padding: 1.8rem;
            margin-bottom: 2rem;
            box-shadow: 0 20px 35px -12px rgba(0,0,0,0.3);
        }
        h1 {
            font-size: 2rem;
            font-weight: 700;
            margin-bottom: 0.5rem;
            background: linear-gradient(145deg, #c084fc, #60a5fa);
            background-clip: text;
            -webkit-background-clip: text;
            color: transparent;
        }
        h2 {
            font-size: 1.5rem;
            margin: 1.5rem 0 1rem 0;
            border-left: 4px solid #3b82f6;
            padding-left: 1rem;
        }
        .form-group {
            margin-bottom: 1.2rem;
        }
        label {
            display: block;
            font-weight: 500;
            margin-bottom: 0.4rem;
            font-size: 0.85rem;
            letter-spacing: 0.3px;
            color: #cbd5e1;
        }
        input, textarea {
            width: 100%;
            padding: 0.8rem 1rem;
            background: #1e293b;
            border: 1px solid #475569;
            border-radius: 1rem;
            color: #f1f5f9;
            font-size: 0.95rem;
            transition: 0.2s;
        }
        input:focus, textarea:focus {
            outline: none;
            border-color: #3b82f6;
            box-shadow: 0 0 0 2px rgba(59,130,246,0.3);
        }
        button {
            background: #3b82f6;
            border: none;
            padding: 0.7rem 1.5rem;
            border-radius: 2rem;
            font-weight: 600;
            color: white;
            cursor: pointer;
            transition: 0.2s;
            font-size: 0.85rem;
        }
        button:hover {
            background: #2563eb;
            transform: scale(0.98);
        }
        .btn-outline {
            background: transparent;
            border: 1px solid #5b6e8c;
            color: #cbd5e1;
        }
        .btn-outline:hover {
            background: #334155;
            border-color: #94a3b8;
        }
        .btn-danger {
            background: #dc2626;
        }
        .btn-danger:hover {
            background: #b91c1c;
        }
        .project-list {
            display: flex;
            flex-direction: column;
            gap: 1rem;
            margin-top: 1rem;
        }
        .project-item {
            background: #0f172a;
            border-radius: 1.2rem;
            padding: 1rem 1.2rem;
            display: flex;
            flex-wrap: wrap;
            justify-content: space-between;
            align-items: center;
            gap: 0.8rem;
            border: 1px solid #334155;
        }
        .project-info {
            flex: 3;
        }
        .project-title {
            font-weight: 700;
            font-size: 1.1rem;
        }
        .project-desc-sm {
            font-size: 0.8rem;
            color: #94a3b8;
        }
        .project-actions {
            display: flex;
            gap: 0.6rem;
        }
        .edit-mode {
            background: #1e293b;
            padding: 0.5rem;
            border-radius: 1rem;
            margin-top: 0.5rem;
        }
        .flex-btns {
            display: flex;
            gap: 0.8rem;
            flex-wrap: wrap;
            margin-top: 1rem;
        }
        .login-box {
            max-width: 480px;
            margin: 5rem auto;
            background: #1e293b;
            border-radius: 2rem;
            padding: 2rem;
            text-align: center;
        }
        .logout-bar {
            display: flex;
            justify-content: flex-end;
            margin-bottom: 1.5rem;
        }
        .toast-msg {
            background: #10b981;
            color: white;
            padding: 0.5rem 1rem;
            border-radius: 60px;
            font-size: 0.8rem;
            position: fixed;
            bottom: 20px;
            right: 20px;
            z-index: 1000;
            animation: fade 2s ease;
        }
        @keyframes fade {
            0% { opacity: 0; transform: translateY(10px);}
            10% { opacity: 1; transform: translateY(0);}
            90% { opacity: 1; }
            100% { opacity: 0; display: none;}
        }
        hr {
            border-color: #334155;
            margin: 1rem 0;
        }
        .preview-img {
            width: 60px;
            height: 60px;
            border-radius: 50%;
            object-fit: cover;
            margin-top: 0.5rem;
            border: 1px solid #475569;
        }
    </style>
</head>
<body>
<div id="adminRoot" class="admin-container"></div>

<script>
    const STORAGE_KEY = "portfolio_data";
    const PASSWORD = "Santonur2077runner";
    let currentData = null;
    let editingProjectId = null;   // for inline editing UI state

    // helper load from localStorage
    function loadData() {
        const stored = localStorage.getItem(STORAGE_KEY);
        if (stored) {
            try {
                const parsed = JSON.parse(stored);
                if (!parsed.projects) parsed.projects = [];
                if (!parsed.profile) parsed.profile = { name: "Alex Rivera", description: "Developer", pictureUrl: "https://randomuser.me/api/portraits/men/32.jpg" };
                currentData = parsed;
                return parsed;
            } catch(e) {}
        }
        const defaultData = {
            profile: {
                name: "Alex Rivera",
                description: "Creative Full-Stack Developer with 6+ years of passion for building sleek web apps.",
                pictureUrl: "https://randomuser.me/api/portraits/men/32.jpg"
            },
            projects: [
                { id: "proj1", name: "Nebula Dashboard", description: "Analytics dashboard with live data & real-time charts.", liveLink: "https://github.com/" },
                { id: "proj2", name: "Horizon E-commerce", description: "Full-stack e-commerce platform with cart & payments.", liveLink: "https://github.com/" }
            ]
        };
        localStorage.setItem(STORAGE_KEY, JSON.stringify(defaultData));
        currentData = defaultData;
        return defaultData;
    }

    function saveDataToStorage(data) {
        localStorage.setItem(STORAGE_KEY, JSON.stringify(data));
        currentData = data;
        // trigger storage event for portfolio page
        window.dispatchEvent(new StorageEvent('storage', { key: STORAGE_KEY, newValue: JSON.stringify(data) }));
    }

    function showToast(msg, isError = false) {
        const toast = document.createElement('div');
        toast.className = 'toast-msg';
        toast.style.backgroundColor = isError ? '#ef4444' : '#10b981';
        toast.innerText = msg;
        document.body.appendChild(toast);
        setTimeout(() => toast.remove(), 2000);
    }

    // ==== RENDER ADMIN (protected) ====
    function renderAdminPanel() {
        if (!currentData) loadData();
        const root = document.getElementById("adminRoot");
        const profile = currentData.profile;
        const projects = currentData.projects || [];

        root.innerHTML = `
            <div class="logout-bar">
                <button id="logoutBtn" class="btn-outline" style="background:#1e293b;">🚪 Logout</button>
            </div>
            <h1>⚙️ Portfolio Control Center</h1>
            <p style="color:#94a3b8; margin-bottom: 1.5rem;">Manage profile, projects, and content — real-time sync with portfolio</p>
            
            <!-- Profile Section -->
            <div class="glass-card">
                <h2>👤 Profile Settings</h2>
                <div class="form-group">
                    <label>Full Name</label>
                    <input type="text" id="adminName" value="${escapeHtml(profile.name || '')}" placeholder="Your name">
                </div>
                <div class="form-group">
                    <label>Bio / Description</label>
                    <textarea id="adminBio" rows="3" placeholder="Short professional intro">${escapeHtml(profile.description || '')}</textarea>
                </div>
                <div class="form-group">
                    <label>Profile Picture URL (online image link)</label>
                    <input type="text" id="adminPictureUrl" value="${escapeHtml(profile.pictureUrl || '')}" placeholder="https://... image">
                </div>
                <div class="flex-btns">
                    <button id="updateProfileBtn">💾 Update Profile</button>
                    <div><img id="previewAvatar" class="preview-img" src="${escapeHtml(profile.pictureUrl) || 'https://randomuser.me/api/portraits/men/1.jpg'}" alt="preview"></div>
                </div>
            </div>
            
            <!-- Projects Management -->
            <div class="glass-card">
                <h2>📁 Projects (Add / Edit / Remove)</h2>
                <div style="background:#0f172a; padding:1rem; border-radius:1.2rem; margin-bottom:1.5rem;">
                    <h3 style="margin-bottom:0.8rem;">➕ Add New Project</h3>
                    <div class="form-group">
                        <label>Project Name</label>
                        <input type="text" id="newProjName" placeholder="e.g., AI Image Generator">
                    </div>
                    <div class="form-group">
                        <label>Description</label>
                        <textarea id="newProjDesc" rows="2" placeholder="Project description"></textarea>
                    </div>
                    <div class="form-group">
                        <label>Live Link (URL)</label>
                        <input type="text" id="newProjLink" placeholder="https://example.com">
                    </div>
                    <button id="addProjectBtn">✨ Add Project</button>
                </div>
                
                <h3>📋 Current Projects (manage all)</h3>
                <div id="projectsListContainer" class="project-list"></div>
            </div>
        `;

        // attach listeners
        document.getElementById("updateProfileBtn")?.addEventListener("click", updateProfileHandler);
        document.getElementById("addProjectBtn")?.addEventListener("click", addProjectHandler);
        document.getElementById("logoutBtn")?.addEventListener("click", logoutHandler);
        
        // live preview image
        const picInput = document.getElementById("adminPictureUrl");
        const previewImg = document.getElementById("previewAvatar");
        if(picInput && previewImg) {
            picInput.addEventListener("input", (e) => {
                previewImg.src = e.target.value || "https://randomuser.me/api/portraits/men/1.jpg";
            });
        }
        
        renderProjectsList(projects);
    }
    
    function renderProjectsList(projects) {
        const container = document.getElementById("projectsListContainer");
        if (!container) return;
        if (!projects.length) {
            container.innerHTML = `<div style="padding:1rem; background:#1e293b; border-radius:1rem; text-align:center;">✨ No projects yet — add your first project above ✨</div>`;
            return;
        }
        container.innerHTML = "";
        projects.forEach(proj => {
            const isEditing = (editingProjectId === proj.id);
            const projectDiv = document.createElement("div");
            projectDiv.className = "project-item";
            if(!isEditing) {
                projectDiv.innerHTML = `
                    <div class="project-info">
                        <div class="project-title">📌 ${escapeHtml(proj.name)}</div>
                        <div class="project-desc-sm">${escapeHtml(proj.description.substring(0, 80))}${proj.description.length>80 ? '...' : ''}</div>
                        <div style="font-size:0.7rem; margin-top:0.2rem; color:#7e8aa2;">🔗 ${escapeHtml(proj.liveLink)}</div>
                    </div>
                    <div class="project-actions">
                        <button class="edit-proj-btn" data-id="${proj.id}" style="background:#4b5563;">✏️ Edit</button>
                        <button class="delete-proj-btn" data-id="${proj.id}" style="background:#b91c1c;">🗑️ Delete</button>
                    </div>
                `;
            } else {
                // inline edit mode
                projectDiv.innerHTML = `
                    <div style="width:100%;">
                        <div class="form-group"><label>Name</label><input id="edit_name_${proj.id}" value="${escapeHtml(proj.name)}"></div>
                        <div class="form-group"><label>Description</label><textarea id="edit_desc_${proj.id}" rows="2">${escapeHtml(proj.description)}</textarea></div>
                        <div class="form-group"><label>Live Link</label><input id="edit_link_${proj.id}" value="${escapeHtml(proj.liveLink)}"></div>
                        <div class="flex-btns" style="justify-content:flex-end;">
                            <button class="save-edit-btn" data-id="${proj.id}" style="background:#3b82f6;">💾 Save</button>
                            <button class="cancel-edit-btn" data-id="${proj.id}" class="btn-outline">Cancel</button>
                        </div>
                    </div>
                `;
            }
            container.appendChild(projectDiv);
        });
        
        // attach delete / edit / save listeners
        document.querySelectorAll(".delete-proj-btn").forEach(btn => {
            btn.addEventListener("click", (e) => {
                const id = btn.getAttribute("data-id");
                deleteProjectById(id);
            });
        });
        document.querySelectorAll(".edit-proj-btn").forEach(btn => {
            btn.addEventListener("click", (e) => {
                const id = btn.getAttribute("data-id");
                editingProjectId = id;
                renderAdminPanel(); // re-render with edit mode
            });
        });
        document.querySelectorAll(".save-edit-btn").forEach(btn => {
            btn.addEventListener("click", (e) => {
                const id = btn.getAttribute("data-id");
                const newName = document.getElementById(`edit_name_${id}`)?.value.trim();
                const newDesc = document.getElementById(`edit_desc_${id}`)?.value.trim();
                const newLink = document.getElementById(`edit_link_${id}`)?.value.trim();
                if (!newName) return showToast("Project name required", true);
                const projectsArr = currentData.projects;
                const index = projectsArr.findIndex(p => p.id === id);
                if (index !== -1) {
                    projectsArr[index] = { ...projectsArr[index], name: newName, description: newDesc || "", liveLink: newLink || "#" };
                    saveDataToStorage(currentData);
                    showToast("Project updated ✅");
                    editingProjectId = null;
                    renderAdminPanel();
                }
            });
        });
        document.querySelectorAll(".cancel-edit-btn").forEach(btn => {
            btn.addEventListener("click", () => {
                editingProjectId = null;
                renderAdminPanel();
            });
        });
    }
    
    // Profile update handler
    function updateProfileHandler() {
        const name = document.getElementById("adminName")?.value.trim();
        const bio = document.getElementById("adminBio")?.value;
        const pictureUrl = document.getElementById("adminPictureUrl")?.value.trim();
        if (!name) return showToast("Name cannot be empty", true);
        currentData.profile = {
            name: name,
            description: bio || "",
            pictureUrl: pictureUrl || "https://randomuser.me/api/portraits/men/1.jpg"
        };
        saveDataToStorage(currentData);
        showToast("Profile updated successfully 🎉");
        renderAdminPanel(); // refresh preview
    }
    
    function addProjectHandler() {
        const name = document.getElementById("newProjName")?.value.trim();
        const desc = document.getElementById("newProjDesc")?.value.trim();
        const link = document.getElementById("newProjLink")?.value.trim();
        if (!name) return showToast("Project name required", true);
        const newProject = {
            id: "proj_" + Date.now() + "_" + Math.random().toString(36).substr(2, 6),
            name: name,
            description: desc || "No description",
            liveLink: link || "#"
        };
        currentData.projects.push(newProject);
        saveDataToStorage(currentData);
        document.getElementById("newProjName").value = "";
        document.getElementById("newProjDesc").value = "";
        document.getElementById("newProjLink").value = "";
        showToast("Project added! 🚀");
        renderAdminPanel();
    }
    
    function deleteProjectById(id) {
        if (confirm("Remove this project permanently?")) {
            const filtered = currentData.projects.filter(p => p.id !== id);
            currentData.projects = filtered;
            saveDataToStorage(currentData);
            editingProjectId = null;
            showToast("Project removed");
            renderAdminPanel();
        }
    }
    
    function logoutHandler() {
        sessionStorage.removeItem("portfolio_admin_auth");
        showToast("Logged out");
        renderAuthScreen();
    }
    
    // ---------- AUTHENTICATION ----------
    function renderAuthScreen() {
        const root = document.getElementById("adminRoot");
        root.innerHTML = `
            <div class="login-box">
                <h2>🔒 Admin Access</h2>
                <p style="margin-bottom: 1.5rem;">Enter secure password to manage portfolio</p>
                <input type="password" id="adminPassword" placeholder="Password" style="margin-bottom: 1rem;">
                <button id="loginBtn">Unlock Panel</button>
            </div>
        `;
        document.getElementById("loginBtn")?.addEventListener("click", () => {
            const pass = document.getElementById("adminPassword")?.value;
            if (pass === PASSWORD) {
                sessionStorage.setItem("portfolio_admin_auth", "true");
                showToast("Access granted");
                initAdmin();
            } else {
                showToast("Invalid password ❌", true);
            }
        });
    }
    
    function checkAuth() {
        return sessionStorage.getItem("portfolio_admin_auth") === "true";
    }
    
    function initAdmin() {
        if (!checkAuth()) {
            renderAuthScreen();
            return;
        }
        loadData();
        editingProjectId = null;
        renderAdminPanel();
    }
    
    function escapeHtml(str) {
        if (!str) return "";
        return str.replace(/[&<>]/g, function(m) {
            if(m === '&') return '&amp;';
            if(m === '<') return '&lt;';
            if(m === '>') return '&gt;';
            return m;
        });
    }
    
    // start
    initAdmin();
    // optional: storage sync across tabs
    window.addEventListener("storage", (e) => {
        if(e.key === STORAGE_KEY && checkAuth()) {
            loadData();
            renderAdminPanel();
        }
    });
</script>
</body>
</html>
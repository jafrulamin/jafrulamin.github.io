# Homework 1 Reflection

## 1. HTTP Request Path from Browser to GitHub Pages

When a user visits a GitHub Pages site (e.g., `https://jafrulamin.github.io`), the HTTP request follows this path:

1. **Browser** → User enters URL or clicks a link
2. **DNS Resolution** → Browser queries DNS to resolve `jafrulamin.github.io` to GitHub's IP address
3. **TCP Connection** → Browser establishes a TCP connection to GitHub's servers
4. **HTTP Request** → Browser sends an HTTP GET request:
   - Request line: `GET / HTTP/1.1` (or `GET /index.html HTTP/1.1`)
   - Host header: `Host: jafrulamin.github.io`
   - Additional headers (User-Agent, Accept, etc.)
5. **GitHub Pages Server** → Receives the request and serves the static files from the repository
6. **HTTP Response** → Server sends back:
   - Status code (200 OK)
   - HTML content (index.html)
   - Headers indicating content type
7. **Browser Rendering** → Browser receives HTML, parses it, and makes additional requests for linked resources (CSS, images from `assets/headshot.jpg`)

The actual HTTP request path is: `GET / HTTP/1.1` sent to GitHub's servers, which then serves the static files from the repository.

## 2. Docker Container vs GitHub Pages Environment

**Docker Container:**
- Runs in an isolated, containerized environment
- Requires Docker daemon and container runtime to be installed
- Can run any application stack (Node.js, Python, databases, web servers, etc.)
- Full control over the operating system, dependencies, and configuration
- Requires building Docker images and running containers
- Suitable for dynamic applications with backends, databases, and server-side processing
- More complex setup but provides flexibility for full-stack applications

**GitHub Pages:**
- Static file hosting only (HTML, CSS, JavaScript, images)
- No server-side processing capabilities (no PHP, Python, Node.js backends)
- Automatically deployed from the repository when files are pushed
- Free hosting with automatic HTTPS
- Simple workflow: push files to repo, GitHub Pages serves them
- Limited to static content only (no databases, no server-side code execution)
- Automatically handles CDN distribution and caching

**Key Difference:** Docker containers can run dynamic applications with backends and databases, while GitHub Pages only serves static files. For this homework assignment (plain HTML + CSS), GitHub Pages is the simpler and more appropriate choice since no server-side processing is needed.

## 3. AI Attribution

**Exact Prompt Used:**
"You are Cursor. Update my GitHub Pages portfolio to a clean, resume-style layout, using only plain HTML + CSS (no frameworks, no JS)."

**Logic Error AI Made:**
I asked the AI to add a `<nav>` element with navigation links in the header to meet the assignment requirement for semantic HTML tags. However, when I later requested to remove the navigation buttons for design reasons, the AI removed the `<nav>` element entirely. This created a problem because the assignment requirements specifically state that semantic HTML must include `<nav>`. The AI failed to recognize that removing the navigation would cause the project to fail the semantic HTML requirement, even if the navigation wasn't visually needed for the design.

**How I Fixed It:**
I re-added the `<nav>` element to the HTML structure to satisfy the assignment requirement for semantic HTML tags, ensuring the project meets all criteria even if the navigation isn't prominently displayed in the final design.

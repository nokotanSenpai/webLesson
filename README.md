TỔNG HỢP KIẾN THỨC & KEYWORD LẬP TRÌNH WEB (HTML, CSS, JS)Tài liệu này tổng hợp toàn bộ các từ khóa (keywords) cốt lõi, cấu trúc và mã mẫu chuẩn từ giáo trình HTML5, CSS3, JavaScript và AI Integration.MỤC LỤCHTML5: Cấu trúc & Ngữ nghĩa (Semantic Layout)HTML5: Forms, Inputs & MultimediaHTML5: Canvas, Storage & Browser APIsCSS3: Selectors, Specificity & Box ModelCSS3: Layouts (Flexbox & Grid)CSS3: Animations, Modern Units & NestingJavaScript: Cốt lõi & DOM ManipulationJavaScript: Modern ES6+ & Asynchronous (Async/Await)Tích hợp AI & Chatbot Frontend1. HTML5: Cấu trúc & Ngữ nghĩa (Semantic Layout)📌 Keyword Cốt Lõi:<!DOCTYPE html>: Khai báo chuẩn HTML5.<header>: Phần đầu trang (logo, title, main menu).<nav>: Khối chứa các liên kết điều hướng (navigation).<main>: Nội dung chính độc nhất của trang.<section>: Phân đoạn nội dung có cùng chủ đề.<article>: Bài viết hoặc nội dung độc lập (blog post, news item).<aside>: Nội dung phụ, sidebar, quảng cáo, tin liên quan.<footer>: Chân trang (bản quyền, contact, links).<figure>, <figcaption>: Chứa hình ảnh/đồ họa đi kèm chú thích.💻 Mẫu Code Chuẩn:<!DOCTYPE html>
<html lang="vi">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>HTML5 Semantic Structure</title>
</head>
<body>
    <header>
        <h1>Website BookStore</h1>
        <nav>
            <ul>
                <li><a href="#home">Trang chủ</a></li>
                <li><a href="#products">Sản phẩm</a></li>
            </ul>
        </nav>
    </header>

    <main>
        <section id="featured">
            <article>
                <h2>Sách Lập Trình Web</h2>
                <figure>
                    <img src="book.jpg" alt="Mô tả sách">
                    <figcaption>Hình 1: Sách Hướng Dẫn HTML5 & CSS3</figcaption>
                </figure>
                <p>Nội dung chi tiết bài viết...</p>
            </article>
        </section>

        <aside>
            <h3>Bài viết xem nhiều</h3>
        </aside>
    </main>

    <footer>
        <p>&copy; 2026 BookStore. All rights reserved.</p>
    </footer>
</body>
</html>
2. HTML5: Forms, Inputs & Multimedia📌 Keyword Cốt Lõi:Input Types: email, url, tel, number, range, date, color, search.Form Attributes: placeholder, required, pattern, autofocus, multiple, form.Form Elements: <datalist>, <progress>, <meter>.Multimedia Tags & Attributes: <audio>, <video>, <track> (subtitles/captions).Media Attributes: controls, autoplay, loop, muted, preload="auto|metadata|none".💻 Mẫu Code Chuẩn:<!-- Form chuẩn với HTML5 Validation -->
<form action="/submit" method="POST">
    <label for="user-email">Email:</label>
    <input type="email" id="user-email" placeholder="example@gmail.com" required autofocus>

    <label for="phone">Số điện thoại (8-10 số):</label>
    <input type="tel" id="phone" pattern="[0-9]{8,10}" required>

    <label for="rating">Đánh giá (1 - 10):</label>
    <input type="range" id="rating" min="1" max="10" step="1">

    <label for="browser">Trình duyệt gợi ý:</label>
    <input list="browsers" name="browser">
    <datalist id="browsers">
        <option value="Chrome">
        <option value="Firefox">
        <option value="Edge">
    </datalist>

    <button type="submit">Gửi thông tin</button>
</form>

<!-- Video Player chuẩn có Phụ đề -->
<video width="640" height="360" controls preload="metadata">
    <source src="video.mp4" type="video/mp4">
    <source src="video.webm" type="video/webm">
    <track src="subtitles_vi.vtt" kind="subtitles" srclang="vi" label="Tiếng Việt" default>
    Trình duyệt của bạn không hỗ trợ thẻ video.
</video>
3. HTML5: Canvas, Storage & Browser APIs📌 Keyword Cốt Lõi:canvas: getContext('2d'), beginPath(), moveTo(), lineTo(), rect(), arc(), fillStyle, strokeStyle, stroke(), fill(), drawImage().Web Storage: localStorage (lưu vĩnh viễn), sessionStorage (lưu theo tab/session).Storage Methods: setItem(k, v), getItem(k), removeItem(k), clear().Geolocation API: navigator.geolocation, getCurrentPosition(), watchPosition(), clearWatch().Drag & Drop: draggable="true", ondragstart, ondragover, ondrop, event.preventDefault(), event.dataTransfer.💻 Mẫu Code Chuẩn:3.1 Vẽ trên Canvas (JS):const canvas = document.getElementById('myCanvas');
const ctx = canvas.getContext('2d');

// Vẽ hình chữ nhật filled
ctx.fillStyle = '#FF0000';
ctx.fillRect(10, 10, 150, 80);

// Vẽ đường tròn (arc)
ctx.beginPath();
ctx.arc(200, 100, 50, 0, 2 * Math.PI);
ctx.strokeStyle = '#00FF00';
ctx.lineWidth = 4;
ctx.stroke();
3.2 Web Storage & Geolocation:// LocalStorage
localStorage.setItem('theme', 'dark');
const currentTheme = localStorage.getItem('theme');

// Geolocation API
if ('geolocation' in navigator) {
    navigator.geolocation.getCurrentPosition(
        (position) => {
            console.log(`Lat: ${position.coords.latitude}, Lng: ${position.coords.longitude}`);
        },
        (error) => {
            console.error(`Lỗi vị trí: Code ${error.code} - ${error.message}`);
        },
        { enableHighAccuracy: true, timeout: 5000 }
    );
}
4. CSS3: Selectors, Specificity & Box Model📌 Keyword Cốt Lõi:Selectors: Type (p), Class (.btn), ID (#main), Universal (*).Combinators: Descendant (div p), Child (div > p), Adjacent Sibling (h1 + p).Pseudo-classes: :hover, :active, :focus, :first-child, :nth-child(), :has().Specificity Order: Inline Style > ID > Class/Attribute/Pseudo-class > Type/Element.CSS Box Model: content -> padding -> border -> margin.Box Sizing: box-sizing: border-box; (tính cả padding và border vào kích thước tổng).Positioning: static, relative, absolute, fixed, sticky, z-index.💻 Mẫu Code Chuẩn:/* Reset căn bản & Box Model chuẩn */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Selector & State */
.card {
    width: 300px;
    padding: 20px;
    border: 1px solid #ccc;
    position: relative;
    background-color: #fff;
    transition: transform 0.2s ease;
}

/* Pseudo-class chọn thẻ cha khi có thẻ con cụ thể (:has) */
.card:has(img) {
    border-color: #007bff;
}

.card:hover {
    transform: translateY(-5px);
}

/* Fixed Header */
.navbar {
    position: fixed;
    top: 0;
    left: 0;
    width: 100%;
    z-index: 1000;
}
5. CSS3: Layouts (Flexbox & Grid)📌 Keyword Cốt Lõi:Flexbox Container: display: flex, flex-direction (row/column), justify-content (main axis), align-items (cross axis), flex-wrap, gap.Flexbox Items: flex-grow, flex-shrink, flex-basis, align-self, order.Grid Container: display: grid, grid-template-columns (ví dụ: repeat(auto-fit, minmax(250px, 1fr))), grid-template-rows, grid-template-areas, gap.Grid Items: grid-column (ví dụ: 1 / span 2), grid-row, grid-area.Subgrid (CSS Grid Level 2): grid-template-columns: subgrid; (thừa hưởng lưới từ parent).💻 Mẫu Code Chuẩn:5.1 Flexbox Layout:.flex-container {
    display: flex;
    flex-direction: row;
    justify-content: space-between;
    align-items: center;
    gap: 20px;
}

.flex-item {
    flex: 1; /* Shorthand cho grow, shrink, basis */
}
5.2 Responsive Grid Layout:.grid-container {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 20px;
}

/* Grid Area Layout */
.page-layout {
    display: grid;
    grid-template-areas:
        "header header"
        "sidebar main"
        "footer footer";
    grid-template-columns: 250px 1fr;
}

.header { grid-area: header; }
.sidebar { grid-area: sidebar; }
.main { grid-area: main; }
.footer { grid-area: footer; }
6. CSS3: Animations, Modern Units & Nesting📌 Keyword Cốt Lõi:Units: Relative (em, rem, %), Viewport Units (vw, vh, vmin, vmax).Transitions: transition-property, transition-duration, transition-timing-function, transition-delay.Animations: @keyframes, animation-name, animation-duration, animation-iteration-count (infinite), animation-direction (alternate).CSS Nesting: Lồng trực tiếp selector con vào trong selector cha.Accent Color: accent-color: #ff0000; (đổi màu UI gốc của checkbox/radio).💻 Mẫu Code Chuẩn:/* Modern Viewport & Variables */
:root {
    --primary-color: #007bff;
}

/* CSS Nesting chuẩn hiện đại */
.nav-menu {
    background-color: #f8f9fa;
    padding: 1rem;

    & ul {
        list-style: none;
    }

    & a {
        color: var(--primary-color);
        text-decoration: none;

        &:hover {
            text-decoration: underline;
        }
    }
}

/* Keyframe Animation */
@keyframes pulse {
    0% { transform: scale(1); opacity: 1; }
    50% { transform: scale(1.05); opacity: 0.8; }
    100% { transform: scale(1); opacity: 1; }
}

.button-animated {
    animation: pulse 2s infinite ease-in-out;
    width: 20vmin; /* 20% kích thước cạnh nhỏ hơn của màn hình */
}
7. JavaScript: Cốt lõi & DOM Manipulation📌 Keyword Cốt Lõi:Khai báo biến: let (block scope, có thể gán lại), const (block scope, hằng số).DOM Selection: document.getElementById(), document.querySelector(), document.querySelectorAll().DOM Manipulation: textContent, innerHTML, setAttribute(), classList.add(), classList.toggle(), appendChild(), createElement().Event Handling: addEventListener(event, callback), preventDefault(), stopPropagation().Event Types: click, submit, keyup, DOMContentLoaded, mouseover.💻 Mẫu Code Chuẩn:document.addEventListener('DOMContentLoaded', () => {
    const mainTitle = document.querySelector('#main-title');
    const addBtn = document.querySelector('.btn-add');
    const container = document.querySelector('.item-list');

    // Đổi style & class
    mainTitle.textContent = 'Danh Sách Đã Cập Nhật';
    mainTitle.classList.add('active');

    // Bắt sự kiện Click
    addBtn.addEventListener('click', (e) => {
        e.preventDefault();

        // Tạo element mới
        const newItem = document.createElement('li');
        newItem.className = 'list-item';
        newItem.innerHTML = `Sản phẩm mới <button class="btn-del">Xóa</button>`;

        container.appendChild(newItem);
    });

    // Event Delegation (Ủy quyền sự kiện cho phần tử động)
    container.addEventListener('click', (e) => {
        if (e.target.classList.contains('btn-del')) {
            e.target.parentElement.remove();
        }
    });
});
8. JavaScript: Modern ES6+ & Asynchronous (Async/Await)📌 Keyword Cốt Lõi:ES6+ Features: Arrow Functions (() => {}), Template Literals (`text ${var}`), Destructuring, Spread/Rest Operator (...), Object.hasOwn().Arrays Non-Mutating (ES2023): toSorted(), toReversed(), toSpliced(), with().Class Private Fields: #privateField, #privateMethod().Asynchronous: Promise, async / await, fetch(), JSON.parse(), JSON.stringify().💻 Mẫu Code Chuẩn:8.1 Modern Class & Array Methods:class UserAccount {
    #password; // Private Field

    constructor(username, password) {
        this.username = username;
        this.#password = password;
    }

    verifyPassword(input) {
        return this.#password === input;
    }
}

// Immutable Array Methods (ES2023)
const numbers = [3, 1, 4, 1, 5];
const sortedNumbers = numbers.toSorted(); // Tạo bản sao, không sửa numbers gốc
console.log(numbers); // [3, 1, 4, 1, 5]
console.log(sortedNumbers); // [1, 1, 3, 4, 5]
8.2 Fetch API với Async/Await & Handling Errors:async function fetchProducts(url) {
    try {
        const response = await fetch(url);
        
        if (!response.ok) {
            throw new Error(`HTTP error! status: ${response.status}`);
        }

        const data = await response.json();
        return data;
    } catch (error) {
        console.error('Không thể lấy dữ liệu:', error.message);
    }
}

// Gọi hàm async với Top-level await (Module environment)
const products = await fetchProducts('https://api.example.com/products');
console.log(products);
9. Tích hợp AI & Chatbot Frontend📌 Keyword Cốt Lõi:AI Integration Methods: One-line Widget Scripts, Hand-coded Logic, API Integration.Chatbot Components: #chatbox, #messages (overflow-y: auto), #userInput, #sendBtn.Accessibility (Inclusive Design): Text-to-Speech (SpeechSynthesisUtterance), Alt-Text Generator, WCAG Compliance.Security & Ethics: Data Minimization (chỉ thu thập thông tin cần thiết), Client Consent, Encryption (HTTPS).💻 Mẫu Code Chuẩn (Hand-Coded Rule-Based Chatbot Logic):const chatMessages = document.getElementById('messages');
const userInput = document.getElementById('userInput');
const sendBtn = document.getElementById('sendBtn');

// Rule-based logic đơn giản
const botKnowledge = {
    "chào": "Xin chào! Tôi có thể giúp gì cho bạn về tài liệu lập trình?",
    "học phí": "Các tài liệu hướng dẫn trên trang đều miễn phí hoàn toàn.",
    "liên hệ": "Bạn có thể gửi mail tới support@example.com."
};

function appendMessage(sender, text) {
    const msgDiv = document.createElement('div');
    msgDiv.className = `message ${sender}-message`;
    msgDiv.textContent = text;
    chatMessages.appendChild(msgDiv);
    // Auto-scroll xuống tin nhắn mới nhất
    chatMessages.scrollTop = chatMessages.scrollHeight;
}

function handleSend() {
    const text = userInput.value.trim().toLowerCase();
    if (!text) return;

    appendMessage('user', userInput.value);
    userInput.value = '';

    // Xử lý phản hồi từ AI / Bot
    setTimeout(() => {
        let reply = "Xin lỗi, tôi chưa hiểu ý bạn. Bạn hãy thử từ khóa khác nhé!";
        for (let key in botKnowledge) {
            if (text.includes(key)) {
                reply = botKnowledge[key];
                break;
            }
        }
        appendMessage('bot', reply);
    }, 500);
}

sendBtn.addEventListener('click', handleSend);
userInput.addEventListener('keypress', (e) => {
    if (e.key === 'Enter') handleSend();
});

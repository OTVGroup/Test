<!DOCTYPE html>
<html lang="vi">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Mẫu XD01</title>
    <link
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css"
      rel="stylesheet"
    />

    <style>
      body {
        display: flex;
        justify-content: center; /* Căn giữa ngang */
        align-items: center; /* Căn giữa dọc */
        min-height: 100vh; /* Chiếm đủ chiều cao màn hình */
        width: calc(100% - 20px);
        margin: auto; /* Bỏ margin mặc định */
        font-family: Arial, sans-serif;
      }

      section {
        width: max(360px, 100%);
        padding: 10px;
        background: radial-gradient(
            150% 30px at 50% 0,
            var(--shadow) 0%,
            rgba(0, 0, 0, 0.2) 25%,
            rgba(0, 0, 0, 0.12) 50%,
            rgba(0, 0, 0, 0.08) 75%,
            transparent 100%
          ),
          var(--background);
        box-shadow: inset 0 1px 0 rgba(0, 0, 0, 0.06);
      }

      .main1 {
        font-size: calc(5px + 0.9vh + 0.9vw);
        font-weight: 600;
        line-height: 1.2;
        color: #000;
        text-align: center;
        margin: 0px auto 7.5px auto;
      }

      .main2 {
        font-size: calc(5px + 0.8vh + 0.8vw);
        font-weight: 600;
        line-height: 1.1;
        width: max-content;
        color: #202020;
        text-align: center;
        margin: 0px auto 5px auto;
      }

      .contact,
      .review {
        flex: 1;
        min-width: 340px;
        padding-top: 10px;
        border-top: 1px dashed white;
      }

      .contact-meta,
      .contact-social {
        margin-top: 10px;
        display: flex;
        align-items: center;
        justify-content: left;
      }

      .contact-meta i {
        width: calc(9px + 0.7vh + 0.7vw);
        font-size: calc(5px + 0.7vh + 0.7vw);
        margin-right: 5px;
        text-align: center;
      }

      .contact-meta a {
        font-size: calc(5px + 0.7vh + 0.7vw);
        color: white;
        text-decoration: none;
      }

      .contact-social i {
        font-size: calc(5px + 1.2vh + 1.2vw);
        margin: 10px clamp(10px, 10%, 20px);
        color: white;
        text-align: center;
      }

      .contact-copyright {
        font-size: calc(5px + 0.7vh + 0.7vw);
        text-align: center;
        margin-top: 10px;
        opacity: 0.8;
      }

      .review-form {
        display: flex;
        flex-direction: column;
        gap: 5px;
      }

      .review-form input,
      .review-form textarea {
        padding: 4px;
        border: 1px solid #ccc;
        border-radius: 5px;
        font-size: calc(5px + 0.7vh + 0.7vw);
        width: calc(100% - 10px);
        resize: vertical; /* chỉ cho phép kéo dọc, KHÓA kéo ngang */
        overflow-y: hidden; /* ẩn thanh cuộn ngang */
        white-space: pre-wrap; /* tự xuống dòng khi chữ dài */
        word-wrap: break-word; /* bẻ dòng khi từ quá dài */
      }

      .review button {
        padding: 5px;
        margin-top: 5px;
        background: #00d90e;
        color: rgb(0, 0, 0);
        border: none;
        border-radius: 5px;
        cursor: pointer;
        width: 100%;
        font-size: calc(5px + 0.8vh + 0.8vw);
        font-weight: 600;
      }

      .review button:hover {
        background: #2db500;
      }

      :root {
        --bg-color-bottom: #1e55ee;
      }
    </style>
  </head>
  <body>
    <section
      style="
        display: flex;
        gap: 20px;
        flex-wrap: wrap;
        --background: var(--bg-color-bottom);
        --shadow: rgba(0, 0, 0, 0.4);
        color: white;
      "
      id="contact"
    >
      <!-- Bên trái: Liên hệ -->
      <div class="contact">
        <div class="main2" style="color: white">LIÊN HỆ</div>
        <div class="contact-meta">
          <i class="fa-solid fa-phone"></i>
          <a href="tel:0329022431">+84 329 022 431</a>
        </div>
        <div class="contact-meta">
          <i class="fa-solid fa-envelope"></i>
          <a href="mailto:thinhkvtm2k6@gmail.com">thinhkvtm2k6@gmail.com</a>
        </div>
        <div class="contact-meta">
          <i class="fa-solid fa-location-dot"></i>
          <a href="https://maps.app.goo.gl/La6cgkz2bDgJ1uqe7"
            >Ho Chi Minh, Việt Nam</a
          >
        </div>

        <div class="contact-social">
          <a href="https://facebook.com/" target="_blank" aria-label="Facebook">
            <i class="fa-brands fa-facebook-f"></i>
          </a>
          <a href="https://youtube.com/" target="_blank" aria-label="YouTube">
            <i class="fa-brands fa-youtube"></i>
          </a>
          <a href="https://tiktok.com/" target="_blank" aria-label="TikTok">
            <i class="fa-brands fa-tiktok"></i>
          </a>
          <a
            href="https://instagram.com/"
            target="_blank"
            aria-label="Instagram"
          >
            <i class="fa-brands fa-instagram"></i>
          </a>
          <a href="https://threads.com" target="_blank" aria-label="Threads">
            <i class="fa-brands fa-threads"></i>
          </a>
        </div>

        <!-- Copyright -->
        <div class="contact-copyright">© <span id="year"></span> OTVGroup</div>
      </div>

      <!-- Bên phải: Form đánh giá -->
      <div class="review">
        <div class="main2" style="color: white">ĐÁNH GIÁ</div>
        <form class="review-form" id="reviewForm">
          <input type="text" name="name" placeholder="Họ và tên" required />
          <input type="email" name="email" placeholder="Email" required />
          <textarea
            rows="2"
            name="massage"
            placeholder="Nội dung đánh giá..."
            required
          ></textarea>
        </form>
        <button type="submit">Gửi đánh giá</button>
      </div>
    </section>

    <script>
      document.getElementById("year").textContent = new Date().getFullYear();
    </script>

    <script>
      const scriptURL =
        "https://script.google.com/macros/s/AKfycbzFxrKrkJ2Mp3oG0eAkZpo6AKJ0m6LOrfEq1LQy3M2ZZvWVwtFWNQY0oAPwHbAlFkBM4g/exec"; // dán URL Apps Script ở đây
      const form = document.getElementById("reviewForm");

      form.addEventListener("submit", (e) => {
        e.preventDefault();

        const data = {
          source: "OTVGroup",
          name: form.name.value,
          email: form.email.value,
          message: form.message.value,
        };

        fetch(scriptURL, {
          method: "POST",
          body: JSON.stringify(data),
          headers: { "Content-Type": "application/json" },
        })
          .then((res) => res.json())
          .then((res) => {
            if (res.result === "success") {
              alert("Gửi Thành Công!");
              form.reset();
            }
          })
          .catch((err) => {
            console.error(err);
            alert("Gửi Thất Bại!");
          });
      });
    </script>
  </body>
</html>

<!DOCTYPE html>
<html lang="vi">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <meta name="description" content="Uy Tín Tạo Nên Thương Hiệu!" />
    <meta name="author" content="OTISStore" />
    <meta
      name="image"
      content="https://i.pinimg.com/474x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
    />
    <title>OTISStore | Uy Tín Tạo Nên Thương Hiệu!</title>
    <link
      rel="icon"
      type="image/jpeg"
      href="https://i.pinimg.com/474x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
    />

    <!-- Google Analytics -->
    <script
      async
      src="https://www.googletagmanager.com/gtag/js?id=G-H6LM2XKZTS"
    ></script>
    <script>
      window.dataLayer = window.dataLayer || [];
      function gtag() {
        dataLayer.push(arguments);
      }
      gtag("js", new Date());
      gtag("config", "G-H6LM2XKZTS");
    </script>

    <style>
      body {
        margin: 0;
        padding: 0;
        font-family: "Segoe UI", sans-serif;
        background-color: #ffffff;
        color: #000000;
      }

      /* Header */
      .header {
        width: 100vw;
        height: 70px;
        background-color: #ffffff;
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        display: flex; /* dùng flexbox để căn giữa nội dung */
        align-items: center;
        justify-content: center;
        border-bottom: 2px solid #000000;
      }

      .header img {
        height: 80%;
        border-radius: 50%;
        object-fit: contain;
      }

      .header img:hover {
        transform: scale(1.05);
        border: 2px solid #ffffff; /* thêm kiểu border solid */
        transition: transform 0.3s ease, border-color 0.3s ease;
        cursor: pointer; /* thêm con trỏ khi hover */
      }

      .products {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
        gap: 15px;
        padding: 20px;
      }

      /* Sản phẩm */
      .itemp {
        width: 150px;
        height: 70px;
        padding: 2.5px;
        background-color: #444;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 5px;
        border-radius: 5px;
        box-shadow: 0 2px 6px rgba(0, 0, 0, 0.3);
        cursor: pointer;
      }

      .itemp img {
        width: 65px;
        height: 65px;
      }

      .itemp-content {
        width: 75px;
        height: 65px;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        gap: 2px;
        font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
      }

      .infor,
      .name,
      .no,
      .price,
      .time {
        line-height: 1;
        font-size: 13px; /* thêm px để chuẩn */
      }

      .name {
        color: rgb(255, 124, 124);
        font-weight: 600;
      }

      .infor {
        color: white;
      }

      .no {
        color: rgb(63, 140, 255);
      }

      .price {
        color: rgb(255, 222, 58);
      }

      .flex-row {
        display: flex;
        align-items: center;
        gap: 2px;
      }

      .time {
        width: 53px;
        height: 18px;
        border-radius: 2px;
        display: flex;
        align-items: center;
        justify-content: center;
        color: rgb(0, 0, 0);
        background-color: white;
      }

      .itemp button {
        width: 20px;
        height: 20px;
        border: none;
        display: flex;
        border-radius: 2px;
        align-items: center;
        justify-content: center;
        background-color: #34ff19; /* Fix lỗi thiếu dấu # */
        cursor: pointer;
      }

      .container2 {
        position: fixed;
        bottom: 20px;
        right: 20px;
        z-index: 999;
      }

      .icon img {
        width: 50px;
        height: 50px;
        border-radius: 50%;
        cursor: pointer;
        transition: transform 0.3s ease;
      }

      .icon img:hover {
        transform: rotate(15deg) scale(1.1);
      }

      .contact-Content {
        display: none;
        position: fixed;
        bottom: 80px;
        right: 20px;
        width: 300px;
        background-color: #1c1c1c;
        border: 1px solid #444;
        border-radius: 10px;
        padding: 15px;
        z-index: 1000;
        animation: slideUp 0.4s ease-in-out;
      }

      .contact-Content.active {
        display: block;
      }

      .contact-Content img {
        width: 100%;
        border-radius: 8px;
        margin-top: 10px;
      }

      .contact-Content button {
        cursor: pointer;
      }

      .order {
        padding: 5px 10px;
        background-color: #404040;
        color: #fff;
        border: none;
        border-radius: 4px;
        font-size: 14px;
        transition: background-color 0.2s ease;
      }

      .order:hover {
        background-color: #606060;
      }

      @keyframes slideUp {
        from {
          transform: translateY(30px);
          opacity: 0;
        }
        to {
          transform: translateY(0);
          opacity: 1;
        }
      }

      /* Responsive */
      @media (max-width: 600px) {
        .products {
          grid-template-columns: repeat(auto-fill, minmax(140px, 1fr));
          gap: 10px;
          padding: 10px;
        }

        .contact-Content {
          width: 90vw;
          bottom: 100px;
        }
      }
    </style>
  </head>
  <body>
    <!-- Header Logo -->
    <div class="header">
      <img
        src="https://i.pinimg.com/474x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
        alt="Background"
      />
    </div>

    <div style="height: 70px"></div>

    <!-- Danh sách sản phẩm -->
    <div class="products" id="product-list">
      <!-- Sản phẩm sẽ được render ở đây -->
      <div class="itemp">
        <img
          src="https://i.pinimg.com/474x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
          alt="SP"
        />
        <div class="itemp-content">
          <div class="name">SP1</div>

          <div class="flex-row">
            <div class="infor">No:</div>
            <div class="no">x100</div>
          </div>

          <div class="flex-row">
            <div class="infor">Price:</div>
            <div class="price">10k</div>
          </div>
          <div class="flex-row">
            <div class="time">17h45m</div>
            <button>🛒</button>
          </div>
        </div>
      </div>

      <div class="itemp">
        <img
          src="https://i.pinimg.com/474x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
          alt="SP"
        />
        <div class="itemp-content">
          <div class="name">SP1</div>

          <div class="flex-row">
            <div class="infor">No:</div>
            <div class="no">x100</div>
          </div>

          <div class="flex-row">
            <div class="infor">Price:</div>
            <div class="price">10k</div>
          </div>
          <div class="flex-row">
            <div class="time">17h45m</div>
            <button>🛒</button>
          </div>
        </div>
      </div>

      <div class="itemp">
        <img
          src="https://i.pinimg.com/474x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
          alt="SP"
        />
        <div class="itemp-content">
          <div class="name">SP1</div>

          <div class="flex-row">
            <div class="infor">No:</div>
            <div class="no">x100</div>
          </div>

          <div class="flex-row">
            <div class="infor">Price:</div>
            <div class="price">10k</div>
          </div>
          <div class="flex-row">
            <div class="time">17h45m</div>
            <button>🛒</button>
          </div>
        </div>
      </div>

      <div class="itemp">
        <img
          src="https://i.pinimg.com/474x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
          alt="SP"
        />
        <div class="itemp-content">
          <div class="name">SP1</div>

          <div class="flex-row">
            <div class="infor">No:</div>
            <div class="no">x100</div>
          </div>

          <div class="flex-row">
            <div class="infor">Price:</div>
            <div class="price">10k</div>
          </div>
          <div class="flex-row">
            <div class="time">17h45m</div>
            <button>🛒</button>
          </div>
        </div>
      </div>

      <div class="itemp">
        <img
          src="https://i.pinimg.com/474x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
          alt="SP"
        />
        <div class="itemp-content">
          <div class="name">SP1</div>

          <div class="flex-row">
            <div class="infor">No:</div>
            <div class="no">x100</div>
          </div>

          <div class="flex-row">
            <div class="infor">Price:</div>
            <div class="price">10k</div>
          </div>
          <div class="flex-row">
            <div class="time">17h45m</div>
            <button>🛒</button>
          </div>
        </div>
      </div>

      <div class="itemp">
        <img
          src="https://i.pinimg.com/474x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
          alt="SP"
        />
        <div class="itemp-content">
          <div class="name">SP1</div>

          <div class="flex-row">
            <div class="infor">No:</div>
            <div class="no">x100</div>
          </div>

          <div class="flex-row">
            <div class="infor">Price:</div>
            <div class="price">10k</div>
          </div>
          <div class="flex-row">
            <div class="time">17h45m</div>
            <button>🛒</button>
          </div>
        </div>
      </div>

      <div class="itemp">
        <img
          src="https://i.pinimg.com/474x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
          alt="SP"
        />
        <div class="itemp-content">
          <div class="name">SP1</div>

          <div class="flex-row">
            <div class="infor">No:</div>
            <div class="no">x100</div>
          </div>

          <div class="flex-row">
            <div class="infor">Price:</div>
            <div class="price">10k</div>
          </div>
          <div class="flex-row">
            <div class="time">17h45m</div>
            <button>🛒</button>
          </div>
        </div>
      </div>

      <div class="itemp">
        <img
          src="https://i.pinimg.com/474x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
          alt="SP"
        />
        <div class="itemp-content">
          <div class="name">SP1</div>

          <div class="flex-row">
            <div class="infor">No:</div>
            <div class="no">x100</div>
          </div>

          <div class="flex-row">
            <div class="infor">Price:</div>
            <div class="price">10k</div>
          </div>
          <div class="flex-row">
            <div class="time">17h45m</div>
            <button>🛒</button>
          </div>
        </div>
      </div>

      <div class="itemp">
        <img
          src="https://i.pinimg.com/474x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
          alt="SP"
        />
        <div class="itemp-content">
          <div class="name">SP1</div>

          <div class="flex-row">
            <div class="infor">No:</div>
            <div class="no">x100</div>
          </div>

          <div class="flex-row">
            <div class="infor">Price:</div>
            <div class="price">10k</div>
          </div>
          <div class="flex-row">
            <div class="time">17h45m</div>
            <button>🛒</button>
          </div>
        </div>
      </div>

      <div class="itemp">
        <img
          src="https://i.pinimg.com/474x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
          alt="SP"
        />
        <div class="itemp-content">
          <div class="name">SP1</div>

          <div class="flex-row">
            <div class="infor">No:</div>
            <div class="no">x100</div>
          </div>

          <div class="flex-row">
            <div class="infor">Price:</div>
            <div class="price">10k</div>
          </div>
          <div class="flex-row">
            <div class="time">17h45m</div>
            <button>🛒</button>
          </div>
        </div>
      </div>

      <div class="itemp">
        <img
          src="https://i.pinimg.com/474x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
          alt="SP"
        />
        <div class="itemp-content">
          <div class="name">SP1</div>

          <div class="flex-row">
            <div class="infor">No:</div>
            <div class="no">x100</div>
          </div>

          <div class="flex-row">
            <div class="infor">Price:</div>
            <div class="price">10k</div>
          </div>
          <div class="flex-row">
            <div class="time">17h45m</div>
            <button>🛒</button>
          </div>
        </div>
      </div>

      <div class="itemp">
        <img
          src="https://i.pinimg.com/474x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
          alt="SP"
        />
        <div class="itemp-content">
          <div class="name">SP1</div>

          <div class="flex-row">
            <div class="infor">No:</div>
            <div class="no">x100</div>
          </div>

          <div class="flex-row">
            <div class="infor">Price:</div>
            <div class="price">10k</div>
          </div>
          <div class="flex-row">
            <div class="time">17h45m</div>
            <button>🛒</button>
          </div>
        </div>
      </div>
    </div>

    <!-- Nút điều hướng & thông tin chi tiết -->
    <div class="container2">
      <div class="icon" onclick="toggleContact('contact-Content')">
        <img
          src="https://i.pinimg.com/474x/42/bc/f8/42bcf85126a5757cd190602a4952db32.jpg"
          alt="Content"
        />
      </div>
      <div class="contact-Content" id="contact-Content">
        <div style="text-align: center; width: 100%">
          <div style="font-size: 18px; font-weight: 600; color: white">
            Hướng Dẫn!
          </div>
          <button
            style="
              position: absolute;
              right: 5px;
              top: 5px;
              background-color: #202020;
              color: white;
              border: none;
            "
            onclick="toggleContact('contact-Content')"
          >
            x
          </button>
          <button
            class="order"
            style="
              position: absolute;
              left: 10px;
              top: 10px;
              font-size: 14px;
              background-color: #404040;
              color: white;
              border-radius: 2px;
            "
            onclick="sendMessageWithClipboard('');"
          >
            Liên Hệ
          </button>
        </div>
        <img
          src="https://i.pinimg.com/474x/b7/ff/a7/b7ffa7483252e829d97ce2978c82ce01.jpg"
          alt="Hướng Dẫn"
        />
        <p style="text-align: center; font-size: 14px; color: white">
          OTISStore | Uy Tín Tạo Nên Thương Hiệu!
        </p>
      </div>
    </div>

    <!-- Script chức năng -->
    <script>
      function infor(ID) {
        const contents = document.querySelectorAll(".gallery");
        const element = document.getElementById(ID);
        if (ID === "OFF") {
          contents.forEach((content) => (content.style.display = "none"));
        } else {
          contents.forEach((content) => (content.style.display = "none"));
          element.style.display =
            element.style.display === "none" ? "block" : "none";
        }
      }

      function toggleContact(id) {
        const el = document.getElementById(id);
        el.classList.toggle("active");
      }

      function sendMessageWithClipboard() {
        try {
          var url = "https://m.me/61569836535180";
          window.open(url, "_blank");
        } catch (err) {
          console.error("Không thể chuyển đến liên kết! : ", err);
          alert("Đã xảy ra lỗi. Vui lòng thử lại.");
        }
      }
    </script>
  </body>
</html>

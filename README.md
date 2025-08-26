<html lang="vi">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Mẫu XD01</title>
    <!-- Chèn Font Awesome CDN vào <head> -->
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css"
    />

    <style>
      :root {
        --bg-color-header: #00509e;
        --text-color-header: white;

        --bg-color-menu: #8bb7d6;
        --text-color-menu: black;

        --bg-color-intro-1: #fffbea;
        --bg-color-intro-2: #fff1b8;
        --bg-color-intro-3: #ffe066;
        --bg-color-intro-4: #fcd34d;
        --bg-color-intro-5: #fbbf24;
        --text-color-intro: #fff;

        --bg-color-0: #b3e0e5;
        --text-color-0: white;

        --bg-color-brand: #b3e0e5;
        --text-color-brand: white;

        --bg-color-contact: #00509e;
        --text-color-contact: white;

        --bg-color-box: #f9f9f9;

        --bg-color-bottom: #00509e;
      }

      html {
        scroll-behavior: smooth; /* cuộn mượt khi click link */
      }

      body {
        margin: 0;
        font-family: Arial, sans-serif;
        display: flex;
        flex-direction: column;
        align-items: center;
        align-content: center;
        justify-content: center;
        width: 100vw;
        height: 100vh;
      }

      .body-top {
        position: fixed; /* cố định theo màn hình */
        top: 0;
        left: 0;
        width: 100vw; /* chiếm full ngang màn hình */
        z-index: 1000; /* nổi lên trên */
      }

      /* Nội dung bên dưới */
      .body-bottom {
        position: fixed;
        top: 92px; /* đúng bằng chiều cao header */
        left: 0;
        padding-bottom: 0;
        width: 100vw;
        height: calc(100vh - 92px); /* chiếm phần còn lại */
        overflow-y: auto; /* cuộn dọc */
      }

      /* Thanh hotline + email */
      .contact-bar {
        background: var(--bg-color-header);
        color: var(--text-color-header);
        display: flex;
        height: 45px;
        justify-content: space-between;
        align-items: center;
      }

      .logo {
        display: flex;
        align-items: center;
        height: 100%;
        background: #adf4f82e;
        padding: 0 10px;
      }

      .logo-img {
        border-radius: 50%;
        margin-right: 5px;
        border: 2px solid #fff;
        width: 36px;
      }

      .logo-text h1 {
        margin: 0;
        font-size: 16px;
        font-weight: bold;
        line-height: 1;
        padding: 0;
      }

      .logo-text p {
        margin: 0;
        font-size: 10px;
        font-style: italic;
        line-height: 1;
        padding: 0;
        color: #000000;
      }

      .marquee {
        position: relative;
        flex: 1;
        overflow: hidden;
        display: flex;
        align-items: center;
      }

      .marquee-inner {
        display: inline-block;
        white-space: nowrap;
        padding: 15px 0;
        animation: scrollLeft linear infinite;
      }

      .marquee .link {
        display: inline-block;
        margin-right: 50px; /* khoảng cách giữa các link */
      }

      .marquee .link a {
        text-decoration: none;
        color: white;
        font-size: 15px;
        line-height: 15px;
      }

      .marquee .link a .see-more {
        color: rgb(0, 0, 0);
      }

      @keyframes scrollLeft {
        0% {
          transform: translateX(50%);
        }
        100% {
          transform: translateX(-50%);
        }
      }

      .social {
        display: flex;
        padding: 0 10px;
        height: 100%;
        background: #adf4f82e;
        justify-content: center; /* căn giữa ngang */
        align-items: center;
      }

      .social-icon {
        width: 145px;
        display: flex;
        justify-content: center; /* căn giữa ngang */
        align-items: center;
      }

      .social-icon a {
        font-size: 20px;
        color: #fff;
        display: flex; /* dùng flex để căn giữa icon */
        align-items: center;
        justify-content: center;
        width: 36.25px; /* ô icon đều nhau */
        text-decoration: none;
        transition: color 0.5s;
      }

      .social-icon a:hover {
        color: #333;
      }

      /* Navbar chính */
      nav {
        background: var(--bg-color-menu);
        display: flex;
        width: 100%;
        align-items: center;
        justify-content: center;
        padding: 5px 0;
        gap: 5px;
        flex: 1;
        flex-wrap: wrap;
      }

      /* Menu */
      .nav-1 {
        list-style: none;
        display: flex;
        padding: 0;
      }

      .nav-2 {
        color: var(--text-color-menu);
        margin: 0 auto;
        position: relative;
      }

      .nav-2 a {
        color: var(--text-color-menu);
        font-size: 24px;
        text-decoration: none;
      }

      .nav-2 a:hover {
        text-decoration: underline;
      }

      /* Submenu */
      .nav-3 {
        display: none;
        position: absolute;
        top: 100%;
        right: -18px;
        background: #efefef;
        padding: 0;
        list-style: none;
        width: min-content;
        border-radius: 5px;
      }

      .nav-2:hover .nav-3 {
        display: block;
      }

      .nav-4 a {
        display: block;
        color: #000000;
        padding: 5px;
        font-size: min(18px, calc(5px + 0.8vh + 0.9vw));
        text-decoration: none;
        white-space: nowrap;
      }

      .search-box {
        height: 24px;
        background-color: rgb(255, 255, 255);
        display: flex; /* xếp ngang */
        align-items: center; /* căn giữa theo chiều dọc */
        border: 1px solid #ccc; /* viền chung cho cả input + button */
        border-radius: 3px; /* bo góc toàn khung */
        overflow: hidden; /* ẩn tràn viền */
        margin: 0;
        font-size: 15px;
        width: 320px;
      }

      .search-box input {
        height: 100%;
        padding: 2px 5px 2px 7px;
        width: calc(100% - 30px);
        border: none; /* bỏ viền riêng */
        outline: none;
      }

      .search-box a {
        width: 20px;
        cursor: pointer;
        padding: 0;
        background: transparent; /* nền trong suốt */
        display: flex;
        justify-items: center;
        justify-content: center;
      }

      /* Responsive */
      @media (max-width: 500px) {
        .logo-text {
          display: none;
        }

        .social {
          padding: 0 10px;
        }

        .social-icon {
          display: grid;
          grid-template-columns: 1fr 1fr; /* 2 cột */
          grid-template-rows: 1fr 1fr; /* 2 hàng */
          width: 36px;
          height: 36px;
          padding: 2px;
          justify-items: center;
          justify-content: center;
        }

        .social-icon a {
          font-size: 14px;
          width: 18px;
          height: 18px;
          justify-items: center;
          justify-content: center;
          color: #fff;
          text-decoration: none;
        }
        .social-icon a:hover {
          color: #a4a4a4;
        }

        nav {
          display: flex;
          flex-direction: column; /* xếp dọc */
        }

        .search-box input {
          flex: 1;
        }

        .body-bottom {
          top: 121px; /* đúng bằng chiều cao header */
          height: calc(100vh - 121px); /* chiếm phần còn lại */
        }
      }

      .banner {
        width: calc(100% - 2px);
        /* max-width: 1200px; */
        aspect-ratio: 851 / 315;
        display: flex;
        align-items: center;
        justify-content: center;
        font-weight: bold;
        position: relative;
        border-radius: 5px;
        background-size: cover;
        background-position: center;
        transition: background-image 1s ease-in-out;
        margin: auto;
        margin-bottom: 1px;
      }

      .banner-text {
        position: absolute; /* bắt buộc để ép xuống đáy */
        left: 0;
        bottom: 0;
        width: 100%; /* full chiều ngang */
        font-size: calc(5px + 0.8vh + 0.8vw);
        color: #fff;
        background-color: rgba(0, 0, 0, 0.3); /* nền mờ */
        padding: 5px 10px;
        text-shadow: 2px 4px 8px rgba(0, 0, 0, 1);
        text-align: left;
        box-sizing: border-box; /* đảm bảo padding không phá layout */
        border-bottom-left-radius: 5px;
        border-bottom-right-radius: 5px;
      }

      .banner button {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        background: rgba(0, 0, 0, 0.4);
        color: #fff;
        border: none;
        padding: 3px 6px;
        font-size: 14px;
        cursor: pointer;
        border-radius: 50%;
        z-index: 3;
      }

      .banner .prev {
        left: 10px;
      }

      .banner .next {
        right: 10px;
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

      .section-introduce {
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        margin: 0 auto;
      }

      /* Kỹ năng */
      .section-skill {
        display: grid;
        width: min(1500px, 100%);
        grid-template-columns: repeat(
          auto-fit,
          minmax(clamp(160px, 30%, 480px), 1fr)
        );
        gap: 10px;
        margin: 0 auto;
      }

      .box-introduce {
        flex: 1 1 160px;
        padding: 5px;
        border-radius: 10px;
        background-color: var(--bg-color-box);
        transition: transform 0.5s ease;
      }

      .box-introduce:hover {
        transform: scale(1.05);
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
      }

      .box-introduce i {
        width: calc(10px + 0.5vh + 0.5vw);
        text-align: center;
      }

      .box-skill {
        display: flex;
        align-items: center;
        gap: 5px;
        font-size: calc(5px + 0.6vh + 0.6vw);
        color: #333;
        background-color: var(--bg-color-box);
        padding: 5px;
        border-radius: 5px;
        transition: background 0.5s ease;
      }

      .box-skill:hover .button {
        background-color: #383838;
        color: #efefef;
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

      .main3 {
        font-size: calc(5px + 0.7vh + 0.7vw);
        color: #404040;
        line-height: 1;
        text-align: center;
      }

      .note {
        font-size: calc(5px + 0.6vh + 0.6vw);
        color: #404040;
        line-height: 1;
        text-align: center;
        margin: 0px auto 7.5px auto;
      }

      .box-skill i {
        width: calc(7px + 0.6vh + 0.6vw);
        text-align: center;
        line-height: 1;
      }

      .box-skill .button {
        margin-left: auto;
        align-items: center;
        background: none;
        color: #000000;
        padding: 0 1px;
        border-radius: 10%;
        font-weight: 600;
        font-size: calc(5px + 0.5vh + 0.5vw);
        cursor: pointer;
        transition: all 0.5s ease;
      }

      .box-skill .button.open i {
        transform: rotate(180deg); /* mũi tên lật khi mở */
      }

      .wrapper {
        position: relative;
      }

      /* Nội dung ẩn */
      .skill-content {
        display: none; /* mặc định ẩn */
        position: absolute;
        top: 100%; /* nằm ngay dưới skill */
        left: 0;
        gap: 2px;
        background: #f9f9f9;
        padding: 5px;
        width: 100%; /* điều chỉnh theo ý bạn */
        max-height: 120px;
        overflow-y: auto; /* cuộn dọc */
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2);
        z-index: 10;
      }

      /* Hiển thị khi mở */
      .wrapper.open .skill-content {
        display: block;
      }

      .skill-content a,
      .skill-content i {
        margin-left: 5px;
        font-size: calc(5px + 0.45vh + 0.45vw);
        color: #000;
        text-decoration: none;
      }
    </style>
  </head>
  <body>
    <div class="body-top">
      <!-- Hotline + email -->
      <div class="contact-bar">
        <div class="logo">
          <img
            src="https://i.pinimg.com/736x/15/c2/33/15c233ab5cce7b9e60094a36653a3dc5.jpg"
            alt="Logo-OTVGroup"
            class="logo-img"
          />
          <div class="logo-text">
            <h1>OTVGroup</h1>
            <p>
              <em>Entertainment Media<br />E-commerce Solutions</em>
            </p>
          </div>
        </div>
        <!-- Phần thông báo chạy giữa -->
        <div class="marquee">
          <div class="marquee-inner" id="marquee"></div>
        </div>

        <!-- Icon mạng xã hội -->
        <div class="social">
          <div class="social-icon">
            <a href="https://www.facebook.com/OtisVo586" target="_blank">
              <i class="fab fa-facebook-f"></i>
            </a>

            <a href="https://www.youtube.com/@otvchannelvn" target="_blank">
              <i class="fab fa-youtube"></i>
            </a>

            <a href="https://www.tiktok.com/@otvgroup" target="_blank">
              <i class="fab fa-tiktok"></i>
            </a>

            <a href="https://www.instagram.com/otvgroup/" target="_blank">
              <i class="fab fa-instagram"></i>
            </a>
          </div>
        </div>
      </div>

      <!-- Navbar -->
      <nav>
        <div class="nav-1" style="min-width: 360px">
          <div class="nav-2">
            <a href="#banner"> <i class="fa-solid fa-house"></i></a>
          </div>
          <div class="nav-2">
            <a href="#introduce"> <i class="fa-solid fa-info-circle"></i></a>
          </div>
          <div class="nav-2">
            <a><i class="fa-solid fa-star"></i></a>
            <div class="nav-3">
              <div class="nav-4">
                <a
                  href="https://otvgroup.github.io/OTISShop.com.vn/"
                  target="_blank"
                >
                  OTISShop
                </a>
              </div>
              <div class="nav-4">
                <a
                  href="https://otvgroup.github.io/OTISStore.com.vn/"
                  target="_blank"
                >
                  OTISStore
                </a>
              </div>
              <div class="nav-4">
                <a
                  href="https://otvgroup.github.io/OTISMusisStudio.com.vn/"
                  target="_blank"
                >
                  OTISMusisStudio
                </a>
              </div>
            </div>
          </div>
          <div class="nav-2">
            <a href="#"><i class="fa-solid fa-envelope"></i></a>
          </div>
        </div>
        <div class="search-box">
          <input type="text" id="searchInput" placeholder="Nhập từ khóa ..." />
          <a onclick="searchText()">
            <i class="fa-solid fa-magnifying-glass"></i>
          </a>
        </div>
      </nav>
    </div>

    <div class="body-bottom">
      <!-- Banner -->
      <div class="banner" id="banner">
        <div class="banner-text" id="bannerText"></div>
        <button class="prev">❮</button>
        <button class="next">❯</button>
      </div>

      <!-- Nội dung -->
      <section
        style="
          --background: var(--bg-color-intro-1);
          --shadow: rgba(0, 0, 0, 0.4);
        "
        id="introduce"
      >
        <div class="main1">GIỚI THIỆU</div>
        <div class="section-introduce">
          <div class="box-introduce">
            <div class="main2">
              <i class="fa-solid fa-lightbulb"></i> <a>Đổi mới</a>
            </div>
            <div class="main3 marquee" id="marquee-change">
              Luôn tiên phong sáng tạo và ứng dụng giải pháp đột phá để mang lại
              lợi thế cạnh tranh.
            </div>
          </div>

          <div class="box-introduce">
            <div class="main2">
              <i class="fa-solid fa-gem"></i> <a>Chất lượng</a>
            </div>
            <div class="main3 marquee" id="marquee-quality">
              Cam kết sản phẩm và dịch vụ đạt chuẩn cao với quy trình minh bạch,
              chuyên nghiệp.
            </div>
          </div>

          <div class="box-introduce">
            <div class="main2">
              <i class="fa-solid fa-user-check"></i> <a>Tin cậy</a>
            </div>
            <div class="main3 marquee" id="marquee-reputation">
              Xây dựng niềm tin bằng sự tận tâm, trách nhiệm và đảm bảo đúng cam
              kết với khách hàng.
            </div>
          </div>
        </div>
      </section>

      <section
        style="
          --background: var(--bg-color-intro-2);
          --shadow: rgba(0, 0, 0, 0.4);
        "
        id="skill"
      >
        <div class="main2">Chúng tôi có thể?</div>
        <div class="note">
          "Chúng tôi mang đến giải pháp tiếp thị kỹ thuật số và SEO toàn diện,
          kết hợp chiến lược sáng tạo và công nghệ tối ưu, để doanh nghiệp phát
          triển mạnh mẽ trong kỷ nguyên số."
        </div>
        <div class="section-skill">
          <!-- Truyền thông -->
          <div class="wrapper">
            <div class="box-skill">
              <i class="fa-solid fa-network-wired"></i><a>Truyền thông</a>
              <div class="button">
                <i class="fa-solid fa-chevron-down"></i>
              </div>
              <div class="skill-content">
                <a>Nghiên Cứu & Phân Tích Thị Trường</a>
                <i class="fa-solid fa-chart-line"></i><br />
                <a>Chiến Lược Truyền Thông Tổng Thể</a>
                <i class="fa-solid fa-bullseye"></i><br />
                <a>Tối Ưu Hiệu Quả Truyền Thông</a>
                <i class="fa-solid fa-share-nodes"></i><br />
                <a>Sản Xuất & Quảng Cáo</a>
                <i class="fa-solid fa-photo-film"></i>
              </div>
            </div>
          </div>

          <!-- Giải trí & Nội dung số -->
          <div class="wrapper">
            <div class="box-skill">
              <i class="fa-solid fa-film"></i><a>Giải trí</a>
              <div class="button">
                <i class="fa-solid fa-chevron-down"></i>
              </div>
              <div class="skill-content">
                <a>Phát Triển Game & Trải Nghiệm Số</a>
                <i class="fa-solid fa-gamepad"></i><br />
                <a>Xây Dựng Cộng Đồng & Fanbase</a>
                <i class="fa-solid fa-users"></i><br />
                <a>Âm Nhạc & Giải Trí Trực Tuyến</a>
                <i class="fa-solid fa-music"></i><br />
                <a>Thiết Kế & Sáng Tạo Nội Dung</a>
                <i class="fa-solid fa-palette"></i>
              </div>
            </div>
          </div>

          <!-- Thương mại -->
          <div class="wrapper">
            <div class="box-skill">
              <i class="fa-solid fa-cart-shopping"></i><a>Thương mại</a>
              <div class="button">
                <i class="fa-solid fa-chevron-down"></i>
              </div>
              <div class="skill-content">
                <a>Xây Dựng & Phát Triển Thương Hiệu</a>
                <i class="fa-solid fa-star"></i><br />
                <a>Hoạch Định Chiến Lược Kinh Doanh</a>
                <i class="fa-solid fa-lightbulb"></i><br />
                <a>Chuyển Đổi Công Nghệ Số</a>
                <i class="fa-solid fa-diagram-project"></i><br />
                <a>Giải Pháp Pháp Lý</a>
                <i class="fa-solid fa-scale-balanced"></i>
              </div>
            </div>
          </div>

          <!-- Học thuật & Nghiên cứu -->
          <div class="wrapper">
            <div class="box-skill">
              <i class="fa-solid fa-graduation-cap"></i><a>Học thuật</a>
              <div class="button">
                <i class="fa-solid fa-chevron-down"></i>
              </div>
              <div class="skill-content">
                <a>Tư Liệu & Nghiên Cứu Khoa Học</a>
                <i class="fa-solid fa-book-open"></i><br />
                <a>Báo Cáo & Phân Tích Dữ Liệu</a>
                <i class="fa-solid fa-chart-pie"></i>
              </div>
            </div>
          </div>

          <!-- Kỹ thuật & Công nghệ -->
          <div class="wrapper">
            <div class="box-skill">
              <i class="fa-solid fa-microchip"></i><a>Kỹ thuật</a>
              <div class="button">
                <i class="fa-solid fa-chevron-down"></i>
              </div>
              <div class="skill-content">
                <a>Cải Tiến & Triển Khai & Ứng Dụng</a>
                <i class="fa-solid fa-gears"></i><br />
                <a>Đào Tạo & Thiết Kế & Phát Triển</a>
                <i class="fa-solid fa-chalkboard-user"></i>
              </div>
            </div>
          </div>

          <!-- Dịch vụ khách hàng -->
          <div class="wrapper">
            <div class="box-skill">
              <i class="fa-solid fa-handshake-angle"></i><a>Dịch vụ</a>
              <div class="button">
                <i class="fa-solid fa-chevron-down"></i>
              </div>
              <div class="skill-content">
                <a>Chăm Sóc & Tư Vấn & Hỗ Trợ</a>
                <i class="fa-solid fa-headset"></i><br />
                <a>Bảo Hành & Bảo Trì</a>
                <i class="fa-solid fa-screwdriver-wrench"></i>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section
        style="
          --background: var(--bg-color-intro-3);
          --shadow: rgba(0, 0, 0, 0.4);
        "
        id="skill"
      >
        <div class="main2">Mani2</div>
        <div class="note">"Note"</div>
      </section>

      <section
        style="
          --background: var(--bg-color-intro-4);
          --shadow: rgba(0, 0, 0, 0.4);
        "
        id="skill"
      >
        <div class="main2">Mani2</div>
        <div class="note">"Note"</div>
      </section>

      <section
        style="
          --background: var(--bg-color-intro-5);
          --shadow: rgba(0, 0, 0, 0.4);
        "
        id="skill"
      >
        <div class="main2">Mani2</div>
        <div class="note">"Note"</div>
      </section>

      <section
        style="
          --background: var(--bg-color-bottom);
          --shadow: rgba(0, 0, 0, 0.4);
          height: var(--height-bottom);
        "
        id="skill"
      >
        <div class="main2">Bottom</div>
        <div class="note">"Note"</div>
      </section>
    </div>

    <script>
      document.addEventListener("DOMContentLoaded", () => {
        const contents = document.querySelectorAll("div[id^='marquee-']");
        const marqueeInner = document.getElementById("marquee");

        const timePerItem = 20; // giây / item
        const total = contents.length;

        contents.forEach((el) => {
          const div = document.createElement("div");
          div.classList.add("link");

          const id = el.id;
          let text = el.textContent.trim() || id.replace("marquee-", "");

          // 🔹 Giới hạn 25 từ
          let words = text.split(/\s+/);
          let mainText = words.slice(0, 20).join(" ");

          // 🔹 Xóa dấu câu cuối
          mainText = mainText.replace(/[.,!?;]+$/, "");

          // 🔹 Thêm " ... Xem thêm."
          const extra = `<span class="see-more">...Xem thêm.</span>`;

          div.innerHTML = `<a href="#${id}" title="${el.textContent.trim()}">${mainText}${extra}</a>`;
          marqueeInner.appendChild(div);
        });

        // set tốc độ cuộn (dựa trên số lượng item)
        const duration = total * timePerItem;
        marqueeInner.style.animationDuration = `${duration}s`;
      });
    </script>

    <script>
      document.querySelectorAll('a[href^="#"]').forEach((anchor) => {
        anchor.addEventListener("click", function (e) {
          e.preventDefault();
          const target = document.querySelector(this.getAttribute("href"));
          if (target) {
            target.scrollIntoView({
              behavior: "smooth",
              block: "start",
            });
          }
        });
      });
    </script>

    <script>
      function searchText() {
        const keyword = document.getElementById("searchInput").value.trim();
        if (!keyword) return;

        const regex = new RegExp(keyword, "i");
        let foundEl = null;

        document.querySelectorAll("section").forEach((sec) => {
          if (!foundEl && regex.test(sec.textContent)) {
            foundEl = sec;
          }
        });

        if (foundEl) {
          foundEl.scrollIntoView({ behavior: "smooth", block: "center" });
        } else {
          alert("Không tìm thấy kết quả!");
        }
      }

      // Lắng nghe Enter
      document
        .getElementById("searchInput")
        .addEventListener("keydown", (e) => {
          if (e.key === "Enter") searchText();
        });
    </script>

    <script>
      const banners = [
        {
          img: "https://raw.githubusercontent.com/OTVGroup/OTVGroup.com.vn/main/Background%20-%20OTVGroup.jpeg",
          text: "OTVGroup | Hết Mình Với Đam Mê!",
        },
        {
          img: "https://raw.githubusercontent.com/OTVGroup/OTVGroup.com.vn/main/BackGround%20-%20OTISMusicStudio.jpg",
          text: "OTVMusic | Nghệ Thuật Là Linh Hồn Cuộc Sống.",
        },
        {
          img: "https://raw.githubusercontent.com/OTVGroup/OTVGroup.com.vn/main/Background%20-%20OTISShop.jpeg",
          text: "OTISShop | Uy Tín - Chất Lượng - Tin Cậy.",
        },
        {
          img: "https://raw.githubusercontent.com/OTVGroup/OTVGroup.com.vn/main/Background%20-%20OTISStore.jpeg",
          text: "OTISStore | Uy Tín Tạo Nên Thương Hiệu.",
        },
      ];

      let idx = 0;
      const bannerEl = document.getElementById("banner");
      const bannerText = document.getElementById("bannerText");

      function showBanner(i) {
        if (i < 0) idx = banners.length - 1;
        else if (i >= banners.length) idx = 0;
        else idx = i;

        bannerEl.style.backgroundImage = `url('${banners[idx].img}')`;
        bannerText.textContent = banners[idx].text;
      }

      document.querySelector(".prev").onclick = () => showBanner(idx - 1);
      document.querySelector(".next").onclick = () => showBanner(idx + 1);

      // load ban đầu
      showBanner(0);

      // auto chuyển
      setInterval(() => showBanner(idx + 1), 5999);
    </script>

    <script>
      document.querySelectorAll(".box-skill .button").forEach((btn) => {
        btn.addEventListener("click", (e) => {
          const currentWrapper = btn.closest(".wrapper");

          // Đóng tất cả wrapper khác
          document.querySelectorAll(".wrapper.open").forEach((wrapper) => {
            if (wrapper !== currentWrapper) {
              wrapper.classList.remove("open");
              wrapper.querySelector(".button.open")?.classList.remove("open");
            }
          });

          // Toggle wrapper hiện tại
          currentWrapper.classList.toggle("open");
          btn.classList.toggle("open");
        });
      });
    </script>
  </body>
</html>

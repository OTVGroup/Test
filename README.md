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
      body {
        margin: 0;
        font-family: Arial, sans-serif;
        display: flex;
        flex-direction: column;
        align-items: center;
        align-content: center;
        width: 100vw;
        justify-content: center;
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
        padding-bottom: 5px;
        width: 100vw;
        height: calc(100vh - 92px); /* chiếm phần còn lại */
        overflow-y: auto; /* cuộn dọc */
        background: #ffffff;
      }

      /* Thanh hotline + email */
      .contact-bar {
        background: #17c0c9;
        color: #fff;
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
        margin-right: 10px;
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
        color: #333;
      }

      .contact-marquee {
        flex: 1; /* chiếm hết không gian giữa */
        padding: 0;
        text-align: center;
        border: none; /* không viền */
      }

      .contact-marquee marquee {
        font-size: 16px;
        color: #fff;
        font-weight: 500;
        line-height: 1.2;
      }

      .social-icon {
        display: flex;
        padding: 0 10px;
        margin-left: 10px;
        height: 100%;
        background: #adf4f82e;
        justify-content: center; /* căn giữa ngang */
        align-items: center;
      }

      .icon a {
        font-size: 24px;
        color: #fff;
        display: flex; /* dùng flex để căn giữa icon */
        align-items: center;
        justify-content: center;
        width: 38px; /* ô icon đều nhau */
        text-decoration: none;
        transition: color 0.3s;
      }

      .icon a:last-child {
        border-right: none;
      }

      .icon a:hover {
        color: #333;
      }

      /* Navbar chính */
      nav {
        background: #012b86;
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
        color: #fff;
        margin: 0 auto;
        position: relative;
      }

      .nav-2 a {
        color: #fff;
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
        width: 200px;
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
        font-size: 15px; /* chỉnh to nhỏ icon/chữ */
      }

      /* Responsive */
      @media (max-width: 720px) {
        nav {
          display: flex;
          flex-direction: column; /* xếp dọc */
        }

        nav .search-box {
          width: 360px;
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
        font-size: calc(5px + 0.8vh + 1vw);
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
        padding: 4px 8px;
        font-size: 18px;
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

      .about-introduce {
        display: flex;
        flex-wrap: wrap;
        gap: 10px;
        justify-content: center;
      }

      .about-introduce .box {
        flex: 1 1 120px;
        padding: 5px 10px;
        border-radius: 10px;
        background: #fff;
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.08);
        transition: transform 0.5s ease;
      }

      .about-introduce .box:hover {
        transform: translateY(-10px);
      }

      .about-introduce .box .icon {
        font-size: calc(5px + 0.8vh + 1.5vw);
        text-align: center;
      }

      .about-introduce .box .mains {
        text-align: center;
        margin: 5px auto;
      }

      .about-introduce .box .idea-box {
        font-size: calc(5px + 0.6vh + 0.5vw);
        text-align: center;
        color: #929191;
        line-height: 1;
      }

      /* Nội dung */
      .about-content {
        width: 100%;
        min-width: 240px;
      }

      .main {
        font-size: calc(5px + 0.6vh + 1vw);
        font-weight: 600;
        line-height: 1.2;
        color: #000;
        text-align: center;
        margin: 0 auto 10px auto;
      }

      .mains {
        font-size: calc(5px + 0.6vh + 0.75vw);
        font-weight: 600;
        line-height: 1;
        width: calc(100% - 20px);
        color: #1e1e1e;
        text-align: center;
        margin: 0 auto 5px auto;
      }

      .description {
        font-size: calc(5px + 0.6vh + 0.5vw);
        color: #555;
        text-align: center;
      }

      /* Kỹ năng */
      .skills {
        display: grid;
        width: min(1500px, 100%);
        grid-template-columns: repeat(
          auto-fit,
          minmax(clamp(120px, 30%, 480px), 1fr)
        );
        gap: 10px;
        margin-top: 10px;
      }

      .skill-wrapper {
        position: relative; /* dùng để skill-content định vị tương đối */
      }

      .skill {
        display: flex;
        align-items: center;
        gap: 5px;
        font-size: calc(5px + 0.6vh + 0.5vw);
        color: #333;
        background: #f9f9f9;
        padding: 5px;
        border-radius: 5px;
        transition: background 0.5s ease;
      }

      .skill:hover {
        background: #888888;
        color: #ffffff;
      }

      .skill i {
        font-size: calc(5px + 0.6vh + 0.5vw);
        width: calc(7px + 0.6vh + 0.5vw);
        text-align: center;
      }

      .skill .button {
        margin-left: auto;
        align-items: center;
        background: none;
        color: #000000;
        padding: 0 1px;
        border-radius: 20%;
        font-weight: 600;
        font-size: calc(5px + 0.4vh + 0.5vw);
        cursor: pointer;
        transition: all 0.5s ease;
      }

      .button:hover {
        background-color: white;
        transform: scale(1.1); /* phóng to 110% khi hover */
      }

      .button.open i {
        transform: rotate(180deg); /* mũi tên lật khi mở */
      }

      /* Nội dung ẩn */
      .skill-content {
        display: none; /* mặc định ẩn */
        position: absolute;
        top: 100%; /* nằm ngay dưới skill */
        left: 0;
        margin-bottom: 5px;
        background: #ececec;
        padding: 0px 5px 0px 5px;
        width: 100%; /* điều chỉnh theo ý bạn */
        height: 120px;
        overflow-y: auto; /* cuộn dọc */
        box-shadow: 0 2px 8px rgba(0, 0, 0, 0.2);
        z-index: 10;
      }

      /* Hiển thị khi mở */
      .skill-wrapper.open .skill-content {
        display: block;
      }

      .skill-content p {
        margin: 0;
        line-height: 1.1;
        padding: 5px 5px 2px 5px;
        font-size: calc(5px + 0.6vh + 0.5vw);
        color: #000;
      }

      .skill-content a {
        padding: 0 5px 2px 5px;
        margin-left: 5px;
        width: calc(100% - 15px);
        font-size: calc(5px + 0.4vh + 0.5vw);
        color: #000;
        line-height: 1.1;
        text-decoration: none;
      }

      .skill-content a:hover {
        color: #000;
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
        <div class="contact-marquee">
          <marquee behavior="scroll" direction="left" scrollamount="5">
            <nav style="background: none">
              OTVGroup là một hệ sinh thái nội dung sôi động, sáng tạo và đa
              dạng, nổi bật trong các lĩnh vực giải trí, nghệ thuật và đổi mới
              kỹ thuật số.
            </nav>
          </marquee>
        </div>
        <!-- Icon mạng xã hội -->
        <div class="social-icon">
          <div class="icon">
            <a href="https://www.facebook.com/OtisVo586" target="_blank">
              <i class="fab fa-facebook-f"></i>
            </a>
          </div>
          <div class="icon">
            <a href="https://www.youtube.com/@otvchannelvn" target="_blank">
              <i class="fab fa-youtube"></i>
            </a>
          </div>
          <div class="icon">
            <a href="https://www.tiktok.com/@otvgroup" target="_blank">
              <i class="fab fa-tiktok"></i>
            </a>
          </div>
          <div class="icon">
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
        <div class="banner-text" id="bannerText">WELCOME</div>
        <button class="prev">❮</button>
        <button class="next">❯</button>
      </div>

      <!-- Nội dung -->
      <section
        style="--background: rgb(246, 225, 143); --shadow: rgba(0, 0, 0, 0.4)"
        id="introduce"
      >
        <div class="main">GIỚI THIỆU</div>
        <div class="about-introduce">
          <div class="box">
            <div class="mains">
              <i class="fa-solid fa-lightbulb"></i> Đổi mới
            </div>
            <div class="description">
              Không ngừng sáng tạo, áp dụng giải pháp mới để mang lại giá trị
              tối ưu.
            </div>
          </div>

          <div class="box">
            <div class="mains"><i class="fa-solid fa-gem"></i> Chất lượng</div>
            <div class="description">
              Cam kết chất lượng tốt nhất với quy trình minh bạch và chuyên
              nghiệp.
            </div>
          </div>

          <div class="box">
            <div class="mains">
              <i class="fa-solid fa-handshake"></i> Tin cậy
            </div>
            <div class="description">
              Xây dựng niềm tin bằng sự tận tâm, trách nhiệm và đúng cam kết.
            </div>
          </div>
        </div>
      </section>
      <section
        style="--background: rgb(143, 217, 246); --shadow: rgba(0, 0, 0, 0.4)"
      >
        <div class="about-content">
          <div class="mains">Chúng tôi có thể?</div>
          <div class="description">
            Chúng tôi là một cơ quan tiếp thị kỹ thuật số và SEO chuyên giúp các
            doanh nghiệp phát triển sự hiện diện trực tuyến và thực sự phát
            triển.
          </div>
          <div class="skills">
            <div class="skill-wrapper">
              <div class="skill">
                <i class="fa-solid fa-laptop-code"></i><a>Kỹ thuật số</a>
                <div class="button">
                  <i class="fa-solid fa-chevron-down"></i>
                </div>
                <div class="skill-content">
                  <p>Nội dung chi tiết về Phát triển</p>
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <p>Có thể thêm nhiều thông tin khác</p>
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a>
                </div>
              </div>
            </div>
            <div class="skill-wrapper">
              <div class="skill">
                <i class="fa-solid fa-cart-shopping"></i><a>Thương mại</a>
                <div class="button">
                  <i class="fa-solid fa-chevron-down"></i>
                </div>
                <div class="skill-content">
                  <p>Nội dung chi tiết về Phát triển</p>
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <p>Có thể thêm nhiều thông tin khác</p>
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a>
                </div>
              </div>
            </div>
            <div class="skill-wrapper">
              <div class="skill">
                <i class="fa-solid fa-lightbulb"></i><a>Sáng tạo</a>
                <div class="button">
                  <i class="fa-solid fa-chevron-down"></i>
                </div>
                <div class="skill-content">
                  <p>Nội dung chi tiết về Phát triển</p>
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <p>Có thể thêm nhiều thông tin khác</p>
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a>
                </div>
              </div>
            </div>
            <div class="skill-wrapper">
              <div class="skill">
                <i class="fa-solid fa-people-roof"></i><a>Dịch vụ</a>
                <div class="button">
                  <i class="fa-solid fa-chevron-down"></i>
                </div>
                <div class="skill-content">
                  <p>Nội dung chi tiết về Phát triển</p>
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <p>Có thể thêm nhiều thông tin khác</p>
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a>
                </div>
              </div>
            </div>
            <div class="skill-wrapper">
              <div class="skill">
                <i class="fa-solid fa-film"></i><a>Giải trí</a>
                <div class="button">
                  <i class="fa-solid fa-chevron-down"></i>
                </div>
                <div class="skill-content">
                  <p>Nội dung chi tiết về Phát triển</p>
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <p>Có thể thêm nhiều thông tin khác</p>
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a>
                </div>
              </div>
            </div>
            <div class="skill-wrapper">
              <div class="skill">
                <i class="fa-solid fa-network-wired"></i><a>Truyền thông</a>
                <div class="button">
                  <i class="fa-solid fa-chevron-down"></i>
                </div>
                <div class="skill-content">
                  <p>Nội dung chi tiết về Phát triển</p>
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <p>Có thể thêm nhiều thông tin khác</p>
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a><br />
                  <a>Idea</a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section id="trademark">Thương Hiệu</section>
    </div>

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
          text: "Khám phá thế giới",
        },
        {
          img: "https://raw.githubusercontent.com/OTVGroup/OTVGroup.com.vn/main/BackGround%20-%20OTISMusicStudio.jpg",
          text: "Ưu đãi hấp dẫn",
        },
        {
          img: "https://raw.githubusercontent.com/OTVGroup/OTVGroup.com.vn/main/Background%20-%20OTISShop.jpeg",
          text: "Chào đón trải nghiệm mới",
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
      document.querySelectorAll(".skill .button").forEach((btn) => {
        btn.addEventListener("click", (e) => {
          const wrapper = btn.closest(".skill-wrapper");
          wrapper.classList.toggle("open");
          btn.classList.toggle("open");
        });
      });
    </script>
  </body>
</html>

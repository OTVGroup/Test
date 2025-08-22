<!DOCTYPE html>
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
        top: 93px; /* đúng bằng chiều cao header */
        left: 0;
        width: 100vw;
        height: calc(100vh - 93px); /* chiếm phần còn lại */
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
        font-size: 18px;
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
        padding: 10px 0;
        gap: 10px;
        flex: 1;
        flex-wrap: wrap;
        flex-direction: row; /* xếp dọc */
      }

      /* Menu */
      .nav-1 {
        list-style: none;
        display: flex;
        margin: 0;
        padding: 0;
      }

      .nav-2 {
        color: #fff;
        margin: 0 5px;
        position: relative;
      }

      .nav-2 a {
        color: #fff;
        font-size: 16px;
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
        left: 0;
        background: #ececec;
        padding: 0;
        margin: 0;
        list-style: none;
        width: 160px;
        border-radius: 5px;
      }

      .nav-2:hover .nav-3 {
        display: block;
      }

      .nav-4 a {
        display: block;
        color: #000000;
        padding: 5px 10px;
        text-decoration: none;
        white-space: nowrap;
      }

      .search-box {
        height: 25px;
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
        padding: 2px 3px;
        border: none; /* bỏ viền riêng */
        outline: none;
      }

      .search-button {
        width: 24px;
        height: 100%;
        border: none; /* bỏ viền */
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
          width: 380px;
        }

        .search-box input {
          flex: 1;
        }

        .body-bottom {
          top: 121px; /* đúng bằng chiều cao header */
          height: calc(100vh - 121px); /* chiếm phần còn lại */
        }
      }

      section {
        border: 1px solid #ccc;
        padding: 20px;
        width: 100vw;
        min-width: 380px;
      }

      section h2 {
        margin-bottom: 20px;
      }

      mark {
        background: yellow; /* tô màu kết quả tìm */
      }

      .banner {
        width: 100%;
        max-width: 1200px;
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
        font-size: calc(10px + 3vh);
        color: #fff;
        background-color: rgba(0, 0, 0, 0.4); /* nền mờ */
        padding: 10px 20px;
        text-shadow: 2px 4px 8px rgba(0, 0, 0, 0.7);
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
        padding: 8px 12px;
        font-size: 20px;
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
            <a href="#banner"> <i class="fa-solid fa-house"></i> Home</a>
          </div>
          <div class="nav-2">
            <a href="#introduce">
              <i class="fa-solid fa-info-circle"></i> Giới thiệu</a
            >
          </div>
          <div class="nav-2">
            <a><i class="fa-solid fa-star"></i> Thương hiệu</a>
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
            <a href="#"><i class="fa-solid fa-envelope"></i> Liên hệ</a>
          </div>
        </div>
        <div class="search-box">
          <input type="text" id="searchInput" placeholder="Tìm kiếm ..." />
          <button class="search-button" onclick="searchText()">🔍</button>
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
      <section class="content" id="introduce">
        <h2>GIỚI THIỆU</h2>
        <p>
          OTVGroup là một hệ sinh thái nội dung sôi động, sáng tạo và đa dạng,
          nổi bật trong các lĩnh vực giải trí, nghệ thuật và đổi mới kỹ thuật
          số.
        </p>
      </section>
      <section id="trademark">Thương Hiệu</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
      <section>LIÊN HỆ</section>
    </div>

    <!-- <script>
      function searchText() {
        // Xóa highlight cũ
        document
          .querySelectorAll("mark")
          .forEach((m) => m.replaceWith(m.textContent));

        const keyword = document.getElementById("searchInput").value.trim();
        if (!keyword) return;

        // KHÔNG dùng flag g ở đây
        const regex = new RegExp(keyword, "i");
        let foundEl = null;

        function highlight(node) {
          if (node.nodeType === 3) {
            // text node
            if (regex.test(node.textContent)) {
              const newHTML = node.textContent.replace(
                new RegExp(keyword, "gi"),
                (match) => `<mark>${match}</mark>`
              );
              const span = document.createElement("span");
              span.innerHTML = newHTML;
              node.replaceWith(...span.childNodes);
              if (!foundEl) foundEl = span.querySelector("mark");
            }
          } else {
            node.childNodes.forEach(highlight);
          }
        }

        document.querySelectorAll("section").forEach((sec) => highlight(sec));

        if (foundEl) {
          foundEl.scrollIntoView({ behavior: "smooth", block: "center" });
        } else {
          alert("Không tìm thấy kết quả!");
        }
      }
    </script> -->
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
  </body>
</html>

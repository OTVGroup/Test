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
        min-width: 480px;

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
        min-width: 480px;
        z-index: 1000; /* nổi lên trên */
      }

      /* Nội dung bên dưới */
      .body-bottom {
        position: fixed;
        top: 119px; /* đúng bằng chiều cao header */
        left: 0;
        width: 100vw;
        min-width: 480px;
        height: calc(100vh - 120px); /* chiếm phần còn lại */
        overflow-y: auto; /* cuộn dọc */
        background: #ffffff;
      }

      /* Thanh hotline + email */
      .contact-bar {
        background: #17c0c9;
        color: #fff;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 5px 10px;
      }

      .contact-bar a {
        font-size: 15px;
        color: #fff;
        text-decoration: none;
        margin-left: 15px;
      }

      .contact-bar span {
        margin-right: 15px;
      }

      .contact-marquee {
        flex: 1; /* chiếm hết không gian giữa */
        padding: 0 5%;
        text-align: center;
        border: none; /* không viền */
      }

      .contact-marquee marquee {
        font-size: 15px;
        color: #fff;
        font-weight: 500;
      }

      .social-icons {
        display: flex;
        justify-content: center; /* căn giữa ngang */
        align-items: center;
      }

      .social-icons a {
        color: #fff;
        font-size: 15px;
        display: flex; /* dùng flex để căn giữa icon */
        align-items: center;
        justify-content: center;
        width: 30px; /* ô icon đều nhau */
        text-decoration: none;
        border-right: 1px solid #fff; /* sọc ngăn trắng */
        transition: color 0.3s;
      }

      .social-icons a i {
        width: 30px;
      }

      .social-icons a:last-child {
        border-right: none;
      }

      .social-icons a:hover {
        color: #333;
      }

      /* Navbar chính */
      nav {
        background: #002779;
        display: flex;
        align-items: center;
        justify-content: space-between;
        padding: 10px 20px;
        flex-wrap: wrap; /* Cho phép xuống dòng khi cần */
      }

      nav .logo {
        border-radius: 50%;
        border: 2px solid #fff;
        width: 61px;
      }

      /* Container giữa (menu + search) */
      .middle-container {
        display: flex;
        align-items: center;
        justify-content: center;
        flex: 1;
        gap: 10px;
        flex-wrap: wrap;
      }

      /* Menu */
      nav ul {
        list-style: none;
        display: flex;
        margin: 0;
        padding: 0;
      }

      nav ul li {
        margin: 0 10px;
        position: relative;
      }

      nav ul li a {
        color: #fff;
        font-size: 16px;
        text-decoration: none;
      }

      nav ul li a:hover {
        text-decoration: underline;
      }

      /* Submenu */
      nav ul li ul {
        display: none;
        position: absolute;
        top: 100%;
        left: 0;
        background: #003cbf;
        padding: 0;
        margin: 0;
        list-style: none;
        width: 160px;
        border-radius: 5px;
      }

      nav ul li:hover ul {
        display: block;
      }

      nav ul li ul li a {
        display: block;
        color: #fff;
        padding: 5px 10px;
        text-decoration: none;
        white-space: nowrap;
      }

      nav ul li ul li a:hover {
        background: #282f3e;
      }

      .search-box {
        width: 200px;
        height: 25px;
        background-color: rgb(255, 255, 255);
        display: flex; /* xếp ngang */
        align-items: center; /* căn giữa theo chiều dọc */
        border: 1px solid #ccc; /* viền chung cho cả input + button */
        border-radius: 3px; /* bo góc toàn khung */
        overflow: hidden; /* ẩn tràn viền */
      }

      .search-box input {
        flex: 1; /* chiếm hết chỗ còn lại */
        height: 100%;
        padding: 3px;
        border: none; /* bỏ viền riêng */
        outline: none;
      }

      .search-button {
        width: auto;
        height: 100%;
        border: none; /* bỏ viền */
        cursor: pointer;
        background: transparent; /* nền trong suốt */
        display: flex;
        justify-items: center;
        justify-content: center;
        font-size: 15px; /* chỉnh to nhỏ icon/chữ */
      }

      /* Responsive */
      @media (max-width: 750px) {
        nav {
          justify-content: flex-start; /* Logo luôn trái */
        }

        .middle-container {
          width: 100%;
          flex-direction: column; /* xếp dọc */
        }

        nav ul {
          justify-content: center; /* căn giữa menu */
          width: 100%;
        }

        .search-box {
          justify-content: center; /* căn giữa ô tìm kiếm */
          margin: 0 auto;
          max-width: 420px;
          width: calc(100% - 20px); /* chiếm toàn bộ chiều rộng phần tử cha */
          box-sizing: border-box; /* bao gồm padding và border nếu có */
          height: 25px;
        }
      }

      section {
        border: 1px solid #ccc;
        padding: 20px;
        width: 100vw;
        min-width: 440px;
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
        transition: background-image 0.8s ease-in-out;
        margin: auto;
        margin-bottom: 1px;
      }

      .banner-text {
        position: absolute; /* bắt buộc để ép xuống đáy */
        left: 0;
        bottom: 0;
        width: 100%; /* full chiều ngang */
        font-size: 24px;
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
        <span>
          <a href="tel:+84329022431" target="_blank"> ☎ +84 329 022 431 </a>
        </span>
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
        <div class="social-icons">
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

      <!-- Navbar -->
      <nav>
        <img
          src="https://i.pinimg.com/736x/15/c2/33/15c233ab5cce7b9e60094a36653a3dc5.jpg"
          alt="Logo-OTVGroup"
          class="logo"
        />
        <div class="middle-container">
          <ul style="min-width: 360px">
            <li><a href="#banner">TRANG CHỦ</a></li>
            <li><a href="#introduce">GIỚI THIỆU</a></li>
            <li>
              <a>THƯƠNG HIỆU</a>
              <ul style="width: 180px">
                <li>
                  <a
                    href="https://otvgroup.github.io/OTISShop.com.vn/"
                    target="_blank"
                  >
                    OTISShop
                  </a>
                </li>
                <li>
                  <a
                    href="https://otvgroup.github.io/OTISStore.com.vn/"
                    target="_blank"
                  >
                    OTISStore
                  </a>
                </li>
                <li>
                  <a
                    href="https://otvgroup.github.io/OTISMusisStudio.com.vn/"
                    target="_blank"
                  >
                    OTISMusisStudio
                  </a>
                </li>
              </ul>
            </li>
            <li><a href="#">LIÊN HỆ</a></li>
          </ul>
          <div class="search-box">
            <input type="text" id="searchInput" placeholder="Tìm kiếm ..." />
            <button class="search-button" onclick="searchText()">🔍</button>
          </div>
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
      setInterval(() => showBanner(idx + 1), 9999);
    </script>
  </body>
</html>

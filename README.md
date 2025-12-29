<html lang="vi">
  <head>
    <meta charset="UTF-8" />
    <meta
      name="viewport"
      content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no"
    />
    <meta name="description" content="Hết Mình Với Đam Mê!" />
    <meta name="author" content="OTVGroup" />
    <meta
      name="image"
      content="https://raw.githubusercontent.com/OTVGroup/OTVGroup.com.vn/main/LOGO%20-%20OTVGroup.png"
    />
    <title>OTVGroup | Hết Mình Với Đam Mê!</title>
    <link
      rel="icon"
      type="image/png"
      href="https://raw.githubusercontent.com/OTVGroup/OTVGroup.com.vn/main/LOGO%20-%20OTVGroup.png"
    />
    <link
      rel="stylesheet"
      href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.0/css/all.min.css"
    />
    <style>
      /* 🎯 Loại bỏ hoàn toàn không gian thanh cuộn */
      html {
        overflow: -moz-scrollbars-none; /* Firefox cũ */
        scrollbar-width: none; /* Firefox mới */
        scroll-behavior: smooth; /* Cuộn mượt */
      }
      ::-webkit-scrollbar {
        width: 0 !important; /* 🎯 Không chiếm không gian */
        height: 0 !important;
        display: none !important; /* 🎯 Ẩn hoàn toàn */
      }
      /* 🎯 Đảm bảo không có padding/margin cho thanh cuộn */
      * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
      }

      :root {
        --text-size-1: 24px;
      }

      a {
        color: #fff;
        text-decoration: none; /* bỏ gạch chân */
      }

      a:hover {
        color: blue;
      }

      body {
        font-family: sans-serif;
        margin: 0;
      }

      /* Thẻ phủ toàn màn hình */
      .full-screen {
        position: fixed;
        inset: 0; /* top right bottom left = 0 */
        z-index: 1;
        display: flex;
        height: 100%;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        background: #1e1e1e;
      }

      .top {
        display: flex;
        flex-direction: row;
        align-items: center;
        height: 75px;
        padding: 0;
        background: #000000;
        width: 95vw;
        border-top-left-radius: 10px;
        border-top-right-radius: 10px;
        border-bottom: 2px solid #2a2a2a;
      }

      .top .img {
        width: calc(95vw * 0.125);
        display: flex;
        align-items: center;
        justify-content: center;
      }

      .top .img img {
        width: 80%;
        min-width: 24px;
        max-width: 60px;
        border-radius: 50%;
        box-shadow: 0 0 5px rgb(226, 226, 226), 0 0 5px rgb(250, 250, 250);
      }

      .top nav.menu {
        display: flex;
        position: relative;
        height: 100%;
        padding: 0;
        border-top-right-radius: 10px;
        background: #181818;
        align-items: flex-end;
        width: 95vw;
      }

      .top nav.menu label {
        color: #aaa;
        text-align: center;
        width: calc(95vw * 0.75 / 4);
        cursor: pointer;
        transition: color 0.3s ease;
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-bottom: 10px;
      }

      .top nav.menu label i {
        font-size: var(--text-size-1);
        margin-bottom: 5px;
        transition: 0.3s;
      }

      .top nav.menu label.active i,
      .top nav.menu label:hover i {
        color: #0f0;
        text-shadow: 0 0 10px rgb(0, 217, 43), 0 0 20px rgb(0, 213, 0);
      }

      .top nav.menu label span {
        font-size: 15px;
        text-transform: uppercase;
      }

      .top .indicator {
        position: absolute;
        bottom: 0;
        left: 10px;
        width: calc(95vw * 0.75 / 4 - 20px);
        height: 5px;
        background: #0f0;
        transition: left 0.5s ease, box-shadow 0.5s ease;
        pointer-events: none;
        z-index: 0;
      }

      .top .tab-menu {
        position: absolute;
        display: flex;
        justify-content: center;
        align-items: center;
        bottom: 0;
        right: 0;
        width: calc(95vw * 0.125);
        height: 100%;
        border-top-right-radius: 10px;
        background: rgb(0, 0, 0);
        z-index: 0;
      }

      .top .tab-menu i {
        font-size: var(--text-size-1);
        transition: 0.3s;
        color: #aaa;
        text-align: center;
        width: calc(95vw * 0.75 / 4);
        cursor: pointer;
        transition: color 0.3s ease;
        display: flex;
        flex-direction: column;
        align-items: center;
      }

      .top .tab-menu.active i,
      .top .tab-menu:hover i {
        color: #0f0;
        text-shadow: 0 0 10px rgb(0, 217, 43), 0 0 20px rgb(0, 213, 0);
      }

      .top .tab-content {
        display: none;
        position: absolute;
        top: 75px;
        right: 2.5vw;
        width: 250px;
        height: auto;
        background: #111;
        color: #fff;
        border-bottom-left-radius: 10px;
        box-sizing: border-box;
        padding: 10px;
        z-index: 999;
      }

      .top .tab-content.active {
        display: block;
      }

      /* Reset cơ bản */
      .accordion {
        margin-left: 15px;
        padding: 0;
        list-style: none;
      }

      /* Cấp 1 */
      .accordion > li {
        position: relative;
        padding-top: 5px;
        cursor: pointer;
        background: none;
        color: #fff;
        font-size: 18px;
        border-bottom: 1px solid #444;
        transition: background 0.2s;
      }

      /* Mũi tên cho cấp 1 và 2 */
      .accordion li > span::before {
        content: "▶";
        position: absolute;
        left: -15px;
        transition: transform 0.3s;
        font-size: 12px;
      }

      /* Submenu */
      .submenu1,
      .submenu2 {
        display: none;
        list-style: none;
        transition: all 0.3s ease;
      }

      .submenu1 li {
        color: #ddd;
        font-size: 15px;
        cursor: pointer;
        padding: 5px 15px 5px 5px;
        border-bottom: 1px solid #333;
      }

      .submenu1 li .submenu2 li {
        color: #ddd;
        font-size: 12px;
        cursor: pointer;
        padding: 5px 15px 5px 0;
        border-bottom: 1px solid #333;
      }

      .submenu1 li:hover,
      .submenu2 li:hover {
        color: #fff;
      }

      .submenu1 li > span::before {
        content: "▶";
        position: absolute;
        left: -5px;
        transition: transform 0.3s;
        font-size: 10px;
      }

      .submenu2 li > span::before {
        display: none;
      }

      /* Xoay khi active */
      .accordion li.active > span::before,
      .submenu1 li.active > span::before {
        transform: rotate(90deg);
      }

      @media (max-width: 540px) {
        .top {
          height: 50px;
        }
        .top .img img {
          box-shadow: 0 0 2px rgb(226, 226, 226), 0 0 2px rgb(250, 250, 250);
        }
        .top nav.menu label span {
          display: none;
        }
        .top .tab-content {
          display: none;
          position: absolute;
          top: 50px;
        }
      }

      .bottom {
        display: flex;
        position: relative;
        flex-direction: row;
        align-items: center;
        margin-top: 3px;
        height: calc(100vh - 77px);
        padding: 0;
        background: #000000;
        width: 95vw;
      }

      @media (max-width: 540px) {
        .bottom {
          height: calc(100vh - 52px);
        }
      }

      .bottom section {
        display: none;
        background-color: #000000;
      }

      .bottom section.active {
        width: 100%;
        height: 100%;
        gap: 5px;
        margin: auto;
        display: flex;
        overflow-x: scroll;
        align-items: center;
        align-content: center;
        flex-direction: column;
      }

      /* HOME */
      #video-container {
        width: 100%;
        height: auto;
        max-width: 895px;
        min-width: 315px;
        aspect-ratio: 16 / 9;
        margin: 0 auto;
        border-radius: 5px;
        border: 2.5px solid rgb(0, 0, 0);
        display: flex;
        background: #2a2a2a;
        align-items: center; /* Căn giữa theo chiều dọc */
        align-content: center;
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        position: relative;
        flex-direction: column; /* Nếu bạn có nhiều post, vẫn xếp theo dòng */
      }

      /* NEMS */
      .post {
        width: 100%;
        height: auto;
        min-width: 300px;
        margin: 0 auto;
        display: flex;
        flex-wrap: wrap;
        background: #2a2a2a;
        align-items: center; /* Căn giữa theo chiều dọc */
        align-content: center;
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        position: relative;
      }

      .post .p_1,
      .post .p_2 {
        width: calc(100% / 3);
        height: min-content;
        min-width: 300px;
        margin: 0px;
        padding: 0px;
        display: flex;
        align-items: center; /* Căn giữa theo chiều dọc */
        align-content: center;
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        position: relative;
        border: 1px solid #000;
        flex-direction: column; /* Nếu bạn có nhiều post, vẫn xếp theo dòng */
      }

      .post .p_1 iframe {
        width: 100%; /* Chiều rộng đầy div */
        aspect-ratio: 16/9;
        border: none;
      }

      .post .p_header {
        width: 100%;
        height: 30px;
        margin: 0;
        line-height: 1;
        display: flex;
        padding: 0 15px;
        font-size: var(--font-size);
        font-weight: 600;
        color: white;
        background-color: rgba(67, 67, 67, 0.708);
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        position: relative;
        flex-direction: column; /* Nếu bạn có nhiều post, vẫn xếp theo dòng */
      }

      .post .p_content {
        width: 100%;
        height: 22px;
        margin: 0;
        display: flex;
        flex-wrap: wrap;
        padding: 5px 10px;
        align-content: start;
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        overflow: hidden;
        text-align: justify;
      }

      .post .p_bottom {
        width: 100%;
        display: flex;
        flex-direction: row;
        justify-content: center;
        gap: 2%;
      }

      .post .p_bottom .p_infor,
      .post .p_bottom .p_btn {
        width: 47%;
        padding: 5px 10px;
        margin: 5px 0;
        display: flex;
        justify-content: center;
        line-height: 1;
        color: #fff;
        box-shadow: 2px 2px 2px #000000;
        text-decoration: none;
        border-radius: 5px;
      }

      .post .p_bottom .p_btn:hover a {
        color: #000;
      }

      @media (max-width: 990px) {
        .post .p_1 {
          width: calc(100% / 2);
        }

        .post .p_2 {
          width: calc(100%);
        }
      }

      @media (max-width: 660px) {
        .post .p_1,
        .post .p_2 {
          width: calc(100%);
        }
      }

      /* CONTACT */
      .s-contact .content {
        width: 100%;
        height: auto;
        min-width: 300px;
        margin: 0 auto;
        display: flex;
        flex-wrap: wrap;
        background: #2a2a2a;
        align-items: center;
        align-content: center;
        justify-content: center;
        justify-items: center;
        position: relative;
      }

      .s-contact .content .c-left,
      .s-contact .content .c-right {
        width: calc(100% / 2);
        min-width: 300px;
        max-width: 540px;
        gap: 10px;
        display: flex;
        flex-wrap: wrap;
        align-items: center;
        align-content: center;
        justify-content: center;
        justify-items: center;
        aspect-ratio: 1;
      }

      .s-contact .content .c-form {
        min-height: 50px;
        display: flex;
        flex-direction: column;
        align-items: center;
        align-content: center;
        justify-content: center;
        justify-items: center;
        padding: 10px;
        border-radius: 10px;
        border: 1px solid #000000;
      }

      .s-contact .content .c-form span {
        color: #ffffff;
        font-size: 18px;
        line-height: 1.1;
        width: 100%;
        display: flex;
        align-items: center;
        align-content: center;
        justify-content: center;
        justify-items: center;
      }

      .s-contact .content .c-form a {
        color: #ffffff;
        font-size: 15px;
        line-height: 1;
        width: 100%;
        display: flex;
        align-items: center;
        align-content: center;
        justify-content: center;
        justify-items: center;
      }

      .s-contact .content .c-form i {
        color: #e9d500;
        font-size: 15px;
        line-height: 1;
        margin: auto 2px;
        width: 20px;
      }

      .s-contact .content .c-form a:hover,
      .s-contact .content .c-form a:active {
        color: #0080ff;
        font-size: 15px;
        line-height: 1;
        width: 100%;
      }

      @media (max-width: 660px) {
        .s-contact .content .c-left,
        .s-contact .content .c-right {
          width: 100%;
        }

        .s-contact .content .c-left {
          aspect-ratio: unset;
        }
      }

      /* FOOTER */
      .footer {
        width: 100%;
        height: auto;
        min-width: 300px;
        margin: 0 auto;
        display: flex;
        flex-wrap: wrap;
        background: #2a2a2a;
        align-items: center; /* Căn giữa theo chiều dọc */
        align-content: center;
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        position: relative;
      }

      .footer .f-left,
      .footer .f-center,
      .footer .f-right {
        width: calc(100% / 3);
        height: min-content;
        min-width: 300px;
        margin: 0 auto;
        display: flex;
        align-items: center; /* Căn giữa theo chiều dọc */
        align-content: center;
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        position: relative;
        flex-direction: column; /* Nếu bạn có nhiều post, vẫn xếp theo dòng */
      }

      .footer .f-header {
        width: 100%;
        height: 30px;
        min-width: 300px;
        margin: 0;
        display: flex;
        padding: 0 15px;
        font-size: 18px;
        font-weight: 600;
        color: white;
        background-color: rgba(67, 67, 67, 0.708);
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        position: relative;
        flex-direction: column; /* Nếu bạn có nhiều post, vẫn xếp theo dòng */
      }

      .footer .f-content {
        width: 100%;
        height: fit-content;
        min-height: 30px;
        min-width: 300px;
        margin: 0;
        display: flex;
        padding: 5px 10px;
        align-items: center; /* Căn giữa theo chiều dọc */
        align-content: center;
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        position: relative;
        flex-direction: column; /* Nếu bạn có nhiều post, vẫn xếp theo dòng */
      }

      .f-content a {
        color: rgb(195, 195, 195);
        width: 100%;
        display: flex;
        height: 20px;
        font-size: 15px;
        text-decoration: none;
      }

      .f-content a i {
        margin-right: 3px;
        width: 20px;
        display: flex;
        align-items: center;
        justify-content: center;
        justify-items: center;
      }

      .f-content a:hover,
      .f-content a:active {
        color: #ededed;
      }

      @media (max-width: 990px) {
        .footer .f-left,
        .footer .f-center {
          width: calc(100% / 2);
        }

        .footer .f-right {
          width: 100%;
        }
      }

      @media (max-width: 660px) {
        .footer .f-left,
        .footer .f-center,
        .footer .f-right {
          width: 100%;
        }
      }

      /* COPYRIGHT */
      .copyright {
        font-size: 15px;
        text-align: center;
        opacity: 0.8;
        color: #c1c1c1; /* xám dịu */
      }
    </style>
  </head>
  <body>
    <div class="full-screen">
      <!-- Form Top -->
      <div class="top">
        <div class="img">
          <img
            src="https://raw.githubusercontent.com/OTVGroup/OTVGroup.com.vn/main/LOGO%20-%20OTVGroup.png"
            alt="Logo"
          />
        </div>
        <nav class="menu">
          <div class="indicator"></div>

          <label class="active" id="id-home">
            <i class="fa fa-home"></i>
            <span>Trang chủ</span>
          </label>
          <label id="id-info">
            <i class="fa-solid fa-address-card"></i>
            <span>Giới Thiệu</span>
          </label>
          <label id="id-news">
            <i class="fa-solid fa-newspaper"></i>
            <span>Tin Tức</span>
          </label>
          <label id="id-contact">
            <i class="fa-solid fa-headset"></i>
            <span>Liên hệ</span>
          </label>

          <div class="tab-menu">
            <i class="fa-solid fa-bars"></i>
          </div>
        </nav>
        <div class="tab-content">
          <ul class="accordion">
            <!-- Cấp 1 -->

            <li>
              <span>About</span>
              <!-- Cấp 2 -->
              <ul class="submenu1">
                <li>
                  <a href="https://otvgroup.github.io/OTVGroup" target="_blank">
                    <span>OTVGroup.com</span>
                  </a>
                </li>
                <li>
                  <a href="https://otvgroup.github.io/OTISShop" target="_blank">
                    <span>OTISShop.com</span>
                  </a>
                </li>
                <li>
                  <a
                    href="https://otvgroup.github.io/OTISStore"
                    target="_blank"
                  >
                    <span>OTISStore.com</span>
                  </a>
                </li>
                <li>
                  <a
                    href="https://otvgroup.github.io/OTISStudy"
                    target="_blank"
                  >
                    <span>OTISStudy.com</span>
                  </a>
                </li>
                <li>
                  <a
                    href="https://otvgroup.github.io/OTISStudio.com.vn"
                    target="_blank"
                  >
                    <span>OTISStudio.com</span>
                  </a>
                </li>
              </ul>
            </li>

            <li>
              <span>Services</span>
              <!-- Cấp 2 -->
              <ul class="submenu1">
                <li>
                  <span>Truyền thông & Giải trí</span>
                  <!-- Cấp 3 -->
                  <ul class="submenu2">
                    <li>
                      <a href="https://otvgroup.github.io/#">
                        <span>Nghiên Cứu Thị Trường</span>
                      </a>
                      <i class="fa-solid fa-chart-line"></i>
                    </li>
                    <li>
                      <a href="https://otvgroup.github.io/#">
                        <span>Truyền Thông Tổng Thể</span>
                      </a>
                      <i class="fa-solid fa-share-nodes"></i>
                    </li>
                    <li>
                      <a href="https://otvgroup.github.io/#">
                        <span>Sản Xuất & Quảng Cáo</span>
                      </a>
                      <i class="fa-solid fa-photo-film"></i>
                    </li>
                    <li>
                      <a href="https://otvgroup.github.io/#">
                        <span>Phát Triển Game</span>
                      </a>
                      <i class="fa-solid fa-gamepad"></i>
                    </li>
                    <li>
                      <a href="https://otvgroup.github.io/#">
                        <span>Âm Nhạc & Giải Trí</span>
                      </a>
                      <i class="fa-solid fa-music"></i>
                    </li>
                    <li>
                      <a href="https://otvgroup.github.io/#">
                        <span>Sáng Tạo Nội Dung</span>
                      </a>
                      <i class="fa-solid fa-palette"></i>
                    </li>
                  </ul>
                </li>
                <li>
                  <span>Thương mại</span>
                  <!-- Cấp 3 -->
                  <ul class="submenu2">
                    <li>
                      <a href="https://otvgroup.github.io/#">
                        <span>Xây Dựng Thương Hiệu</span>
                      </a>
                      <i class="fa-solid fa-star"></i>
                    </li>
                    <li>
                      <a href="https://otvgroup.github.io/#">
                        <span>Hoạch Định Chiến Lược</span>
                      </a>
                      <i class="fa-solid fa-lightbulb"></i>
                    </li>
                    <li>
                      <a href="https://otvgroup.github.io/#">
                        <span>Chuyển Đổi Công Nghệ</span>
                      </a>
                      <i class="fa-solid fa-diagram-project"></i>
                    </li>
                  </ul>
                </li>
                <li>
                  <span>Học thuật</span>
                  <!-- Cấp 3 -->
                  <ul class="submenu2">
                    <li>
                      <a href="https://otvgroup.github.io/#">
                        <span>Tư Liệu Nghiên Cứu</span>
                      </a>
                      <i class="fa-solid fa-book-open"></i>
                    </li>
                    <li>
                      <a href="https://otvgroup.github.io/#">
                        <span>Báo Cáo & Phân Tích</span>
                      </a>
                      <i class="fa-solid fa-chart-pie"></i>
                    </li>
                  </ul>
                </li>
                <li>
                  <span>Kỹ thuật</span>
                  <!-- Cấp 3 -->
                  <ul class="submenu2">
                    <li>
                      <a href="https://otvgroup.github.io/#">
                        <span>Thiết Kế & Phát Triển</span>
                      </a>
                      <i class="fa-solid fa-chalkboard-user"></i>
                    </li>
                    <li>
                      <a href="https://otvgroup.github.io/#">
                        <span>Cải Tiến & Ứng Dụng</span>
                      </a>
                      <i class="fa-solid fa-gears"></i>
                    </li>
                  </ul>
                </li>
                <li>
                  <span>Dịch vụ</span>
                  <!-- Cấp 3 -->
                  <ul class="submenu2">
                    <li>
                      <a href="https://otvgroup.github.io/#">
                        <span>Chăm Sóc & Tư Vấn</span>
                      </a>
                      <i class="fa-solid fa-headset"></i>
                    </li>
                    <li>
                      <a href="https://otvgroup.github.io/#">
                        <span>Bảo Hành & Bảo Trì</span>
                      </a>
                      <i class="fa-solid fa-screwdriver-wrench"></i>
                    </li>
                  </ul>
                </li>
              </ul>
            </li>

            <li>
              <span>Contact</span>
              <!-- Cấp 2 -->
              <ul class="submenu1">
                <li>
                  <a href="https://facebook.com/OtisVo586" target="_blank">
                    <span> Facebook </span>
                  </a>
                </li>
                <li>
                  <a href="tel:0329022431" target="_blank">
                    <span> Hotline </span>
                  </a>
                </li>
                <li>
                  <a href="mailto:thinhkvtm2006@gmail.com" target="_blank">
                    <span> E-mail </span>
                  </a>
                </li>
              </ul>
            </li>
          </ul>
        </div>
      </div>
      <script>
        const labels = document.querySelectorAll(".menu label");
        const indicator = document.querySelector(".indicator");
        labels.forEach((label, index) => {
          label.addEventListener("click", () => {
            document.querySelector(".active").classList.remove("active");
            label.classList.add("active");
            indicator.style.left = `calc(${index} * (95vw * 0.75 / 4) + 10px)`;
          });
        });
      </script>
      <script>
        const icons = document.querySelectorAll(".tab-menu i");
        const contents = document.querySelectorAll(".tab-content");

        icons.forEach((icon, index) => {
          icon.addEventListener("click", () => {
            // Nếu tab này đang mở thì ẩn đi
            if (contents[index].classList.contains("active")) {
              contents[index].classList.remove("active");
              icon.classList.remove("active");
              return;
            }

            // Ẩn hết các tab khác
            contents.forEach((c) => c.classList.remove("active"));
            icons.forEach((i) => i.classList.remove("active"));

            // Mở tab được chọn
            contents[index].classList.add("active");
            icon.classList.add("active");
          });
        });
      </script>
      <script>
        const accordionItems = document.querySelectorAll(".accordion > li");

        // Cấp 1
        accordionItems.forEach((item) => {
          const submenu1 = item.querySelector(".submenu1");

          item.addEventListener("click", (e) => {
            e.stopPropagation();

            if (!submenu1) return; // nếu không có cấp 2 thì bỏ qua

            const isOpen = item.classList.contains("active");

            // Đóng tất cả cấp 1 khác
            accordionItems.forEach((i) => {
              if (i !== item) {
                i.classList.remove("active");
                const sm1 = i.querySelector(".submenu1");
                if (sm1) sm1.style.display = "none";

                // đóng luôn cấp 3 bên trong nó
                const sm2 = i.querySelectorAll(".submenu2");
                sm2.forEach((s) => (s.style.display = "none"));
              }
            });

            // Toggle item được bấm
            if (isOpen) {
              item.classList.remove("active");
              submenu1.style.display = "none";
            } else {
              item.classList.add("active");
              submenu1.style.display = "block";
            }
          });

          // Cấp 2
          if (submenu1) {
            const submenu2Items = submenu1.querySelectorAll("li");

            submenu2Items.forEach((subItem) => {
              const submenu2 = subItem.querySelector(".submenu2");

              subItem.addEventListener("click", (e2) => {
                e2.stopPropagation();

                if (!submenu2) return;

                const isOpen = subItem.classList.contains("active");

                // Đóng tất cả cấp 3 khác trong cùng cấp 2
                submenu2Items.forEach((i) => {
                  if (i !== subItem) {
                    i.classList.remove("active");
                    const sm2 = i.querySelector(".submenu2");
                    if (sm2) sm2.style.display = "none";
                  }
                });

                // Toggle cấp 3
                if (isOpen) {
                  subItem.classList.remove("active");
                  submenu2.style.display = "none";
                } else {
                  subItem.classList.add("active");
                  submenu2.style.display = "block";
                }
              });
            });
          }
        });
      </script>

      <!-- Form Bottom -->
      <div class="bottom">
        <section class="s-home active">
          <!-- VIDEO -->
          <div id="video-container"></div>
          <script>
            const channels = [
              { id: "UCv-PFwjDGSfgozwLVCJEv0w", num: 2 },
              { id: "UC4UOBFi4HJHU_EhynZbrefw", num: 1 },
            ];

            const fixedVideo = "-lIuqy0Rycw"; // Video cố định
            let playlist = [];
            let currentvideo = 0;
            let player;

            // Load YouTube API
            function loadYouTubeAPI() {
              return new Promise((resolve) => {
                if (window.YT && YT.Player) return resolve();
                const tag = document.createElement("script");
                tag.src = "https://www.youtube.com/iframe_api";
                document.body.appendChild(tag);
                window.onYouTubeIframeAPIReady = () => resolve();
              });
            }

            // Lấy video ID từ guid (chuẩn hơn)
            function getVideoIdFromItem(item) {
              // guid: yt:video:VIDEO_ID
              return item.guid.split(":")[2] || null;
            }

            async function getLatestVideos(channel) {
              try {
                const res = await fetch(
                  `https://api.rss2json.com/v1/api.json?rss_url=https://www.youtube.com/feeds/videos.xml?channel_id=${channel.id}`
                );
                const data = await res.json();
                return data.items
                  .slice(0, channel.num) // <-- số video riêng cho từng kênh
                  .map((item) => item.guid.split(":")[2])
                  .filter((v) => v);
              } catch (err) {
                console.error("Lỗi RSS:", err);
                return [];
              }
            }

            async function buildPlaylist() {
              const allVideoLists = await Promise.all(
                channels.map((c) => getLatestVideos(c))
              );
              return [fixedVideo, ...allVideoLists.flat()].filter((v) => v);
            }

            function createPlayer() {
              player = new YT.Player("video-container", {
                videoId: playlist[currentvideo],
                playerVars: {
                  autoplay: 1,
                  mute: 1,
                  controls: 1, // ẩn controls YouTube
                  modestbranding: 1,
                  rel: 0,
                },
                events: {
                  onReady: (e) => e.target.playVideo(),
                  onStateChange: (e) => {
                    if (e.data === YT.PlayerState.ENDED) {
                      currentvideo = (currentvideo + 1) % playlist.length;
                      player.loadVideoById(playlist[currentvideo]);
                    }
                  },
                  // ✅ Thêm phần này
                  onError: (e) => {
                    console.warn(
                      "Video lỗi, chuyển sang video tiếp theo:",
                      e.data
                    );
                    currentvideo = (currentvideo + 1) % playlist.length;
                    player.loadVideoById(playlist[currentvideo]);
                  },
                },
              });
            }

            async function init() {
              playlist = await buildPlaylist();
              if (!playlist.length) return console.error("Playlist rỗng");
              await loadYouTubeAPI();
              createPlayer();
            }

            init();
          </script>

          <!-- INTRO -->

          <!-- POST -->
          <div class="post">
            <div class="p_header" style="--font-size: 18px">GROUP FACEBOOK</div>
            <div class="p_2" style="background: #daf3ffdd">
              <img
                src="https://scontent.fsgn5-14.fna.fbcdn.net/v/t39.30808-6/468426620_122122770164552182_2194104395195010555_n.jpg?_nc_cat=101&ccb=1-7&_nc_sid=2285d6&_nc_eui2=AeFpOB3VIGTT4g_qysqdEcSiKYy0lgannDYpjLSWBqecNkO2NVfb_lcSm6Bs-dYOCy5koTp3ax8x-6cq6EOlYKSD&_nc_ohc=S9hlq0vaxdYQ7kNvwES5iYW&_nc_oc=AdmWSFaPrPEZilHH_z4SYod0nonHbRTpNdhJ_br7wXEn8D68jNpJrX0Kdpz4WP5NXyE&_nc_zt=23&_nc_ht=scontent.fsgn5-14.fna&_nc_gid=Rdaf6jsLOVUcZToF_omH6Q&oh=00_Afn6d7VW44ATevy2kkEqt0Lq4d7E0FIucchuWEXcwfkhTw&oe=6957C30B"
                alt="Facebook Group_1"
                style="width: 100%; aspect-ratio: 2.5"
              />
              <div
                class="p_header"
                style="align-items: center; --font-size: 15px"
              >
                GÓC NHỎ
              </div>
              <div class="p_content" id="box_1">
                <span>
                  Góc Nhỏ - nơi mỗi câu chuyện, mỗi chia sẻ đều được lắng nghe.
                  Nơi chúng ta cùng nhau trò chuyện, học hỏi, và gắn kết. Dù bạn
                  đến để tâm sự, tìm cảm hứng hay đơn giản chỉ để ghé thăm, ở
                  đây luôn có một chỗ dành cho bạn.
                </span>
              </div>
              <i
                style="
                  color: #1877f2;
                  width: 100%;
                  padding: 0 10px;
                  display: flex;
                  justify-content: right;
                "
                onclick="changeHeight('box_1', this)"
              >
                ...Xem thêm
              </i>
              <div class="p_bottom">
                <div class="p_infor" style="background: #55ad4d">
                  Thành Viên: <i>144</i>
                </div>
                <div class="p_btn" style="background: #1877f2">
                  <a
                    href="https://www.facebook.com/share/g/1QXWdsNv8d/"
                    target="_blank"
                  >
                    👉 Tham gia
                  </a>
                </div>
              </div>
            </div>
            <div class="p_1" style="background: #daf3ffdd">
              <img
                src="https://scontent.fsgn5-9.fna.fbcdn.net/v/t39.30808-6/588843585_122194789730552182_3801606182584356093_n.jpg?_nc_cat=105&ccb=1-7&_nc_sid=2285d6&_nc_eui2=AeET72wqB2PkWp5i-Eb2iazOICeMEY6D7rcgJ4wRjoPutwO6LcPdGjZxJL-7FQXHE-txqJ5_ssbteAiGICKqmFvy&_nc_ohc=bwvxe8HnjvkQ7kNvwGfXbqW&_nc_oc=Adns_rMQCbcy3r5ganyXlzQOjkrbKrRH3lW-YVzTqe0GMN9Lvui93F_imMGbreqC5nk&_nc_zt=23&_nc_ht=scontent.fsgn5-9.fna&_nc_gid=ipZ87KIAmDn253sSlTWzMg&oh=00_AflhSREcArHCyFb3WAsvEvpkqRibpAe3mqmQ38pvabm_1g&oe=6957F3EE"
                alt="Facebook Group_2"
                style="width: 100%; aspect-ratio: 2.5"
              />
              <div
                class="p_header"
                style="align-items: center; --font-size: 15px"
              >
                THƯ VIỆN CẢM XÚC
              </div>
              <div class="p_content" id="box_2">
                <span>
                  Thư Viện Cảm Xúc - nơi mọi tâm tư, suy nghĩ, và cảm xúc đều
                  được trân trọng. Nơi để bạn chia sẻ những câu chuyện vui, nỗi
                  buồn, những khoảnh khắc nhỏ trong cuộc sống, hoặc đơn giản là
                  tìm một không gian để lắng nghe và được lắng nghe.
                </span>
              </div>
              <i
                style="
                  color: #1877f2;
                  width: 100%;
                  padding: 0 10px;
                  display: flex;
                  justify-content: right;
                "
                onclick="changeHeight('box_2', this)"
              >
                ...Xem thêm
              </i>
              <div class="p_bottom">
                <div class="p_infor" style="background: #55ad4d">
                  Thành Viên: <i>120</i>
                </div>
                <div class="p_btn" style="background: #1877f2">
                  <a
                    href="https://www.facebook.com/share/g/1ALyzrv8bd/"
                    target="_blank"
                  >
                    👉 Tham gia
                  </a>
                </div>
              </div>
            </div>
            <div class="p_1" style="background: #daf3ffdd">
              <img
                src="https://scontent.fsgn5-10.fna.fbcdn.net/v/t39.30808-6/604517169_122194791110552182_1561466510739720352_n.webp?stp=dst-jpg_tt6&_nc_cat=110&ccb=1-7&_nc_sid=2285d6&_nc_eui2=AeECUNinpN2JCsmcfKo5N-uFd2TGhEt5aiF3ZMaES3lqIcoBz3-ti_HX7e3LcZ2MEwrYId0p9kLLuA4gAW2ov36E&_nc_ohc=1b83OYf-hqAQ7kNvwGdtsNU&_nc_oc=AdlcGOssn0D1_bIeJ8DmkjIDSIMWYiFF9oCWzrX6y3nZq-7eqguskc4Jpph5CK8YFzA&_nc_zt=23&_nc_ht=scontent.fsgn5-10.fna&_nc_gid=BdoxFdiz-5WpbxYk60wkNQ&oh=00_AfnhO86UD8Ni0smAWJL4QPtuLej7KB3qSyb-4BpSohyMnw&oe=6957C9DE"
                alt="Facebook Group_3"
                style="width: 100%; aspect-ratio: 2.5"
              />
              <div
                class="p_header"
                style="align-items: center; --font-size: 15px"
              >
                TÂM THƯ GỬI NGƯỜI
              </div>
              <div class="p_content" id="box_3">
                <span>
                  Tâm Thư Gửi Người - nơi mọi tâm tư, nỗi niềm và cảm xúc đều
                  được gửi gắm và trân trọng. Nơi những lá thư chưa từng gửi đi,
                  những câu chuyện đời thường, niềm vui giản đơn, thậm chí cả
                  nỗi buồn hay những suy nghĩ sâu sắc về cuộc sống đều được lắng
                  nghe và đồng cảm.
                </span>
              </div>
              <i
                style="
                  color: #1877f2;
                  width: 100%;
                  padding: 0 10px;
                  display: flex;
                  justify-content: right;
                "
                onclick="changeHeight('box_3', this)"
              >
                ...Xem thêm
              </i>
              <div class="p_bottom">
                <div class="p_infor" style="background: #55ad4d">
                  Thành Viên: <i>122</i>
                </div>
                <div class="p_btn" style="background: #1877f2">
                  <a
                    href="https://www.facebook.com/share/g/1AbU625DZz/"
                    target="_blank"
                  >
                    👉 Tham gia
                  </a>
                </div>
              </div>
            </div>
          </div>
          <script>
            function changeHeight(ID, el) {
              const box = document.getElementById(ID);
              const currentHeight = getComputedStyle(box).height;

              if (currentHeight === "22px") {
                box.style.height = "max-content";
                el.innerText = "Thu gọn";
              } else {
                box.style.height = "22px";
                el.innerText = "...Xem thêm";
              }
            }
          </script>

          <div id="playlist" class="post">
            <div class="p_header">YOUTUBE SHORTS</div>
            <!-- Các video sẽ tự động tạo div .p_1 và nhúng iframe ở đây -->
          </div>

          <script>
            document.addEventListener("DOMContentLoaded", () => {
              const playlists = [
                // Kênh 1
                "https://www.youtube.com/playlist?list=PLr-nq1_tAgasf6lDFzZ34LCXk7WIScTmu",
                "https://www.youtube.com/playlist?list=PLr-nq1_tAgatx2oBmmzTCDbT3fknqYlYU",
                "https://www.youtube.com/playlist?list=PLr-nq1_tAgas2QA44VzY93Z6GqXpBt_vv",

                // Kênh 2
                "https://www.youtube.com/playlist?list=PL038F8U56LOuuPeCx2Yee_qXY9oWD-KNG",
                "https://www.youtube.com/playlist?list=PL038F8U56LOsyRWTAlSywFzqmx8NwYl5g",
                "https://www.youtube.com/playlist?list=PL038F8U56LOtvUTkMDYTZA7xaCHLHdVky",
              ];

              const container = document.getElementById("playlist");
              if (!container) return;

              playlists.forEach((link) => {
                const listId = new URL(link).searchParams.get("list");
                if (!listId) return;

                container.insertAdjacentHTML(
                  "beforeend",
                  `<div class="p_1">
                     <iframe
                       src="https://www.youtube.com/embed/videoseries?list=${listId}"
                       allowfullscreen>
                     </iframe>
                   </div>`
                );
              });
            });
          </script>

          <!-- F - CONTACT -->
          <div class="footer">
            <div class="f-left">
              <a class="f-header" style="align-items: left">OTVGroup</a>
              <div class="f-content">
                <a
                  href="https://maps.app.goo.gl/6Eh4xp7Ainpmf6FZ9"
                  target="_blank"
                >
                  <i class="fas fa-map-marker-alt"></i>Ho Chi Minh, Viet Nam
                </a>
                <a href="tel:+84329022431" target="_blank">
                  <i class="fa fa-phone"></i>0329 022 431
                </a>
                <a href="mailto:thinhkvtm2006@gmail.com" target="_blank">
                  <i class="fas fa-envelope"></i>thinhkvtm2006@gmail.com
                </a>
              </div>
            </div>
            <div class="f-center">
              <a class="f-header" style="align-items: left">MENU</a>
              <div class="f-content">
                <a href=""><i class="fa fa-home"></i>Trang Chủ</a>
                <a href=""
                  ><i class="fa-solid fa-address-card"></i>Giới Thiệu</a
                >
                <a href=""><i class="fa-solid fa-newspaper"></i>Tin Tức</a>
              </div>
            </div>
            <div class="f-right">
              <a class="f-header" style="align-items: left">LIÊN KẾT</a>
              <div class="f-content">
                <a href=""><i class="fab fa-facebook-f"></i>Facebook</a>
                <a href=""><i class="fab fa-youtube"></i>YouTube</a>
                <a href=""><i class="fab fa-tiktok"></i>Tik Tok</a>
              </div>
            </div>
          </div>

          <div class="copyright">
            © <span id="year"></span> OTVGroup. Tất cả các quyền được bảo lưu.
          </div>
        </section>
        <section class="s-info">
          <!-- F - CONTACT -->
          <div class="footer">
            <div class="f-left">
              <a class="f-header" style="align-items: left">OTVGroup</a>
              <div class="f-content">
                <a
                  href="https://maps.app.goo.gl/6Eh4xp7Ainpmf6FZ9"
                  target="_blank"
                >
                  <i class="fas fa-map-marker-alt"></i>Ho Chi Minh, Viet Nam
                </a>
                <a href="tel:+84329022431" target="_blank">
                  <i class="fa fa-phone"></i>0329 022 431
                </a>
                <a href="mailto:thinhkvtm2006@gmail.com" target="_blank">
                  <i class="fas fa-envelope"></i>thinhkvtm2006@gmail.com
                </a>
              </div>
            </div>
            <div class="f-center">
              <a class="f-header" style="align-items: left">MENU</a>
              <div class="f-content">
                <a href=""><i class="fa fa-home"></i>Trang Chủ</a>
                <a href=""
                  ><i class="fa-solid fa-address-card"></i>Giới Thiệu</a
                >
                <a href=""><i class="fa-solid fa-newspaper"></i>Tin Tức</a>
              </div>
            </div>
            <div class="f-right">
              <a class="f-header" style="align-items: left">LIÊN KẾT</a>
              <div class="f-content">
                <a href=""><i class="fab fa-facebook-f"></i>Facebook</a>
                <a href=""><i class="fab fa-youtube"></i>YouTube</a>
                <a href=""><i class="fab fa-tiktok"></i>Tik Tok</a>
              </div>
            </div>
          </div>

          <div class="copyright">
            © <span id="year"></span> OTVGroup. Tất cả các quyền được bảo lưu.
          </div>
        </section>
        <section class="s-news">
          <!-- F - CONTACT -->
          <div class="footer">
            <div class="f-left">
              <a class="f-header" style="align-items: left">OTVGroup</a>
              <div class="f-content">
                <a
                  href="https://maps.app.goo.gl/6Eh4xp7Ainpmf6FZ9"
                  target="_blank"
                >
                  <i class="fas fa-map-marker-alt"></i>Ho Chi Minh, Viet Nam
                </a>
                <a href="tel:+84329022431" target="_blank">
                  <i class="fa fa-phone"></i>0329 022 431
                </a>
                <a href="mailto:thinhkvtm2006@gmail.com" target="_blank">
                  <i class="fas fa-envelope"></i>thinhkvtm2006@gmail.com
                </a>
              </div>
            </div>
            <div class="f-center">
              <a class="f-header" style="align-items: left">MENU</a>
              <div class="f-content">
                <a href=""><i class="fa fa-home"></i>Trang Chủ</a>
                <a href=""
                  ><i class="fa-solid fa-address-card"></i>Giới Thiệu</a
                >
                <a href=""><i class="fa-solid fa-newspaper"></i>Tin Tức</a>
              </div>
            </div>
            <div class="f-right">
              <a class="f-header" style="align-items: left">LIÊN KẾT</a>
              <div class="f-content">
                <a href=""><i class="fab fa-facebook-f"></i>Facebook</a>
                <a href=""><i class="fab fa-youtube"></i>YouTube</a>
                <a href=""><i class="fab fa-tiktok"></i>Tik Tok</a>
              </div>
            </div>
          </div>

          <div class="copyright">
            © <span id="year"></span> OTVGroup. Tất cả các quyền được bảo lưu.
          </div>
        </section>
        <section class="s-contact">
          <div class="content">
            <div class="c-left">
              <div
                class="c-form"
                onclick="window.open('#')"
                style="
                  width: calc(90% + 10px);
                  background: #272727;
                  box-shadow: 2px 2px 2px #000000;
                "
              >
                <span>LIÊN HỆ NGAY</span>
                <div
                  style="
                    width: 100%;
                    display: flex;
                    flex-direction: row;
                    align-items: center;
                    align-items: center;
                    justify-content: center;
                    justify-items: center;
                  "
                >
                  <img
                    src="https://raw.githubusercontent.com/OTVGroup/OTVGroup.com.vn/main/LOGO%20-%20OTVGroup.png"
                    alt="Logo"
                    style="
                      width: 30%;
                      min-width: 90px;
                      max-width: 120px;
                      aspect-ratio: 1;
                      margin-right: clamp(5px, 1vw, 30px);
                    "
                  />
                  <div
                    style="
                      width: 70%;
                      min-width: 180px;
                      max-width: 230px;
                      margin-left: clamp(5px, 1vw, 30px);
                      display: flex;
                      gap: 15px;
                      flex-direction: column;
                    "
                  >
                    <a
                      href="https://maps.app.goo.gl/6Eh4xp7Ainpmf6FZ9"
                      target="_blank"
                      style="width: fit-content; font-size: 16px"
                    >
                      <i class="fas fa-map-marker-alt"></i>Ho Chi Minh, Viet Nam
                    </a>
                    <a
                      href="mailto:thinhkvtm2006@gmail.com"
                      target="_blank"
                      style="width: fit-content; font-size: 16px"
                    >
                      <i class="fas fa-envelope"></i>thinhkvtm2006@gmail.com
                    </a>
                    <a
                      href="tel:+84329022431"
                      target="_blank"
                      style="width: fit-content; font-size: 16px"
                    >
                      <i class="fa fa-phone"></i>0329 022 431
                    </a>
                  </div>
                </div>
              </div>
              <div
                class="c-form"
                onclick="window.open('#')"
                onmouseout=" this.style.transform='scale(1)';"
                onmouseover="this.style.transform='scale(1.02)';"
                style="
                  width: calc(90% / 2);
                  transition: ease 0.5s;
                  background: #2232c2;
                  box-shadow: 2px 2px 2px #000000;
                "
              >
                <span>ĐÁNH GIÁ</span>
                <a>
                  <i class="fa-solid fa-star"></i>
                  <i class="fa-solid fa-star"></i>
                  <i class="fa-solid fa-star"></i>
                  <i class="fa-solid fa-star"></i>
                  <i class="fa-solid fa-star"></i>
                </a>
              </div>
              <div
                class="c-form"
                onclick="window.open('#')"
                onmouseout=" this.style.transform='scale(1)';"
                onmouseover="this.style.transform='scale(1.02)';"
                style="
                  width: calc(90% / 2);
                  transition: ease 0.5s;
                  background: #2a9f00;
                  box-shadow: 2px 2px 2px #000000;
                "
              >
                <span>ĐỀ XUẤT</span>
                <a>
                  <i class="fa-solid fa-book-open"></i>
                  <i class="fa-solid fa-check"></i>
                  <i class="fa-solid fa-note-sticky"></i>
                  <i class="fa-solid fa-check"></i>
                  <i class="fa-solid fa-book-open"></i>
                </a>
              </div>
              <div
                class="c-form"
                onclick="window.open('#')"
                onmouseout=" this.style.transform='scale(1)';"
                onmouseover="this.style.transform='scale(1.02)';"
                style="
                  width: calc(90% + 10px);
                  transition: ease 0.5s;
                  background: #c22222;
                  box-shadow: 2px 2px 2px #000000;
                "
              >
                <span>ĐĂNG KÝ THÀNH VIÊN</span>
                <a>
                  <i class="fa-solid fa-paper-plane"></i>
                  <i class="fa-solid fa-paper-plane"></i>
                  <i class="fa-solid fa-paper-plane"></i>
                  <i class="fa-solid fa-paper-plane"></i>
                  <i class="fa-solid fa-paper-plane"></i>
                </a>
              </div>
            </div>

            <div class="c-right">
              <iframe
                style="width: calc(90% + 10px); aspect-ratio: 1"
                loading="lazy"
                src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d15673.237375022063!2d106.61597899409112!3d10.864059701878784!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x31752a1dd5849c15%3A0x74da5b070b51174e!2zVMOibiBDaMOhbmggSGnhu4dwLCBRdeG6rW4gMTIsIFRow6BuaCBwaOG7kSBI4buTIENow60gTWluaCwgVmnhu4d0IE5hbQ!5e0!3m2!1svi!2s!4v1765463292309!5m2!1svi!2s"
                title="Tân Chánh Hiệp, Quận 12, Thành phố Hồ Chí Minh, Việt Nam"
                aria-label="Tân Chánh Hiệp, Quận 12, Thành phố Hồ Chí Minh, Việt Nam"
              ></iframe>
            </div>
          </div>

          <!-- F - CONTACT -->
          <div class="footer">
            <div class="f-left">
              <a class="f-header" style="align-items: left">OTVGroup</a>
              <div class="f-content">
                <a
                  href="https://maps.app.goo.gl/6Eh4xp7Ainpmf6FZ9"
                  target="_blank"
                >
                  <i class="fas fa-map-marker-alt"></i>Ho Chi Minh, Viet Nam
                </a>
                <a href="tel:+84329022431" target="_blank">
                  <i class="fa fa-phone"></i>0329 022 431
                </a>
                <a href="mailto:thinhkvtm2006@gmail.com" target="_blank">
                  <i class="fas fa-envelope"></i>thinhkvtm2006@gmail.com
                </a>
              </div>
            </div>
            <div class="f-center">
              <a class="f-header" style="align-items: left">MENU</a>
              <div class="f-content">
                <a href=""><i class="fa fa-home"></i>Trang Chủ</a>
                <a href=""
                  ><i class="fa-solid fa-address-card"></i>Giới Thiệu</a
                >
                <a href=""><i class="fa-solid fa-newspaper"></i>Tin Tức</a>
              </div>
            </div>
            <div class="f-right">
              <a class="f-header" style="align-items: left">LIÊN KẾT</a>
              <div class="f-content">
                <a href=""><i class="fab fa-facebook-f"></i>Facebook</a>
                <a href=""><i class="fab fa-youtube"></i>YouTube</a>
                <a href=""><i class="fab fa-tiktok"></i>Tik Tok</a>
              </div>
            </div>
          </div>

          <div class="copyright">
            © <span id="year"></span> OTVGroup. Tất cả các quyền được bảo lưu.
          </div>
        </section>
      </div>
      <script>
        // ánh xạ id button -> class section
        const map = {
          "id-home": "s-home",
          "id-info": "s-info",
          "id-news": "s-news",
          "id-contact": "s-contact",
        };

        // Lặp qua từng nút
        Object.keys(map).forEach((id) => {
          document.getElementById(id).addEventListener("click", () => {
            // Ẩn hết section
            document.querySelectorAll(".bottom section").forEach((sec) => {
              sec.classList.remove("active");
            });

            // Hiện đúng section
            document.querySelector("." + map[id]).classList.add("active");
          });
        });
      </script>
    </div>
  </body>
</html>

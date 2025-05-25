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

    <!-- Google tag (gtag.js) -->
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
        font-family: Arial, sans-serif;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: flex-start;
        background-color: #000000;
        color: #ffffff;
        width: auto;
        user-select: none;
      }

      .header {
        background-color: #000000;
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 2%;
        padding: 15px;
        z-index: 999;
      }

      .header img {
        cursor: pointer;
        border-radius: 50%;
        transition: transform 1s ease;
      }

      .container1,
      .container2 {
        position: fixed;
        bottom: 10px;
        height: auto;
        display: flex;
        flex-direction: column;
        align-items: center;
        justify-content: center;
        gap: 10px;
      }

      .container1 {
        left: 10px;
      }

      .container2 {
        right: 10px;
      }

      .icon {
        border-radius: 50%;
        display: flex;
        cursor: pointer;
        align-items: center;
        justify-content: center;
        transition: transform 1.5s ease;
      }

      .icon:active,
      .header img:active {
        transform: scale(1.2);
        border-radius: 50%;
      }

      .icon img {
        width: 40px;
        height: 40px;
        object-fit: cover;
        border-radius: 50%;
      }

      .contact-Content {
        position: fixed;
        color: white;
        background-color: #202020;
        border-radius: 10px;
        padding: 10px;
        width: 95%;
        max-width: 400px;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%) scale(0.9);
        display: none;
        transition: transform 0.3s ease, opacity 0.3s ease;
        z-index: 1;
      }

      .contact-Content.active {
        transform: translate(-50%, -50%) scale(1);
        display: block;
        z-index: 999;
      }

      .contact-Content img {
        width: 75%;
        margin: 10px 12.5% 0 12.5%;
      }

      .products {
        margin-top: 17px;
        display: flex;
        flex-wrap: wrap;
        justify-content: center;
        gap: 10px;
        width: auto;
      }

      .productss,
      .productss0,
      .productss1,
      .productss2,
      .productss3,
      .productss4,
      .productss5,
      .productss6 {
        width: 100%;
        min-width: 320px;
        height: auto;
        padding: 2.5px 0;
        text-align: center;
        background-color: #252525;
        font-size: 14px;
      }

      .productss0 {
        background-color: #000;
        height: 0;
      }

      .product {
        background-color: #252525;
        border-radius: 5px;
        padding: 5px;
        text-align: center;
        align-items: center;
        color: #ffffff;
        width: auto;
        box-sizing: border-box;
        opacity: 0;
        transform: translateY(50px);
      }

      .product.hidden {
        opacity: 0;
        transform: translateY(0px);
        transition: opacity 1s ease, transform 1s ease;
      }

      .product.active {
        opacity: 1;
        transform: translateY(0);
        transition: opacity 1s ease, transform 1s ease;
      }

      .product-img {
        display: flex; /* Kích hoạt Flexbox */
        gap: 5px; /* Tạo khoảng cách giữa các phần tử */
      }

      .product-img > * {
        flex: 1; /* Đảm bảo các phần tử có kích thước bằng nhau */
      }

      .product-img1,
      .product-img2 {
        height: auto;
        position: relative;
        display: inline-block;
      }

      .product-no {
        position: absolute;
        width: 100%;
        height: 15px;
        font-size: 10px;
        text-align: center;
        justify-content: center;
        text-shadow: 0 0 12px rgba(0, 0, 0, 0.7);
      }

      .product-img1 .product-no {
        top: 60px;
      }
      .product-img2 .product-no {
        top: 125px;
        background-color: #555555;
      }

      .product-img1 img {
        width: 85px;
        height: 85px;
      }
      .product-img2 img {
        width: 140px;
        height: 140px;
      }

      .product-name {
        display: flex; /* Kích hoạt Flexbox */
        flex-direction: row; /* Sắp xếp phần tử theo hàng ngang */
        justify-content: center; /* Căn giữa các phần tử theo chiều ngang */
        align-items: center; /* Căn giữa các phần tử theo chiều dọc */
        width: auto; /* Đảm bảo chỉ chiếm diện tích vừa đủ nội dung */
        font-weight: bold;
        height: 12px;
        font-size: 10px;
        gap: 1px;
      }

      .product-price {
        color: #ff5733;
      }

      .product-pcs {
        color: #ffd22d;
      }

      .arrow-btn1,
      .arrow-btn6 {
        cursor: pointer;
        font-size: 28px;
        font-weight: bold;
        color: white;
        width: 40px;
        height: auto;
        background-color: #00000000;
        border-radius: 3px;
        display: flex;
        text-align: center;
        justify-content: center;
        transition: background-color 0.5s, transform 0.5s;
      }

      .arrow-btn1:active,
      .arrow-btn6:active {
        border-radius: 3px;
        box-shadow: 0 0 5px 5px rgba(255, 255, 255, 0.2);
      }

      /* Hiệu ứng phát sáng */
      .glow-effect {
        border-radius: 3px;
        box-shadow: 0 0 15px 3px rgba(255, 255, 255, 0.805); /* Màu vàng phát sáng */
      }

      .home-button {
        display: inline-flex;
        align-items: center;
        position: fixed;
        justify-content: center;
        top: 0;
        right: 0;
        width: 24px;
        height: 24px;
        z-index: 1001;
        background-color: #2e2e2e;
        border-radius: 0% 0% 0% 10%;
      }

      .home-button a {
        color: white;
        bottom: 1px;
        text-decoration: none;
        font-size: 24px;
      }
      .home-button:hover {
        background-color: #858585;
        transform: scale(1.1);
      }
      .gallery {
        width: 100%;
        height: 100%;
        position: fixed;
        display: flex;
        flex-direction: column;
        flex-wrap: wrap;
        background-color: #000000;
        z-index: 1000;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        overflow-x: auto; /* Cuộn dọc */
        scroll-behavior: smooth; /* Cuộn mượt */
        align-content: center;
      }
      .gallery img {
        width: 80%;
        height: auto;
        box-shadow: 0 0 5px 5px rgb(125, 125, 125);
        margin: 10px 10%;
      }
    </style>
  </head>
  <div style="display: none">
    <!-- Thẻ Tìm Kiếm -->
    <h6>Nick KVTM</h6>
    <h6>Mua acc KVTM</h6>
    <h6>Bán acc KVTM</h6>
    <h6>KVTM VIP</h6>
    <h6>Acc KVTM rẻ nhất</h6>
    <h6>KVTM full tài nguyên</h6>
    <h6>Mua acc KVTM giá rẻ</h6>
    <h6>Bán acc KVTM uy tín</h6>
    <h6>Tặng acc KVTM</h6>
    <h6>Cửa hàng acc KVTM</h6>
    <h6>Nick Free Fire</h6>
    <h6>Mua acc Free Fire</h6>
    <h6>Bán acc Free Fire</h6>
    <h6>Free Fire VIP</h6>
    <h6>Acc Free Fire rẻ nhất</h6>
    <h6>Free Fire full nhân vật</h6>
    <h6>Acc Free Fire full skin</h6>
    <h6>Mua acc Free Fire giá rẻ</h6>
    <h6>Bán acc Free Fire uy tín</h6>
    <h6>Tặng acc Free Fire</h6>
    <h6>Cửa hàng acc Free Fire</h6>
    <h6>Nick Clash of Clans</h6>
    <h6>Mua acc Clash of Clans</h6>
    <h6>Bán acc Clash of Clans</h6>
    <h6>Clash of Clans VIP</h6>
    <h6>Acc Clash of Clans rẻ nhất</h6>
    <h6>Clash of Clans full tài nguyên</h6>
    <h6>Acc Clash of Clans full cấp</h6>
    <h6>Mua acc Clash of Clans giá rẻ</h6>
    <h6>Bán acc Clash of Clans uy tín</h6>
    <h6>Tặng acc Clash of Clans</h6>
    <h6>Cửa hàng acc Clash of Clans</h6>
    <h6>Nick Dragon City</h6>
    <h6>Mua acc Dragon City</h6>
    <h6>Bán acc Dragon City</h6>
    <h6>Dragon City VIP</h6>
    <h6>Acc Dragon City rẻ nhất</h6>
    <h6>Dragon City full rồng</h6>
    <h6>Acc Dragon City full tài nguyên</h6>
    <h6>Mua acc Dragon City giá rẻ</h6>
    <h6>Bán acc Dragon City uy tín</h6>
    <h6>Tặng acc Dragon City</h6>
    <h6>Cửa hàng acc Dragon City</h6>
    <h6>Nick Liên Quân</h6>
    <h6>Mua acc Liên Quân</h6>
    <h6>Bán acc Liên Quân</h6>
    <h6>Liên Quân VIP</h6>
    <h6>Acc Liên Quân rẻ nhất</h6>
    <h6>Liên Quân full tướng</h6>
    <h6>Acc Liên Quân full skin</h6>
    <h6>Mua acc Liên Quân giá rẻ</h6>
    <h6>Bán acc Liên Quân uy tín</h6>
    <h6>Tặng acc Liên Quân</h6>
    <h6>Mua bán acc Liên Quân</h6>
    <h6>Cửa hàng acc Liên Quân</h6>
    <h6>Tài khoản</h6>
    <h6>Nick</h6>
    <h6>Mua ac</h6>
    <h6>Bán acc</h6>
    <h6>VIP</h6>
    <h6>Giá rẻ</h6>
    <h6>Full tài nguyên</h6>
    <h6>Full nhân vật</h6>
    <h6>Full skin</h6>
    <h6>Cửa hàng acc</h6>
    <h6>Cửa hàng uy tín</h6>
    <h6>Tặng acc</h6>
    <h6>Mua bán acc</h6>
    <h6>Mùa mới</h6>
    <h6>Cao thủ</h6>
  </div>
  <body>
    <img
      src="https://i.pinimg.com/474x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
      alt="Logo"
      style="display: none"
    />
    <div class="home-button" onclick="infor('OFF')">
      <a href="#" title="Go to Home">&#8962;</a>
    </div>
    <div class="header">
      <img
        src="https://i.pinimg.com/474x/39/2f/3a/392f3a868a6a44adb7b4514709941445.jpg"
        alt="Logo Khu Vườn Trên Mây"
        style="width: 40px; height: 40px"
        onclick="filterProducts('kvtm')"
      />

      <img
        src="https://i.pinimg.com/474x/e1/14/f3/e114f324ca6461bb9b342f34292b60ad.jpg"
        alt="Logo Liên Quân"
        style="width: 40px; height: 40px"
        onclick="filterProducts('lq')"
      />

      <img
        src="https://i.pinimg.com/474x/8e/ae/cd/8eaecd44d50cf21bead6c2c9d540ceaf.jpg"
        alt="Logo Clash of Clans"
        style="width: 40px; height: 40px"
        onclick="filterProducts('coc')"
      />

      <img
        src="https://i.pinimg.com/474x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
        alt="Logo Home"
        style="border: 2px solid rgb(255, 255, 255); width: 60px; height: 60px"
        onclick="filterProducts('all')"
      />

      <img
        src="https://i.pinimg.com/474x/4b/2f/39/4b2f39d773c23626002eb7eeaacaebd7.jpg"
        alt="Logo Dragon City"
        style="width: 40px; height: 40px"
        onclick="filterProducts('dc')"
      />

      <img
        src="https://i.pinimg.com/474x/bc/12/70/bc1270fbfd9b08f0a98cef6ead98dc7c.jpg"
        alt="Logo Free Fire"
        style="width: 40px; height: 40px"
        onclick="filterProducts('ff')"
      />

      <img
        src="https://i.pinimg.com/474x/a6/6e/d5/a66ed5d684d002c477014c942c803fde.jpg"
        alt="Logo Khác"
        style="width: 40px; height: 40px"
        onclick="filterProducts('khac')"
      />
    </div>
    <!-- Danh Sách Hiển Thị -->
    <div class="products" id="product-list">
      <!-- COMBO -->
      <!-- <div class="productss1" id="kvtm">Combo</div> -->
      <!-- COMBO -->

      <div class="productss0" id="pd0"></div>

      <!-- VP.KVTM -->
      <!-- Sấy 0 -->
      <!-- Nước Ép 0 -->
      <!-- Vải 0 -->
      <!-- Ngọc 0 -->
      <!-- Tinh Dầu 0 -->
      <!-- Trà 0 -->
      <!-- Hoa Tươi 0 -->
      <!-- Nước Hoa 0 -->
      <!-- Túi Hương 0 -->
      <!-- Vật Phẩm May 0 -->
      <!-- Hạt Giống 0 -->
      <!-- Bọ 0 -->
      <!-- Vật Phẩm Khác 0 -->
      <!-- Vàng & Vật Phẩm Sự Kiện 0 -->
      <!-- VP.KVTM -->

      <div class="productss0" id="pd0"></div>

      <!-- ACC Game --><!-- Acc Khu Vườn Trên Mây 1 -->
      <div class="productss1" id="kvtm">ACC Khu Vườn Trên Mây</div>
      <div class="product kvtm">
        <div class="product-img2">
          <img
            src="https://i.pinimg.com/736x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
            alt="KVTM"
            onclick="infor('KVTM')"
          />
          <div class="product-no">KVTM</div>
        </div>
        <div class="product-name">
          <div class="product-price">100k VNĐ</div>
        </div>
      </div>
      <!-- Thẻ Game 2 -->
      <div class="productss6" id="khac">Thẻ Game</div>
      <div class="product khac">
        <div class="product-img2">
          <img
            src="https://i.pinimg.com/736x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
            alt="Thẻ Garena"
            onclick="infor('Thẻ Garena')"
          />
          <div class="product-no">Thẻ Garena</div>
        </div>
        <div class="product-name">
          <div class="product-price">100k VNĐ</div>
        </div>
      </div>
      <div class="product khac">
        <div class="product-img2">
          <img
            src="https://i.pinimg.com/736x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
            alt="Thẻ Zing"
            onclick="infor('Thẻ Zing')"
          />
          <div class="product-no">Thẻ Zing</div>
        </div>
        <div class="product-name">
          <div class="product-price">100k VNĐ</div>
        </div>
      </div>
      <!-- ACC Game -->

      <!-- NỘI DUNG HIỂN THỊ -->
      <div class="productss" id="Test1" style="display: none">
        Không Có Mục Nào
      </div>
      <div class="productss" id="Test2" style="display: none">
        Không Có Mục Nào
      </div>
      <div class="productss" id="Test3" style="display: none">
        Không Có Mục Nào
      </div>
      <div class="productss" id="Test4" style="display: none">
        Không Có Mục Nào
      </div>
      <div class="productss" id="Test5" style="display: none">
        Không Có Mục Nào
      </div>
      <div class="productss" id="Test6" style="display: none">
        Không Có Mục Nào
      </div>
    </div>

    <!-- Nút Điều Hướng -->
    <div class="container1">
      <div id="arrowUp1" class="arrow-btn1" style="transform: rotate(-90deg)">
        >
      </div>
      <div id="arrowDown1" class="arrow-btn1" style="transform: rotate(90deg)">
        >
      </div>
    </div>
    <div class="container1">
      <div id="arrowUp6" class="arrow-btn6" style="transform: rotate(-90deg)">
        >
      </div>
      <div id="arrowDown6" class="arrow-btn6" style="transform: rotate(90deg)">
        >
      </div>
    </div>

    <div class="container2">
      <div class="icon" onclick="toggleContact('contact-Content')">
        <img
          src="https://i.pinimg.com/474x/42/bc/f8/42bcf85126a5757cd190602a4952db32.jpg"
          alt="Content"
        />
      </div>
      <div class="contact-Content" id="contact-Content">
        <div style="text-align: center; width: 100%">
          <div style="font-size: 18px; font-weight: 600">
            Thông Tin Chi Tiết!
          </div>
          <button
            style="
              position: absolute;
              right: 5px;
              top: 3px;
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
        <p style="text-align: center; font-size: 14px">
          OTISStore | Uy Tín Tạo Nên Thương Hiệu!
        </p>
      </div>
    </div>

    <!-- Thông Tin --><!-- Acc Khu Vườn Trên Mây 1 -->
    <div class="gallery" style="display: none" id="KVTM">
      <img
        src="https://scontent.fsgn5-9.fna.fbcdn.net/v/t39.30808-6/492354735_122136206864661217_7949125846570999972_n.jpg?stp=dst-jpg_s960x960_tt6&_nc_cat=102&ccb=1-7&_nc_sid=cc71e4&_nc_ohc=t4YCY0IsaDMQ7kNvwGbQhwZ&_nc_oc=AdmJOu-3jVS8-j3615CcfVUkWOcXfubWYXyHjn8CYw0y57KKrAZdx1aFJmAPUy2RpzY&_nc_zt=23&_nc_ht=scontent.fsgn5-9.fna&_nc_gid=kdhQM6XKI_wPVsF4j4KXDQ&oh=00_AfL6IM8U9mskCPWwEaxgDCQsYWhh-A44k5D28UICMUbKYA&oe=6838AE8D"
        alt="KVTM"
      />
    </div>
    <!-- Thẻ Game 2 -->
    <div class="gallery" style="display: none" id="Thẻ Garena">
      <img
        src="https://scontent.fsgn5-9.fna.fbcdn.net/v/t39.30808-6/492354735_122136206864661217_7949125846570999972_n.jpg?stp=dst-jpg_s960x960_tt6&_nc_cat=102&ccb=1-7&_nc_sid=cc71e4&_nc_ohc=t4YCY0IsaDMQ7kNvwGbQhwZ&_nc_oc=AdmJOu-3jVS8-j3615CcfVUkWOcXfubWYXyHjn8CYw0y57KKrAZdx1aFJmAPUy2RpzY&_nc_zt=23&_nc_ht=scontent.fsgn5-9.fna&_nc_gid=kdhQM6XKI_wPVsF4j4KXDQ&oh=00_AfL6IM8U9mskCPWwEaxgDCQsYWhh-A44k5D28UICMUbKYA&oe=6838AE8D"
        alt="Thẻ Garena"
      />
    </div>
    <div class="gallery" style="display: none" id="Thẻ Zing">
      <img
        src="https://scontent.fsgn5-9.fna.fbcdn.net/v/t39.30808-6/492354735_122136206864661217_7949125846570999972_n.jpg?stp=dst-jpg_s960x960_tt6&_nc_cat=102&ccb=1-7&_nc_sid=cc71e4&_nc_ohc=t4YCY0IsaDMQ7kNvwGbQhwZ&_nc_oc=AdmJOu-3jVS8-j3615CcfVUkWOcXfubWYXyHjn8CYw0y57KKrAZdx1aFJmAPUy2RpzY&_nc_zt=23&_nc_ht=scontent.fsgn5-9.fna&_nc_gid=kdhQM6XKI_wPVsF4j4KXDQ&oh=00_AfL6IM8U9mskCPWwEaxgDCQsYWhh-A44k5D28UICMUbKYA&oe=6838AE8D"
        alt="Thẻ Zing"
      />
    </div>
    <!-- Thông Tin -->

    <script>
      function filterProducts(category) {
        const products = document.querySelectorAll(".product");
        const element0 = document.querySelectorAll('[id="pd0"]');
        const element1 = document.querySelectorAll('[id="kvtm"]');
        const element2 = document.querySelectorAll('[id="lq"]');
        const element3 = document.querySelectorAll('[id="coc"]');
        const element4 = document.querySelectorAll('[id="dc"]');
        const element5 = document.querySelectorAll('[id="ff"]');
        const element6 = document.querySelectorAll('[id="khac"]');
        const arrow1 = document.querySelectorAll(".arrow-btn1");
        const arrow6 = document.querySelectorAll(".arrow-btn6");
        const Image0 = document.querySelector('img[alt="Logo Home"]');
        const Image1 = document.querySelector(
          'img[alt="Logo Khu Vườn Trên Mây"]'
        );
        const Image2 = document.querySelector('img[alt="Logo Liên Quân"]');
        const Image3 = document.querySelector('img[alt="Logo Clash of Clans"]');
        const Image4 = document.querySelector('img[alt="Logo Dragon City"]');
        const Image5 = document.querySelector('img[alt="Logo Free Fire"]');
        const Image6 = document.querySelector('img[alt="Logo Khác"]');

        // Tìm tất cả các thẻ có class "product kvtm"
        const product1 = document.querySelectorAll(".product.kvtm");
        // Tìm thẻ có id="Test1"
        const test1 = document.getElementById("Test1");
        // Tìm tất cả các thẻ có class "product kvtm"
        const product2 = document.querySelectorAll(".product.lq");
        // Tìm thẻ có id="Test2"
        const test2 = document.getElementById("Test2");
        // Tìm tất cả các thẻ có class "product kvtm"
        const product3 = document.querySelectorAll(".product.coc");
        // Tìm thẻ có id="Test3"
        const test3 = document.getElementById("Test3");
        // Tìm tất cả các thẻ có class "product kvtm"
        const product4 = document.querySelectorAll(".product.dc");
        // Tìm thẻ có id="Test4"
        const test4 = document.getElementById("Test4");
        // Tìm tất cả các thẻ có class "product kvtm"
        const product5 = document.querySelectorAll(".product.ff");
        // Tìm thẻ có id="Test5"
        const test5 = document.getElementById("Test5");
        // Tìm tất cả các thẻ có class "product kvtm"
        const product6 = document.querySelectorAll(".product.khac");
        // Tìm thẻ có id="Test6"
        const test6 = document.getElementById("Test6");
        const delay = 50; // Thời gian delay giữa các phần tử
        let index = 0; // Dùng để tạo hiệu ứng nổi lên lần lượt

        // Hiện hoặc ẩn sản phẩm dựa trên category
        products.forEach((product) => {
          // Kiểm tra nếu sản phẩm phù hợp với bộ lọc
          if (category === "all" || product.classList.contains(category)) {
            product.style.display = "block";
            product.classList.remove("hidden"); // Loại bỏ trạng thái ẩn nếu có

            // Xóa hiệu ứng cũ và thêm lại hiệu ứng để làm mới
            product.classList.remove("active");
            setTimeout(() => {
              product.classList.add("active");
            }, delay * index++);
          } else {
            // Xử lý các sản phẩm không thuộc bộ lọc
            product.classList.remove("active");
            product.classList.add("hidden");
            product.style.display = "none";
          }

          if (category === "all") {
            Image0.classList.add("glow-effect");
            element0.forEach((element0) => {
              element0.style.display = "block";
            });
          } else {
            Image0.classList.remove("glow-effect");
            element0.forEach((element0) => {
              element0.style.display = "none";
            });
          }

          // Nếu category là "kvtm", hiển thị các phần tử có id="kvtm", arrowUp và arrowDown
          if (category === "kvtm") {
            element1.forEach((element1) => {
              element1.style.display = "block";
            });
            arrow1.forEach((el) => {
              el.style.display = "block";
            });
            Image1.classList.add("glow-effect");
            // Nếu không có thẻ nào với class "product kvtm"
            if (product1.length === 0) {
              test1.style.display = "block"; // Hiển thị thẻ có id="Test1"
            } else {
              test1.style.display = "none"; // Ẩn thẻ có id="Test1"
            }
          } else {
            // Ngược lại, ẩn các phần tử có id="kvtm", arrowUp1 và arrowDown1
            element1.forEach((element1) => {
              element1.style.display = "none";
            });
            arrow1.forEach((el) => {
              el.style.display = "none";
            });
            Image1.classList.remove("glow-effect");
            test1.style.display = "none"; // Ẩn thẻ có id="Test1"
          }

          if (category === "lq") {
            element2.forEach((element2) => {
              element2.style.display = "block";
            });
            Image2.classList.add("glow-effect");
            // Nếu không có thẻ nào với class "product lq"
            if (product2.length === 0) {
              test2.style.display = "block"; // Hiển thị thẻ có id="Test2"
            } else {
              test2.style.display = "none"; // Ẩn thẻ có id="Test2"
            }
          } else {
            element2.forEach((element2) => {
              element2.style.display = "none";
            });
            Image2.classList.remove("glow-effect");
            test2.style.display = "none"; // Ẩn thẻ có id="Test2"
          }

          if (category === "coc") {
            element3.forEach((element3) => {
              element3.style.display = "block";
            });
            Image3.classList.add("glow-effect");
            // Nếu không có thẻ nào với class "product lq"
            if (product3.length === 0) {
              test3.style.display = "block"; // Hiển thị thẻ có id="Test3"
            } else {
              test3.style.display = "none"; // Ẩn thẻ có id="Test3"
            }
          } else {
            element3.forEach((element3) => {
              element3.style.display = "none";
            });
            Image3.classList.remove("glow-effect");
            test3.style.display = "none"; // Ẩn thẻ có id="Test3"
          }

          if (category === "dc") {
            element4.forEach((element4) => {
              element4.style.display = "block";
            });
            Image4.classList.add("glow-effect");
            // Nếu không có thẻ nào với class "product lq"
            if (product4.length === 0) {
              test4.style.display = "block"; // Hiển thị thẻ có id="Test4"
            } else {
              test4.style.display = "none"; // Ẩn thẻ có id="Test4"
            }
          } else {
            element4.forEach((element4) => {
              element4.style.display = "none";
            });
            Image4.classList.remove("glow-effect");
            test4.style.display = "none"; // Ẩn thẻ có id="Test4"
          }

          if (category === "ff") {
            element5.forEach((element5) => {
              element5.style.display = "block";
            });
            Image5.classList.add("glow-effect");
            // Nếu không có thẻ nào với class "product ff"
            if (product5.length === 0) {
              test5.style.display = "block"; // Hiển thị thẻ có id="Test5"
            } else {
              test5.style.display = "none"; // Ẩn thẻ có id="Test5"
            }
          } else {
            element5.forEach((element5) => {
              element5.style.display = "none";
            });
            Image5.classList.remove("glow-effect");
            test5.style.display = "none"; // Ẩn thẻ có id="Test5"
          }

          // Nếu category là "khac", hiển thị các phần tử có id="khac", arrowUp2 và arrowDown6
          if (category === "khac") {
            element6.forEach((element6) => {
              element6.style.display = "block";
            });
            arrow6.forEach((el) => {
              el.style.display = "block";
            });
            Image6.classList.add("glow-effect");
            // Nếu không có thẻ nào với class "product khac"
            if (product6.length === 0) {
              test6.style.display = "block"; // Hiển thị thẻ có id="Test6"
            } else {
              test6.style.display = "none"; // Ẩn thẻ có id="Test6"
            }
          } else {
            // Ngược lại, ẩn các phần tử có id="khac", arrowUp và arrowDown
            element6.forEach((element6) => {
              element6.style.display = "none";
            });
            arrow6.forEach((el) => {
              el.style.display = "none";
            });
            Image6.classList.remove("glow-effect");
            test6.style.display = "none"; // Ẩn thẻ có id="Test6"
          }
        });
      }

      // Gọi function filterProducts với "all" để hiển thị tất cả sản phẩm khi DOM đã tải
      document.addEventListener("DOMContentLoaded", () => {
        filterProducts("all");
      });

      let currentIndex1 = 0; // Vị trí phần tử hiện tại

      document.getElementById("arrowUp1").addEventListener("click", () => {
        const productss1 = document.querySelectorAll(".productss1");
        if (currentIndex1 > 0) {
          currentIndex1--;
          navigateTo(productss1, currentIndex1);
        }
      });

      document.getElementById("arrowDown1").addEventListener("click", () => {
        const productss1 = document.querySelectorAll(".productss1");
        if (currentIndex1 < productss1.length - 1) {
          currentIndex1++;
          navigateTo(productss1, currentIndex1);
        }
      });

      let currentIndex6 = 0; // Vị trí phần tử hiện tại

      document.getElementById("arrowUp6").addEventListener("click", () => {
        const productss6 = document.querySelectorAll(".productss6");
        if (currentIndex6 > 0) {
          currentIndex6--;
          navigateTo(productss6, currentIndex6);
        }
      });

      document.getElementById("arrowDown6").addEventListener("click", () => {
        const productss6 = document.querySelectorAll(".productss6");
        if (currentIndex6 < productss6.length - 1) {
          currentIndex6++;
          navigateTo(productss6, currentIndex6);
        }
      });

      function navigateTo(elements, index) {
        elements[index].scrollIntoView({ behavior: "smooth", block: "center" });

        // Làm nổi bật phần tử hiện tại
        elements.forEach((el, i) => {
          if (i === index) {
            el.style.background = "#555555";
          } else {
            el.style.background = "#252525";
          }
        });
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

      function toggleContact(contentID) {
        var content = document.getElementById(contentID);
        content.classList.toggle("active");
      }

      window.onload = function () {
        const content = document.getElementById("contact-Content");
        content.classList.add("active");
      };

      function infor(ID) {
        let contents = document.querySelectorAll(".gallery"); // Lấy tất cả phần tử có class 'gallery'
        let element = document.getElementById(ID); // Lấy phần tử có ID được gọi
        if (ID === "OFF") {
          // Nếu ID là "OFF", ẩn tất cả các phần tử
          contents.forEach(function (content) {
            content.style.display = "none";
          });
        } else {
          if (element.style.display === "none") {
            // Nếu phần tử đang ẩn, hiển thị phần tử đó và ẩn tất cả các phần tử khác
            contents.forEach(function (content) {
              content.style.display = "none";
            });
            element.style.display = "block"; // Hiển thị phần tử đã chọn
          } else {
            // Nếu phần tử đang hiển thị, ẩn tất cả các phần tử
            contents.forEach(function (content) {
              content.style.display = "none";
            });
          }
        }
      }
    </script>
  </body>
</html>

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
        height: 90px;
        background-color: #ffffff;
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        gap: 5px;
        padding: 0 5px;
        display: flex; /* dùng flexbox để căn giữa nội dung */
        align-items: center;
        justify-content: center;
        border-bottom: 2px solid #000000;
      }

      .header img {
        height: 70px;
        border-radius: 50%;
        object-fit: contain;
      }

      .header img:hover {
        transform: scale(1.05);
        border: 2px solid #ffffff; /* thêm kiểu border solid */
        transition: transform 0.3s ease, border-color 0.3s ease;
        cursor: pointer; /* thêm con trỏ khi hover */
      }

      .header-section {
        width: calc(100% - 90px);
        min-width: 200px;
        max-width: 720px;
        height: auto;
        gap: 5px;
        display: flex;
        line-height: 0.9;
        flex-wrap: wrap;
        justify-content: center;
        align-items: center;
        align-content: center;
      }

      .header-section a {
        width: auto;
        padding: 0px 5px;
        color: #000000;
        font-weight: 600;
        text-decoration: none;
      }

      .header-section a:hover {
        color: #000000;
        text-decoration: underline; /* underline, overline, line-through */
      }

      .header-content {
        width: 100%;
        height: auto;
        min-height: 10px;
        background-color: #000000;
        display: flex;
        align-items: center;
        justify-content: center;
      }

      .products,
      .productss {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(180px, 1fr));
        gap: 10px;
        padding: 20px;
        justify-items: center; /* 👉 Canh giữa item trong mỗi ô */
      }

      /* Sản phẩm */
      .items {
        width: 160px;
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

      .items img {
        width: 65px;
        height: 65px;
      }

      .items-content {
        width: 85px;
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
      .quantity {
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

      .quantity {
        width: 63px;
        height: 18px;
        border-radius: 2px;
        display: flex;
        align-items: center;
        justify-content: center;
        color: rgb(0, 0, 0);
        background-color: white;
      }

      .items button {
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

      /* ACC */
      .itemss {
        width: 160px;
        height: 130px;
        padding: 2.5px;
        background-color: #444;
        display: flex;
        align-items: center;
        justify-content: center;
        gap: 5px;
        border-radius: 5px;
        box-shadow: 0 2px 6px rgba(0, 0, 0, 0.3);
        cursor: pointer;

        flex-direction: column; /* 🔄 Chuyển từ row → column */
      }

      .itemss img {
        width: 155px;
        height: 85px;
      }

      .itemss-content {
        width: 150px;
        height: 35px;
        display: flex;
        flex-direction: column;
        justify-content: flex-start;
        gap: 2px;
        font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
      }

      .itemss button {
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

      .containers {
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
        gap: 10px;
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

      .overlay {
        position: fixed;
        top: 0;
        left: 0;
        width: 100vw;
        height: 100vh;
        background: #fff;
        display: none;
        z-index: 9999;

        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;

        overflow-y: auto; /* Cuộn dọc */
        scroll-behavior: smooth;
      }

      .overlay button {
        position: fixed;
        top: 5px;
        width: 20px;
        height: 20px;
        border: none;
        display: flex;
        border-radius: 2px;
        align-items: center;
        justify-content: center;
        cursor: pointer;
      }

      .overlay-img {
        display: flex;
        width: 100vw;
        height: auto;
        padding: 5px;
        gap: 5px;
        background-color: #444;
        flex-direction: row;
        overflow-x: auto;
        scroll-behavior: smooth;
      }

      .overlay-img img {
        height: 180px;
        width: 320px;
      }

      .overlay-content {
        padding: 20px;
        font-size: 13px;
        color: #000000;
      }

      #video-container {
        max-width: 720px; /* Giới hạn chiều ngang tối đa */
        width: 100%; /* Tự động co giãn theo màn hình */
        aspect-ratio: 16/9; /* Giữ đúng tỉ lệ video HD */
        display: flex;
        justify-content: center;
        align-items: center;
        align-content: center;
        margin: 10px auto; /* Căn giữa, có khoảng cách phía trên dưới */
        border-radius: 12px; /* Bo góc mềm mại, tinh tế */
        box-shadow: 0 0 20px rgba(0, 0, 0, 0.5); /* Đổ bóng mạnh, tạo chiều sâu */
      }

      @media (max-width: 480px) {
        #video-container {
          max-width: 100%;
          margin: 5px auto;
        }
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
        .products,
        .productss {
          grid-template-columns: repeat(auto-fill, minmax(160px, 1fr));
          gap: 10px;
          padding: 10px;
          justify-items: center; /* 👉 Canh giữa item trong mỗi ô */
        }

        .contact-Content {
          width: calc(90% - 40px);
          bottom: 100px;
        }
      }
      html {
        scroll-behavior: smooth;
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
      <div class="header-section">
        <a href="#">Trang Chủ</a>
        <a href="#header-KVTM">Khu Vườn Trên Mây</a>
        <a href="#header-LQ">Liên Quân Mobile</a>
        <a href="#header-COC">Clash Of Clans</a>
        <a href="#header-DC">Dragon City</a>
        <a href="#header-FF">Free Fire</a>
      </div>
    </div>

    <!-- <div style="height: 20px"></div> -->

    <div id="video-container">
      <div id="video-player"></div>
      <!-- Đây là nơi player YouTube được tạo vào -->
    </div>

    <script>
      const channelId = "UCM8xwnvLQ60wfEgduDRzRMg";
      const fixedVideo = "Hm6MqHYRzcw"; // video cố định
      let playlist = [],
        current = 0,
        player;

      // Load YouTube IFrame API
      const tag = document.createElement("script");
      tag.src = "https://www.youtube.com/iframe_api";
      document.body.appendChild(tag);

      async function getLatestVideos() {
        try {
          const res = await fetch(
            `https://api.rss2json.com/v1/api.json?rss_url=https://www.youtube.com/feeds/videos.xml?channel_id=${channelId}`
          );
          const data = await res.json();
          return data.items.slice(0, 2).map((item) => {
            const url = new URL(item.link);
            return url.searchParams.get("v");
          });
        } catch (err) {
          console.error("Lỗi lấy RSS:", err);
          return [];
        }
      }

      function onPlayerReady(e) {
        e.target.playVideo();
      }

      function onPlayerStateChange(e) {
        if (e.data === YT.PlayerState.ENDED) {
          current = (current + 1) % playlist.length;
          player.loadVideoById(playlist[current]);
        }
      }

      async function init() {
        const latest = await getLatestVideos();
        playlist = [fixedVideo, ...latest];
        if (window.YT && YT.Player) createPlayer();
        else window.onYouTubeIframeAPIReady = createPlayer;
      }

      function createPlayer() {
        player = new YT.Player("video-player", {
          videoId: playlist[current],
          playerVars: {
            autoplay: 1,
            controls: 1,
            modestbranding: 1,
            rel: 0,
          },
          events: {
            onReady: onPlayerReady,
            onStateChange: onPlayerStateChange,
          },
        });
      }

      init();
    </script>

    <!-- Khu Vườn Trên Mây -->
    <div class="header-content" id="header-KVTM">
      <img
        src="https://i.pinimg.com/736x/39/2f/3a/392f3a868a6a44adb7b4514709941445.jpg"
        alt="Logo-kvtm"
        style="width: 35px; margin: 5px; border-radius: 50%"
      />
      <strong style="font-size: 18px; color: #d1d1d1">
        🌿 Khu Vườn Trên Mây 🌿
      </strong>
      <img
        src="https://i.pinimg.com/736x/39/2f/3a/392f3a868a6a44adb7b4514709941445.jpg"
        alt="Logo-kvtm"
        style="width: 35px; margin: 5px; border-radius: 50%"
      />
    </div>
    <!-- Show VP - Khu Vườn Trên Mây -->
    <div class="products" id="product-items"></div>
    <!-- <div style="width: 100%; height: 5px; background-color: #343434"></div> -->
    <!-- Show ACC - Khu Vườn Trên Mây -->
    <!-- <div class="productss" id="product-items1"></div> -->

    <!-- Show ACC - Liên Quân Mobile -->
    <div class="header-content" id="header-LQ">
      <img
        src="https://i.pinimg.com/736x/e1/14/f3/e114f324ca6461bb9b342f34292b60ad.jpg"
        alt="Logo-lq"
        style="width: 35px; margin: 5px; border-radius: 50%"
      />
      <strong style="font-size: 18px; color: #d1d1d1">
        🛡️ Liên Quân Mobile 🛡️
      </strong>
      <img
        src="https://i.pinimg.com/736x/e1/14/f3/e114f324ca6461bb9b342f34292b60ad.jpg"
        alt="Logo-lq"
        style="width: 35px; margin: 5px; border-radius: 50%"
      />
    </div>
    <!-- <div class="productss" id="product-items2"></div> -->

    <!-- Show ACC - Clash Of Clans -->
    <div class="header-content" id="header-COC">
      <img
        src="https://i.pinimg.com/736x/8e/ae/cd/8eaecd44d50cf21bead6c2c9d540ceaf.jpg"
        alt="Logo-coc"
        style="width: 35px; margin: 5px; border-radius: 50%"
      />
      <strong style="font-size: 18px; color: #d1d1d1">
        ⚔️ Clash Of Clans ⚔️
      </strong>
      <img
        src="https://i.pinimg.com/736x/8e/ae/cd/8eaecd44d50cf21bead6c2c9d540ceaf.jpg"
        alt="Logo-coc"
        style="width: 35px; margin: 5px; border-radius: 50%"
      />
    </div>
    <!-- <div class="productss" id="product-items3"></div> -->

    <!-- Show ACC - Dragon City -->
    <div class="header-content" id="header-DC">
      <img
        src="https://i.pinimg.com/736x/4b/2f/39/4b2f39d773c23626002eb7eeaacaebd7.jpg"
        alt="Logo-dc"
        style="width: 35px; margin: 5px; border-radius: 50%"
      />
      <strong style="font-size: 18px; color: #d1d1d1">
        🐉 Dragon City 🐉
      </strong>
      <img
        src="https://i.pinimg.com/736x/4b/2f/39/4b2f39d773c23626002eb7eeaacaebd7.jpg"
        alt="Logo-dc"
        style="width: 35px; margin: 5px; border-radius: 50%"
      />
    </div>
    <!-- <div class="productss" id="product-items4"></div> -->

    <!-- Show ACC - Free Fire -->
    <div class="header-content" id="header-FF">
      <img
        src="https://i.pinimg.com/736x/bc/12/70/bc1270fbfd9b08f0a98cef6ead98dc7c.jpg"
        alt="Logo-ff"
        style="width: 35px; margin: 5px; border-radius: 50%"
      />
      <strong style="font-size: 18px; color: #d1d1d1"> 🔥 Free Fire 🔥 </strong>
      <img
        src="https://i.pinimg.com/736x/bc/12/70/bc1270fbfd9b08f0a98cef6ead98dc7c.jpg"
        alt="Logo-ff"
        style="width: 35px; margin: 5px; border-radius: 50%"
      />
    </div>
    <!-- <div class="productss" id="product-items5"></div> -->

    <!-- Footer -->
    <div
      style="
        background: #0d0d0d;
        color: #ccc;
        padding: 20px 15px;
        font-family: sans-serif;
        text-align: center;
      "
    >
      <!-- Dòng bản quyền nằm riêng, căn giữa -->
      <p style="margin: 0 0 15px 0; font-size: 14px">
        &copy; 2024, Copyright by <strong>OTISStore</strong> |
        <em>Uy Tín Tạo Nên Thương Hiệu!</em>
      </p>

      <!-- Khối thông tin còn lại chia 3 cột -->
      <div
        style="
          display: flex;
          flex-wrap: wrap;
          justify-content: center;
          align-items: flex-start;
          gap: 10px;
          text-align: left;
          max-width: 1000px;
          margin: auto;
        "
      >
        <!-- Hotline -->
        <div
          style="
            background: #222;
            border: 1px solid #888;
            flex: 1;
            min-width: 240px;
            border-radius: 6px;
            padding: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
          "
        >
          <img
            src="https://i.pinimg.com/736x/ba/6f/1d/ba6f1dcaebce3bef7a97cd4675c18cbf.jpg"
            alt="hotline"
            style="width: 35px; border-radius: 50%"
          />
          <div>
            <div style="color: #ffcc00; font-weight: bold">
              Hotline: 0329 022 431
            </div>
            <div style="color: #fff; font-weight: bold">Admin: Otis Võ</div>
          </div>
        </div>

        <!-- Giao dịch -->
        <div
          style="
            background: #222;
            border: 1px solid #888;
            flex: 1;
            min-width: 240px;
            border-radius: 6px;
            padding: 10px;
            display: flex;
            align-items: center;
            gap: 10px;
          "
        >
          <img
            src="https://i.pinimg.com/736x/95/66/98/9566980106d7b8592e066b2a887b0b97.jpg"
            alt="change"
            style="width: 35px; border-radius: 50%"
          />
          <div>
            <b style="color: white">Phương Thức Giao Dịch</b> <br />
            <span style="color: #fff">Trực Tiếp</span> – Cam Kết 100%
          </div>
        </div>

        <!-- Liên kết MXH -->
        <div
          style="
            flex: 1;
            min-width: 240px;
            display: flex;
            flex-direction: column;
            gap: 10px;
            align-items: center;
          "
        >
          <strong>Liên kết chia sẻ:</strong>
          <div style="display: flex; gap: 10px">
            <!-- Facebook -->
            <a href="https://facebook.com/OtisGamerVN" target="_blank">
              <img
                src="https://i.pinimg.com/736x/c6/75/4f/c6754f858018877052f6b25bb2918b83.jpg"
                alt="Facebook"
                style="width: 30px; height: 30px; border-radius: 50%"
              />
            </a>

            <!-- YouTube -->
            <a href="https://youtube.com/@otisstorevn" target="_blank">
              <img
                src="https://i.pinimg.com/736x/2e/f9/5e/2ef95eb650ca01e10a56d6933f1a4ebd.jpg"
                alt="YouTube"
                style="width: 30px; height: 30px; border-radius: 50%"
              />
            </a>

            <!-- Zalo -->
            <a href="https://zalo.me/0329022431" target="_blank">
              <img
                src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/91/Icon_of_Zalo.svg/1024px-Icon_of_Zalo.svg.png"
                alt="Zalo"
                style="width: 30px; height: 30px; border-radius: 50%"
              />
            </a>
          </div>
        </div>
      </div>
    </div>

    <script>
      // VP - Khu Vườn Trên Mây
      const products = [
        {
          name: "Trà Sấy",
          image:
            "https://i.pinimg.com/474x/3a/cc/0f/3acc0fff30a54670af357237b0fc897d.jpg",
          no: "x200",
          price: "1k",
          quantity: "",
        },
        // VP.KVTM
        // Sấy 0
        // Nước Ép 0
        // Vải 0
        // Ngọc 0
        // Tinh Dầu 0
        // Trà 0
        // Hoa Tươi 0
        // Nước Hoa 0
        // Túi Hương 0
        // Vật Phẩm May 0
        // Hạt Giống 0
        // Bọ 0
        // Vật Phẩm Khác 0
        // Vàng & Vật Phẩm Sự Kiện 1
      ];
      const container = document.getElementById("product-items");
      container.innerHTML = products
        .map(
          (product) => `<div class="items">
                          <img src="${product.image}" alt="${product.name}" />
                          <div class="items-content">
                            <div class="name">${product.name}</div>
                            <div class="flex-row">
                              <div class="infor">SL:</div>
                              <div class="no">${product.no}</div>
                            </div>
                            <div class="flex-row">
                              <div class="infor">Giá:</div>
                              <div class="price">${product.price}</div>
                            </div>
                            <div class="flex-row">
                              <div class="quantity">Còn: ${product.quantity}</div>
                              <button onclick='sendMessage("${product.name} ${product.no}")'>🛒</button>
                            </div>
                          </div>
                        </div>`
        )
        .join("");

      // Danh sách ACC - Game
      const categories = [
        {
          id: 1,
          name: "Khu Vườn Trên Mây",
          products: [],
        },
        { id: 2, name: "Liên Quân Mobile", products: [] },
        { id: 3, name: "Clash Of Clans", products: [] },
        { id: 4, name: "Dragon City", products: [] },
        { id: 5, name: "Free Fire", products: [] },
        { id: 6, name: "Game Khác", products: [] },
        { id: 7, name: "Thẻ Game", products: [] },
      ];

      function generateProductHTML(product) {
        return `
          <div class="itemss">
            <img src="${product.image}" alt="${product.id}" />
            <div class="itemss-content">
              <div class="name">${product.id}</div>
              <div class="flex-row">
                <button onclick="Overlay('${product.id}')">🔍</button>
                <div class="infor">Giá:</div>
                <div class="price">${product.price}</div>
              </div>
            </div>
          </div>
          <div class="overlay" id="${product.id}">
            <h2>Thông Tin Chi Tiết</h2>
            <div class="overlay-img">
              ${[...Array(10).keys()]
                .map(
                  (i) =>
                    `<img src="${product[`image${i + 1}`]}" alt="img${i + 1}"/>`
                )
                .join("\n")}
            </div>
            <button style="left: 5px; background-color: #34ff19" onclick='sendMessage("${
              product.id
            }")'>🛒</button>  
            <div class="overlay-content">${product.title}</div>
            <button style="right: 5px; background-color: #ff7676" onclick="Overlay('${
              product.id
            }')">x</button>
          </div>
        `;
      }

      categories.forEach((category) => {
        const container = document.getElementById(
          `product-items${category.id}`
        );
        if (container && category.products.length > 0) {
          container.innerHTML = category.products
            .map(generateProductHTML)
            .join("");
        }
      });

      // x Mở Title Acc
      function Overlay(ID) {
        const contents = document.querySelectorAll(".overlay");
        const target = document.getElementById(ID);

        if (!target) {
          console.warn("Không tìm thấy phần tử với ID:", ID);
          return;
        }

        const currentDisplay = window.getComputedStyle(target).display;
        console.log("Phần tử", ID, "hiện trạng display:", currentDisplay);

        if (currentDisplay === "flex") {
          target.style.display = "none";
        } else {
          contents.forEach((el) => (el.style.display = "none"));
          target.style.display = "flex";
        }
      }

      // Chặn chuột phải
      document.addEventListener("contextmenu", function (e) {
        e.preventDefault();
      });

      // Chặn Ctrl+C, Ctrl+U, Ctrl+S, Ctrl+Shift+I, F12...
      document.addEventListener("keydown", function (e) {
        if (
          (e.ctrlKey &&
            (e.key === "c" ||
              e.key === "u" ||
              e.key === "s" ||
              e.key === "a")) ||
          (e.ctrlKey && e.shiftKey && e.key.toLowerCase() === "i") ||
          e.key === "F12"
        ) {
          e.preventDefault();
        }
      });

      // Chặn kéo chọn văn bản
      document.addEventListener("selectstart", function (e) {
        e.preventDefault();
      });

      // Chặn kéo văn bản bằng chuột
      document.addEventListener("dragstart", function (e) {
        e.preventDefault();
      });
    </script>

    <!-- Nút điều hướng & thông tin chi tiết -->
    <div class="containers">
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
            onclick="sendMessage('');"
          >
            Hỗ Trợ
          </button>
        </div>
        <img
          src="https://i.pinimg.com/736x/d7/a9/bd/d7a9bd5d702fac221ee7b6f9994750bc.jpg"
          alt="Hướng Dẫn 1"
        />
        <img
          src="https://i.pinimg.com/736x/61/88/a0/6188a0ed4358ad9c6b75ba65a879ddfb.jpg"
          alt="Hướng Dẫn 2"
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

      function sendMessage(data) {
        try {
          const pageId = "488283351040349";
          let url = `https://m.me/${pageId}`; // Link Messenger chuẩn cho cả điện thoại & máy tính

          if (typeof data === "string" && data.trim() !== "") {
            alert(`Đang gửi đơn hàng: ${data}`);
            const encodedMessage = encodeURIComponent(`Order: ${data}`);
            url += `?text=${encodedMessage}`; // Gửi dữ liệu qua ref param (bên chatbot có thể xử lý)
          }

          window.open(url, "_blank");
        } catch (err) {
          console.error("Không thể mở Messenger:", err);
          alert("Đã xảy ra lỗi. Vui lòng thử lại.");
        }
      }
    </script>
  </body>
</html>

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
        font-family: "Segoe UI", sans-serif;
        min-width: 480px;
        background-color: #000000;
        color: #ffffff;
        -ms-overflow-style: none; /* IE/Edge */
      }

      /* 🎯 Loại bỏ hoàn toàn không gian thanh cuộn */
      html {
        overflow: -moz-scrollbars-none; /* Firefox cũ */
        scrollbar-width: none; /* Firefox mới */
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

      .body-background {
        margin: 100px auto 0 auto;
        width: 100vw;
        min-width: 480px;
        height: 100vh;
        font-family: "Segoe UI", sans-serif;
        background-color: #000000;
        color: #ffffff;
      }

      /* Header */
      .header {
        width: 100vw;
        min-width: 480px;
        height: 90px;
        background-color: #000000;
        position: fixed;
        top: 0;
        left: 0;
        right: 0;
        gap: 5px;
        z-index: 999;
        padding: 5px;
        display: flex; /* dùng flexbox để căn giữa nội dung */
        align-items: center;
        justify-content: center;
      }

      .header img {
        height: 80px;
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
        min-width: 380px;
        max-width: 490px;
        height: auto;
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
        gap: 5px;
        justify-items: center; /* 👉 Canh giữa item trong mỗi ô */
        line-height: 0.9;
      }

      .header-section a {
        width: auto;
        padding: 0px 5px;
        color: #ffffff;
        font-weight: 600;
        text-decoration: none;
      }

      .header-section a:hover {
        color: blue;
        text-decoration: underline; /* underline, overline, line-through */
      }

      .header-content {
        width: 100%;
        min-width: 480px;
        height: auto;
        min-height: 10px;
        background-color: #272727;
        display: flex;
        align-items: center;
        justify-content: center;
      }

      .products,
      .productss {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(180px, 1fr));
        gap: 5px;
        padding: 5px;
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

      .overlay-content img {
        width: 65px;
        height: 65px;
      }

      #video-container {
        max-width: 480px;
        width: calc(100% - 20px);
        aspect-ratio: 16/9; /* Giữ đúng tỉ lệ video HD */
        margin: 0 auto 10px auto;
        border-radius: 5px;
        position: relative;
        border: 2px solid red;
        display: flex;
        flex-direction: column;
        align-items: center;
        aspect-ratio: 16 / 9; /* Áp tỉ lệ luôn cho container */
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
          grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
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

    <div class="body-background">
      <!-- <div style="height: 20px"></div> -->
      <div
        style="
          width: 970px;
          height: auto;
          display: grid;
          margin: 0 auto;
          grid-template-columns: repeat(auto-fit, minmax(480px, 1fr));
          gap: 10px;
          justify-content: center;
          align-items: center;
          align-content: center;
          justify-items: center;
        "
      >
        <div id="video-container"></div>
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
          player = new YT.Player("video-container", {
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
        <strong style="font-size: 18px; color: white">
          🌿 Khu Vườn Trên Mây 🌿
        </strong>
        <img
          src="https://i.pinimg.com/736x/39/2f/3a/392f3a868a6a44adb7b4514709941445.jpg"
          alt="Logo-kvtm"
          style="width: 35px; margin: 5px; border-radius: 50%"
        />
      </div>
      <!-- Show VP - Khu Vườn Trên Mây -->
      <!-- <div class="products" id="product-items_VP"></div> -->
      <!-- <div style="width: 100%; height: 5px; background-color: #343434"></div> -->
      <!-- Show COMBO - Khu Vườn Trên Mây -->
      <div class="products" id="product-items_CB"></div>
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
        <strong style="font-size: 18px; color: white">
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
        <strong style="font-size: 18px; color: white">
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
        <strong style="font-size: 18px; color: white">
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
        <strong style="font-size: 18px; color: white"> 🔥 Free Fire 🔥 </strong>
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
          background: #131313;
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
              <span style="color: #fff">Trực Tiếp</span> – Uy Tín 100%
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
    </div>

    <script>
      // VP - Khu Vườn Trên Mây
      // const products = [];

      // const containers = document.getElementById("product-items_VP");
      // containers.innerHTML = products
      //   .map(
      //     (p) => `
      //     <div class="items">
      //       <img src="${p.image}" alt="${p.name}" />
      //       <div class="items-content">
      //         <div class="name">${p.name}</div>
      //         <div class="flex-row">
      //           <div class="infor">SL:</div>
      //           <div class="no">${p.no}</div>
      //         </div>
      //         <div class="flex-row">
      //           <div class="infor">Giá:</div>
      //           <div class="price">${p.price}</div>
      //         </div>
      //         <div class="flex-row">
      //           <div class="quantity">Còn: ${p.quantity}</div>
      //           <button onclick='sendMessage("${p.name} x${p.no}")'>🛒</button>
      //         </div>
      //       </div>
      //     </div>`
      //   )
      //   .join("");

      // === Combo Products === //
      const productss = [
        {
          name: "CB.Vợt",
          image:
            "https://i.pinimg.com/736x/3f/db/13/3fdb13d11443042c1c61b2cf2e7b8082.jpg",
          name1: "Vợt Trắng",
          image1:
            "https://i.pinimg.com/474x/cd/80/c0/cd80c01c223117492d6f11b31cbfb297.jpg",
          no1: "40",
          name2: "Vợt Xanh",
          image2:
            "https://i.pinimg.com/474x/4d/e1/3c/4de13ce0975519b0ab30911689682d37.jpg",
          no2: "40",
          price: "1k",
          quantity: "1",
        },
        // {
        //   name: "CB.Nâng Tầng",
        //   image:
        //     "https://i.pinimg.com/736x/ab/06/18/ab0618b2f3f52bf76751aff15d0ec7a8.jpg",
        //   name1: "Keo D.Mây",
        //   image1:
        //     "https://i.pinimg.com/474x/88/a7/e4/88a7e40dc4c265cd76cf491c50aa16e4.jpg",
        //   no1: "6",
        //   name2: "Lọ N.Thần",
        //   image2:
        //     "https://i.pinimg.com/474x/95/f8/0a/95f80ae795637d540e04105123cd216b.jpg",
        //   no2: "7",
        //   price: "1k",
        //   quantity: "1",
        // },
        // {
        //   name: "CB.Mít",
        //   image:
        //     "https://i.pinimg.com/736x/5e/b5/a0/5eb5a052951e40351ae71119b4113018.jpg",
        //   name1: "Mít",
        //   image1:
        //     "https://i.pinimg.com/474x/c8/d4/74/c8d4743a5801357e670e039858ca4d04.jpg",
        //   no1: "75",
        //   name2: "Mít Sấy",
        //   image2:
        //     "https://i.pinimg.com/474x/3c/63/59/3c6359a8032cef802b8be4968941c97e.jpg",
        //   no2: "75",
        //   name3: "Sinh Tố Mít",
        //   image3:
        //     "https://i.pinimg.com/474x/d3/ee/32/d3ee320098453df46b882e405e4a1b5f.jpg",
        //   no3: "75",
        //   price: "1k",
        //   quantity: "1",
        // },
        // {
        //   name: "CB.Dứa",
        //   image:
        //     "https://i.pinimg.com/736x/35/6a/de/356ade871bdd852893744006d5e01d47.jpg",
        //   name1: "Dứa",
        //   image1:
        //     "https://i.pinimg.com/474x/a3/3e/fc/a33efcd72ff80a699778a2d5f7f6882a.jpg",
        //   no1: "75",
        //   name2: "Dứa Sấy",
        //   image2:
        //     "https://i.pinimg.com/474x/44/48/b1/4448b17a17ed37068a9b1dd5f07f85f5.jpg",
        //   no2: "75",
        //   name3: "Nước Dứa",
        //   image3:
        //     "https://i.pinimg.com/736x/f3/15/ae/f315aeb25f643210a486c2cad55a27cc.jpg",
        //   no3: "75",
        //   price: "1k",
        //   quantity: "1",
        // },
        // {
        //   name: "CB.Xoài",
        //   image:
        //     "https://i.pinimg.com/736x/3c/9f/1c/3c9f1cb9c3137423f5dd967bef128b7b.jpg",
        //   name1: "Xoài",
        //   image1:
        //     "https://i.pinimg.com/474x/ea/df/b2/eadfb2be03c048433f58f29084a952da.jpg",
        //   no1: "75",
        //   name2: "Xoài Sấy",
        //   image2:
        //     "https://i.pinimg.com/474x/d9/b3/b1/d9b3b10cdb34e0b97cd8b6b7b08c9c20.jpg",
        //   no2: "75",
        //   name3: "Sinh Tố Xoài",
        //   image3:
        //     "https://i.pinimg.com/474x/20/f4/2d/20f42d7c2acac57126e5806054068d53.jpg",
        //   no3: "75",
        //   price: "1k",
        //   quantity: "1",
        // },
        // {
        //   name: "CB.Nho",
        //   image:
        //     "https://i.pinimg.com/736x/43/64/d2/4364d2e61b2dd4d45bf8c764dd6e04fd.jpg",
        //   name1: "Nho",
        //   image1:
        //     "https://i.pinimg.com/474x/cb/d8/2c/cbd82c87ffbb674d04e60bbf852e0780.jpg",
        //   no1: "45",
        //   name2: "Nho Sấy",
        //   image2:
        //     "https://i.pinimg.com/474x/77/19/34/77193423f65343aef01b697688c12337.jpg",
        //   no2: "45",
        //   name3: "Nước Nho",
        //   image3:
        //     "https://i.pinimg.com/474x/fb/c9/ae/fbc9ae57da21c3821e3b45741a803d5d.jpg",
        //   no3: "45",
        //   price: "1k",
        //   quantity: "1",
        // },
        // {
        //   name: "CB.Ngọc-1",
        //   image:
        //     "https://i.pinimg.com/736x/bf/20/50/bf2050c0b0b43c314c2366060a386f74.jpg",
        //   name1: "Ngọc Đỏ",
        //   image1:
        //     "https://i.pinimg.com/474x/cd/d2/04/cdd204f58ab6b093a94617f692f91398.jpg",
        //   no1: "33",
        //   name2: "Ngọc X.Biển",
        //   image2:
        //     "https://i.pinimg.com/736x/00/99/27/009927a35caced1eaa1598e8d5149f32.jpg",
        //   no2: "33",
        //   name3: "Ngọc Vàng",
        //   image3:
        //     "https://i.pinimg.com/474x/bc/19/9c/bc199c0f7626e3ab3f6cc0babf75086e.jpg",
        //   no3: "33",
        //   price: "1k",
        //   quantity: "1",
        // },
        // {
        //   name: "CB.Ngọc-2",
        //   image:
        //     "https://i.pinimg.com/736x/a2/3e/c4/a23ec4c2c7cbcf478fbeeea031758ab0.jpg",
        //   name1: "Ngọc Tím",
        //   image1:
        //     "https://i.pinimg.com/474x/a7/ef/ca/a7efca33165c810e1c81f31263fd50db.jpg",
        //   no1: "9",
        //   name2: "Ngọc Cam",
        //   image2:
        //     "https://i.pinimg.com/474x/fa/4c/f6/fa4cf62cb997beb2d999646501971b08.jpg",
        //   no2: "9",
        //   name3: "Ngọc X.Lá",
        //   image3:
        //     "https://i.pinimg.com/474x/b0/37/3b/b0373bb243f8aaaa0c6e16bda1af4d68.jpg",
        //   no3: "9",
        //   price: "1k",
        //   quantity: "1",
        // },
        // {
        //   name: "CB.Bọ-1",
        //   image:
        //     "https://i.pinimg.com/736x/ca/db/87/cadb8705ddc1ab633f5d00959fa7f48d.jpg",
        //   name1: "Bọ Rùa",
        //   image1:
        //     "https://i.pinimg.com/474x/b5/59/07/b559076ad355aa4b1675ac55e08f165e.jpg",
        //   no1: "27",
        //   name2: "Ốc Sên",
        //   image2:
        //     "https://i.pinimg.com/474x/ba/04/c8/ba04c8afd5021cb8cc55900cdb0d5c2b.jpg",
        //   no2: "27",
        //   name3: "Đom Đóm",
        //   image3:
        //     "https://i.pinimg.com/474x/6d/d7/db/6dd7dbdb030a5f337fa762378e8f07de.jpg",
        //   no3: "27",
        //   price: "1k",
        //   quantity: "1",
        // },
        // {
        //   name: "CB.Bọ-2",
        //   image:
        //     "https://i.pinimg.com/736x/2b/70/d9/2b70d9d15c7bd6eeb814c09080b1e706.jpg",
        //   name1: "Ong Mật",
        //   image1:
        //     "https://i.pinimg.com/474x/5f/0e/76/5f0e76aae9169c4663d9a8759fdf7bc0.jpg",
        //   no1: "27",
        //   name2: "Chuồn Chuồn",
        //   image2:
        //     "https://i.pinimg.com/474x/02/8e/0e/028e0e144ec65a0c0673da30de975976.jpg",
        //   no2: "27",
        //   name3: "Bươm Bướm",
        //   image3:
        //     "https://i.pinimg.com/474x/98/d4/b8/98d4b83c4711d7781c08618317219397.jpg",
        //   no3: "27",
        //   price: "1k",
        //   quantity: "1",
        // },
        // {
        //   name: "CB.Thỏi",
        //   image:
        //     "https://i.pinimg.com/736x/68/51/ee/6851eede92a5ad3e0a5589c9933f9d49.jpg",
        //   name1: "Thỏi Đồng",
        //   image1:
        //     "https://i.pinimg.com/736x/30/e9/10/30e910a6889550872708484b49942ae8.jpg",
        //   no1: "30",
        //   name2: "Thỏi Bạc",
        //   image2:
        //     "https://i.pinimg.com/474x/f9/8f/19/f98f198b25c78d9edddfee506f253856.jpg",
        //   no2: "60",
        //   name3: "Thỏi Vàng",
        //   image3:
        //     "https://i.pinimg.com/474x/3a/54/ad/3a54ade9144b0869933585794f7ab560.jpg",
        //   no3: "45",
        //   name4: "Thỏi B.Kim",
        //   image4:
        //     "https://i.pinimg.com/474x/7f/7a/2a/7f7a2a9dc91d6b8262a305782ff50e0b.jpg",
        //   no4: "45",
        //   price: "5k",
        //   quantity: "1",
        // },
        // {
        //   name: "CB.Cám",
        //   image:
        //     "https://i.pinimg.com/736x/48/a9/f2/48a9f28a149120c1f5445e7340fc6da9.jpg",
        //   name1: "Cám Gà",
        //   image1:
        //     "https://i.pinimg.com/474x/84/4f/09/844f09c991c8f830677e481208fbaf18.jpg",
        //   no1: "540",
        //   name2: "Cám Cừu",
        //   image2:
        //     "https://i.pinimg.com/474x/2d/fa/67/2dfa67fd37658939adfd696a0cd11c08.jpg",
        //   no2: "540",
        //   name3: "Cám Heo",
        //   image3:
        //     "https://i.pinimg.com/474x/a8/57/be/a857be4bb38f986a3879f10941b674ff.jpg",
        //   no3: "540",
        //   name4: "Cám Bò",
        //   image4:
        //     "https://i.pinimg.com/474x/fc/8e/2d/fc8e2d55c8e3b125d28eec5e62683f74.jpg",
        //   no4: "540",
        //   price: "10k",
        //   quantity: "1",
        // },
        // {
        //   name: "CB.Mùa Hè",
        //   image:
        //     "https://i.pinimg.com/736x/3e/08/00/3e08005b4a6df5d0dfa615174e74a85d.jpg",
        //   name1: "VP. Kem",
        //   image1:
        //     "https://i.pinimg.com/474x/15/32/fc/1532fc9620e3cebcaa897498294a9e4a.jpg",
        //   no1: "990",
        //   name2: "VP. Kính",
        //   image2:
        //     "https://i.pinimg.com/474x/f7/4a/ca/f74aca49da4092b3ef935e2179d1c770.jpg",
        //   no2: "660",
        //   name3: "VP. Dừa",
        //   image3:
        //     "https://i.pinimg.com/474x/cf/dc/71/cfdc7156657b869915baf8cda120891b.jpg",
        //   no3: "330",
        //   price: "10k",
        //   quantity: "1",
        // },
      ];
      const containerss = document.getElementById("product-items_CB");
      containerss.innerHTML = productss
        .map((combo) => {
          // Tính tổng số lượng các item con
          const items = [1, 2, 3, 4]
            .map((i) => ({
              image: combo[`image${i}`],
              name: combo[`name${i}`],
              no: combo[`no${i}`],
            }))
            .filter((item) => item.name); // chỉ lấy những item có dữ liệu

          const totalNo = items.reduce(
            (sum, item) => sum + Number(item.no || 0),
            0
          );

          const overlayItems = items
            .map(
              (item) => `
              ${
                item.image
                  ? `<img src="${item.image}" alt="${item.name}" /><br>`
                  : ""
              }
                 <strong>${item.name}: x${item.no}</strong><br><br>`
            )
            .join("");

          return `<div class="items">
                    <img src="${combo.image}" alt="${combo.name}" />
                    <div class="items-content">
                      <div class="name">${combo.name}</div>
                      <div class="flex-row">
                        <div class="infor">SL:</div>
                        <div class="no">${totalNo}</div>
                      </div>
                      <div class="flex-row">
                        <div class="infor">Giá:</div>
                        <div class="price">${combo.price}</div>
                      </div>
                      <div class="flex-row">
                        <div class="quantity">Còn: ${combo.quantity}</div>
                        <button onclick="Overlay('${combo.name}')">🔍</button>
                      </div>
                    </div>
                  </div>

                  <div class="overlay" id="${combo.name}">
                    <h2>Thông Tin Chi Tiết</h2>
                    <button style="left: 5px; background-color: #34ff19" onclick="sendMessage('${combo.name} x${totalNo}')">🛒</button>
                    <div class="overlay-content">${overlayItems}</div>
                    <button style="right: 5px; background-color: #ff7676" onclick="Overlay('${combo.name}')">x</button>
                  </div>`;
        })
        .join("");

      // Danh sách ACC - Game
      const categories = [
        { id: 1, name: "Khu Vườn Trên Mây", productsss: [] },
        { id: 2, name: "Liên Quân Mobile", productsss: [] },
        { id: 3, name: "Clash Of Clans", productsss: [] },
        { id: 4, name: "Dragon City", productsss: [] },
        { id: 5, name: "Free Fire", productsss: [] },
        { id: 6, name: "Game Khác", productsss: [] },
        { id: 7, name: "Thẻ Game", productsss: [] },
      ];
      function generateProductHTML(productsss) {
        return `
          <div class="itemss">
            <img src="${productsss.image}" alt="${productsss.id}" />
            <div class="itemss-content">
              <div class="name">${productsss.id}</div>
              <div class="flex-row">
                <button onclick="Overlay('${productsss.id}')">🔍</button>
                <div class="infor">Giá:</div>
                <div class="price">${productsss.price}</div>
              </div>
            </div>
          </div>
          <div class="overlay" id="${productsss.id}">
            <h2>Thông Tin Chi Tiết</h2>
            <div class="overlay-img">
              ${[...Array(10).keys()]
                .map(
                  (i) =>
                    `<img src="${productsss[`image${i + 1}`]}" alt="img${
                      i + 1
                    }"/>`
                )
                .join("\n")}
            </div>
            <button style="left: 5px; background-color: #34ff19" onclick="sendMessage("${
              productsss.id
            }")"">🛒</button>  
            <div class="overlay-content">${productsss.title}</div>
            <button style="right: 5px; background-color: #ff7676" onclick="Overlay('${
              productsss.id
            }')">x</button>
          </div>
        `;
      }
      categories.forEach((category) => {
        const containersss = document.getElementById(
          `product-items${category.id}`
        );
        if (containersss && category.productsss.length > 0) {
          containersss.innerHTML = category.productsss
            .map(generateProductHTML)
            .join("");
        }
      });

      // Mở Title Acc
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
      // document.addEventListener("contextmenu", function (e) {
      //   e.preventDefault();
      // });

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
          let url = `https://www.messenger.com/t/488283351040349`; // Link Messenger chuẩn cho cả điện thoại & máy tính

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

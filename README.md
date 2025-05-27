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
        display: flex; /* dùng flexbox để căn giữa nội dung */
        align-items: center;
        justify-content: center;
        border-bottom: 2px solid #000000;
      }

      .header img {
        height: 90%;
        border-radius: 50%;
        object-fit: contain;
      }

      .header img:hover {
        transform: scale(1.05);
        border: 2px solid #ffffff; /* thêm kiểu border solid */
        transition: transform 0.3s ease, border-color 0.3s ease;
        cursor: pointer; /* thêm con trỏ khi hover */
      }

      .header-content {
        width: 100vw;
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
        height: 135px;
        width: 240px;
      }

      .overlay-content {
        padding: 20px;
        font-size: 13px;
        color: #000000;
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

    <div style="height: 100px"></div>

    <!-- Khu Vườn Trên Mây -->
    <div class="header-content">
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
    <div style="width: 100vw; height: 5px; background-color: #343434"></div>
    <!-- Show ACC - Khu Vườn Trên Mây -->
    <div class="productss" id="product-items1"></div>

    <!-- Show ACC - Liên Quân Mobile -->
    <div class="header-content">
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
    <div class="productss" id="product-items2"></div>

    <!-- Show ACC - Clash Of Clans -->
    <div class="header-content">
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
    <div class="productss" id="product-items3"></div>

    <!-- Show ACC - Dragon City -->
    <div class="header-content">
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
    <div class="productss" id="product-items3"></div>

    <!-- Show ACC - Free Fire -->
    <div class="header-content">
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
    <div class="productss" id="product-items5"></div>

    <script>
      // VP - Khu Vườn Trên Mây
      const products = [
        // VP.KVTM
        // Sấy 0
        {
          name: "##########",
          image:
            "https://i.pinimg.com/736x/fc/22/1a/fc221aaf928fb13bc0a30b915acf5a2e.jpg",
          no: "x999",
          price: "999đ",
          quantity: "999",
        },
        {
          name: "Táo Sấy",
          image:
            "https://i.pinimg.com/474x/c4/a7/cc/c4a7ccf71acdb6aec54daa5e6d71fb6a.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "O.Hương Sấy",
          image:
            "https://i.pinimg.com/474x/44/d5/db/44d5db02f58245d0eaa29ac8f5ea8ea4.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Dừa Sấy",
          image:
            "https://i.pinimg.com/474x/d1/36/ac/d136ac2f9613e3c9b7613d6eea3153c1.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Hạt Dưa",
          image:
            "https://i.pinimg.com/474x/fe/37/47/fe3747ac5fb68ea29eaacb7335194a2a.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Trà Sấy",
          image:
            "https://i.pinimg.com/474x/3a/cc/0f/3acc0fff30a54670af357237b0fc897d.jpg",
          no: "x200",
          price: "1k",
          quantity: "",
        },
        {
          name: "Mít Sấy",
          image:
            "https://i.pinimg.com/474x/3c/63/59/3c6359a8032cef802b8be4968941c97e.jpg",
          no: "x200",
          price: "1k",
          quantity: "",
        },
        {
          name: "Dứa Sấy",
          image:
            "https://i.pinimg.com/474x/44/48/b1/4448b17a17ed37068a9b1dd5f07f85f5.jpg",
          no: "x200",
          price: "1k",
          quantity: "",
        },
        {
          name: "Xoài Sấy",
          image:
            "https://i.pinimg.com/474x/d9/b3/b1/d9b3b10cdb34e0b97cd8b6b7b08c9c20.jpg",
          no: "x200",
          price: "1k",
          quantity: "",
        },
        {
          name: "Lài Sấy",
          image:
            "https://i.pinimg.com/474x/bf/ca/31/bfca3109ec4d1139edd23d6cfa892064.jpg",
          no: "x100",
          price: "1k",
          quantity: "",
        },
        {
          name: "Cúc Sấy",
          image:
            "https://i.pinimg.com/474x/1a/55/8a/1a558a5de7056e3e92255d782146282c.jpg",
          no: "x80",
          price: "1k",
          quantity: "",
        },
        {
          name: "Hạt Sen",
          image:
            "https://i.pinimg.com/474x/db/dc/f3/dbdcf339aca99d0f379dd7b832b176c5.jpg",
          no: "x70",
          price: "1k",
          quantity: "",
        },
        {
          name: "Nho Sấy",
          image:
            "https://i.pinimg.com/474x/77/19/34/77193423f65343aef01b697688c12337.jpg",
          no: "x100",
          price: "1k",
          quantity: "",
        },
        {
          name: "Hạt H.Dương",
          image:
            "https://i.pinimg.com/474x/f0/7f/5c/f07f5c64972ae0a6b36e68852dbae018.jpg",
          no: "x60",
          price: "1k",
          quantity: "",
        },
        {
          name: "V.Quất Sấy",
          image:
            "https://i.pinimg.com/474x/41/87/22/418722c2007d0dd224d1445fb03eec31.jpg",
          no: "x50",
          price: "1k",
          quantity: "",
        },
        // Nước Ép 0
        {
          name: "Nước Táo",
          image:
            "https://i.pinimg.com/474x/24/89/30/2489301bc6cfbf6c06117e6b2bc18d88.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Nước T.Khiết",
          image:
            "https://i.pinimg.com/474x/31/7b/00/317b00880e894b49e97d85877c2b0112.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Nước Dừa",
          image:
            "https://i.pinimg.com/474x/4d/3d/ce/4d3dce43fc370f7b88dd83a2b79898c8.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Nước Chanh",
          image:
            "https://i.pinimg.com/474x/f0/ca/f1/f0caf199abebfe35629b35424ddb58c1.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Nước D.Hấu",
          image:
            "https://i.pinimg.com/474x/df/40/b0/df40b07fd8795ca1bd668510bf916401.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Sinh Tố Mít",
          image:
            "https://i.pinimg.com/474x/d3/ee/32/d3ee320098453df46b882e405e4a1b5f.jpg",
          no: "x150",
          price: "1k",
          quantity: "",
        },
        {
          name: "Nước Dứa",
          image:
            "https://i.pinimg.com/736x/f3/15/ae/f315aeb25f643210a486c2cad55a27cc.jpg",
          no: "x150",
          price: "1k",
          quantity: "",
        },
        {
          name: "Sinh Tố Xoài",
          image:
            "https://i.pinimg.com/474x/20/f4/2d/20f42d7c2acac57126e5806054068d53.jpg",
          no: "x150",
          price: "1k",
          quantity: "",
        },
        {
          name: "Nước Nho",
          image:
            "https://i.pinimg.com/474x/fb/c9/ae/fbc9ae57da21c3821e3b45741a803d5d.jpg",
          no: "x100",
          price: "1k",
          quantity: "",
        },
        {
          name: "Nước V.Quất",
          image:
            "https://i.pinimg.com/474x/ed/36/f0/ed36f00669c8617fcc2129ddaa8edd9f.jpg",
          no: "x60",
          price: "1k",
          quantity: "",
        },
        {
          name: "Nước Dâu",
          image:
            "https://i.pinimg.com/474x/a5/6a/7d/a56a7dfa4d5453650c2af919e4ff2806.jpg",
          no: "x55",
          price: "1k",
          quantity: "",
        },
        // Vải 0
        {
          name: "Vải Đỏ",
          image:
            "https://i.pinimg.com/736x/34/de/0a/34de0a0b909827f42dc53d00e0b8760d.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Vải Vàng",
          image:
            "https://i.pinimg.com/474x/9c/e8/53/9ce853e70a0fc549d85bc38662d55540.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Vải Tím",
          image:
            "https://i.pinimg.com/474x/04/4f/04/044f04650a308ece32d597a7a7a435cf.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Vải X.Lá",
          image:
            "https://i.pinimg.com/474x/e1/3a/29/e13a2958d046f137fbaa8f4c8efca934.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Vải Trắng",
          image:
            "https://i.pinimg.com/474x/26/f1/da/26f1da5a75e6c469c5ff9f0bc67bf5ae.jpg",
          no: "x70",
          price: "1k",
          quantity: "",
        },
        {
          name: "Vải Hồng",
          image:
            "https://i.pinimg.com/474x/15/f4/70/15f470c482380b1650fcc500939c045a.jpg",
          no: "x70",
          price: "1k",
          quantity: "",
        },
        {
          name: "Vải Đen",
          image:
            "https://i.pinimg.com/474x/67/56/9e/67569e1d046ca36d4b09003802c29ea0.jpg",
          no: "x70",
          price: "1k",
          quantity: "",
        },
        {
          name: "Vải X.Biển",
          image:
            "https://i.pinimg.com/474x/5e/12/b7/5e12b7c896ab6d647368c945befc26d1.jpg",
          no: "x55",
          price: "1k",
          quantity: "",
        },
        // Ngọc 0
        {
          name: "Ngọc Đỏ",
          image:
            "https://i.pinimg.com/474x/cd/d2/04/cdd204f58ab6b093a94617f692f91398.jpg",
          no: "x200",
          price: "1k",
          quantity: "",
        },
        {
          name: "Ngọc X.Biển",
          image:
            "https://i.pinimg.com/736x/00/99/27/009927a35caced1eaa1598e8d5149f32.jpg",
          no: "x150",
          price: "1k",
          quantity: "",
        },
        {
          name: "Ngọc Vàng",
          image:
            "https://i.pinimg.com/474x/bc/19/9c/bc199c0f7626e3ab3f6cc0babf75086e.jpg",
          no: "x55",
          price: "1k",
          quantity: "",
        },
        {
          name: "Ngọc Tím",
          image:
            "https://i.pinimg.com/474x/a7/ef/ca/a7efca33165c810e1c81f31263fd50db.jpg",
          no: "x25",
          price: "1k",
          quantity: "",
        },
        {
          name: "Ngọc Cam",
          image:
            "https://i.pinimg.com/474x/fa/4c/f6/fa4cf62cb997beb2d999646501971b08.jpg",
          no: "x35",
          price: "1k",
          quantity: "",
        },
        {
          name: "Ngọc X.Lá",
          image:
            "https://i.pinimg.com/474x/b0/37/3b/b0373bb243f8aaaa0c6e16bda1af4d68.jpg",
          no: "x23",
          price: "1k",
          quantity: "",
        },
        {
          name: "Ngọc C.Vòng",
          image:
            "https://i.pinimg.com/474x/53/5f/04/535f041f4fda0806ad0cdacbe2a8c1ac.jpg",
          no: "x45",
          price: "1k",
          quantity: "",
        },
        // Tinh Dầu 0
        {
          name: "TD H.Hồng",
          image:
            "https://i.pinimg.com/474x/17/bb/c3/17bbc3a474173a2a3606b5c52a09b1d2.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "TD Táo",
          image:
            "https://i.pinimg.com/474x/95/6a/8b/956a8b1f1615d9ad44ec8f17bd932a99.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "TD O.Hương",
          image:
            "https://i.pinimg.com/474x/a8/d0/59/a8d059c90b1c0317e6a3b6e016eb4337.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "TD Dừa",
          image:
            "https://i.pinimg.com/474x/77/47/92/774792634d8e265cfef841cdf916f4b9.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "TD Chanh",
          image:
            "https://i.pinimg.com/474x/5a/7d/25/5a7d2535ebc04bc9c0995b23936e9edd.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "TD Sen",
          image:
            "https://i.pinimg.com/474x/63/8f/a0/638fa0d5611df72ebdfeea0eb0314502.jpg",
          no: "x60",
          price: "1k",
          quantity: "",
        },
        {
          name: "TD V.Quất",
          image:
            "https://i.pinimg.com/474x/37/7f/5a/377f5a7747c0f94595338dcccdf28020.jpg",
          no: "x50",
          price: "1k",
          quantity: "",
        },
        {
          name: "TD Dâu",
          image:
            "https://i.pinimg.com/474x/42/34/cc/4234cc123fe4c6bb98cade9ea1e81e5f.jpg",
          no: "x50",
          price: "1k",
          quantity: "",
        },
        // Trà 0
        {
          name: "Trà H.Hồng",
          image:
            "https://i.pinimg.com/474x/14/82/c8/1482c876db5b1feb655e3153cc70f2a5.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Trà Đá",
          image:
            "https://i.pinimg.com/474x/11/f5/8e/11f58e166036ba5945e000548b05c19a.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Trà Táo",
          image:
            "https://i.pinimg.com/474x/b5/dd/fa/b5ddfa07ceb81f1d59e12235a982a003.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Trà Chanh",
          image:
            "https://i.pinimg.com/474x/80/5c/88/805c88803e4c4fb07f3c5bb67476ce74.jpg",
          no: "x75",
          price: "1k",
          quantity: "",
        },
        {
          name: "Trà Nho",
          image:
            "https://i.pinimg.com/474x/da/e8/b3/dae8b3a5ebedb5fcbbf20d45837a9f82.jpg",
          no: "x60",
          price: "1k",
          quantity: "",
        },
        {
          name: "Trà Hoa Cúc",
          image:
            "https://i.pinimg.com/474x/2b/18/db/2b18db2f31c5c7a354057237b104e6ec.jpg",
          no: "x55",
          price: "1k",
          quantity: "",
        },
        {
          name: "Trà Trái Cây",
          image:
            "https://i.pinimg.com/474x/6b/09/56/6b09567b8140b76c3d6841788ce34c8d.jpg",
          no: "x50",
          price: "1k",
          quantity: "",
        },
        {
          name: "Trà V.Quất",
          image:
            "https://i.pinimg.com/474x/3d/d0/e3/3dd0e3866a96a1bb47283350ef05ac1b.jpg",
          no: "x35",
          price: "1k",
          quantity: "",
        },
        {
          name: "Trà Sen",
          image:
            "https://i.pinimg.com/474x/44/03/9b/44039b6151c6f60c22855f4e47087c98.jpg",
          no: "x35",
          price: "1k",
          quantity: "",
        },
        // Hoa Tươi 0
        {
          name: "Bó Hồng",
          image:
            "https://i.pinimg.com/474x/34/51/18/345118545c002472189aed34cb76839b.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Bó O.Hương",
          image:
            "https://i.pinimg.com/474x/46/0a/36/460a362f2bd6ea7703bff97ad83e38b3.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Bó Cúc",
          image:
            "https://i.pinimg.com/474x/b3/04/4b/b3044bd9c3ed15c7ebd84bd077df0b74.jpg",
          no: "x50",
          price: "1k",
          quantity: "",
        },
        {
          name: "Bó H.Dương",
          image:
            "https://i.pinimg.com/474x/2a/58/29/2a5829719ac9e81ebf82ecaa920990b3.jpg",
          no: "x40",
          price: "1k",
          quantity: "",
        },
        {
          name: "Bó Sen",
          image:
            "https://i.pinimg.com/474x/1e/ff/cd/1effcd81a91deb90557b18cc61bfcd2e.jpg",
          no: "x30",
          price: "1k",
          quantity: "",
        },
        {
          name: "Bó Lài",
          image:
            "https://i.pinimg.com/474x/e7/6d/18/e76d18c99eaa470d21876e32535e46e8.jpg",
          no: "x15",
          price: "1k",
          quantity: "",
        },
        // Nước Hoa 0
        {
          name: "NH Hồng",
          image:
            "https://i.pinimg.com/474x/3d/89/52/3d8952a7333c2c119e40ba7d3b3bacdb.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "NH H.Táo",
          image:
            "https://i.pinimg.com/474x/18/cb/4e/18cb4ee1b6ce58fe61f8f1cb76775391.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "NH O.Hương",
          image:
            "https://i.pinimg.com/474x/30/b8/23/30b823bb3ef9ef2ecbb5389a9e385177.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "NH H.Chanh",
          image:
            "https://i.pinimg.com/474x/5a/4a/eb/5a4aeba7b8e7b850133bde04f292622f.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "NH V.Quất",
          image:
            "https://i.pinimg.com/474x/e0/42/d5/e042d563b47c00913f57e2660181002c.jpg",
          no: "x16",
          price: "1k",
          quantity: "",
        },
        {
          name: "NH H.Sen",
          image:
            "https://i.pinimg.com/474x/85/41/e3/8541e3afc4e5c1d14d280de8066e15bd.jpg",
          no: "x15",
          price: "1k",
          quantity: "",
        },
        {
          name: "NH H.Dâu",
          image:
            "https://i.pinimg.com/474x/32/9f/7a/329f7ab3017aaf1beb177ff2195ebc45.jpg",
          no: "x14",
          price: "1k",
          quantity: "",
        },
        // Túi Hương 0
        {
          name: "Túi H.Hồng",
          image:
            "https://i.pinimg.com/474x/56/17/fd/5617fd802158c3e7a87bfde533800659.jpg",
          no: "x100",
          price: "1k",
          quantity: "",
        },
        {
          name: "Túi H.Táo",
          image:
            "https://i.pinimg.com/474x/1b/08/e7/1b08e7abeac16908dee04440f1b1e4f6.jpg",
          no: "x80",
          price: "1k",
          quantity: "",
        },
        {
          name: "Túi O.Hương",
          image:
            "https://i.pinimg.com/474x/b5/f9/9f/b5f99f87baee64677c914432e05c9c0f.jpg",
          no: "x50",
          price: "1k",
          quantity: "",
        },
        {
          name: "Túi H.Chanh",
          image:
            "https://i.pinimg.com/474x/73/fa/ab/73faabb95c4a1d6fe5685cf0fd387421.jpg",
          no: "x30",
          price: "1k",
          quantity: "",
        },
        {
          name: "Túi V.Quất",
          image:
            "https://i.pinimg.com/474x/95/8a/3b/958a3b4992061a2bc62893e2e919897f.jpg",
          no: "x10",
          price: "1k",
          quantity: "",
        },
        {
          name: "Túi H.Sen",
          image:
            "https://i.pinimg.com/474x/be/b4/d8/beb4d8fb2b98de8dfbbc4e261b198eeb.jpg",
          no: "x10",
          price: "1k",
          quantity: "",
        },
        // Vật Phẩm May 0
        {
          name: "Khăn Đỏ",
          image:
            "https://i.pinimg.com/474x/8d/03/89/8d0389c5521ee6438f8d4f756ca9df25.jpg",
          no: "x60",
          price: "1k",
          quantity: "",
        },
        {
          name: "Đầm B.Tuyết",
          image:
            "https://i.pinimg.com/474x/31/cd/c8/31cdc871dc99cce25fea576a239d3048.jpg",
          no: "x40",
          price: "1k",
          quantity: "",
        },
        {
          name: "Thảm Bay",
          image:
            "https://i.pinimg.com/474x/fe/75/3c/fe753c0de0157c26d17bae1fd1eee402.jpg",
          no: "x30",
          price: "1k",
          quantity: "",
        },
        {
          name: "Nón B.Tước",
          image:
            "https://i.pinimg.com/474x/df/93/2f/df932f0f676eaeafccf5bf00bdb06066.jpg",
          no: "x10",
          price: "1k",
          quantity: "",
        },
        {
          name: "Túi C.Chù",
          image:
            "https://i.pinimg.com/474x/0c/dd/ab/0cddabbd2d098015252612f5c4d4f717.jpg",
          no: "x10",
          price: "1k",
          quantity: "",
        },
        {
          name: "Nơ C.Chúa",
          image:
            "https://i.pinimg.com/474x/5c/f2/41/5cf24177b04536fef40c7f57546954ec.jpg",
          no: "x10",
          price: "1k",
          quantity: "",
        },
        {
          name: "Áo Choàng",
          image:
            "https://i.pinimg.com/474x/5e/0b/ff/5e0bff47ac3a79c04ac36942474ac2b3.jpg",
          no: "x10",
          price: "1k",
          quantity: "",
        },
        {
          name: "Giày Đi Hia",
          image:
            "https://i.pinimg.com/474x/b5/83/0d/b5830d6bff4472662b7c6ead86d126e6.jpg",
          no: "x10",
          price: "1k",
          quantity: "",
        },
        // Hạt Giống 0
        {
          name: "Hồng",
          image:
            "https://i.pinimg.com/474x/0e/42/bd/0e42bd37a7df13b7f5148b4506747a44.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Táo",
          image:
            "https://i.pinimg.com/474x/50/b4/e0/50b4e0c0a8529aecb463a3d95b9d72f9.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Bông",
          image:
            "https://i.pinimg.com/474x/d8/61/a3/d861a3624e9085350724a4e852cfdd45.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Tuyết",
          image:
            "https://i.pinimg.com/474x/04/4e/c3/044ec3aa766ef7fbdcf1c11e9d95e379.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "O.Hương",
          image:
            "https://i.pinimg.com/474x/cd/72/ef/cd72ef092b254db4579e94f15352170b.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Dừa",
          image:
            "https://i.pinimg.com/474x/ed/ba/fb/edbafbfc9ceac4bbefa40c39d54bb0bb.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Chanh",
          image:
            "https://i.pinimg.com/474x/0a/4b/f5/0a4bf5ace4ac08a31f7a40c2af31dd6f.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "D.Hấu",
          image:
            "https://i.pinimg.com/474x/c8/a9/7b/c8a97b486670349beebf540a343d896b.jpg",
          no: "x0",
          price: "1k",
          quantity: "",
        },
        {
          name: "Trà",
          image:
            "https://i.pinimg.com/474x/4d/26/e9/4d26e92b76b8aea854cb58e0746b29f3.jpg",
          no: "x600",
          price: "1k",
          quantity: "",
        },
        {
          name: "Mít",
          image:
            "https://i.pinimg.com/474x/c8/d4/74/c8d4743a5801357e670e039858ca4d04.jpg",
          no: "x600",
          price: "1k",
          quantity: "",
        },
        {
          name: "Dứa",
          image:
            "https://i.pinimg.com/474x/a3/3e/fc/a33efcd72ff80a699778a2d5f7f6882a.jpg",
          no: "x600",
          price: "1k",
          quantity: "",
        },
        {
          name: "Xoài",
          image:
            "https://i.pinimg.com/474x/ea/df/b2/eadfb2be03c048433f58f29084a952da.jpg",
          no: "x600",
          price: "1k",
          quantity: "",
        },
        {
          name: "Nho",
          image:
            "https://i.pinimg.com/474x/cb/d8/2c/cbd82c87ffbb674d04e60bbf852e0780.jpg",
          no: "x500",
          price: "1k",
          quantity: "",
        },
        {
          name: "Lài",
          image:
            "https://i.pinimg.com/736x/5d/c2/9e/5dc29ee4b04df68cea8b27e21fdbbf8a.jpg",
          no: "x500",
          price: "1k",
          quantity: "",
        },
        {
          name: "Cúc",
          image:
            "https://i.pinimg.com/474x/01/d3/ff/01d3ffb9b03bc825b0669078947fe645.jpg",
          no: "x400",
          price: "1k",
          quantity: "",
        },
        {
          name: "Bi",
          image:
            "https://i.pinimg.com/736x/71/81/5d/71815dd8824f0f053a44347271199173.jpg",
          no: "x400",
          price: "1k",
          quantity: "",
        },
        {
          name: "Sen",
          image:
            "https://i.pinimg.com/474x/ae/78/f5/ae78f5769cf8fd98022af0d1bd3ad883.jpg",
          no: "x350",
          price: "1k",
          quantity: "",
        },
        {
          name: "H.Dương",
          image:
            "https://i.pinimg.com/474x/ec/10/23/ec102359c85185194c358439b198cdf7.jpg",
          no: "x350",
          price: "1k",
          quantity: "",
        },
        {
          name: "V.Quất",
          image:
            "https://i.pinimg.com/474x/e2/f6/b1/e2f6b14b164297f46626c737d94337ce.jpg",
          no: "x300",
          price: "1k",
          quantity: "",
        },
        {
          name: "Dâu",
          image:
            "https://i.pinimg.com/474x/8f/87/9b/8f879b0d0877bac37e3d53e477a310ac.jpg",
          no: "x300",
          price: "1k",
          quantity: "",
        },
        // Bọ 0
        {
          name: "Bọ Rùa",
          image:
            "https://i.pinimg.com/474x/b5/59/07/b559076ad355aa4b1675ac55e08f165e.jpg",
          no: "x80",
          price: "1k",
          quantity: "",
        },
        {
          name: "Ốc Sên",
          image:
            "https://i.pinimg.com/474x/ba/04/c8/ba04c8afd5021cb8cc55900cdb0d5c2b.jpg",
          no: "x80",
          price: "1k",
          quantity: "",
        },
        {
          name: "Đom Đóm",
          image:
            "https://i.pinimg.com/474x/6d/d7/db/6dd7dbdb030a5f337fa762378e8f07de.jpg",
          no: "x80",
          price: "1k",
          quantity: "",
        },
        {
          name: "Ong Mật",
          image:
            "https://i.pinimg.com/474x/5f/0e/76/5f0e76aae9169c4663d9a8759fdf7bc0.jpg",
          no: "x80",
          price: "1k",
          quantity: "",
        },
        {
          name: "Chuồn Chuồn",
          image:
            "https://i.pinimg.com/474x/02/8e/0e/028e0e144ec65a0c0673da30de975976.jpg",
          no: "x80",
          price: "1k",
          quantity: "",
        },
        {
          name: "Bươm Bướm",
          image:
            "https://i.pinimg.com/474x/98/d4/b8/98d4b83c4711d7781c08618317219397.jpg",
          no: "x80",
          price: "1k",
          quantity: "",
        },
        {
          name: "Sâu Xanh",
          image:
            "https://i.pinimg.com/474x/b4/0e/0a/b40e0ac8ebec442655827025a39dbc27.jpg",
          no: "x80",
          price: "1k",
          quantity: "",
        },
        // Vật Phẩm Khác 0
        {
          name: "Vợt Trắng",
          image:
            "https://i.pinimg.com/474x/cd/80/c0/cd80c01c223117492d6f11b31cbfb297.jpg",
          no: "x80",
          price: "1k",
          quantity: "",
        },
        {
          name: "Vợt Xanh",
          image:
            "https://i.pinimg.com/474x/4d/e1/3c/4de13ce0975519b0ab30911689682d37.jpg",
          no: "x80",
          price: "1k",
          quantity: "",
        },
        {
          name: "Thỏi Đồng",
          image:
            "https://i.pinimg.com/474x/30/e9/10/30e910a6889550872608484b49942ae8.jpg",
          no: "x25",
          price: "1k",
          quantity: "",
        },
        {
          name: "Thỏi Bạc",
          image:
            "https://i.pinimg.com/474x/f9/8f/19/f98f198b25c78d9edddfee506f253856.jpg",
          no: "x50",
          price: "1k",
          quantity: "",
        },
        {
          name: "Thỏi Vàng",
          image:
            "https://i.pinimg.com/474x/3a/54/ad/3a54ade9144b0869933585794f7ab560.jpg",
          no: "x35",
          price: "1k",
          quantity: "",
        },
        {
          name: "Thỏi B.Kim",
          image:
            "https://i.pinimg.com/474x/7f/7a/2a/7f7a2a9dc91d6b8262a305782ff50e0b.jpg",
          no: "x35",
          price: "1k",
          quantity: "",
        },
        {
          name: "Keo D.Mây",
          image:
            "https://i.pinimg.com/474x/88/a7/e4/88a7e40dc4c265cd76cf491c50aa16e4.jpg",
          no: "x12",
          price: "1k",
          quantity: "",
        },
        {
          name: "Lọ N.Thần",
          image:
            "https://i.pinimg.com/474x/95/f8/0a/95f80ae795637d540e04105123cd216b.jpg",
          no: "x15",
          price: "1k",
          quantity: "",
        },
        // Vàng & Vật Phẩm Sự Kiện 1
        {
          name: "Vàng",
          image:
            "https://i.pinimg.com/474x/eb/6f/98/eb6f98c146554c6a1706063d3b0ccda8.jpg",
          no: "x32000",
          price: "1k",
          quantity: "",
        },
        {
          name: "Phân Bón",
          image:
            "https://i.pinimg.com/474x/1a/22/3b/1a223b40d7212bce78cf2062b1fcb60f.jpg",
          no: "x412",
          price: "1k",
          quantity: "",
        },
        {
          name: "Cám Gà",
          image:
            "https://i.pinimg.com/474x/84/4f/09/844f09c991c8f830677e481208fbaf18.jpg",
          no: "x300",
          price: "1k",
          quantity: "",
        },
        {
          name: "Cám Cừu",
          image:
            "https://i.pinimg.com/474x/2d/fa/67/2dfa67fd37658939adfd696a0cd11c08.jpg",
          no: "x300",
          price: "1k",
          quantity: "",
        },
        {
          name: "Cám Heo",
          image:
            "https://i.pinimg.com/474x/a8/57/be/a857be4bb38f986a3879f10941b674ff.jpg",
          no: "x200",
          price: "1k",
          quantity: "",
        },
        {
          name: "Cám Bò",
          image:
            "https://i.pinimg.com/474x/fc/8e/2d/fc8e2d55c8e3b125d28eec5e62683f74.jpg",
          no: "x150",
          price: "1k",
          quantity: "",
        },
        {
          name: "VP. Kem",
          image:
            "https://i.pinimg.com/474x/15/32/fc/1532fc9620e3cebcaa897498294a9e4a.jpg",
          no: "x300",
          price: "1k",
          quantity: "",
        },
        {
          name: "VP. Kính",
          image:
            "https://i.pinimg.com/474x/f7/4a/ca/f74aca49da4092b3ef935e2179d1c770.jpg",
          no: "x200",
          price: "1k",
          quantity: "",
        },
        {
          name: "VP. Dừa",
          image:
            "https://i.pinimg.com/474x/cf/dc/71/cfdc7156657b869915baf8cda120891b.jpg",
          no: "x100",
          price: "1k",
          quantity: "",
        },
        {
          name: "Heo K.Cương",
          image: "",
          no: "x50",
          price: "1k",
          quantity: "",
        },
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

      // Acc - Khu Vườn Trên Mây
      const productss1 = [
        {
          id: "001",
          price: "1k",
          title: "",
          image:
            "https://i.pinimg.com/474x/21/4a/df/214adf99940201d44be9846e9285232e.jpg",
          image1:
            "https://i.pinimg.com/474x/21/4a/df/214adf99940201d44be9846e9285232e.jpg",
          image2:
            "https://i.pinimg.com/474x/21/4a/df/214adf99940201d44be9846e9285232e.jpg",
          image3:
            "https://i.pinimg.com/474x/21/4a/df/214adf99940201d44be9846e9285232e.jpg",
          image4:
            "https://i.pinimg.com/474x/21/4a/df/214adf99940201d44be9846e9285232e.jpg",
          image5:
            "https://i.pinimg.com/474x/21/4a/df/214adf99940201d44be9846e9285232e.jpg",
          image6:
            "https://i.pinimg.com/474x/21/4a/df/214adf99940201d44be9846e9285232e.jpg",
          image7:
            "https://i.pinimg.com/474x/21/4a/df/214adf99940201d44be9846e9285232e.jpg",
          image8:
            "https://i.pinimg.com/474x/21/4a/df/214adf99940201d44be9846e9285232e.jpg",
          image9:
            "https://i.pinimg.com/474x/21/4a/df/214adf99940201d44be9846e9285232e.jpg",
          image10:
            "https://i.pinimg.com/474x/21/4a/df/214adf99940201d44be9846e9285232e.jpg",
        },
      ];
      const container1 = document.getElementById("product-items1");
      container1.innerHTML = productss1
        .map(
          (product1) => `<div class="itemss">
                          <img src="${product1.image}" alt="${product1.id}" />
                          <div class="itemss-content">
                            <div class="name">${product1.id}</div>
                            <div class="flex-row">
                              <button onclick="Overlay('${product1.id}')">🔍</button>
                              <div class="infor">Giá:</div>
                              <div class="price">${product1.price}</div>
                            </div>
                          </div>
                        </div>
                        <div class="overlay" id="${product1.id}">
                          <h2>Thông Tin Chi Tiết</h2>
                          <div class="overlay-img">
                            <img src="${product1.image1}" alt="img1"/>
                            <img src="${product1.image2}" alt="img2"/>
                            <img src="${product1.image3}" alt="img3"/>
                            <img src="${product1.image4}" alt="img4"/>
                            <img src="${product1.image5}" alt="img5"/>
                            <img src="${product1.image6}" alt="img6"/>
                            <img src="${product1.image7}" alt="img7"/>
                            <img src="${product1.image8}" alt="img8"/>
                            <img src="${product1.image9}" alt="img9"/>
                            <img src="${product1.image10}" alt="img10"/>
                          </div>
                          <button style="left: 5px; background-color: #34ff19" onclick='sendMessage("${product1.id}")'>🛒</button>  
                          <div class="overlay-content">${product1.title}</div>
                          <button style="right: 5px; background-color: #ff7676" onclick="Overlay('${product1.id}')">x</button>
                        </div>`
        )
        .join("");

      // Acc - Liên Quân Mobile
      const productss2 = [];
      const container2 = document.getElementById("product-items2");
      container2.innerHTML = productss2
        .map(
          (product2) => `<div class="itemss">
                          <img src="${product2.image}" alt="${product2.id}" />
                          <div class="itemss-content">
                            <div class="name">${product2.id}</div>
                            <div class="flex-row">
                              <button onclick="Overlay('${product2.id}')">🔍</button>
                              <div class="infor">Giá:</div>
                              <div class="price">${product2.price}</div>
                            </div>
                          </div>
                        </div>
                        <div class="overlay" id="${product2.id}">
                          <h2>Thông Tin Chi Tiết</h2>
                          <div class="overlay-img">
                            <img src="${product2.image1}" alt="img1"/>
                            <img src="${product2.image2}" alt="img2"/>
                            <img src="${product2.image3}" alt="img3"/>
                            <img src="${product2.image4}" alt="img4"/>
                            <img src="${product2.image5}" alt="img5"/>
                            <img src="${product2.image6}" alt="img6"/>
                            <img src="${product2.image7}" alt="img7"/>
                            <img src="${product2.image8}" alt="img8"/>
                            <img src="${product2.image9}" alt="img9"/>
                            <img src="${product2.image10}" alt="img10"/>
                          </div>
                          <button style="left: 5px; background-color: #34ff19" onclick='sendMessage("${product2.id}")'>🛒</button>  
                          <div class="overlay-content">${product2.title}</div>
                          <button style="right: 5px; background-color: #ff7676" onclick="Overlay('${product2.id}')">x</button>
                        </div>`
        )
        .join("");

      // Acc - Clash Of Clans
      const productss3 = [];
      const container3 = document.getElementById("product-items3");
      container3.innerHTML = productss3
        .map(
          (product3) => `<div class="itemss">
                          <img src="${product3.image}" alt="${product3.id}" />
                          <div class="itemss-content">
                            <div class="name">${product3.id}</div>
                            <div class="flex-row">
                              <button onclick="Overlay('${product3.id}')">🔍</button>
                              <div class="infor">Giá:</div>
                              <div class="price">${product3.price}</div>
                            </div>
                          </div>
                        </div>
                        <div class="overlay" id="${product3.id}">
                          <h2>Thông Tin Chi Tiết</h2>
                          <div class="overlay-img">
                            <img src="${product3.image1}" alt="img1"/>
                            <img src="${product3.image2}" alt="img2"/>
                            <img src="${product3.image3}" alt="img3"/>
                            <img src="${product3.image4}" alt="img4"/>
                            <img src="${product3.image5}" alt="img5"/>
                            <img src="${product3.image6}" alt="img6"/>
                            <img src="${product3.image7}" alt="img7"/>
                            <img src="${product3.image8}" alt="img8"/>
                            <img src="${product3.image9}" alt="img9"/>
                            <img src="${product3.image10}" alt="img10"/>
                          </div>
                          <button style="left: 5px; background-color: #34ff19" onclick='sendMessage("${product3.id}")'>🛒</button>  
                          <div class="overlay-content">${product3.title}</div>
                          <button style="right: 5px; background-color: #ff7676" onclick="Overlay('${product3.id}')">x</button>
                        </div>`
        )
        .join("");

      // Acc - Dragon City
      const productss4 = [];
      const container4 = document.getElementById("product-items4");
      container4.innerHTML = productss4
        .map(
          (product4) => `<div class="itemss">
                          <img src="${product4.image}" alt="${product4.id}" />
                          <div class="itemss-content">
                            <div class="name">${product4.id}</div>
                            <div class="flex-row">
                              <button onclick="Overlay('${product4.id}')">🔍</button>
                              <div class="infor">Giá:</div>
                              <div class="price">${product4.price}</div>
                            </div>
                          </div>
                        </div>
                        <div class="overlay" id="${product4.id}">
                          <h2>Thông Tin Chi Tiết</h2>
                          <div class="overlay-img">
                            <img src="${product4.image1}" alt="img1"/>
                            <img src="${product4.image2}" alt="img2"/>
                            <img src="${product4.image3}" alt="img3"/>
                            <img src="${product4.image4}" alt="img4"/>
                            <img src="${product4.image5}" alt="img5"/>
                            <img src="${product4.image6}" alt="img6"/>
                            <img src="${product4.image7}" alt="img7"/>
                            <img src="${product4.image8}" alt="img8"/>
                            <img src="${product4.image9}" alt="img9"/>
                            <img src="${product4.image10}" alt="img10"/>
                          </div>
                          <button style="left: 5px; background-color: #34ff19" onclick='sendMessage("${product4.id}")'>🛒</button>  
                          <div class="overlay-content">${product4.title}</div>
                          <button style="right: 5px; background-color: #ff7676" onclick="Overlay('${product4.id}')">x</button>
                        </div>`
        )
        .join("");

      // Acc - Free Fire
      const productss5 = [];
      const container5 = document.getElementById("product-items5");
      container5.innerHTML = productss5
        .map(
          (product5) => `<div class="itemss">
                          <img src="${product5.image}" alt="${product5.id}" />
                          <div class="itemss-content">
                            <div class="name">${product5.id}</div>
                            <div class="flex-row">
                              <button onclick="Overlay('${product5.id}')">🔍</button>
                              <div class="infor">Giá:</div>
                              <div class="price">${product5.price}</div>
                            </div>
                          </div>
                        </div>
                        <div class="overlay" id="${product5.id}">
                          <h2>Thông Tin Chi Tiết</h2>
                          <div class="overlay-img">
                            <img src="${product5.image1}" alt="img1"/>
                            <img src="${product5.image2}" alt="img2"/>
                            <img src="${product5.image3}" alt="img3"/>
                            <img src="${product5.image4}" alt="img4"/>
                            <img src="${product5.image5}" alt="img5"/>
                            <img src="${product5.image6}" alt="img6"/>
                            <img src="${product5.image7}" alt="img7"/>
                            <img src="${product5.image8}" alt="img8"/>
                            <img src="${product5.image9}" alt="img9"/>
                            <img src="${product5.image10}" alt="img10"/>
                          </div>
                          <button style="left: 5px; background-color: #34ff19" onclick='sendMessage("${product5.id}")'>🛒</button>  
                          <div class="overlay-content">${product5.title}</div>
                          <button style="right: 5px; background-color: #ff7676" onclick="Overlay('${product5.id}')">x</button>
                        </div>`
        )
        .join("");

      // Acc - Khác
      const productss6 = [];
      const container6 = document.getElementById("product-items6");
      container6.innerHTML = productss6
        .map(
          (product6) => `<div class="itemss">
                          <img src="${product6.image}" alt="${product6.id}" />
                          <div class="itemss-content">
                            <div class="name">${product6.id}</div>
                            <div class="flex-row">
                              <button onclick="Overlay('${product6.id}')">🔍</button>
                              <div class="infor">Giá:</div>
                              <div class="price">${product6.price}</div>
                            </div>
                          </div>
                        </div>
                        <div class="overlay" id="${product6.id}">
                          <h2>Thông Tin Chi Tiết</h2>
                          <div class="overlay-img">
                            <img src="${product6.image1}" alt="img1"/>
                            <img src="${product6.image2}" alt="img2"/>
                            <img src="${product6.image3}" alt="img3"/>
                            <img src="${product6.image4}" alt="img4"/>
                            <img src="${product6.image5}" alt="img5"/>
                            <img src="${product6.image6}" alt="img6"/>
                            <img src="${product6.image7}" alt="img7"/>
                            <img src="${product6.image8}" alt="img8"/>
                            <img src="${product6.image9}" alt="img9"/>
                            <img src="${product6.image10}" alt="img10"/>
                          </div>
                          <button style="left: 5px; background-color: #34ff19" onclick='sendMessage("${product6.id}")'>🛒</button>  
                          <div class="overlay-content">${product6.title}</div>
                          <button style="right: 5px; background-color: #ff7676" onclick="Overlay('${product6.id}')">x</button>
                        </div>`
        )
        .join("");

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

      // // Chặn chuột phải
      // document.addEventListener("contextmenu", function (e) {
      //   e.preventDefault();
      // });

      // // Chặn Ctrl+C, Ctrl+U, Ctrl+S, Ctrl+Shift+I, F12...
      // document.addEventListener("keydown", function (e) {
      //   if (
      //     (e.ctrlKey &&
      //       (e.key === "c" ||
      //         e.key === "u" ||
      //         e.key === "s" ||
      //         e.key === "a")) ||
      //     (e.ctrlKey && e.shiftKey && e.key.toLowerCase() === "i") ||
      //     e.key === "F12"
      //   ) {
      //     e.preventDefault();
      //   }
      // });

      // // Chặn kéo chọn văn bản
      // document.addEventListener("selectstart", function (e) {
      //   e.preventDefault();
      // });

      // // Chặn kéo văn bản bằng chuột
      // document.addEventListener("dragstart", function (e) {
      //   e.preventDefault();
      // });
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

      function sendMessage(data) {
        try {
          const baseUrl = "https://www.messenger.com/t/488283351040349";

          if (typeof data === "string" && data.trim() !== "") {
            alert(`Đang gửi đơn hàng: ${data}`); // Thông báo UX
            const encodedMessage = encodeURIComponent(`Order: ${data}`);
            const fullUrl = `${baseUrl}?text=${encodedMessage}`;
            window.open(fullUrl, "_blank");
          } else {
            // Nếu không có data thì mở trang chat mặc định
            window.open(baseUrl, "_blank");
          }
        } catch (err) {
          console.error("Không thể mở Messenger:", err);
          alert("Đã xảy ra lỗi. Vui lòng thử lại.");
        }
      }
    </script>
  </body>
</html>

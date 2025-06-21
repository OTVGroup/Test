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
      content="https://i.pinimg.com/736x/15/c2/33/15c233ab5cce7b9e60094a36653a3dc5.jpg"
    />
    <title>OTVGroup | Hết Mình Với Đam Mê!</title>
    <link
      rel="icon"
      type="image/jpeg"
      href="https://i.pinimg.com/736x/15/c2/33/15c233ab5cce7b9e60094a36653a3dc5.jpg"
    />
    <style>
      /* Cấu hình chung cho toàn bộ trang */
      body {
        font-family: Arial, sans-serif; /* Phông chữ hiện đại, dễ đọc */
        display: flex;
        flex-direction: column; /* Các phần tử con sắp xếp theo chiều dọc */
        align-items: center; /* Căn giữa theo trục ngang */
        justify-content: center; /* Căn giữa theo trục dọc */
        background-color: #000000; /* Màu nền fallback khi ảnh không load */
        color: #000000; /* Màu chữ mặc định */
        user-select: none; /* Ngăn người dùng chọn văn bản (trải nghiệm cao cấp) */
        margin: 0 auto;
        width: 100vw;
        overflow-x: hidden; /* Ẩn tràn ngang */
        box-sizing: border-box;
        touch-action: manipulation; /* Ngăn gesture zoom/double-tap */
      }

      /* Cấu hình chung cho từng ngăn (section) */
      section {
        text-align: center; /* Căn giữa nội dung trong ngăn */
        width: 380px; /* Bắt buộc để ngăn chiếm toàn bộ chiều ngang */
        box-sizing: border-box; /* Đảm bảo padding không làm vỡ bố cục */
      }

      /* Ngăn 1: Hero */
      #hero {
        background-color: #000000;
        color: white; /* Nội dung màu trắng nổi bật trên ảnh nền */
      }

      /* Ngăn 2: Thông Tin */
      #event-streams {
        background: #363636; /* Màu xám chủ đạo */
        width: 100%;
        max-width: 1100px;
        min-width: 380px;
      }

      /* Ngăn 3: Youtube */
      #information {
        background: white; /* Màu trắng giúp nội dung nhẹ nhàng */
        width: 100%;
        min-width: 380px;
        max-width: 1100px;
        grid-template-columns: repeat(auto-fit, minmax(360px, 1fr));
        gap: 5px;
        padding-bottom: 5px;
        justify-items: center; /* 👉 Canh giữa item trong mỗi ô */
      }

      .heading {
        width: 100%;
        display: flex;
        background-color: black;
        justify-content: center;
        align-items: center;
      }

      .heading img {
        width: 100%;
        height: auto;
        max-width: 535px;
        min-height: 45px;
        aspect-ratio: 851 / 315;
        object-fit: contain; /* Đảm bảo ảnh không bị méo và hiển thị toàn bộ */
        display: block;
      }

      /* Ngăn 4: Tin Mới */
      #facebook-reels {
        background: #e0f7fa; /* Xanh nhạt, thân thiện */
      }

      /* Ngăn 5: Footer */
      #footer {
        background: #121212;
        color: #e4e4e4;
        font-family: sans-serif;
      }
    </style>
  </head>
  <body>
    <!-- Giao Diện -->
    <!-- Ngăn 1: Hero -->
    <section id="hero">
      <img
        src="https://i.pinimg.com/736x/15/c2/33/15c233ab5cce7b9e60094a36653a3dc5.jpg"
        alt="Logo-OTVGroup"
        height="150px"
        style="
          border-radius: 50%;
          box-shadow: 0 0 50px rgba(255, 255, 255, 0.519);
        "
      />
      <h1>
        OTVGroup
        <p style="text-align: center; font-size: 16px; color: #c9c9c9">
          Hết Mình Với Đam Mê!
        </p>
      </h1>
    </section>

    <!-- Ngăn 2: Event -->
    <section id="event-streams" style="color: white">
      <h2 style="text-align: center">🎬 Event Feed</h2>
      <p
        style="
          text-align: center;
          font-size: 14px;
          color: #aaa;
          margin-bottom: 10px;
        "
      >
        Swipe to explore our latest shows.
      </p>

      <div
        style="
          display: flex;
          overflow-x: auto;
          gap: 0;
          margin: 0 10px;
          scroll-snap-type: x mandatory;
          -webkit-overflow-scrolling: touch;
        "
      >
        <!-- OTVChannel -->
        <div
          id="videosOTVChannel1"
          style="
            width: 100%;
            min-width: 360px;
            background: #1a1a1a;
            overflow: hidden;
            scroll-snap-align: start;
            color: #fff;
          "
        ></div>
        <!-- OTVStory -->
        <div
          id="videosOTVStory1"
          style="
            width: 100%;
            min-width: 360px;
            background: #1a1a1a;
            overflow: hidden;
            scroll-snap-align: start;
            color: #fff;
          "
        ></div>
        <!-- OTVGaming -->
        <div
          id="videosOTVGaming1"
          style="
            width: 100%;
            min-width: 360px;
            background: #1a1a1a;
            overflow: hidden;
            scroll-snap-align: start;
            color: #fff;
          "
        ></div>

        <!-- OTVChannel -->
        <div
          id="videosOTVChannel2"
          style="
            width: 100%;
            min-width: 360px;
            background: #1a1a1a;
            overflow: hidden;
            scroll-snap-align: start;
            color: #fff;
          "
        ></div>
        <!-- OTVStory -->
        <div
          id="videosOTVStory2"
          style="
            width: 100%;
            min-width: 360px;
            background: #1a1a1a;
            overflow: hidden;
            scroll-snap-align: start;
            color: #fff;
          "
        ></div>
        <!-- OTVGaming -->
        <div
          id="videosOTVGaming2"
          style="
            width: 100%;
            min-width: 360px;
            background: #1a1a1a;
            overflow: hidden;
            scroll-snap-align: start;
            color: #fff;
          "
        ></div>

        <!-- OTVChannel -->
        <div
          id="videosOTVChannel3"
          style="
            width: 100%;
            min-width: 360px;
            background: #1a1a1a;
            overflow: hidden;
            scroll-snap-align: start;
            color: #fff;
          "
        ></div>
        <!-- OTVStory -->
        <div
          id="videosOTVStory3"
          style="
            width: 100%;
            min-width: 360px;
            background: #1a1a1a;
            overflow: hidden;
            scroll-snap-align: start;
            color: #fff;
          "
        ></div>
        <!-- OTVGaming -->
        <div
          id="videosOTVGaming3"
          style="
            width: 100%;
            min-width: 360px;
            background: #1a1a1a;
            overflow: hidden;
            scroll-snap-align: start;
            color: #fff;
          "
        ></div>
      </div>
    </section>

    <!-- Ngăn 3: OTVGroup -->
    <section id="information">
      <div class="heading">
        <img
          src="https://raw.githubusercontent.com/OTVGroup/OTVGroup.com.vn/main/Background%20-%20OTVGroup.jpeg"
          alt="Poster-OTVGroup"
        />
      </div>
      <div
        style="
          display: flex;
          justify-content: center;
          gap: 15px;
          flex-wrap: wrap;
          padding: 10px;
        "
      >
        <div style="width: 100px; text-align: center">
          <a href="https://www.facebook.com/OtisVo586" target="_blank">
            <img
              src="https://i.pinimg.com/736x/15/c2/33/15c233ab5cce7b9e60094a36653a3dc5.jpg"
              width="80px"
              style="border-radius: 50%; box-shadow: 0 0 5px rgba(0, 0, 0, 0.2)"
            />
            <p>
              <img
                src="https://img.icons8.com/color/20/facebook-new.png"
                style="vertical-align: middle; margin-right: 5px"
              />Otis Võ
            </p>
          </a>
        </div>
        <div style="width: 100px; text-align: center">
          <a href="https://www.youtube.com/@otvchannelvn" target="_blank">
            <img
              src="https://i.pinimg.com/736x/15/c2/33/15c233ab5cce7b9e60094a36653a3dc5.jpg"
              width="80px"
              style="border-radius: 50%; box-shadow: 0 0 5px rgba(0, 0, 0, 0.2)"
            />
            <p>
              <img
                src="https://img.icons8.com/color/20/youtube-play.png"
                style="vertical-align: middle; margin-right: 5px"
              />OTV Channel
            </p>
          </a>
        </div>

        <div style="width: 100px; text-align: center">
          <a href="https://www.youtube.com/@otvstoryvn" target="_blank">
            <img
              src="https://i.pinimg.com/736x/09/44/f6/0944f6cacd07b3a164a82d62f02d2709.jpg"
              width="80px"
              style="border-radius: 50%; box-shadow: 0 0 5px rgba(0, 0, 0, 0.2)"
            />
            <p>
              <img
                src="https://img.icons8.com/color/20/youtube-play.png"
                style="vertical-align: middle; margin-right: 5px"
              />OTV Story
            </p>
          </a>
        </div>
      </div>
    </section>

    <!-- Ngăn 4: OTISSHOP -->
    <section id="information">
      <div class="heading">
        <img
          src="https://raw.githubusercontent.com/OTVGroup/OTVGroup.com.vn/main/Background%20-%20OTISShop.jpeg"
          alt="Poster-OTISShop"
          style="width: 100%; height: auto"
        />
      </div>
      <div
        style="
          display: flex;
          justify-content: center;
          gap: 15px;
          flex-wrap: wrap;
          padding: 10px;
        "
      >
        <div style="width: 100px; text-align: center">
          <a href="https://www.facebook.com/OtisSeller" target="_blank">
            <img
              src="https://i.pinimg.com/736x/ea/24/e1/ea24e1a0ed40857020ab39336b9fc78c.jpg"
              width="80px"
              style="border-radius: 50%; box-shadow: 0 0 5px rgba(0, 0, 0, 0.2)"
            />
            <p>
              <img
                src="https://img.icons8.com/color/20/facebook-new.png"
                style="vertical-align: middle; margin-right: 5px"
              />OTISShop
            </p>
          </a>
        </div>
        <div style="width: 100px; text-align: center">
          <a href="https://www.instagram.com/otisshopvn" target="_blank">
            <img
              src="https://i.pinimg.com/736x/ea/24/e1/ea24e1a0ed40857020ab39336b9fc78c.jpg"
              width="80px"
              style="border-radius: 50%; box-shadow: 0 0 5px rgba(0, 0, 0, 0.2)"
            />
            <p>
              <img
                src="https://img.icons8.com/color/20/instagram-new.png"
                style="vertical-align: middle; margin-right: 5px"
              />OTISShop
            </p>
          </a>
        </div>
        <div style="width: 100px; text-align: center">
          <a href="https://www.tiktok.com/@otisshop" target="_blank">
            <img
              src="https://i.pinimg.com/736x/ea/24/e1/ea24e1a0ed40857020ab39336b9fc78c.jpg"
              width="80px"
              style="border-radius: 50%; box-shadow: 0 0 5px rgba(0, 0, 0, 0.2)"
            />
            <p>
              <img
                src="https://img.icons8.com/color/20/tiktok--v1.png"
                style="vertical-align: middle; margin-right: 5px"
              />OTISShop
            </p>
          </a>
        </div>
        <div style="width: 100px; text-align: center">
          <a href="https://www.threads.net/@otisshopvn" target="_blank">
            <img
              src="https://i.pinimg.com/736x/ea/24/e1/ea24e1a0ed40857020ab39336b9fc78c.jpg"
              width="80px"
              style="border-radius: 50%; box-shadow: 0 0 5px rgba(0, 0, 0, 0.2)"
            />
            <p>
              <img
                src="https://img.icons8.com/ios-filled/20/000000/threads.png"
                style="vertical-align: middle; margin-right: 5px"
              />OTISShop
            </p>
          </a>
        </div>
      </div>
    </section>

    <!-- Ngăn 5: OTISSTORE -->
    <section id="information">
      <div class="heading">
        <img
          src="https://raw.githubusercontent.com/OTVGroup/OTVGroup.com.vn/main/Background-OTISStore.jpeg"
          alt="Poster-OTISStore"
          style="width: 100%; height: auto"
        />
      </div>
      <div
        style="
          display: flex;
          justify-content: center;
          gap: 15px;
          flex-wrap: wrap;
          padding: 10px;
        "
      >
        <div style="width: 100px; text-align: center">
          <a href="https://www.facebook.com/OtisGamerVN" target="_blank">
            <img
              src="https://i.pinimg.com/736x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
              width="80px"
              style="border-radius: 50%; box-shadow: 0 0 5px rgba(0, 0, 0, 0.2)"
            />
            <p>
              <img
                src="https://img.icons8.com/color/20/facebook-new.png"
                style="vertical-align: middle; margin-right: 5px"
              />OTISStore
            </p>
          </a>
        </div>

        <div style="width: 100px; text-align: center">
          <a href="https://www.youtube.com/@otisstorevn" target="_blank">
            <img
              src="https://i.pinimg.com/736x/34/59/6a/34596a4db3932a3855c872c2f4833e5d.jpg"
              width="80px"
              style="border-radius: 50%; box-shadow: 0 0 5px rgba(0, 0, 0, 0.2)"
            />
            <p>
              <img
                src="https://img.icons8.com/color/20/youtube-play.png"
                style="vertical-align: middle; margin-right: 5px"
              />OTISSTORE
            </p>
          </a>
        </div>
      </div>

      <!-- Video Youtube -->
      <!-- <div
        id="videos-container"
        style="
          display: flex;
          flex-wrap: wrap;
          gap: 15px;
          justify-content: center;
        "
      >
        <div id="videosOTVChannel" style="width: 360px"></div>
        <div id="videosOTVStory" style="width: 360px"></div>
        <div id="videosOTVGaming" style="width: 360px"></div>
      </div> -->
    </section>

    <!-- Ngăn 4: Facebook -->
    <!-- <section id="facebook-reels">
      <h2>Facebook Videos</h2> -->

    <!-- Nhúng reel hoặc bài viết Facebook -->
    <!-- <div id="fb-root"></div>
      <script
        async
        defer
        crossorigin="anonymous"
        src="https://connect.facebook.net/vi_VN/sdk.js#xfbml=1&version=v18.0"
      ></script> -->

    <!-- Container chứa các post -->
    <!-- <div
        style="
          display: flex;
          flex-wrap: wrap;
          gap: 15px;
          justify-content: center;
          max-width: 1200px;
          margin: auto;
        "
      > -->
    <!-- Bài 1 -->
    <!-- <div
          style="
            width: 100%;
            max-width: 360px;
            aspect-ratio: 9 / 16;
            border-radius: 8px;
            box-sizing: border-box;
            overflow: hidden;
            position: relative;
          "
        >
          <iframe
            src="https://www.facebook.com/plugins/video.php?height=476&href=https%3A%2F%2Fwww.facebook.com%2Freel%2F672996332031027%2F&show_text=false&width=267&t=0"
            style="width: 100%; height: 100%; border: none; overflow: hidden"
            scrolling="no"
            frameborder="0"
            allowfullscreen="true"
            allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share"
          ></iframe>
        </div> -->

    <!-- Bài 2 -->
    <!-- <div
          style="
            width: 100%;
            max-width: 360px;
            aspect-ratio: 9 / 16;
            border-radius: 8px;
            box-sizing: border-box;
            overflow: hidden;
            position: relative;
          "
        >
          <iframe
            src="https://www.facebook.com/plugins/video.php?height=314&href=https%3A%2F%2Fwww.facebook.com%2FOtisGamerVN%2Fvideos%2F2050806685329017%2F&show_text=false&width=560&t=0"
            style="width: 100%; height: 100%; border: none; overflow: hidden"
            scrolling="no"
            frameborder="0"
            allowfullscreen="true"
            allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share"
          ></iframe>
        </div> -->

    <!-- Bài 3 -->
    <!-- <div
          style="
            width: 100%;
            max-width: 360px;
            aspect-ratio: 5/7;
            border-radius: 8px;
            box-sizing: border-box;
            overflow: hidden;
            position: relative;
          "
        >
          <iframe
            src="https://www.facebook.com/plugins/post.php?href=https%3A%2F%2Fwww.facebook.com%2FOtisSeller%2Fposts%2F122138746688611769&show_text=true&width=500"
            style="width: 100%; height: 100%; border: none; overflow: hidden"
            scrolling="no"
            frameborder="0"
            allowfullscreen="true"
            allow="autoplay; clipboard-write; encrypted-media; picture-in-picture; web-share"
          ></iframe>
        </div>
      </div>
    </section> -->

    <!-- Footer -->
    <section id="footer">
      <div
        style="
          max-width: 1200px;
          margin: auto;
          padding: 0 15px;
          text-align: center;
        "
      >
        <h3>Donate</h3>

        <div
          style="
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
          "
        >
          <div style="flex: 1 1 30%; max-width: 110px">
            <img
              src="https://i.pinimg.com/736x/40/05/9b/40059b9b00037529a0cad56eb5ae4d1d.jpg"
              alt="Donate Agribank"
              style="width: 100%; border-radius: 8px"
            />
          </div>

          <div style="flex: 1 1 30%; max-width: 110px">
            <img
              src="https://i.pinimg.com/736x/27/17/68/271768775d063a13b76b78bfb4b4befe.jpg"
              alt="Donate MoMo"
              style="width: 100%; border-radius: 8px"
            />
          </div>

          <div style="flex: 1 1 30%; max-width: 110px">
            <img
              src="https://i.pinimg.com/736x/15/81/ed/1581edcd2b862a72f316ce2b84cc0e15.jpg"
              alt="Donate Zalopay"
              style="width: 100%; border-radius: 8px"
            />
          </div>
        </div>
      </div>

      <!-- Keyword SEO -->
      <div
        style="
          max-width: 1200px;
          margin: 20px auto 10px;
          padding: 0 15px;
          text-align: center;
          font-size: 14px;
          line-height: 1.5;
          color: #bbb;
        "
      >
        <strong>Mọi người cũng tìm kiếm:</strong><br />
        OTVGroup | Otis Võ | OTISShop | OTISStore | Chill | Music | Tâm Sự | Tâm
        Trạng | Tình Yêu | Cặp Đôi | Xu Hướng | Viral | Buồn | Hạnh Phúc | Cô
        Đơn | Lofi | Remix | Vinahouse | Deephouse | Thịnh Hành | Mạng Xã Hội |
        Thành Công | Thành Đạt | Tâm Hồn | Ký Ức | Lắng Đọng | Cảm Xúc | Nỗi Nhớ
        | Yêu Thương | Tổn Thương | Vỡ Tan | Bình Yên | Giải Tỏa | Cô Độc | Vấp
        Ngã | Tự Sự | Acoustic | Ballad | EDM | Hiphop | Rap Việt | Mashup |
        V-pop | Cover | Live Session | Trending Song | Nhạc Buồn | Nhạc Tiktok |
        Soundtrack | Melody | Vocal | Động Lực | Đam Mê | Khởi Nghiệp | Kinh
        Doanh | Truyền Cảm Hứng | Yêu Bản Thân | Công Nghệ | Reaction | Bắt
        Trend | Thịnh Hành Tiktok | Drama Showbiz | Viral Video
      </div>

      <!-- Info Legal -->
      <div
        style="
          max-width: 1200px;
          margin: 0 auto;
          padding: 10px 15px;
          text-align: center;
          font-size: 13px;
          color: #888;
        "
      >
        © 2024 - 2025 Công Ty TNHH MTV OTVGroup
        <br />
        • Địa chỉ:
        <a
          href="https://maps.app.goo.gl/au8jubbPqSTZ8FjP7"
          style="color: #007aff; text-decoration: none"
        >
          P.Tân Chánh Hiệp, Q.12, TP. Hồ Chí Minh
        </a>
        <br />
        • Hotline:
        <a href="tel=0329022431" style="color: #007aff; text-decoration: none">
          0329 022 431
        </a>
        • Email:
        <a
          href="mailto:thinhkvtm2006@gmail.com"
          style="color: #007aff; text-decoration: none"
        >
          thinhkvtm2006@gmail.com
        </a>
        <br />
        • Chịu trách nhiệm kỹ thuật: Võ Trường Thịnh
      </div>
    </section>

    <script>
      const channels = [
        { id: "UCv-PFwjDGSfgozwLVCJEv0w", targetPrefix: "videosOTVChannel" }, // otvchannelvn
        { id: "UC4UOBFi4HJHU_EhynZbrefw", targetPrefix: "videosOTVStory" }, // otvstoryvn
        { id: "UCM8xwnvLQ60wfEgduDRzRMg", targetPrefix: "videosOTVGaming" }, // otvgamingvn
      ];

      channels.forEach((channel) => {
        fetch(
          `https://api.rss2json.com/v1/api.json?rss_url=https://www.youtube.com/feeds/videos.xml?channel_id=${channel.id}`
        )
          .then((response) => response.json())
          .then((data) => {
            const videos = data.items.slice(0, 3); // lấy 3 video đầu

            videos.forEach((item, index) => {
              const videoId = item.guid.split(":")[2];
              const targetId = `${channel.targetPrefix}${index + 1}`;

              const videoHTML = `
          <iframe width="100%" height="215" src="https://www.youtube.com/embed/${videoId}" 
            frameborder="0" allowfullscreen loading="lazy"></iframe>
          <h3 style="font-size: 1rem; margin-top: 8px;">${item.title}</h3>
        `;

              const targetElement = document.getElementById(targetId);
              if (targetElement) {
                targetElement.innerHTML = videoHTML;
              } else {
                console.warn(`Không tìm thấy phần tử với ID: ${targetId}`);
              }
            });
          })
          .catch((error) => {
            console.error("Lỗi tải video:", error);
            // Hiển thị lỗi cho cả 3 vị trí nếu có
            for (let i = 1; i <= 3; i++) {
              const errorTarget = document.getElementById(
                `${channel.targetPrefix}${i}`
              );
              if (errorTarget) {
                errorTarget.innerHTML = `<p>Không thể tải video.</p>`;
              }
            }
          });
      });
    </script>
  </body>
</html>

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
      /* body {
              font-family: Arial, sans-serif;
              display: flex;
              flex-direction: column;
              align-items: center;
              justify-content: center;
              background-color: #000000;
              color: #000000;
              user-select: none;
              width: 100vw;
              overflow-x: hidden;
              box-sizing: border-box;
              touch-action: manipulation;
            } */

      body {
        font-family: Arial, sans-serif;
        display: flex;
        flex-direction: column;
        align-items: center;
        align-content: center;
        width: 100vw;
        justify-content: center;
        background-color: #000000;
        color: #000000;
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
        position: absolute;
        top: 0;
        left: 50%;
        transform: translateX(-50%); /* dịch tâm khối về chính giữa */

        flex-direction: column; /* Các phần tử con sắp xếp theo chiều dọc */
        align-items: center; /* Căn giữa theo trục ngang */
        justify-content: center; /* Căn giữa theo trục dọc */

        width: 95vw;
        height: 100vh;

        font-family: "Segoe UI", sans-serif;
        background-color: #000000;
        color: #000000;
      }

      section {
        color: white; /* Nội dung màu trắng nổi bật trên ảnh nền */
        text-align: center; /* Căn giữa nội dung trong ngăn */
        width: 100%; /* Bắt buộc để ngăn chiếm toàn bộ chiều ngang */
        box-sizing: border-box; /* Đảm bảo padding không làm vỡ bố cục */
      }

      #hero,
      #event-streams {
        background: #000000;
      }
      #information {
        background: #212121;
      }
      #footer {
        background: #161616;
      }

      #hero {
        width: 100%;
        min-width: 360px;
        display: flex;
        padding: 5px 10px;
        align-items: center;
      }

      #hero img {
        width: 80px;
        margin: 5px;
        box-shadow: 0 0 10px rgba(255, 255, 255, 0.519);
      }

      #hero h1,
      #hero p,
      #event-streams p {
        margin: 5px auto;
      }

      .video-streams {
        width: 100%;
        min-width: 360px;
        overflow: hidden;
        scroll-snap-align: start;
      }

      #information {
        display: flex;
        flex-wrap: wrap;
        justify-items: center; /* 👉 Canh giữa item trong mỗi ô */
        align-content: center;
        justify-content: center;
      }

      .heading {
        width: auto;
        min-width: 358px;
        max-width: 480px;
        display: flex;
        gap: 5px;
        border: #000000 solid 1px;
        flex-direction: column;
        background: #ffffff;
        align-items: center;
      }

      .heading-img {
        width: 100%;
        height: auto;
        max-width: 480px;
        min-height: 50px;
        aspect-ratio: 851 / 315;
        border-bottom: #000000 solid 1px;
      }

      .heading1 {
        display: flex;
        justify-content: center;
        width: 100%;
        flex-wrap: wrap;
        padding: 0 10px;
      }

      .heading1 a {
        color: #3e3e3e;
        font-size: 15px;
        font-weight: 600;
        line-height: 1;
      }

      .heading1 b {
        color: #000000;
        font-size: 15px;
        font-weight: 700;
        line-height: 1;
      }

      .heading1 strong {
        color: #000000;
        font-size: 13px;
        text-indent: 1cqh;
        text-align: justify;
        font-weight: 400;
        line-height: 1;
      }

      .heading2 {
        display: flex;
        justify-content: center;
        width: 100%;
        height: min-content;
        flex-wrap: wrap;
      }

      .social {
        width: auto;
        min-width: 100px;
        max-width: 150px;
        text-align: center;
        margin: 0 auto 5px auto;
        color: #000000;
        text-decoration: none;
      }

      .social img {
        vertical-align: middle;
        margin-right: 2px;
        width: 15px;
        height: 15px;
        border-radius: 50%;
        box-shadow: 0 0 5px rgba(0, 0, 0, 0.2);
      }

      .social a {
        color: #000000;
        font-size: 13px;
        font-weight: 600;
        line-height: 1;
      }

      #footer {
        color: #e4e4e4;
        display: flex;
        flex-direction: column;
        gap: 10px;
        padding: 10px 0;
        font-family: sans-serif;
      }
    </style>
  </head>
  <body>
    <div class="body-background">
      <!-- Giao Diện -->
      <!-- Ngăn 1: Hero -->
      <section id="hero">
        <img
          src="https://i.pinimg.com/736x/15/c2/33/15c233ab5cce7b9e60094a36653a3dc5.jpg"
          alt="Logo-OTVGroup"
          style="border-radius: 50%"
        />
        <h1>
          OTVGroup
          <p style="text-align: center; font-size: 16px; color: #c9c9c9">
            Hết Mình Với Đam Mê!
          </p>
        </h1>
        <a
          href="https://drive.google.com/file/d/17N1bAsvmtmM9ARnHNDBjAeW6TOfT2yXR/view?usp=sharing"
          target="_blank"
        >
          <img
            src="https://i.pinimg.com/736x/29/4d/be/294dbeb6dad25f31f15d14a897af1849.jpg"
            alt="Logo-Profile"
            style="border-radius: 5%"
          />
        </a>
      </section>

      <!-- Ngăn 2: Event -->
      <section id="event-streams">
        <p
          style="
            text-align: center;
            font-size: 12px;
            font-weight: 600;
            color: #bbb;
          "
        >
          SWIPE TO EXPLORE OUR LATEST SHOWS.
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
          <div id="videosOTVChannel1" class="video-streams"></div>
          <!-- OTVStory -->
          <div id="videosOTVStory1" class="video-streams"></div>
          <!-- OTVGaming -->
          <div id="videosOTVGaming1" class="video-streams"></div>

          <!-- OTVChannel -->
          <div id="videosOTVChannel2" class="video-streams"></div>
          <!-- OTVStory -->
          <div id="videosOTVStory2" class="video-streams"></div>
          <!-- OTVGaming -->
          <div id="videosOTVGaming2" class="video-streams"></div>

          <!-- OTVChannel -->
          <div id="videosOTVChannel3" class="video-streams"></div>
          <!-- OTVStory -->
          <div id="videosOTVStory3" class="video-streams"></div>
          <!-- OTVGaming -->
          <div id="videosOTVGaming3" class="video-streams"></div>
        </div>
      </section>

      <!-- Ngăn 3: Information -->
      <section id="information">
        <div class="heading">
          <img
            src="https://raw.githubusercontent.com/OTVGroup/OTVGroup.com.vn/main/Background%20-%20OTVGroup.jpeg"
            alt="Poster-OTVGroup"
            class="heading-img"
          />
          <div class="heading1">
            <a><b>OTVGroup</b> - Hết Mình Với Đam Mê!</a>
            <div
              style="
                width: 100%;
                height: 2px;
                margin: 5px auto;
                background-color: #000000;
              "
            ></div>
            <strong>
              OTVGroup is a vibrant, creative, and diverse content ecosystem
              that stands out in the fields of entertainment, arts, and digital
              innovation.
            </strong>
          </div>
          <div class="heading2">
            <div class="social">
              <img src="https://img.icons8.com/color/20/facebook-new.png" />
              <a href="https://www.facebook.com/OtisVo586" target="_blank">
                Otis Võ
              </a>
            </div>
            <div class="social">
              <img src="https://img.icons8.com/color/20/youtube-play.png" />
              <a href="https://www.youtube.com/@otvchannelvn" target="_blank">
                OTV Channel
              </a>
            </div>

            <div class="social">
              <img src="https://img.icons8.com/color/20/youtube-play.png" />
              <a href="https://www.youtube.com/@otvstoryvn" target="_blank">
                OTV Story
              </a>
            </div>
          </div>
        </div>

        <!-- Ngăn 3: OTIS Music Studio -->
        <div class="heading">
          <img
            src="https://raw.githubusercontent.com/OTVGroup/OTVGroup.com.vn/main/Background%20-%20OTISMusicStudio.jpg"
            alt="Poster-OTVGroup"
            class="heading-img"
          />
          <div class="heading1">
            <a><b>OTIS Music Studio</b> - Nghệ Thuật Là Linh Hồn Cuộc Sống!</a>
            <div
              style="
                width: 100%;
                height: 2px;
                margin: 5px auto;
                background-color: #000000;
              "
            ></div>
            <strong>
              A dynamic brand specializing in the creation and distribution of
              music videos-with a strong focus on quality, artistic vision, and
              global engagement.
            </strong>
          </div>
          <div class="heading2">
            <div class="social">
              <img src="https://img.icons8.com/color/20/facebook-new.png" />
              <a
                href="https://www.facebook.com/OTISMusicStudio"
                target="_blank"
              >
                OTIS Music Studio
              </a>
            </div>
            <div class="social">
              <img src="https://img.icons8.com/color/20/youtube-play.png" />
              <a
                href="https://www.youtube.com/@otismusicstudiovn"
                target="_blank"
              >
                OTIS Music Studio
              </a>
            </div>
          </div>
        </div>

        <!-- Ngăn 4: OTISSHOP -->
        <div class="heading">
          <img
            src="https://raw.githubusercontent.com/OTVGroup/OTVGroup.com.vn/main/Background%20-%20OTISShop.jpeg"
            alt="Poster-OTISShop"
            class="heading-img"
          />
          <div class="heading1">
            <a><b>OTISShop</b> - Chất Lượng, Uy Tín, Tin Cậy.</a>
            <div
              style="
                width: 100%;
                height: 2px;
                margin: 5px auto;
                background-color: #000000;
              "
            ></div>
            <strong>
              A digital commerce brand offering content-linked products and
              experiences-connecting users with digital services and assets,
              with quality as its top priority.
            </strong>
          </div>
          <div class="heading2">
            <div class="social">
              <img src="https://img.icons8.com/color/20/facebook-new.png" />
              <a href="https://www.facebook.com/OtisSeller" target="_blank">
                OTISShop
              </a>
            </div>
            <div class="social">
              <img src="https://img.icons8.com/color/20/instagram-new.png" />
              <a href="https://www.instagram.com/otisshopvn" target="_blank">
                OTISShop
              </a>
            </div>
            <div class="social">
              <img src="https://img.icons8.com/color/20/tiktok--v1.png" />
              <a href="https://www.tiktok.com/@otisshop" target="_blank">
                OTISShop
              </a>
            </div>
            <div class="social">
              <img
                src="https://img.icons8.com/ios-filled/20/000000/threads.png"
              />
              <a href="https://www.threads.net/@otisshopvn" target="_blank">
                OTISShop
              </a>
            </div>
          </div>
        </div>

        <!-- Ngăn 5: OTISSTORE -->
        <div class="heading">
          <img
            src="https://raw.githubusercontent.com/OTVGroup/OTVGroup.com.vn/main/Background%20-%20OTISStore.jpeg"
            alt="Poster-OTISStore"
            class="heading-img"
          />
          <div class="heading1">
            <a><b>OTISStore</b> - Uy Tín Tạo Nên Thương Hiệu!</a>
            <div
              style="
                width: 100%;
                height: 2px;
                margin: 5px auto;
                background-color: #000000;
              "
            ></div>
            <strong>
              An entertainment brand that engages users through content and
              products focused on gaming, virtual experiences, and interactive
              entertainment-with extensive reach.
            </strong>
          </div>
          <div class="heading2">
            <div class="social">
              <img src="https://img.icons8.com/color/20/facebook-new.png" />
              <a href="https://www.facebook.com/OtisGamerVN" target="_blank">
                OTISStore
              </a>
            </div>

            <div class="social">
              <img src="https://img.icons8.com/color/20/youtube-play.png" />
              <a href="https://www.youtube.com/@otisstorevn" target="_blank">
                OTISSTORE
              </a>
            </div>
          </div>
        </div>
      </section>

      <!-- Footer -->
      <section id="footer">
        <div
          style="
            max-width: 1240px;
            margin: auto;
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            justify-content: center;
          "
        >
          <div
            style="
              max-width: 400px;
              margin: auto;
              padding: 0 10px;
              text-align: center;
            "
          >
            <h3 style="margin: 15px auto">Chăm Sóc Khách Hàng</h3>

            <div
              style="
                display: flex;
                flex-wrap: wrap;
                justify-content: center;
                gap: 10px;
              "
            >
              <div
                style="flex: 1 1 30%; max-width: 80px; aspect-ratio: 80 / 132"
              >
                <a href="https://www.messenger.com/t/OtisVo586" target="_blank">
                  <img
                    src="https://i.pinimg.com/736x/c6/75/4f/c6754f858018877052f6b25bb2918b83.jpg"
                    alt="Facebook"
                    style="width: 100%; border-radius: 50%"
                  />
                </a>
              </div>

              <div
                style="flex: 1 1 30%; max-width: 80px; aspect-ratio: 80 / 132"
              >
                <a href="https://zalo.me/0329022431" target="_blank">
                  <img
                    src="https://i.pinimg.com/736x/e2/82/50/e28250e82662b0c5f4b137d910bd9bf5.jpg"
                    alt="Zalo"
                    style="width: 100%; border-radius: 50%"
                  />
                </a>
              </div>

              <div
                style="flex: 1 1 30%; max-width: 80px; aspect-ratio: 80 / 132"
              >
                <a href="tel:0329022431" target="_blank">
                  <img
                    src="https://i.pinimg.com/736x/b1/9e/57/b19e5724574d749b152488fd7528c2dc.jpg"
                    alt="Hotline"
                    style="width: 100%; border-radius: 50%"
                  />
                </a>
              </div>

              <div
                style="flex: 1 1 30%; max-width: 80px; aspect-ratio: 80 / 132"
              >
                <a href="mailto:thinhkvtm2006@gmail.com" target="_blank">
                  <img
                    src="https://i.pinimg.com/736x/96/4d/94/964d94ca6c98f9e3464060c31b220360.jpg"
                    alt="Gmail"
                    style="width: 100%; border-radius: 50%"
                  />
                </a>
              </div>
            </div>
          </div>

          <div
            style="
              max-width: 400px;
              margin: auto;
              padding: 0 10px;
              text-align: center;
            "
          >
            <h3 style="margin: 15px auto">Cổng Thanh Toán</h3>

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
                  style="width: 100%; border-radius: 5%"
                />
              </div>

              <div style="flex: 1 1 30%; max-width: 110px">
                <img
                  src="https://i.pinimg.com/736x/27/17/68/271768775d063a13b76b78bfb4b4befe.jpg"
                  alt="Donate MoMo"
                  style="width: 100%; border-radius: 5%"
                />
              </div>

              <div style="flex: 1 1 30%; max-width: 110px">
                <img
                  src="https://i.pinimg.com/736x/15/81/ed/1581edcd2b862a72f316ce2b84cc0e15.jpg"
                  alt="Donate Zalopay"
                  style="width: 100%; border-radius: 5%"
                />
              </div>
            </div>
          </div>
        </div>

        <!-- Keyword SEO -->
        <div
          style="
            max-width: 1240px;
            margin: 0 auto;
            padding: 0 10px;
            text-align: center;
            font-size: 14px;
            line-height: 1.5;
            color: #bbb;
          "
        >
          <strong>Mọi người cũng tìm kiếm:</strong><br />
          OTVGroup | Otis Võ | OTISShop | OTISStore | Đa Dạng Nội Dung | Kinh
          Doanh Sáng Tạo | Giải Trí Đa Nền Tảng | Dẫn Đầu Xu Hướng | Trải Nghiệm
          Cuộc Sống | Học Cách Yêu Thương | Học Cách Khởi Nghiệp | Phát Triển
          Bản Thân | Động Lực Sống | Giữ Lửa Đam Mê | Học Để Thành Công | Truyền
          Cảm Hứng | Đổi Mới Tư Duy | Sáng Tạo Nội Dung | Giá Trị Cuộc Sống
        </div>

        <!-- Info Legal -->
        <div
          style="
            max-width: 1240px;
            margin: 0 auto;
            display: flex;
            flex-wrap: wrap;
            gap: 3px;
            line-height: 1;
            padding: 0 10px;
            text-align: center;
            justify-content: center;
            font-size: 13px;
            color: #888;
          "
        >
          <strong>© 2024 - Công Ty TNHH MTV OTVGroup</strong>
          <strong>
            • Địa chỉ:
            <a
              href="https://maps.app.goo.gl/au8jubbPqSTZ8FjP7"
              style="color: #007aff; text-decoration: none"
              target="_blank"
            >
              P.Tân Chánh Hiệp, Q.12, TP. Hồ Chí Minh
            </a>
          </strong>
          <strong>
            • Hotline:
            <a
              href="tel:0329022431"
              style="color: #007aff; text-decoration: none"
              target="_blank"
            >
              0329 022 431
            </a>
            • Email:
            <a
              href="mailto:thinhkvtm2006@gmail.com"
              style="color: #007aff; text-decoration: none"
              target="_blank"
            >
              thinhkvtm2006@gmail.com
            </a>
          </strong>
          <strong>
            • Chịu trách nhiệm kỹ thuật:
            <a
              href="https://www.facebook.com/OtisVo586/"
              style="color: #007aff; text-decoration: none"
              target="_blank"
            >
              Otis Võ
            </a>
          </strong>
        </div>
      </section>
    </div>

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
          <h3 style="font-size: 13px; margin-top: 5px;">${item.title}</h3>
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

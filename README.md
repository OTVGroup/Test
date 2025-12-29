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
        height: 100%;
        display: flex;
        flex-direction: column;
        align-items: center;
        background: #1e1e1e;
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

      .post .p-1,
      .post .p-2 {
        width: calc(100% / 3 - 2px);
        height: min-content;
        min-width: 300px;
        margin: 0;
        padding: 0;
        display: flex;
        align-items: center; /* Căn giữa theo chiều dọc */
        align-content: center;
        justify-content: center; /* Căn giữa theo chiều ngang */
        justify-items: center;
        position: relative;
        border: 1px solid #000;
        flex-direction: column; /* Nếu bạn có nhiều post, vẫn xếp theo dòng */
      }

      .post .p-1 iframe {
        width: 100%; /* Chiều rộng đầy div */
        aspect-ratio: 16/9;
        border: none;
      }

      .post .p-header {
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

      .post .p-content {
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

      .post .p-bottom {
        width: 100%;
        display: flex;
        flex-direction: row;
        justify-content: center;
        gap: 2%;
      }

      .post .p-bottom .p-infor,
      .post .p-bottom .p-btn {
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

      .post .p-bottom .p-btn:hover a {
        color: #000;
      }

      @media (max-width: 990px) {
        .post .p-1 {
          width: calc(100% / 2 - 2px);
        }

        .post .p-2 {
          width: calc(100% - 2px);
        }
      }

      @media (max-width: 660px) {
        .post .p-1,
        .post .p-2 {
          width: calc(100% - 2px);
        }
      }

      .footer {
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

      .footer .f-left,
      .footer .f-center,
      .footer .f-right {
        width: calc(100% / 3);
        height: min-content;
        min-width: 300px;
        margin: 0 auto;
        display: flex;
        align-items: center;
        align-content: center;
        justify-content: center;
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
        justify-content: center;
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
        align-items: center;
        align-content: center;
        justify-content: center;
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
      <!-- Form Bottom -->
      <div class="bottom">
        <!-- NEWS -->
        <section class="s-news active">
          <div class="post">
            <div class="p-header" style="--font-size: 18px">GROUP FACEBOOK</div>
            <div class="p-2" style="background: #daf3ffdd">
              <img
                src="https://scontent.fsgn5-14.fna.fbcdn.net/v/t39.30808-6/468426620_122122770164552182_2194104395195010555_n.jpg?_nc_cat=101&ccb=1-7&_nc_sid=2285d6&_nc_eui2=AeFpOB3VIGTT4g_qysqdEcSiKYy0lgannDYpjLSWBqecNkO2NVfb_lcSm6Bs-dYOCy5koTp3ax8x-6cq6EOlYKSD&_nc_ohc=S9hlq0vaxdYQ7kNvwES5iYW&_nc_oc=AdmWSFaPrPEZilHH_z4SYod0nonHbRTpNdhJ_br7wXEn8D68jNpJrX0Kdpz4WP5NXyE&_nc_zt=23&_nc_ht=scontent.fsgn5-14.fna&_nc_gid=Rdaf6jsLOVUcZToF_omH6Q&oh=00_Afn6d7VW44ATevy2kkEqt0Lq4d7E0FIucchuWEXcwfkhTw&oe=6957C30B"
                alt="Facebook Group-1"
                style="width: 100%; aspect-ratio: 5/2"
              />
              <div
                class="p-header"
                style="align-items: center; --font-size: 15px"
              >
                GÓC NHỎ
              </div>
              <div class="p-content" id="box-1">
                Góc Nhỏ - nơi mỗi câu chuyện, mỗi chia sẻ đều được lắng nghe.
                Nơi chúng ta cùng nhau trò chuyện, học hỏi, và gắn kết. Dù bạn
                đến để tâm sự, tìm cảm hứng hay đơn giản chỉ để ghé thăm, ở đây
                luôn có một chỗ dành cho bạn.
              </div>
              <i
                style="
                  color: #1877f2;
                  width: 100%;
                  padding: 0 10px;
                  display: flex;
                  justify-content: right;
                "
                onclick="changeHeight('box-1', this)"
              >
                ...Xem thêm
              </i>
              <div class="p-bottom">
                <div class="p-infor" style="background: #55ad4d">
                  Thành Viên: <i>144</i>
                </div>
                <div class="p-btn" style="background: #1877f2">
                  <a
                    href="https://www.facebook.com/share/g/1QXWdsNv8d/"
                    target="_blank"
                  >
                    👉 Tham gia
                  </a>
                </div>
              </div>
            </div>
            <div class="p-1" style="background: #daf3ffdd">
              <img
                src="https://scontent.fsgn5-9.fna.fbcdn.net/v/t39.30808-6/588843585_122194789730552182_3801606182584356093_n.jpg?_nc_cat=105&ccb=1-7&_nc_sid=2285d6&_nc_eui2=AeET72wqB2PkWp5i-Eb2iazOICeMEY6D7rcgJ4wRjoPutwO6LcPdGjZxJL-7FQXHE-txqJ5_ssbteAiGICKqmFvy&_nc_ohc=bwvxe8HnjvkQ7kNvwGfXbqW&_nc_oc=Adns_rMQCbcy3r5ganyXlzQOjkrbKrRH3lW-YVzTqe0GMN9Lvui93F_imMGbreqC5nk&_nc_zt=23&_nc_ht=scontent.fsgn5-9.fna&_nc_gid=ipZ87KIAmDn253sSlTWzMg&oh=00_AflhSREcArHCyFb3WAsvEvpkqRibpAe3mqmQ38pvabm_1g&oe=6957F3EE"
                alt="Facebook Group-1"
                style="width: 100%; aspect-ratio: 5/2"
              />
              <div
                class="p-header"
                style="align-items: center; --font-size: 15px"
              >
                THƯ VIỆN CẢM XÚC
              </div>
              <div class="p-content" id="box-2">
                Thư Viện Cảm Xúc - nơi mọi tâm tư, suy nghĩ, và cảm xúc đều được
                trân trọng. Nơi để bạn chia sẻ những câu chuyện vui, nỗi buồn,
                những khoảnh khắc nhỏ trong cuộc sống, hoặc đơn giản là tìm một
                không gian để lắng nghe và được lắng nghe.
              </div>
              <i
                style="
                  color: #1877f2;
                  width: 100%;
                  padding: 0 10px;
                  display: flex;
                  justify-content: right;
                "
                onclick="changeHeight('box-2', this)"
              >
                ...Xem thêm
              </i>
              <div class="p-bottom">
                <div class="p-infor" style="background: #55ad4d">
                  Thành Viên: <i>120</i>
                </div>
                <div class="p-btn" style="background: #1877f2">
                  <a
                    href="https://www.facebook.com/share/g/1ALyzrv8bd/"
                    target="_blank"
                  >
                    👉 Tham gia
                  </a>
                </div>
              </div>
            </div>
            <div class="p-1" style="background: #daf3ffdd">
              <img
                src="https://scontent.fsgn5-10.fna.fbcdn.net/v/t39.30808-6/604517169_122194791110552182_1561466510739720352_n.webp?stp=dst-jpg_tt6&_nc_cat=110&ccb=1-7&_nc_sid=2285d6&_nc_eui2=AeECUNinpN2JCsmcfKo5N-uFd2TGhEt5aiF3ZMaES3lqIcoBz3-ti_HX7e3LcZ2MEwrYId0p9kLLuA4gAW2ov36E&_nc_ohc=1b83OYf-hqAQ7kNvwGdtsNU&_nc_oc=AdlcGOssn0D1_bIeJ8DmkjIDSIMWYiFF9oCWzrX6y3nZq-7eqguskc4Jpph5CK8YFzA&_nc_zt=23&_nc_ht=scontent.fsgn5-10.fna&_nc_gid=BdoxFdiz-5WpbxYk60wkNQ&oh=00_AfnhO86UD8Ni0smAWJL4QPtuLej7KB3qSyb-4BpSohyMnw&oe=6957C9DE"
                alt="Facebook Group-1"
                style="width: 100%; aspect-ratio: 5/2"
              />
              <div
                class="p-header"
                style="align-items: center; --font-size: 15px"
              >
                TÂM THƯ GỬI NGƯỜI
              </div>
              <div class="p-content" id="box-3">
                Tâm Thư Gửi Người - nơi mọi tâm tư, nỗi niềm và cảm xúc đều được
                gửi gắm và trân trọng. Nơi những lá thư chưa từng gửi đi, những
                câu chuyện đời thường, niềm vui giản đơn, thậm chí cả nỗi buồn
                hay những suy nghĩ sâu sắc về cuộc sống đều được lắng nghe và
                đồng cảm.
              </div>
              <i
                style="
                  color: #1877f2;
                  width: 100%;
                  padding: 0 10px;
                  display: flex;
                  justify-content: right;
                "
                onclick="changeHeight('box-3', this)"
              >
                ...Xem thêm
              </i>
              <div class="p-bottom">
                <div class="p-infor" style="background: #55ad4d">
                  Thành Viên: <i>122</i>
                </div>
                <div class="p-btn" style="background: #1877f2">
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
            <div class="p-header">YOUTUBE SHORTS</div>
            <!-- Các video sẽ tự động tạo div .p-1 và nhúng iframe ở đây -->
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
                  `<div class="p-1">
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
      </div>
    </div>
  </body>
</html>

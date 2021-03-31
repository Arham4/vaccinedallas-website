<template>
  <footer class="page-footer bg_color--3 pl--150 pr--150 pl_lg--30 pr_lg--30 pl_md--30 pr_md--30 pl_sm--5 pr_sm--5">
    <!-- Start Footer Top Area -->
    <div class="bk-footer-inner pt--150 pb--30 pt_sm--100">
      <div class="container">
        <div class="row">
          <div class="col-lg-5 col-sm-8">
            <div class="footer-widget text-var--2">
              <div class="logo">
                <n-link to="">
                  <img src="/img/logo/logo.png" alt="VaccineDallas logo">
                </n-link>
              </div>
              <div class="footer-inner">
                <p>
                  VaccineDallas is a drive-through COVID-19 vaccination provider. We provide Pfizer, Moderna, and
                  Johnson & Johnson COVID vaccines.
                </p>
              </div>
            </div>
          </div>

          <div class="col-lg-3 col-sm-8 mt_mobile--60">
            <div class="footer-widget text-var--2 menu--about">
              <h2 class="widgettitle">
                Links
              </h2>
              <div class="footer-menu">
                <ul class="ft-menu-list bk-hover">
                  <li>
                    <n-link to="#">
                      Manage Appointment
                    </n-link>
                  </li>
                  <li>
                    <n-link to="#">
                      Contact Us
                    </n-link>
                  </li>
                </ul>
              </div>
            </div>
          </div>

          <div class="col-lg-4 col-sm-8 mt_md--60 mt_sm--60">
            <div class="footer-widget text-var--2 menu--contact">
              <h2 class="widgettitle">
                Contact
              </h2>
              <div class="footer-address">
                <div class="bk-hover">
                  <p>7589 Preston Road, <br> Suite 500A, <br> Frisco, TX 75034</p>
                  <p>
                    <a href="mailto:info@vaccinedallas.com">info@vaccinedallas.com</a>
                  </p>
                  <!-- <p>
                    <a href="tel:4695794620">(469) 579-4620</a>
                  </p> -->
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Start Footer Top Area -->

    <!-- Start Copyright Area -->
    <div class="copyright ptb--50 text-var-2">
      <div class="container">
        <div class="row justify-content-end">
          <div class="col-md-6">
            <div class="copyright-right text-md-right text-center">
              <p>&copy; 2021 <b>VaccineDallas</b> Made with <i class="fa fa-heart text-danger" /> by <a href="https://hasthemes.com/"><b>HasThemes</b></a></p>
            </div>
            <div class="copyright-right text-md-right text-center">
              <p>
                <a href="https://www.freepik.com/vectors/health">Health</a>,
                <a href="https://www.freepik.com/vectors/doctor">Doctor</a>,
                <a href="https://www.freepik.com/vectors/baby">Baby</a>,
                & <a href="https://www.freepik.com/vectors/people">People</a>
                vectors created by <br> freepik & rawpixel.com - <a href="https://www.freepik.com/">www.freepik.com</a>
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- End Copyright Area -->
  </footer>
</template>

<script>
export default {
  data () {
    return {
      instagramPosts: [
        {
          id: 1,
          image: '/img/instagram/instagram-1.jpg',
          like: '1K',
          comment: '8'
        },
        {
          id: 2,
          image: '/img/instagram/instagram-2.jpg',
          like: '6K',
          comment: '9'
        },
        {
          id: 3,
          image: '/img/instagram/instagram-3.jpg',
          like: '3K',
          comment: '4'
        },
        {
          id: 4,
          image: '/img/instagram/instagram-4.jpg',
          like: '1K',
          comment: '3'
        },
        {
          id: 5,
          image: '/img/instagram/instagram-5.jpg',
          like: '2K',
          comment: '7'
        },
        {
          id: 6,
          image: '/img/instagram/instagram-6.jpg',
          like: '1K',
          comment: '8'
        }
      ]
    }
  }
}
</script>

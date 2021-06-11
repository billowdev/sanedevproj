<template>
        <nav class="navbar navbar-expand-md fixed-top navbar-dark bg-transaparent">
            <div class="container">
                <a class="navbar-brand" href="./">
                    <img src="assets/images/textlogo2.png" height="50px" alt="">
                </a>
                <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarContent" aria-controls="navbarContent" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse" id="navbarContent">
                    <ul class="navbar-nav ms-auto float-end ul-navbar">
                        <li class="nav-item px-3 px-md-0 active">
                            <a class="nav-link" href="./">SaneDev's blog</a>
                        </li>
                        <li class="nav-item px-3 px-md-0">
                            <a class="nav-link" href="register.html">สมัครสมาชิก</a>
                        </li>
                        <li class="nav-item px-3 px-md-0">
                            <a class="nav-link" href="login.html">เข้าสู่ระบบ</a>
                        </li>
    
                        <li class="nav-item dropdown">
                            <a class="nav-link dropdown-toggle" href="#" id="navebarDropdown" role="button" data-bs-toggle="dropdown" aria-haspopup="true" aria-expanded="false"> 
                                <img class="profile-img" src="assets/images/uploads/avatar.png" width="40px" height="40px" alt="avatar">
                                FirstName
                            </a>
                            <ul class="dropdown-menu dropdown-menu-right mb-3" aria-labelledby="navbarDropdown">
                                <li>
                                    <a class="dropdown-item" href="profile.html">
                                    <div class="d-flex align-items-center"> 
                                        <img class="profile-img" src="assets/images/uploads/avatar.png" width="40px" height="40px" alt="avatar">
                                        <div class="p-3 lh-sm">
                                            <span class="fw-bold">FirstName LastName</span><br>
                                            <small>ดูโปรไฟล์ของคุณ</small>
                                        </div>
                                    </div>
                                </a>
                            </li>
                                <li>
                                    <a class="dropdown-item" href="#">ออกจากระบบ</a></li>
                            </ul>
                        </li>
                    </ul>
                </div>
            </div>
              
            <div class="progressContainer">
                 <div class="progressBar"></div>
            </div>

          </nav>
</template>
 
<script>
module.exports = {
    mounted() {
         window.addEventListener('scroll', function(){
            let wintop = this.scrollY
            let navbar = document.querySelector(".navbar")

            let winheight = this.innerHeight
            let docheight = document.querySelector("body").offsetHeight
            let totalScroll = ( wintop / (docheight - winheight) ) * 100

            let bar = document.querySelector(".progressBar")
            bar.style.width = `${totalScroll}%`

            // navbar-light bg-light
            // navbar-dark bg-transaparent
            if (wintop > 150) {
                navbar.classList.remove("navbar-dark", "bg-transaparent")
                navbar.classList.add("navbar-light", "bg-light")
            }else {
                navbar.classList.remove("navbar-light", "bg-light")
                navbar.classList.add("navbar-dark", "bg-transaparent")
            }
        })
    }
}

/**
 * mounted() ในเหตุการณ์นี้ จะเกิดขึ้นเมื่อ DOM ถูกสร้างเสร็จแล้ว เราสามารถเข้าถึง Element ต่างๆ ใน DOM ได้ทั้งหมด
 */


</script>
 
<style scoped>

</style>
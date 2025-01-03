<template>
    <div>
        <nav class="navbar navbar-expand-lg bg-primary bg-body-tertiary">
            <div class="container-fluid">
                <div class="row ms-5">
                    <div class="col-3"><img src="../assets/smk.png" alt="" style="height:100px;"></div>
                    <div class="col">
                        <h5>SMKN 4 TASIKMALAYA</h5>
                        <h6>
                            JL.Depok Kel. Sukamenak Kec.purbaratuKota Kota.Tasikmalaya
                        </h6>
                    </div>
                </div>

                <button class="navbar-toggler " type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                    aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                    <span class="navbar-toggler-icon"></span>
                </button>
                <div class="collapse navbar-collapse ms-5 ps-5" id="navbarNav">
                    <ul class="navbar-nav">
                        <li class="nav-item">
                            <nuxt-link class="nav-link" to="/"> HOME</nuxt-link>
                        </li>
                        <li class="nav-item">
                            <nuxt-link class="nav-link" to="/propil"> PROFIL</nuxt-link>
                        </li>
                        <li class="nav-item">
                            <nuxt-link class="nav-link" to="/eskul"> ESKUL</nuxt-link>
                        </li>
                        <li class="nav-item">
                            <nuxt-link class="nav-link" to="/galeri"> GALERI</nuxt-link>
                        </li>
                        <li class="nav-item">
                            <nuxt-link class="nav-link" to="/pemilik"> PEMILIK</nuxt-link>
                        </li>
                    </ul>
                </div>
            </div>
        </nav>
    </div>
</template>
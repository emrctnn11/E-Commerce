<template>
    <div class="footer bg-secondary text-white pt-5 pb-4">
        <div class="container text-center text-md-left">
            <div class="row text-center text-md-left">
                <div class="col-md-3 col-lg-3 col-xl-3 mx-auto mt-3">
                    <h5 class="text-uppercase mb-4 font-weight-bold text-danger">Akıllı Ticaret</h5>
                    <p>Herhangi bir bilgi yazılabilecek alan.</p>
                </div>
                <div class="col-md-2 col-lg-2 col-xl-2 mx-auto mt-3">
                    <h5 class="text-uppercase mb-4 font-weight-bold text-danger">Ürünler</h5>
                    <p>
                        <a href="#" class="text-white" style="text-decoration: none;">Prov</a>
                    </p>
                    <p>
                        <a href="#" class="text-white" style="text-decoration: none;">Prov2</a>
                    </p>
                    <p>
                        <a href="#" class="text-white" style="text-decoration: none;">Prov3</a>
                    </p>
                    <p>
                        <a href="#" class="text-white" style="text-decoration: none;">Prov4</a>
                    </p>
                </div>
                <div class="col-md-3 col-lg-2 col-xl-2 mx-auto mt-3">
                    <h5 class="text-uppercase mb-4 font-weight-bold text-danger">Bağlantılar</h5>
                        <p>
                            <a href="#" class="text-white" style="text-decoration: none;">Prov5</a>
                        </p>
                        <p>
                            <a href="#" class="text-white" style="text-decoration: none;">Prov6</a>
                        </p>
                        <p>
                            <a href="#" class="text-white" style="text-decoration: none;">Prov7</a>
                        </p>
                        <p>
                            <a href="#" class="text-white" style="text-decoration: none;">Prov8</a>
                        </p>
                </div>
                <div class="col-md-4 col-lg-3 col-xl-3 mx-auto mt-3">
                    <h5 class="text-uppercase mb-4 font-weight-bold text-danger">İletişim</h5>
                    <p>
                        <i class="fa fa-home mr-3"></i> Adres yazım alanı.
                    </p>
                    <p>
                        <i class="fa fa-envelope mr-3"></i> mail@mail.com
                    </p>
                    <p>
                        <i class="fa fa-phone mr-3"></i> +90 511 111 11111
                    </p>
                </div>
            </div>

            <hr class="mb-4">

            <div class="row align-items-center">
                <div class="col-md-7 col-lg-8">
                    <p>Copyright
                        <a href="#" style="text-decoration: none;">
                            <strong class="text-danger"> Tüm haklar saklıdır.</strong>
                        </a>
                    </p>
                </div>
                <div class="col-md-5 col-lg-4">
                    <div class="text-center text-md-right">
                        <ul class="list-unstyled list-inline">
                            <li class="list-inline-item">
                                <a href="#" class="btn-floating btn-sm text-white" style="font-size: 23px;">
                                    <i class="fa fa-facebook"></i>
                                </a>
                            </li>
                            <li class="list-inline-item">
                                <a href="#" class="btn-floating btn-sm text-white" style="font-size: 23px;">
                                    <i class="fa fa-instagram"></i>
                                </a>
                            </li>
                            <li class="list-inline-item">
                                <a href="#" class="btn-floating btn-sm text-white" style="font-size: 23px;">
                                    <i class="fa fa-whatsapp"></i>
                                </a>
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>

export default {
    name: "FooterBar",

    data() {
        return {
            items:[]
        };
    }
};

</script>

<style scoped>
.footer {
    position: absolute;
    bottom: 0px;
    width: 100%;
}

@media only screen and (max-width : 560px) {
	body {min-height:initial}
	.footer {
		min-height: calc(100vh - 11em - 55px);
        position: relative;
	}
}
</style>
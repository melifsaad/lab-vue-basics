<template>
    <div class="footerSection">
        <div class="containerFooter">
            <div class="footerContent">
                <div class="adressFooter">Calle 122 N 11 D 71 Bogotá</div>
            </div>
            <div class="footerLinks">
                <a href="" class="footer-link">Equipo</a>
                <a href="" class="footer-link">Contacto</a>
                <a href="" class="footer-link">Politicas de privacidad</a>
            </div>
        </div>
    </div>

</template>
<script setup>
</script>
<style scoped>
.footerSection {
    margin-left: 20px;
    margin-right: 20px;
    padding-bottom: 100px;
}

.containerFooter {
    display: flex;
    justify-content: space-between;
}

.footerContent {
    display: flex;
    flex-direction: column;
    width: 260px;
}

.adressFooter {
    color: #6B708D;
    font-weight: normal;
    font-size: 14px;
    line-height: 150%;
}

.footerLinks {
    display: grid;
    grid-auto-columns: 1fr;
    grid-column-gap: 16px;
    grid-row-gap: 16px;
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: auto;
}

.footer-link {
    margin: 0%;
    color: brown;
    font-size: 17px;
}
</style>
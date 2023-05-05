<script>
</script>

<template>
    <div class="card">
        <div class="pic">
            <img src="https://picsum.photos/300/?random=10">
        </div>
        <div class="card-header">
            number 1
        </div>
        <div class="card-body">
            <h3 class="title">
                Special title treatment
            </h3>
        </div>
        <div class="card-footer">
            <p class="text">
                This is a wider card with supporting text below as a natural lead-in to additional content. This content is
                a little bit longer.
            </p>
        </div>
    </div>
</template>

<style lang="scss" scoped>
// css樣式寫在這裡
.card {
    background-color: #ffffff;
    border-radius: 3px;
    border: 1px solid #a1a1a1;
    padding: 20px;
    width: 17vw;
}

.card .pic img {
    width: 100%;
}

.card .card-header {
    border-bottom: none;
    background-color: transparent;
}

.card .title {
    color: #444444;
}

.card .text {
    color: #444444;
}

.card-footer {
    border-top: none !important;
    background-color: transparent !important;
}
</style>
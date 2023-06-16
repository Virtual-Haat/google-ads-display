<script>

</script>

<template>
  <div> 
    <div class="conten-wrapper">
        <section class="left-side">
            <div class="left-side__header-section">
                <h3 class="left-side__header">Search Ad</h3>
                <span class="">Downward Chevron</span>
            </div>

            <div class="left-side__form-section">
                <form>
                    <label for="searchQuery">Search Query</label>
                    <input type="text" id="searchQuery">
                </form>
            </div>

        </section>

        <section class="right-side">
            <div class="right-side__header-section">
                <h3 class="right-side__header">Google</h3>
                <div class="search-bar">
                    <input type="text">
                    <span class="">Search Icon</span>
                </div>
            </div>
        </section>

    </div>

  </div>

</template>

<style scoped>

* {
    margin: 0;
}

.conten-wrapper {
    display: flex;

}

.left-side {
    border-right: 1px solid #7c7c7c24;
    /* padding: 50px; */
}

.left-side__header-section {
    padding: 50px;
}

.left-side__header {
    font-size: 20px;
    font-weight: 600;
}

</style>

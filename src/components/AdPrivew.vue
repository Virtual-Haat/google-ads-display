<script>

export default {
    data() {

        return {
            message: "",
        }

    }
}


</script>

<template>
    <div>
        <div class="content-wrapper">
            <section class="left-side">
                <div class="left-side__heading">
                    <div class="left-side__header-section g__headerSection">
                        <h3 class="left-side__header g__header">Search Query</h3>
                        <span class="left-side__arrow g__leftSide-arrow"><i class="arrow down"></i></span>
                    </div>

                    <div class="left-side__querysearch g__querySearch-section">
                        <div class="querysearch__header g__searchHeader">
                            <label for="searchQuery">Search Query</label>
                            <span class="message-counter">{{ 30 - message.length }}</span>

                        </div>

                        <input type="text" id="searchQuery" class="g__searchQuery__input" placeholder="Search Query"
                            v-model="message" name="" maxlength="30" cols="30" rows="10">

                    </div>
                </div>

                <div class="queryAd-details">
                    <div class="queryAd__heading g__headerSection">
                        <h3 class="queryAd__header g__header">Search Ad</h3>
                        <span class="queryAd__arrow g__leftSide-arrow"><i class="arrow down"></i></span>
                    </div>

                    
                    <div class="queryAd__headlineOne g__querySearch-section">
                        <div class="queryAd__headlineOne--header g__searchHeader">
                            <label for="headlineOne">Headline One</label>
                            <span class="message-counter">{{ 30 - message.length }}</span>

                        </div>

                        <input type="text" id="headlineOne" class="headlineOne__input g__searchQuery__input" placeholder="Headline One"
                            v-model="message" name="" maxlength="30" cols="30" rows="10">

                    </div>

                    <div class="queryAd__headlineTwo g__querySearch-section">
                        <div class="queryAd__headlineTwo--header g__searchHeader">
                            <label for="headlineTwo">Headline Two</label>
                            <span class="message-counter">{{ 30 - message.length }}</span>

                        </div>

                        <input type="text" id="headlineTwo" class="headlineTwo__input g__searchQuery__input" placeholder="Headline Two"
                            v-model="message" name="" maxlength="30" cols="30" rows="10">

                    </div>

                    <div class="queryAd__headlineThree g__querySearch-section">
                        <div class="queryAd__headlineThree--header g__searchHeader">
                            <label for="headlineThree">Headline Three</label>
                            <span class="message-counter">{{ 30 - message.length }}</span>

                        </div>

                        <input type="text" id="headlineThree" class="headlineThree__input g__searchQuery__input" placeholder="Headline Three"
                            v-model="message" name="" maxlength="30" cols="30" rows="10">

                    </div>

                </div>




            </section>

            <section class="right-side">
                <div class="right-side__header-section">
                    <h3 class="right-side__header">Google</h3>
                    <div class="search-bar">
                        <input type="text">
                        <span class="">Search Icon</span>
                        <p>Hello!</p>
                    </div>
                </div>
            </section>

        </div>

    </div>
</template>

<style src="../assets/style/AdPreview.css"></style>

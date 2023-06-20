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

                        <input type="text" id="headlineOne" class="headlineOne__input g__searchQuery__input"
                            placeholder="Headline One" v-model="message" name="" maxlength="30" cols="30" rows="10">

                    </div>

                    <div class="queryAd__headlineTwo g__querySearch-section">
                        <div class="queryAd__headlineTwo--header g__searchHeader">
                            <label for="headlineTwo">Headline Two</label>
                            <span class="message-counter">{{ 30 - message.length }}</span>

                        </div>

                        <input type="text" id="headlineTwo" class="headlineTwo__input g__searchQuery__input"
                            placeholder="Headline Two" v-model="message" name="" maxlength="30" cols="30" rows="10">

                    </div>

                    <div class="queryAd__headlineThree g__querySearch-section">
                        <div class="queryAd__headlineThree--header g__searchHeader">
                            <label for="headlineThree">Headline Three</label>
                            <span class="message-counter">{{ 30 - message.length }}</span>

                        </div>

                        <input type="text" id="headlineThree" class="headlineThree__input g__searchQuery__input"
                            placeholder="Headline Three" v-model="message" name="" maxlength="30" cols="30" rows="10">

                    </div>

                    <div class="queryAd__Displayurl g__querySearch-section">
                        <div class="queryAd__Displayurl--header g__searchHeader">
                            <label for="Displayurl">Display URL</label>
                            <span class="message-counter">{{ 60 - message.length }}</span>

                        </div>

                        <input type="text" id="Displayurl" class="Displayurl__input g__searchQuery__input"
                            placeholder="Display URL" v-model="message" name="" maxlength="60" cols="30" rows="10">

                    </div>

                    <div class="path">
                        <div class="queryAd__pathOne">
                            <div class="queryAd__pathOne--header g__searchHeader">
                                <label for="pathOne">Path One</label>
                                <span class="message-counter">{{ 15 - message.length }}</span>

                            </div>

                            <input type="text" id="pathOne" class="pathOne__input g__searchQuery__input"
                                placeholder="Path One" v-model="message" name="" maxlength="15" >

                        </div>

                        <div class="queryAd__pathTwo">
                            <div class="queryAd__pathTwo--header g__searchHeader">
                                <label for="pathTwo">Path Two</label>
                                <span class="message-counter">{{ 15 - message.length }}</span>

                            </div>

                            <input type="text" id="pathTwo" class="pathTwo__input g__searchQuery__input"
                                placeholder="Path Two" v-model="message" name="" maxlength="15">

                        </div>
                    </div>

                    <div class="queryAd__DescriptionOne g__querySearch-section">
                        <div class="queryAd__DescriptionOne--header g__searchHeader">
                            <label for="DescriptionOne">Description One</label>
                            <span class="message-counter">{{ 90 - message.length }}</span>

                        </div>

                        <textarea id="DescriptionOne" class="DescriptionOne__input g__searchQuery__input"
                            placeholder="Description One" v-model="message" name="" maxlength="90" cols="30" rows="5"></textarea>

                    </div>

                    <div class="queryAd__DescriptionTwo g__querySearch-section">
                        <div class="queryAd__DescriptionTwo--header g__searchHeader">
                            <label for="DescriptionTwo">Description Two</label>
                            <span class="message-counter">{{ 90 - message.length }}</span>

                        </div>

                        <textarea id="DescriptionTwo" class="DescriptionTwo__input g__searchQuery__input"
                            placeholder="Description Two" v-model="message" name="" maxlength="90" cols="30" rows="5"></textarea>

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

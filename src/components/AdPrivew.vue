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

                    <div class="left-side__querysearch g__querySearch-section g_sectionDesign">
                        <div class="querysearch__header g__searchHeader">
                            <label for="searchQuery">Search Query</label>
                            <span class="message-counter">{{ 30 - message.length }}</span>

                        </div>

                        <input type="text" id="searchQuery" class="g__searchQuery__input" placeholder="Search Query"
                            v-model="message" name="" maxlength="30" cols="30" rows="10">

                    </div>
                </div>

                <div class="queryAd-details g_sectionDesign">
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
                                placeholder="Path One" v-model="message" name="" maxlength="15">

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
                            placeholder="Description One" v-model="message" name="" maxlength="90" cols="30"
                            rows="5"></textarea>

                    </div>

                    <div class="queryAd__DescriptionTwo g__querySearch-section">
                        <div class="queryAd__DescriptionTwo--header g__searchHeader">
                            <label for="DescriptionTwo">Description Two</label>
                            <span class="message-counter">{{ 90 - message.length }}</span>

                        </div>

                        <textarea id="DescriptionTwo" class="DescriptionTwo__input g__searchQuery__input"
                            placeholder="Description Two" v-model="message" name="" maxlength="90" cols="30"
                            rows="5"></textarea>

                    </div>

                </div>

                <div class="structured-snippets g_sectionDesign">
                    <div class="structured-snippets g__headerSection">
                        <h3 class="structured-snippets__header g__header">Structured Snippets</h3>
                        <span class="structured-snippets__arrow g__leftSide-arrow"><i class="arrow down"></i></span>
                    </div>


                    <div class="snippetHeading g__querySearch-section">
                        <div class="snippetHeader--header g__searchHeader">
                            <label for="snippetHeader">Snippet Header</label>

                        </div>

                        <div class="selectbox">
                            <select name="snippetHeader__selectbox" id="snippetHeader">
                                <option disabled selected value="">Select</option>
                                <option value="brands">Brands</option>
                                <option value="amenities">Amenities</option>
                                <option value="styles">Styles</option>
                                <option value="types">Types</option>
                                <option value="destinations">Destinations</option>
                                <option value="services">Services</option>
                                <option value="courses">Courses</option>
                                <option value="neighbourshoods">Neighbourshoods</option>
                                <option value="shows">Shows</option>
                                <option value="insurance coverage">Insurance Coverage</option>
                                <option value="degree programs">Degree Programs</option>
                                <option value="featured hotels">Featured Hotels</option>
                                <option value="models">Models</option>
                            </select>
                        </div>



                        <!-- <input type="text" id="snippetHeader" class="snippetHeader__input g__searchQuery__input"
                            placeholder="snippetHeader" v-model="message" name="" maxlength="30" cols="30" rows="10"> -->

                    </div>

                    <div class="snippetOne g__querySearch-section">
                        <div class="snippetOne--header g__searchHeader">
                            <label for="snippetOne">Snippet One</label>
                            <span class="message-counter">{{ 25 - message.length }}</span>

                        </div>

                        <input type="text" id="snippetOne" class="snippetOne__input g__searchQuery__input"
                            placeholder="Snippet One" v-model="message" name="" maxlength="25" cols="30" rows="10">

                    </div>

                    <div class="snippetTwo g__querySearch-section">
                        <div class="snippetTwo--header g__searchHeader">
                            <label for="snippetTwo">Snippet Two</label>
                            <span class="message-counter">{{ 25 - message.length }}</span>

                        </div>

                        <input type="text" id="snippetTwo" class="snippetTwo__input g__searchQuery__input"
                            placeholder="Snippet Two" v-model="message" name="" maxlength="25" cols="30" rows="10">

                    </div>

                    <div class="snippetThree g__querySearch-section">
                        <div class="snippetThree--header g__searchHeader">
                            <label for="snippetThree">Snippet Three</label>
                            <span class="message-counter">{{ 25 - message.length }}</span>

                        </div>

                        <input type="text" id="snippetThree" class="snippetThree__input g__searchQuery__input"
                            placeholder="Snippet Three" v-model="message" name="" maxlength="25" cols="30" rows="10">

                    </div>

                    <div class="snippetFour g__querySearch-section">
                        <div class="snippetFour--header g__searchHeader">
                            <label for="snippetFour">Snippet Four</label>
                            <span class="message-counter">{{ 25 - message.length }}</span>

                        </div>

                        <input type="text" id="snippetFour" class="snippetFour__input g__searchQuery__input"
                            placeholder="Snippet Four" v-model="message" name="" maxlength="25" cols="30" rows="10">

                    </div>

                    <div class="snippetFive g__querySearch-section">
                        <div class="snippetFive--header g__searchHeader">
                            <label for="snippetFive">Snippet Five</label>
                            <span class="message-counter">{{ 25 - message.length }}</span>

                        </div>

                        <input type="text" id="snippetFive" class="snippetFive__input g__searchQuery__input"
                            placeholder="Snippet Five" v-model="message" name="" maxlength="25" cols="30" rows="10">

                    </div>



                </div>

                <div class="calloutExtensions g_sectionDesign">
                    <div class="calloutExtensions__heading g__headerSection">
                        <h3 class="calloutExtensions__header g__header">Callout Extensions</h3>
                        <span class="calloutExtensions__arrow g__leftSide-arrow"><i class="arrow down"></i></span>
                    </div>

                    
                    <div class="calloutOne g__querySearch-section">
                        <div class="calloutOne--header g__searchHeader">
                            <label for="calloutOne">Callout One</label>
                            <span class="message-counter">{{ 25 - message.length }}</span>

                        </div>

                        <input type="text" id="calloutOne" class="calloutOne__input g__searchQuery__input"
                            placeholder="Callout One" v-model="message" name="" maxlength="25" cols="30" rows="10">

                    </div>

                    <div class="calloutTwo g__querySearch-section">
                        <div class="calloutTwo--header g__searchHeader">
                            <label for="calloutTwo">Callout Two</label>
                            <span class="message-counter">{{ 25 - message.length }}</span>

                        </div>

                        <input type="text" id="calloutTwo" class="calloutTwo__input g__searchQuery__input"
                            placeholder="Callout Two" v-model="message" name="" maxlength="25" cols="30" rows="10">

                    </div>

                    <div class="calloutThree g__querySearch-section">
                        <div class="calloutThree--header g__searchHeader">
                            <label for="calloutThree">Callout Three</label>
                            <span class="message-counter">{{ 25 - message.length }}</span>

                        </div>

                        <input type="text" id="calloutThree" class="calloutThree__input g__searchQuery__input"
                            placeholder="Callout Three" v-model="message" name="" maxlength="25" cols="30" rows="10">

                    </div>

                    <div class="calloutFour g__querySearch-section">
                        <div class="calloutFour--header g__searchHeader">
                            <label for="calloutFour">Callout Four</label>
                            <span class="message-counter">{{ 25 - message.length }}</span>

                        </div>

                        <input type="text" id="calloutFour" class="calloutFour__input g__searchQuery__input"
                            placeholder="Callout Four" v-model="message" name="" maxlength="25" cols="30" rows="10">

                    </div>

                    <div class="calloutFive g__querySearch-section">
                        <div class="calloutFive--header g__searchHeader">
                            <label for="calloutFive">Callout Five</label>
                            <span class="message-counter">{{ 25 - message.length }}</span>

                        </div>

                        <input type="text" id="calloutFive" class="calloutFive__input g__searchQuery__input"
                            placeholder="Callout Five" v-model="message" name="" maxlength="25" cols="30" rows="10">

                    </div>




                </div>


                <div class="sitelinkExtensions g_sectionDesign">
                    <div class="sitelinkExtensions__heading g__headerSection">
                        <h3 class="sitelinkExtensions__header g__header">Sitelink Extensions</h3>
                        <span class="sitelinkExtensions__arrow g__leftSide-arrow"><i class="arrow down"></i></span>
                    </div>

                    
                    <div class="sitelinkOne g__querySearch-section">
                        <div class="sitelinkOne--header g__searchHeader">
                            <label for="sitelinkOne">Sitelink One</label>
                            <span class="message-counter">{{ 30 - message.length }}</span>

                        </div>

                        <input type="text" id="sitelinkOne" class="sitelinkOne__input g__searchQuery__input"
                            placeholder="Sitelink One" v-model="message" name="" maxlength="30" cols="30" rows="10">

                    </div>

                    <div class="sitelinkOne__firstLine g__querySearch-section">
                        <div class="sitelinkOne__firstLine--header g__searchHeader">
                            <label for="sitelinkOne__firstLine">Sitelink One (First Line)</label>
                            <span class="message-counter">{{ 35 - message.length }}</span>

                        </div>

                        <input type="text" id="sitelinkOne__firstLine" class="sitelinkOne__firstLine--input g__searchQuery__input"
                            placeholder="First Line Description" v-model="message" name="" maxlength="35" cols="30" rows="10">

                    </div>

                    <div class="sitelinkOne__secondLine g__querySearch-section">
                        <div class="sitelinkOne__secondLine--header g__searchHeader">
                            <label for="sitelinkOne__secondLine">Sitelink One (Second Line)</label>
                            <span class="message-counter">{{ 35 - message.length }}</span>

                        </div>

                        <input type="text" id="sitelinkOne__secondLine" class="sitelinkOne__secondLine--input g__searchQuery__input"
                            placeholder="Second Line Description" v-model="message" name="" maxlength="35" cols="30" rows="10">

                    </div>

                    <div class="sitelinktwo g__querySearch-section">
                        <div class="sitelinktwo--header g__searchHeader">
                            <label for="sitelinktwo">Sitelink two</label>
                            <span class="message-counter">{{ 30 - message.length }}</span>

                        </div>

                        <input type="text" id="sitelinktwo" class="sitelinktwo__input g__searchQuery__input"
                            placeholder="Sitelink two" v-model="message" name="" maxlength="30" cols="30" rows="10">

                    </div>

                    <div class="sitelinktwo__firstLine g__querySearch-section">
                        <div class="sitelinktwo__firstLine--header g__searchHeader">
                            <label for="sitelinktwo__firstLine">Sitelink Two (First Line)</label>
                            <span class="message-counter">{{ 35 - message.length }}</span>

                        </div>

                        <input type="text" id="sitelinktwo__firstLine" class="sitelinktwo__firstLine--input g__searchQuery__input"
                            placeholder="First Line Description" v-model="message" name="" maxlength="35" cols="30" rows="10">

                    </div>

                    <div class="sitelinktwo__secondLine g__querySearch-section">
                        <div class="sitelinktwo__secondLine--header g__searchHeader">
                            <label for="sitelinktwo__secondLine">Sitelink Two (Second Line)</label>
                            <span class="message-counter">{{ 35 - message.length }}</span>

                        </div>

                        <input type="text" id="sitelinktwo__secondLine" class="sitelinktwo__secondLine--input g__searchQuery__input"
                            placeholder="Second Line Description" v-model="message" name="" maxlength="35" cols="30" rows="10">

                    </div>

                    

                    <div class="calloutThree g__querySearch-section">
                        <div class="calloutThree--header g__searchHeader">
                            <label for="calloutThree">Callout Three</label>
                            <span class="message-counter">{{ 25 - message.length }}</span>

                        </div>

                        <input type="text" id="calloutThree" class="calloutThree__input g__searchQuery__input"
                            placeholder="Callout Three" v-model="message" name="" maxlength="25" cols="30" rows="10">

                    </div>

                    <div class="calloutFour g__querySearch-section">
                        <div class="calloutFour--header g__searchHeader">
                            <label for="calloutFour">Callout Four</label>
                            <span class="message-counter">{{ 25 - message.length }}</span>

                        </div>

                        <input type="text" id="calloutFour" class="calloutFour__input g__searchQuery__input"
                            placeholder="Callout Four" v-model="message" name="" maxlength="25" cols="30" rows="10">

                    </div>

                    <div class="calloutFive g__querySearch-section">
                        <div class="calloutFive--header g__searchHeader">
                            <label for="calloutFive">Callout Five</label>
                            <span class="message-counter">{{ 25 - message.length }}</span>

                        </div>

                        <input type="text" id="calloutFive" class="calloutFive__input g__searchQuery__input"
                            placeholder="Callout Five" v-model="message" name="" maxlength="25" cols="30" rows="10">

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

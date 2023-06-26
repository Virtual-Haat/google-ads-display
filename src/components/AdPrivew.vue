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
                            <span class="message-counter">{{ 30 - querysearch.length }}</span>

                        </div>

                        <input type="text" id="searchQuery" v-model="querysearch" class="g__searchQuery__input"
                            placeholder="Search Query" name="" maxlength="30" cols="30" rows="10">

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
                            <span class="message-counter">{{ 30 - headlineOne.length }}</span>

                        </div>

                        <input type="text" id="headlineOne" v-model="headlineOne"
                            class="headlineOne__input g__searchQuery__input" placeholder="Headline One" name=""
                            maxlength="30" cols="30" rows="10">

                    </div>

                    <div class="queryAd__headlineTwo g__querySearch-section">
                        <div class="queryAd__headlineTwo--header g__searchHeader">
                            <label for="headlineTwo">Headline Two</label>
                            <span class="message-counter">{{ 30 - headlineTwo.length }}</span>

                        </div>

                        <input type="text" id="headlineTwo" v-model="headlineTwo"
                            class="headlineTwo__input g__searchQuery__input" placeholder="Headline Two" name=""
                            maxlength="30" cols="30" rows="10">

                    </div>

                    <div class="queryAd__headlineThree g__querySearch-section">
                        <div class="queryAd__headlineThree--header g__searchHeader">
                            <label for="headlineThree">Headline Three</label>
                            <span class="message-counter">{{ 30 - headlineThree.length }}</span>

                        </div>

                        <input type="text" id="headlineThree" v-model="headlineThree"
                            class="headlineThree__input g__searchQuery__input" placeholder="Headline Three" name=""
                            maxlength="30" cols="30" rows="10">

                    </div>

                    <div class="queryAd__Displayurl g__querySearch-section">
                        <div class="queryAd__Displayurl--header g__searchHeader">
                            <label for="Displayurl">Display URL</label>
                            <span class="message-counter">{{ 60 - displayUrl.length }}</span>

                        </div>

                        <input type="text" id="Displayurl" v-model="displayUrl"
                            class="Displayurl__input g__searchQuery__input" placeholder="Display URL" name="" maxlength="60"
                            cols="30" rows="10">

                    </div>

                    <div class="path">
                        <div class="queryAd__pathOne">
                            <div class="queryAd__pathOne--header g__searchHeader">
                                <label for="pathOne">Path One</label>
                                <span class="message-counter">{{ 15 - pathOne.length }}</span>

                            </div>

                            <input type="text" id="pathOne" v-model="pathOne" class="pathOne__input g__searchQuery__input"
                                placeholder="Path One" name="" maxlength="15">

                        </div>

                        <div class="queryAd__pathTwo">
                            <div class="queryAd__pathTwo--header g__searchHeader">
                                <label for="pathTwo">Path Two</label>
                                <span class="message-counter">{{ 15 - pathTwo.length }}</span>

                            </div>

                            <input type="text" id="pathTwo" v-model="pathTwo" class="pathTwo__input g__searchQuery__input"
                                placeholder="Path Two" name="" maxlength="15">

                        </div>
                    </div>

                    <div class="queryAd__DescriptionOne g__querySearch-section">
                        <div class="queryAd__DescriptionOne--header g__searchHeader">
                            <label for="DescriptionOne">Description One</label>
                            <span class="message-counter">{{ 90 - descriptionOne.length }}</span>

                        </div>

                        <textarea id="DescriptionOne" v-model="descriptionOne"
                            class="DescriptionOne__input g__searchQuery__input" placeholder="Description One" name=""
                            maxlength="90" cols="30" rows="5"></textarea>

                    </div>

                    <div class="queryAd__DescriptionTwo g__querySearch-section">
                        <div class="queryAd__DescriptionTwo--header g__searchHeader">
                            <label for="DescriptionTwo">Description Two</label>
                            <span class="message-counter">{{ 90 - descriptionTwo.length }}</span>

                        </div>

                        <textarea id="DescriptionTwo" v-model="descriptionTwo"
                            class="DescriptionTwo__input g__searchQuery__input" placeholder="Description Two" name=""
                            maxlength="90" cols="30" rows="5"></textarea>

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
                            placeholder="snippetHeader" name="" maxlength="30" cols="30" rows="10"> -->

                    </div>

                    <div class="snippetOne g__querySearch-section">
                        <div class="snippetOne--header g__searchHeader">
                            <label for="snippetOne">Snippet One</label>
                            <span class="message-counter">{{ 25 - snippetOne.length }}</span>

                        </div>

                        <input type="text" id="snippetOne" v-model="snippetOne"
                            class="snippetOne__input g__searchQuery__input" placeholder="Snippet One" name="" maxlength="25"
                            cols="30" rows="10">

                    </div>

                    <div class="snippetTwo g__querySearch-section">
                        <div class="snippetTwo--header g__searchHeader">
                            <label for="snippetTwo">Snippet Two</label>
                            <span class="message-counter">{{ 25 - snippetTwo.length }}</span>

                        </div>

                        <input type="text" id="snippetTwo" v-model="snippetTwo"
                            class="snippetTwo__input g__searchQuery__input" placeholder="Snippet Two" name="" maxlength="25"
                            cols="30" rows="10">

                    </div>

                    <div class="snippetThree g__querySearch-section">
                        <div class="snippetThree--header g__searchHeader">
                            <label for="snippetThree">Snippet Three</label>
                            <span class="message-counter">{{ 25 - snippetThree.length }}</span>

                        </div>

                        <input type="text" id="snippetThree" v-model="snippetThree"
                            class="snippetThree__input g__searchQuery__input" placeholder="Snippet Three" name=""
                            maxlength="25" cols="30" rows="10">

                    </div>

                    <div class="snippetFour g__querySearch-section">
                        <div class="snippetFour--header g__searchHeader">
                            <label for="snippetFour">Snippet Four</label>
                            <span class="message-counter">{{ 25 - snippetFour.length }}</span>

                        </div>

                        <input type="text" id="snippetFour" v-model="snippetFour"
                            class="snippetFour__input g__searchQuery__input" placeholder="Snippet Four" name=""
                            maxlength="25" cols="30" rows="10">

                    </div>

                    <div class="snippetFive g__querySearch-section">
                        <div class="snippetFive--header g__searchHeader">
                            <label for="snippetFive">Snippet Five</label>
                            <span class="message-counter">{{ 25 - snippetFive.length }}</span>

                        </div>

                        <input type="text" id="snippetFive" v-model="snippetFive"
                            class="snippetFive__input g__searchQuery__input" placeholder="Snippet Five" name=""
                            maxlength="25" cols="30" rows="10">

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
                            <span class="message-counter">{{ 25 - calloutOne.length }}</span>

                        </div>

                        <input type="text" id="calloutOne" v-model="calloutOne"
                            class="calloutOne__input g__searchQuery__input" placeholder="Callout One" name="" maxlength="25"
                            cols="30" rows="10">

                    </div>

                    <div class="calloutTwo g__querySearch-section">
                        <div class="calloutTwo--header g__searchHeader">
                            <label for="calloutTwo">Callout Two</label>
                            <span class="message-counter">{{ 25 - calloutTwo.length }}</span>

                        </div>

                        <input type="text" id="calloutTwo" v-model="calloutTwo"
                            class="calloutTwo__input g__searchQuery__input" placeholder="Callout Two" name="" maxlength="25"
                            cols="30" rows="10">

                    </div>

                    <div class="calloutThree g__querySearch-section">
                        <div class="calloutThree--header g__searchHeader">
                            <label for="calloutThree">Callout Three</label>
                            <span class="message-counter">{{ 25 - calloutThree.length }}</span>

                        </div>

                        <input type="text" id="calloutThree" v-model="calloutThree"
                            class="calloutThree__input g__searchQuery__input" placeholder="Callout Three" name=""
                            maxlength="25" cols="30" rows="10">

                    </div>

                    <div class="calloutFour g__querySearch-section">
                        <div class="calloutFour--header g__searchHeader">
                            <label for="calloutFour">Callout Four</label>
                            <span class="message-counter">{{ 25 - calloutFour.length }}</span>

                        </div>

                        <input type="text" id="calloutFour" v-model="calloutFour"
                            class="calloutFour__input g__searchQuery__input" placeholder="Callout Four" name=""
                            maxlength="25" cols="30" rows="10">

                    </div>

                    <div class="calloutFive g__querySearch-section">
                        <div class="calloutFive--header g__searchHeader">
                            <label for="calloutFive">Callout Five</label>
                            <span class="message-counter">{{ 25 - calloutFive.length }}</span>

                        </div>

                        <input type="text" id="calloutFive" v-model="calloutFive"
                            class="calloutFive__input g__searchQuery__input" placeholder="Callout Five" name=""
                            maxlength="25" cols="30" rows="10">

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
                            <span class="message-counter">{{ 30 - sitelinkOne.length }}</span>

                        </div>

                        <input type="text" id="sitelinkOne" v-model="sitelinkOne"
                            class="sitelinkOne__input g__searchQuery__input" placeholder="Sitelink One" name=""
                            maxlength="30" cols="30" rows="10">

                    </div>

                    <div class="sitelinkOne__firstLine g__querySearch-section">
                        <div class="sitelinkOne__firstLine--header g__searchHeader">
                            <label for="sitelinkOne__firstLine">Sitelink One (First Line)</label>
                            <span class="message-counter">{{ 35 - sitelinkOne__firstLine.length }}</span>

                        </div>

                        <input type="text" id="sitelinkOne__firstLine" v-model="sitelinkOne__firstLine"
                            class="sitelinkOne__firstLine--input g__searchQuery__input" placeholder="First Line Description"
                            name="" maxlength="35" cols="30" rows="10">

                    </div>

                    <div class="sitelinkOne__secondLine g__querySearch-section">
                        <div class="sitelinkOne__secondLine--header g__searchHeader">
                            <label for="sitelinkOne__secondLine">Sitelink One (Second Line)</label>
                            <span class="message-counter">{{ 35 - sitelinkOne__secondLine.length }}</span>

                        </div>

                        <input type="text" id="sitelinkOne__secondLine" v-model="sitelinkOne__secondLine"
                            class="sitelinkOne__secondLine--input g__searchQuery__input"
                            placeholder="Second Line Description" name="" maxlength="35" cols="30" rows="10">

                    </div>

                    <div class="sitelinktwo g__querySearch-section">
                        <div class="sitelinktwo--header g__searchHeader">
                            <label for="sitelinktwo">Sitelink Two</label>
                            <span class="message-counter">{{ 30 - sitelinktwo.length }}</span>

                        </div>

                        <input type="text" id="sitelinktwo" v-model="sitelinktwo"
                            class="sitelinktwo__input g__searchQuery__input" placeholder="Sitelink two" name=""
                            maxlength="30" cols="30" rows="10">

                    </div>

                    <div class="sitelinktwo__firstLine g__querySearch-section">
                        <div class="sitelinktwo__firstLine--header g__searchHeader">
                            <label for="sitelinktwo__firstLine">Sitelink Two (First Line)</label>
                            <span class="message-counter">{{ 35 - sitelinktwo__firstLine.length }}</span>

                        </div>

                        <input type="text" id="sitelinktwo__firstLine" v-model="sitelinktwo__firstLine"
                            class="sitelinktwo__firstLine--input g__searchQuery__input" placeholder="First Line Description"
                            name="" maxlength="35" cols="30" rows="10">

                    </div>

                    <div class="sitelinktwo__secondLine g__querySearch-section">
                        <div class="sitelinktwo__secondLine--header g__searchHeader">
                            <label for="sitelinktwo__secondLine">Sitelink Two (Second Line)</label>
                            <span class="message-counter">{{ 35 - sitelinktwo__secondLine.length }}</span>

                        </div>

                        <input type="text" id="sitelinktwo__secondLine" v-model="sitelinktwo__secondLine"
                            class="sitelinktwo__secondLine--input g__searchQuery__input"
                            placeholder="Second Line Description" name="" maxlength="35" cols="30" rows="10">

                    </div>

                    <div class="sitelinkthree g__querySearch-section">
                        <div class="sitelinkthree--header g__searchHeader">
                            <label for="sitelinkthree">Sitelink Three</label>
                            <span class="message-counter">{{ 30 - sitelinkthree.length }}</span>

                        </div>

                        <input type="text" id="sitelinkthree" v-model="sitelinkthree"
                            class="sitelinkthree__input g__searchQuery__input" placeholder="Sitelink Three" name=""
                            maxlength="30" cols="30" rows="10">

                    </div>

                    <div class="sitelinkthree__firstLine g__querySearch-section">
                        <div class="sitelinkthree__firstLine--header g__searchHeader">
                            <label for="sitelinkthree__firstLine">Sitelink Three (First Line)</label>
                            <span class="message-counter">{{ 35 - sitelinkthree__firstLine.length }}</span>

                        </div>

                        <input type="text" id="sitelinkthree__firstLine" v-model="sitelinkthree__firstLine"
                            class="sitelinkthree__firstLine--input g__searchQuery__input"
                            placeholder="First Line Description" name="" maxlength="35" cols="30" rows="10">

                    </div>

                    <div class="sitelinkthree__secondLine g__querySearch-section">
                        <div class="sitelinkthree__secondLine--header g__searchHeader">
                            <label for="sitelinkthree__secondLine">Sitelink Three (Second Line)</label>
                            <span class="message-counter">{{ 35 - sitelinkthree__secondLine.length }}</span>

                        </div>

                        <input type="text" id="sitelinkthree__secondLine" v-model="sitelinkthree__secondLine"
                            class="sitelinkthree__secondLine--input g__searchQuery__input"
                            placeholder="Second Line Description" name="" maxlength="35" cols="30" rows="10">

                    </div>

                    <div class="sitelinkfour g__querySearch-section">
                        <div class="sitelinkfour--header g__searchHeader">
                            <label for="sitelinkfour">Sitelink Four</label>
                            <span class="message-counter">{{ 30 - sitelinkfour.length }}</span>

                        </div>

                        <input type="text" id="sitelinkfour" v-model="sitelinkfour"
                            class="sitelinkfour__input g__searchQuery__input" placeholder="Sitelink Four" name=""
                            maxlength="30" cols="30" rows="10">

                    </div>

                    <div class="sitelinkfour__firstLine g__querySearch-section">
                        <div class="sitelinkfour__firstLine--header g__searchHeader">
                            <label for="sitelinkfour__firstLine">Sitelink Four (First Line)</label>
                            <span class="message-counter">{{ 35 - sitelinkfour__firstLine.length }}</span>

                        </div>

                        <input type="text" id="sitelinkfour__firstLine" v-model="sitelinkfour__firstLine"
                            class="sitelinkfour__firstLine--input g__searchQuery__input"
                            placeholder="First Line Description" name="" maxlength="35" cols="30" rows="10">

                    </div>

                    <div class="sitelinkfour__secondLine g__querySearch-section">
                        <div class="sitelinkfour__secondLine--header g__searchHeader">
                            <label for="sitelinkfour__secondLine">Sitelink Four (Second Line)</label>
                            <span class="message-counter">{{ 35 - sitelinkfour__secondLine.length }}</span>

                        </div>

                        <input type="text" id="sitelinkfour__secondLine" v-model="sitelinkfour__secondLine"
                            class="sitelinkfour__secondLine--input g__searchQuery__input"
                            placeholder="Second Line Description" name="" maxlength="35" cols="30" rows="10">

                    </div>




                </div>


                <div class="locationExtension g_sectionDesign">
                    <div class="locationExtension__heading g__headerSection">
                        <h3 class="locationExtension__header g__header">Location Extension</h3>
                        <span class="locationExtension__arrow g__leftSide-arrow"><i class="arrow down"></i></span>
                    </div>


                    <div class="location g__querySearch-section">
                        <div class="location--header g__searchHeader">
                            <label for="location">Location Extension</label>
                            <span class="message-counter">{{ 60 - location.length }}</span>

                        </div>

                        <input type="text" id="location" v-model="location" class="location__input g__searchQuery__input"
                            placeholder="London, UK" name="" maxlength="60" cols="30" rows="10">

                    </div>



                </div>

                <div class="callExtension g_sectionDesign">
                    <div class="callExtension__heading g__headerSection">
                        <h3 class="callExtension__header g__header">Call Extension</h3>
                        <span class="callExtension__arrow g__leftSide-arrow"><i class="arrow down"></i></span>
                    </div>


                    <div class="call g__querySearch-section">
                        <div class="call--header g__searchHeader">
                            <label for="call">Call Extension</label>
                            <span class="message-counter">{{ 25 - call.length }}</span>

                        </div>

                        <input type="text" id="call" v-model="call" class="call__input g__searchQuery__input"
                            placeholder="020 3950 6249" name="" maxlength="25" cols="30" rows="10">

                    </div>



                </div>

                <div class="messageExtension g_sectionDesign">
                    <div class="messageExtension__heading g__headerSection">
                        <h3 class="messageExtension__header g__header">Message Extension</h3>
                        <span class="messageExtension__arrow g__leftSide-arrow"><i class="arrow down"></i></span>
                    </div>


                    <div class="message g__querySearch-section">
                        <div class="message--header g__searchHeader">
                            <label for="message">Message Extension</label>
                            <span class="message-counter">{{ 60 - message.length }}</span>

                        </div>

                        <input type="text" id="message" v-model="message" class="message__input g__searchQuery__input"
                            placeholder="Message Extension" name="" maxlength="60" cols="30" rows="10">

                    </div>



                </div>






            </section>

            <section class="right-side">
                <div class="right-side__desktopVersion">
                    <div class="querySearch">
                        <img class="google_icon" src="../img/google_logo.svg" alt="">
                        <div class="search-bar">
                            <div class="searchBarField">
                                <p class="searchBar__input">{{ querysearch }}</p>
                            </div>
                            <img class="searchIcon" src="../img/search_icon.svg" alt="">

                            <!-- <p>Hello!</p> -->
                        </div>
                    </div>
                    <div class="searchTabs">
                        <div class="allSearch">
                            <img src="../img/search_icon_1.svg" alt="">
                            <p>All</p>

                        </div>


                    </div>
                </div>
            </section>

        </div>

    </div>
</template>

<script>

export default {
    data() {

        return {
            message: "",
            querysearch: "",
            headlineOne: "",
            headlineTwo: "",
            headlineThree: "",
            displayUrl: "",
            pathOne: "",
            pathTwo: "",
            descriptionOne: "",
            descriptionTwo: "",
            snippetOne: "",
            snippetTwo: "",
            snippetThree: "",
            snippetFour: "",
            snippetFive: "",
            calloutOne: "",
            calloutTwo: "",
            calloutThree: "",
            calloutFour: "",
            calloutFive: "",
            sitelinkOne: "",
            sitelinkOne__firstLine: "",
            sitelinkOne__secondLine: "",
            sitelinktwo: "",
            sitelinktwo__firstLine: "",
            sitelinktwo__secondLine: "",
            sitelinkthree: "",
            sitelinkthree__firstLine: "",
            sitelinkthree__secondLine: "",
            sitelinkfour: "",
            sitelinkfour__firstLine: "",
            sitelinkfour__secondLine: "",
            location: "",
            call: "",
        }

    }
}


</script>

<style src="../assets/style/AdPreview.css"></style>

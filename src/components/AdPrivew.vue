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

                        <input type="text" id="headlineTwo" v-model="headlineTwo" v-on:keypress="displayHeadlinetwo()"
                            class="headlineTwo__input g__searchQuery__input" placeholder="Headline Two" name=""
                            maxlength="30" cols="30" rows="10">

                    </div>

                    <div class="queryAd__headlineThree g__querySearch-section">
                        <div class="queryAd__headlineThree--header g__searchHeader">
                            <label for="headlineThree">Headline Three</label>
                            <span class="message-counter">{{ 30 - headlineThree.length }}</span>

                        </div>

                        <input type="text" id="headlineThree" v-model="headlineThree" v-on:keypress="displayHeadlinethree()"
                            class="headlineThree__input g__searchQuery__input" placeholder="Headline Three" name=""
                            maxlength="30" cols="30" rows="10">

                    </div>

                    <div class="queryAd__Displayurl g__querySearch-section">
                        <div class="queryAd__Displayurl--header g__searchHeader">
                            <label for="Displayurl">Display URL</label>
                            <span class="message-counter">{{ 60 - displayUrl.length }}</span>

                        </div>

                        <input type="text" id="Displayurl" v-model="displayUrl" v-on:keypress="advert()"
                            class="Displayurl__input g__searchQuery__input" placeholder="Display URL" name="" maxlength="60"
                            cols="30" rows="10">

                    </div>

                    <div class="path">
                        <div class="queryAd__pathOne">
                            <div class="queryAd__pathOne--header g__searchHeader">
                                <label for="pathOne">Path One</label>
                                <span class="message-counter">{{ 15 - pathOne.length }}</span>

                            </div>

                            <input type="text" id="pathOne" v-model="pathOne" v-on:keypress="displayUrlOne()"
                                class="pathOne__input g__searchQuery__input" placeholder="Path One" name="" maxlength="15">

                        </div>

                        <div class="queryAd__pathTwo">
                            <div class="queryAd__pathTwo--header g__searchHeader">
                                <label for="pathTwo">Path Two</label>
                                <span class="message-counter">{{ 15 - pathTwo.length }}</span>

                            </div>

                            <input type="text" id="pathTwo" v-model="pathTwo" v-on:keypress="displayUrlTwo()"
                                class="pathTwo__input g__searchQuery__input" placeholder="Path Two" name="" maxlength="15">

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
                            <select v-model="selected" v-on:click="selectColon()" name="snippetHeader__selectbox"
                                id="snippetHeader">
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

                        <input type="text" id="snippetTwo" v-model="snippetTwo" v-on:keypress="snippetCommaOne()"
                            class="snippetTwo__input g__searchQuery__input" placeholder="Snippet Two" name="" maxlength="25"
                            cols="30" rows="10">

                    </div>

                    <div class="snippetThree g__querySearch-section">
                        <div class="snippetThree--header g__searchHeader">
                            <label for="snippetThree">Snippet Three</label>
                            <span class="message-counter">{{ 25 - snippetThree.length }}</span>

                        </div>

                        <input type="text" id="snippetThree" v-model="snippetThree" v-on:keypress="snippetCommaTwo()"
                            class="snippetThree__input g__searchQuery__input" placeholder="Snippet Three" name=""
                            maxlength="25" cols="30" rows="10">

                    </div>

                    <div class="snippetFour g__querySearch-section">
                        <div class="snippetFour--header g__searchHeader">
                            <label for="snippetFour">Snippet Four</label>
                            <span class="message-counter">{{ 25 - snippetFour.length }}</span>

                        </div>

                        <input type="text" id="snippetFour" v-model="snippetFour" v-on:keypress="snippetCommaThree()"
                            class="snippetFour__input g__searchQuery__input" placeholder="Snippet Four" name=""
                            maxlength="25" cols="30" rows="10">

                    </div>

                    <div class="snippetFive g__querySearch-section">
                        <div class="snippetFive--header g__searchHeader">
                            <label for="snippetFive">Snippet Five</label>
                            <span class="message-counter">{{ 25 - snippetFive.length }}</span>

                        </div>

                        <input type="text" id="snippetFive" v-model="snippetFive" v-on:keypress="snippetCommaFour()"
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

                        <input type="text" id="calloutOne" v-model="calloutOne" v-on:keypress="snippetEnd()"
                            class="calloutOne__input g__searchQuery__input" placeholder="Callout One" name="" maxlength="25"
                            cols="30" rows="10">

                    </div>

                    <div class="calloutTwo g__querySearch-section">
                        <div class="calloutTwo--header g__searchHeader">
                            <label for="calloutTwo">Callout Two</label>
                            <span class="message-counter">{{ 25 - calloutTwo.length }}</span>

                        </div>

                        <input type="text" id="calloutTwo" v-model="calloutTwo" v-on:keypress="calloutSeperatorOne()"
                            class="calloutTwo__input g__searchQuery__input" placeholder="Callout Two" name="" maxlength="25"
                            cols="30" rows="10">

                    </div>

                    <div class="calloutThree g__querySearch-section">
                        <div class="calloutThree--header g__searchHeader">
                            <label for="calloutThree">Callout Three</label>
                            <span class="message-counter">{{ 25 - calloutThree.length }}</span>

                        </div>

                        <input type="text" id="calloutThree" v-model="calloutThree" v-on:keypress="calloutSeperatorTwo()"
                            class="calloutThree__input g__searchQuery__input" placeholder="Callout Three" name=""
                            maxlength="25" cols="30" rows="10">

                    </div>

                    <div class="calloutFour g__querySearch-section">
                        <div class="calloutFour--header g__searchHeader">
                            <label for="calloutFour">Callout Four</label>
                            <span class="message-counter">{{ 25 - calloutFour.length }}</span>

                        </div>

                        <input type="text" id="calloutFour" v-model="calloutFour" v-on:keypress="calloutSeperatorThree()"
                            class="calloutFour__input g__searchQuery__input" placeholder="Callout Four" name=""
                            maxlength="25" cols="30" rows="10">

                    </div>

                    <div class="calloutFive g__querySearch-section">
                        <div class="calloutFive--header g__searchHeader">
                            <label for="calloutFive">Callout Five</label>
                            <span class="message-counter">{{ 25 - calloutFive.length }}</span>

                        </div>

                        <input type="text" id="calloutFive" v-model="calloutFive" v-on:keypress="calloutSeperatorFour()"
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

                        <input type="text" id="sitelinkOne" v-model="sitelinkOne" v-on:keypress="calloutEnd()"
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

                        <input type="text" id="sitelinktwo" v-model="sitelinktwo" v-on:keypress="displayBorder()"
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

                        <input type="text" id="location" v-model="location" v-on:keypress="displayLocation"
                            class="location__input g__searchQuery__input" placeholder="London, UK" name="" maxlength="60"
                            cols="30" rows="10">

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

                        <input type="text" id="call" v-model="call" v-on:keypress="displayNumber"
                            class="call__input g__searchQuery__input" placeholder="020 3950 6249" name="" maxlength="25"
                            cols="30" rows="10">

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

                        <input type="text" id="message" v-model="message" v-on:keypress="displaymessage"
                            class="message__input g__searchQuery__input" placeholder="Message Extension" name=""
                            maxlength="60" cols="30" rows="10">

                    </div>



                </div>






            </section>

            <section class="right-side">
                <div class="right-side__desktop-version">
                    <div class="desktop-version__header">
                        <div class="header__logo">
                            <img class="header__logo-google" src="../assets/img/google_logo.svg" alt="">
                        </div>
                        <div class="header__right-side">
                            <div class="header__search-box">
                                <div class="searchBarField">
                                    <p class="searchBar__input">{{ querysearch }}</p>
                                </div>
                                <img class="searchIcon" src="../assets/img/search_icon.svg" alt="">


                            </div>
                            <div class="header__tabs">
                                <div class="tabs__item has-bottom-border">
                                    <span class="material-symbols-outlined">search</span>
                                    <p class="tab__text">All</p>
                                </div>
                                <div class="tabs__item">
                                    <span class="material-symbols-outlined">Image</span>
                                    <p class="tab__text">Images</p>
                                </div>
                                <div class="tabs__item">
                                    <span class="material-symbols-outlined">location_on</span>
                                    <p class="tab__text">Maps</p>
                                </div>
                                <div class="tabs__item">
                                    <span class="material-symbols-outlined">newsmode</span>
                                    <p class="tab__text">News</p>
                                </div>
                                <div class="tabs__item">
                                    <span class="material-symbols-outlined">slideshow</span>
                                    <p class="tab__text">Videos</p>
                                </div>
                                <div class="tabs__item">
                                    <span class="material-symbols-outlined">more_vert</span>
                                    <p class="tab__text">More</p>
                                </div>

                            </div>
                        </div>
                    </div>

                    <div class="desktop-version__details">
                        <div class="details__result-count">
                            <p>About 368,000,000 results (0.46 seconds)</p>
                        </div>

                        <div class="details__ad-header">
                            <p id="ad-header__heading" class="ad-header__heading">Ad . </p>
                            <p class="displayUrl g__url">{{ displayUrl }}</p>
                            <span class="url__devider__one" id="url__devider__one">/</span>
                            <p class="path-one g__url">{{ pathOne }}</p>
                            <span class="url__devider__two" id="url__devider__two">/</span>
                            <p class="path-two g__url">{{ pathTwo }}</p>


                        </div>

                        <div class="display__headline">
                            <h3 class="display__headline__one g__headline">{{ headlineOne }}</h3>
                            <span class="divider__One" id="divider__One">|</span>
                            <h3 class="display__headline__two g__headline">{{ headlineTwo }}</h3>
                            <span class="divider__Two" id="divider__Two">|</span>
                            <h3 class="display__headline__three g__headline">{{ headlineThree }}</h3>
                        </div>

                        <div class="description">
                            <p class="description__one g__description">{{ descriptionOne }}</p>
                            <p class="description__two g__description">{{ descriptionTwo }}</p>
                            <p class="select-option g__description">{{ selected }}</p>
                            <span class="select-colon" id="selectColon">:</span>


                            <div class="snippet">
                                <p class="snippet__One g__description">{{ snippetOne }}</p>
                                <span class="snippet__comma__One" id="snippet__comma__One">,</span>
                                <p class="snippet__Two g__description">{{ snippetTwo }}</p>
                                <span class="snippet__comma__Two" id="snippet__comma__Two">,</span>
                                <p class="snippet__Three g__description">{{ snippetThree }}</p>
                                <span class="snippet__comma__Three" id="snippet__comma__Three">,</span>
                                <p class="snippet__Four g__description">{{ snippetFour }}</p>
                                <span class="snippet__comma__Four" id="snippet__comma__Four">,</span>
                                <p class="snippet__Five">{{ snippetFive }}</p>
                                <span class="snippet__end" id="snippet__end">.</span>
                            </div>

                            <div class="callout">
                                <p class="callout__one g__description">{{ calloutOne }}</p>
                                <span class="callout__separator--one" id="callout__separator--one">.</span>
                                <p class="callout__two g__description">{{ calloutTwo }}</p>
                                <span class="callout__separator--two" id="callout__separator--two">.</span>
                                <p class="callout__three g__description">{{ calloutThree }}</p>
                                <span class="callout__separator--three" id="callout__separator--three">.</span>
                                <p class="callout__four g__description">{{ calloutFour }}</p>
                                <span class="callout__separator--four" id="callout__separator--four">.</span>
                                <p class="callout__five g__description">{{ calloutFive }}</p>

                            </div>

                            <div class="location-call">
                                <div class="location-display">
                                    <span class="material-symbols-outlined location-icon"
                                        id="location-icon">location_on</span>
                                    <p class="location-text">{{ location }}</p>
                                </div>

                                <div class="call-display">
                                    <span class="call-divider" id="call-divider">-</span>
                                    <p class="call-text">{{ call }}</p>
                                </div>
                            </div>

                            <div class="sitelink">
                                <div class="sitelink__row g__sitelink-container">
                                    <div class="sitelink__one g__sitelink-column">
                                        <h3 class="one__header g__sitelink-headline">{{ sitelinkOne }}</h3>
                                        <p class="one__first-line g__sitelink-lines">{{ sitelinkOne__firstLine }}</p>
                                        <p class="one__second-line g__sitelink-lines">{{ sitelinkOne__secondLine }}</p>
                                    </div>

                                    <div class="sitelink__two g__sitelink-column">
                                        <h3 class="two__header g__sitelink-headline">{{ sitelinktwo }}</h3>
                                        <p class="two__first-line g__sitelink-lines">{{ sitelinktwo__firstLine }}</p>
                                        <p class="two__second-line g__sitelink-lines">{{ sitelinktwo__secondLine }}</p>
                                    </div>
                                </div>

                                <div class="sitelink__row g__sitelink-container">
                                    <div class="sitelink__three g__sitelink-column">
                                        <h3 class="three__header g__sitelink-headline">{{ sitelinkthree }}</h3>
                                        <p class="three__first-line g__sitelink-lines">{{ sitelinkthree__firstLine }}</p>
                                        <p class="three__second-line g__sitelink-lines">{{ sitelinkthree__secondLine }}</p>
                                    </div>

                                    <div class="sitelink__four g__sitelink-column">
                                        <h3 class="four__header g__sitelink-headline">{{ sitelinkfour }}</h3>
                                        <p class="four__first-line g__sitelink-lines">{{ sitelinkfour__firstLine }}</p>
                                        <p class="four__second-line g__sitelink-lines">{{ sitelinkfour__secondLine }}</p>
                                    </div>
                                </div>


                            </div>
                        </div>



                    </div>
                </div>
                <div class="right-side__mobile-version">
                    <div class="mobile-version__header">
                        <span class="material-symbols-outlined">menu</span>
                        <img class="header__logo-google" src="../assets/img/google_logo.svg" alt="">
                        <span class="material-symbols-outlined">apps</span>
                    </div>

                    <div class="searchbar-mobile">
                        <div class="search-outline">
                            <span class="material-symbols-outlined">search</span>
                            <div class="search-text">
                                <p>{{ querysearch }}</p>
                            </div>
                            <span class="material-symbols-outlined">close</span>
                        </div>
                    </div>

                    <div class="mobile-tab">
                        <p class="tab-text tab-design"><b>All</b></p>
                        <p class="tab-text">Shopping</p>
                        <p class="tab-text">Images</p>
                        <p class="tab-text">Maps</p>
                        <p class="tab-text">News</p>
                    </div>

                    <div class="mobile-url-display">
                        <p id="mobile-url-header" class="mobile-ad-header__heading">Ad . </p>
                        <p class="displayUrl g__mobile-url">{{ displayUrl }}</p>
                        <span class="url__devider__one" id="mobile-url-divider__one">/</span>
                        <p class="path-one g__mobile-url">{{ pathOne }}</p>
                        <span class="url__devider__two" id="mobile-url-divider__two">/</span>
                        <p class="path-two g__mobile-url">{{ pathTwo }}</p>

                    </div>

                    <div class="mobile-headline">
                        <div class="headline-first-row">
                            <h3 class="mobile-display__headline__one g__headline">{{ headlineOne }}</h3>
                            <span class="divider__One" id="mobile-divider__One">|</span>
                        </div>

                        <div class="headline-second-row">
                            <h3 class="display__headline__two g__headline">{{ headlineTwo }}</h3>
                            <span class="divider__Two" id="mobile-divider__two">|</span>
                            <h3 class="display__headline__three g__headline">{{ headlineThree }}</h3>
                        </div>

                    </div>

                    <div class="mobile-description">
                        <p class="mobile-description__one g__description">{{ this.getMobileDescription(descriptionOne + ' '
                            + descriptionTwo, 115) }}</p>

                        <!-- <p class="mobile-description__two g__description">{{ descriptionTwo }}</p> -->

                    </div>

                    <div class="mobile-callout" id="mobile-callout">
                        <p class="mobile-callout-text g__description">{{ this.getMobileCallout(50) }}</p>
                    </div>

                    <div class="mobile-sitelink">
                        <!-- <div class="mobile-sitelink__one g__mobile-sitelink" id="mb-sl__one"> -->
                        <p class="mobile-sl__headline" id="mbSLHeadline1">{{ sitelinkOne }}</p>
                        <!-- </div> -->
                        <!-- 
                        <div class="mobile-sitelink__two g__mobile-sitelink" id="mb-sl__two">
                            <p class="mobile-sl__headline">{{ sitelinktwo }}</p>
                        </div> -->
                        <!-- 
                        <div class="mobile-sitelink__three g__mobile-sitelink">
                            <p class="mobile-sl__headline">{{ sitelinkthree }}</p>
                        </div> -->
                    </div>

                    <div class="mobile-location-call">
                        <div class="mobile-location" id="mobile-location">
                            <span class="material-symbols-outlined mobile-location-icon"
                                id="mobile-location-icon">location_on</span>
                            <p class="mobile-location-text">{{ location }}</p>
                        </div>

                        <div class="mobile-call" id="mobile-call">
                            <span class="material-symbols-outlined mobile-call-icon" id="mobile-call-icon">call</span>
                            <p class="mobile-call-text">{{ call }}</p>
                        </div>
                    </div>

                    <div class="mobile-message">
                        <div class="mobile-message-wrapper" id="mobile-message-wrapper">
                            <span class="material-symbols-outlined mobile-message-icon" id="mobile-message-icon">sms</span>
                            <p class="message-text">{{ this.getmessage(message, 40) }}</p>
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
            selected: "",
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

    },

    methods: {

        getMobileDescription(total_description, char_limit) {
            // to display the description within a specified character limit

            let mobile_des = total_description
            if (mobile_des.length > char_limit) {
                mobile_des = mobile_des.slice(0, char_limit) + '...';
            }

            return (mobile_des);
        },

        getMobileCallout(char_limit) {
            // to display the description within a specified character limit

            let mobile_callout = this.calloutOne + '.' + this.calloutTwo + '.' + this.calloutThree + '.' + this.calloutFour + '.' + this.calloutFive;
            if (mobile_callout.length > char_limit) {
                mobile_callout = mobile_callout.slice(0, char_limit) + '...';
            }

            return (mobile_callout);
        },




        advert: function () {
            if (this.displayUrl !== "") {
                document.getElementById("ad-header__heading").style = "display: block";
                document.getElementById("mobile-url-header").style = "display: block";
            }



        },
        displayHeadlinetwo: function () {
            document.getElementById("divider__One").style = "display: block";
            document.getElementById("mobile-divider__One").style = "display: block";
        },

        displayHeadlinethree: function () {
            document.getElementById("divider__Two").style = "display: block";
            document.getElementById("mobile-divider__two").style = "display: block";
        },

        displayUrlOne: function () {
            document.getElementById("url__devider__one").style = "display: block";
            document.getElementById("mobile-url-divider__one").style = "display: block";
        },

        displayUrlTwo: function () {
            document.getElementById("url__devider__two").style = "display: block";
            document.getElementById("mobile-url-divider__two").style = "display: block";
        },

        selectColon: function () {
            document.getElementById("selectColon").style = "display: inline";
        },

        snippetCommaOne: function () {
            document.getElementById("snippet__comma__One").style = "display: inline";
        },

        snippetCommaTwo: function () {
            document.getElementById("snippet__comma__Two").style = "display: inline";
        },

        snippetCommaThree: function () {
            document.getElementById("snippet__comma__Three").style = "display: inline";
        },

        snippetCommaFour: function () {
            document.getElementById("snippet__comma__Four").style = "display: inline";
        },

        snippetEnd: function () {
            document.getElementById("snippet__end").style = "display: inline";
            document.getElementById("mobile-callout").style = "display: block";
        },

        calloutSeperatorOne: function () {
            document.getElementById("callout__separator--one").style = "display: inline";
        },

        calloutSeperatorTwo: function () {
            document.getElementById("callout__separator--two").style = "display: inline";
        },

        calloutSeperatorThree: function () {
            document.getElementById("callout__separator--three").style = "display: inline";
        },

        calloutSeperatorFour: function () {
            document.getElementById("callout__separator--four").style = "display: inline";
        },

        calloutEnd: function () {
            document.getElementById("callout__separator--five").style = "display: inline";
            // document.getElementById("mobile-sl__headline").style = "display: block";
            document.getElementById("mbSLHeadline1").style = "border: 1px solid rgba(182, 182, 182, 0.397)";
        },

        displayLocation: function () {
            document.getElementById("location-icon").style = "display: block";
            document.getElementById("mobile-location-icon").style = "display: block";
            document.getElementById("mobile-location").style = "display: flex";
        },

        displayNumber: function () {
            document.getElementById("call-divider").style = "display: block";
            document.getElementById("mobile-call-icon").style = "display: block";
            document.getElementById("mobile-call").style = "display: flex";
        },

        displaymessage: function () {
            document.getElementById("mobile-message-icon").style = "display: block"
            document.getElementById("mobile-message-wrapper").style = "display: flex"

            
        },

        getmessage: function (messageInput, char_limit) {

            let message_text = messageInput
            if (message_text.length > char_limit) {
                message_text = message_text.slice(0, char_limit)+ '...';
            }

            return (message_text);

        }


        // getMobileDescription(total_description, char_limit) {
        //     // to display the description within a specified character limit

        //     let mobile_des = total_description
        //     if (mobile_des.length > char_limit) {
        //         mobile_des = mobile_des.slice(0, char_limit) + '...';
        //     }

        //     return (mobile_des);
        // },

        // displayBorder: function () {
        //     document.getElementById("mb-sl__two").style = "display: block";
        // },






    }
}


</script>

<style src="../assets/style/AdPreview.css"></style>

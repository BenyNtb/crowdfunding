<template>
    <div class='modal'>

        <h2 class="modal-heading">Back this project</h2>

        <span id="modal-close-btn">
            <svg width="15" height="15" xmlns="http://www.w3.org/2000/svg">
                <path class="close-btn-x"
                    d="M11.314 0l2.828 2.828L9.9 7.071l4.243 4.243-2.828 2.828L7.07 9.9l-4.243 4.243L0 11.314 4.242 7.07 0 2.828 2.828 0l4.243 4.242L11.314 0z"
                    fill="#000" fill-rule="evenodd" opacity=".4" /></svg>
        </span>

        <p id="modal-paragraph">Want to support us in bringing Mastercraft Bamboo Monitor Riser out in the world?</p>

        <div class='modal-pledge-option' id="modal-pledge-option-no-reward">

            <label class="radio">

                <span class="radio__input">

                    <input type="radio" name="pledge" id="pledge-option-no-rewards" />
                    <span class="radio__control"></span>

                </span>

                <span class="radio__label">

                    <span class="product__name">
                        Pledge With No Reward
                    </span>

                </span>

            </label>

            <p class="modal-pledge-paragraph">Choose to support us without a reward if you simply believe in our
                project. As a backer,
                you will be signed up to receive product updates via email.</p>

            <div class="pledge-selection" id="pledge-selection-no-reward">

                <p class="pledge-selection-heading">Enter your pledge</p>

                <div class="input-btn-field">

                    <div class="input-icon" id="no-reward-disable">
                        <input class="pledge-amount-input" type="number" placeholder="0" min="0"
                            id="pledge-amount-input-black">
                        <i>$</i>
                    </div>

                    <button href="#" class="pledge-submit-btn" id="pledge-submit-btn-no-reward">Continue</button>
                </div>
            </div>

        </div>

        <div class='modal-pledge-option' id="modal-pledge-option-bamboo">

            <label class="radio">

                <span class="radio__input">

                    <input type="radio" name="pledge" id="pledge-option-bamboo" />
                    <span class="radio__control"></span>

                </span>

                <span class="radio__label">

                    <span class="product__name">
                        Bamboo stand
                    </span>
                    <span class="pledge__amount">
                        Pledge $25 or more
                    </span>

                </span>

            </label>

            <p class="modal-pledge-paragraph">You get an ergonomic stand made of natural bamboo. You've helped us launch
                our promotional campaign, and
                you’ll be added to a special Backer member list.
            </p>

            <div class="modal-in-stock">
                <span class="in-stock-amount" id="modal-in-stock-amount-bamboo">101</span>
                <p id='left'>left</p>
            </div>

            <!-- Selected pledge start -->

            <div class="pledge-selection" id="pledge-selection-bamboo">

                <p class="pledge-selection-heading">Enter your pledge</p>

                <div class="input-btn-field">

                    <div class="input-icon">
                        <input class="pledge-amount-input" type="number" placeholder="25" min="25"
                            id="pledge-amount-input-bamboo">
                        <i>$</i>
                    </div>

                    <button href="#" class="pledge-submit-btn" id="pledge-submit-btn-bamboo">Continue</button>

                    <small class="error-message" id="error-message">Error message</small>

                </div>
            </div>

        </div>

        <div class='modal-pledge-option' id="modal-pledge-option-black">

            <label class="radio">

                <span class="radio__input">

                    <input type="radio" name="pledge" id="pledge-option-black" />
                    <span class="radio__control"></span>

                </span>

                <span class="radio__label">

                    <span class="product__name">
                        Black edition stand
                    </span>
                    <span class="pledge__amount">
                        Pledge $75 or more
                    </span>

                </span>

            </label>

            <p class="modal-pledge-paragraph">You get a Black Special Edition computer stand and a personal thank you.
                You’ll be added to our Backer
                member list. Shipping is included.</p>

            <div class="modal-in-stock">
                <span class="in-stock-amount" id="modal-in-stock-amount-black">64</span>
                <p id='left'>left</p>
            </div>
            <!-- Selected pledge start -->

            <div class="pledge-selection" id="pledge-selection-black">

                <p class="pledge-selection-heading">Enter your pledge</p>

                <div class="input-btn-field">

                    <div class="input-icon">
                        <input class="pledge-amount-input error" placeholder="75" min="75"
                            id="pledge-amount-input-black" type="text">
                        <i>$</i>
                    </div>

                    <button href="#" class="pledge-submit-btn" id="pledge-submit-btn-black">Continue</button>

                </div>
            </div>
        </div>


        <div class='modal-pledge-option' id="out-of-stock">

            <div class="overlay"></div>

            <label class="radio">

                <span class="radio__input">

                    <input type="radio" name="pledge" id="pledge-option-black" />
                    <span class="radio__control"></span>

                </span>

                <span class="radio__label">

                    <span class="product__name">
                        Mahogany Special Edition
                    </span>
                    <span class="pledge__amount">
                        Pledge $200 or more
                    </span>

                </span>

            </label>

            <p class="modal-pledge-paragraph">You get two Special Edition Mahogany stands, a Backer T-Shirt, and a
                personal thank you. You’ll be added
                to our Backer member list. Shipping is included.</p>

            <div class="modal-in-stock">
                <span class="in-stock-amount">0</span>
                <p id='left'>left</p>
            </div>
        </div>


    </div>
</template>

<script>

</script>

<style>

</style>
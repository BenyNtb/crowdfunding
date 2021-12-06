<template>
    <section class="main-section" id="top-main-section">

        <svg id="mastercraft-logo" width="56" height="56" xmlns="http://www.w3.org/2000/svg">
            <g fill="none" fill-rule="evenodd">
                <circle fill="#000" cx="28" cy="28" r="28" />
                <g fill-rule="nonzero">
                    <path
                        d="M15.565 28.565a1.93 1.93 0 012.606-.113l.122.113 10.142 10.142a1.93 1.93 0 01-2.606 2.84l-.122-.112-10.142-10.142a1.93 1.93 0 010-2.728z"
                        fill="#444" />
                    <path
                        d="M36.19 17.48c1.006-.996 2.706-.34 2.805 1.026l.005.126v10.736c0 .9-.737 1.629-1.646 1.629a1.64 1.64 0 01-1.642-1.507l-.005-.122v-6.805l-8.043 7.957c-1.006.996-2.707.34-2.806-1.026l-.004-.126v-6.805L16.81 30.52a1.66 1.66 0 01-2.224.095l-.105-.095a1.616 1.616 0 01-.096-2.2l.096-.103L25.336 17.48c1.006-.996 2.707-.34 2.806 1.026l.004.126v6.804l8.043-7.956z"
                        fill="#FFF" />
                </g>
            </g>
        </svg>

        <h1>Mastercraft Bamboo Monitor Riser</h1>

        <p>A beautifully handcrafted monitor stand to reduce neck and eye strain.</p>

        <div id="main-section-btn-bookmark">
            <button href="#" id="backProjectBtn">Back this project</button>

            <div id="bookmark-btn-mobile-desktop">
                <svg class="bookmark" id="icon-bookmark" width="56" height="56" xmlns="http://www.w3.org/2000/svg">
                    <g class="marked-cyan" fill="blue" fill-rule="evenodd">
                        <circle class="bookmark-circle" fill="#2F2F2F" cx="28" cy="28" r="28" />
                        <path class="bookmark-shape inner-marked" fill="#B1B1B1" d="M23 19v18l5-5.058L33 37V19z" />
                    </g>

                </svg>
                <span class="bookmark-btn-desktop bookmark-desktop">Bookmark</span>
            </div>

        </div>

    </section>
</template>

<script>

</script>

<style>
.main-section {
    
    background-color: white;
    width: 100%;
    max-width: 45rem;
    position: relative; 
    bottom: 72.5px;
    border-radius: 7px;
    padding: 1.375rem 1.375rem;
    text-align: center;
    border: solid 1.5px rgba(0, 0, 0, 0.1);
    padding-bottom: 0rem;
    margin: 0 auto 1.75rem;

}

#top-main-section h1 {

    font-weight: var(--fw-700);
    font-size: 1.5rem;
    margin-top: var(--margin1);
    margin-bottom: 1.3rem;
    color: black;
    
}

#top-main-section p {

    font-size: 0.95rem;
    opacity: 0.65;
    line-height: 1.7;
    padding-bottom: 0;
}

#main-section-btn-bookmark {

    display: flex;
    justify-content: space-between; 
    width: 100%;

    margin-top: 1.688rem;
    margin-bottom: 2.5rem;
    

}

#main-section-btn-bookmark button {

    background-color: var(--cyan);
    color: white;
    border: none;
    padding-left: 2rem;
    padding-right: 2rem;
    height: 3.5rem;
    font-weight: var(--fw-700);
    border-radius: 2rem;
    display: inline;
    position: relative;
    min-width: 13.375rem;
    transition: var(--trans);

}

#main-section-btn-bookmark button:hover {
    background-color: var(--dark-cyan);
}
</style>
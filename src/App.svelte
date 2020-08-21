<script>
    let footerToggle = false;
    function openFooter() {
        if (!footerToggle) {
            footerToggle = !footerToggle;
        }
    }
    function closeFooter() {
        if (footerToggle) {
            footerToggle = !footerToggle;
        }
    }
</script>

<style type="text/scss">
    main {
        font-family: "Manrope", sans-serif;
        width: 100%;
        // padding: 74px 24px 20px 24px;
    }
    article {
    }
    .card {
        overflow: hidden;
        border-radius: 1rem;
        width: 327px;
        margin: 0 auto;
        background-color: #fff;
        margin-top: 74px;
        box-shadow: 0 4rem 4rem -1rem rgba(201, 213, 225, 0.5);
    }
    .header {
        img {
            height: 200px;
            width: 100%;
        }
    }
    .main-container {
        display: flex;
        flex-direction: column;
        background-color: #fff;
        padding: 36px 32px 20px 32px;
        .first-paragraph {
            p {
                margin-bottom: 12px;
                font-style: normal;
                font-weight: bold;
                font-size: 16px;
                line-height: 24px;
                letter-spacing: 0.1px;
                color: #48556a;
            }
        }
        .second-paragraph {
            p {
                margin-bottom: 52px;
                font-style: normal;
                font-weight: 500;
                font-size: 13px;
                line-height: 20px;
                letter-spacing: 0.13px;
                color: #6e8098;
            }
        }
    }
    .footer-container {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-content: center;
        .personal-logo {
            margin-right: 16px;
            width: 40px;
            height: 40px;
            img {
                border-radius: 50%;
                width: 100%;
            }
        }
        .info {
            flex: 1 0;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            align-content: center;
            .info-name {
                font-style: normal;
                font-weight: bold;
                font-size: 13px;
                line-height: 20px;
                letter-spacing: 0.121875px;
                color: #48556a;
            }
            .info-date {
                font-style: normal;
                font-weight: 500;
                font-size: 13px;
                line-height: 20px;
                letter-spacing: 0.121875px;
                color: #9daec2;
            }
        }
    }
    .share {
        width: 32px;
        height: 32px;
        background-color: var(--light-grayish-blue);
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-self: center;
        img {
            transform: translateY(-1px);
            align-self: center;
            width: 50%;
        }
    }
    // .footer-container:hover{
    //     .hidden-footer{
    //         display: flex;
    //         position: absolute;
    //     }
    // }
    .hideFooter {
        display: none;
        position: absolute;
        animation-name: hideShare;
        animation-duration: 2s;
    }
    .showHiddenFooter {
        animation-name: displayShare;
        animation-duration: 2s;
        display: flex;
        position: absolute;
        border-bottom-left-radius: 5px;
        border-bottom-right-radius: 5px;
        background-color: var(--very-dark-grayish-blue);
        bottom: 0;
        width: 263px;
        left: 0;
        height: 32px;
        padding: 16px 32px 16px 32px;
        .share {
            svg {
                align-self: center;
            }
            background-color: var(--desaturated-dark-blue);
        }
    }
    article {
        position: relative;
    }
    .share-icons {
        display: flex;
        flex: 1 0;
        justify-content: flex-start;
        align-items: center;
        p {
            font-style: normal;
            font-weight: 500;
            font-size: 13px;
            line-height: 20px;
            letter-spacing: 5px;
            color: #9daec2;
            margin-right: 21px;
        }
        .icon {
            width: 20px;
            height: 20px;
            display: flex;
            align-items: center;
            img {
                width: 100%;
            }
        }
    }
    .mr-16 {
        margin-right: 16px;
    }
    // css animation
    @keyframes displayShare {
        from {
            bottom: -50px;
        }
        to {
            bottom: 0px;
        }
    }
    @keyframes hideShare {
        from {
            bottom: 0px;
        }
        to {
            bottom: -50px;
        }
    }
    @media (min-width:1200px){
        .card{
            display:flex;
            width:730px;
            height:280px;
            .header{
                width: 285px;
                height:280px;
                img{
                    width: 100%;
                    height:100%;
                }
            }
            .main-container{
                width:365px;
            }
        }
    }
</style>

<main>
    <article class="card">
        <div class="header">
            <img src="./images/drawers.jpg" alt="" />
        </div>
        <div class="main-container">
            <div class="first-paragraph">
                <p>
                    Shift the overall look and feel by adding these wonderful
                    touches to furniture in your home
                </p>
            </div>
            <div class="second-paragraph">
                <p>
                    Ever been in a room and felt like something was missing?
                    Perhaps it felt slightly bare and uninviting. I’ve got some
                    simple tips to help you make any room feel complete.
                </p>
            </div>
            <div class="footer-container">
                <div class="personal-logo">
                    <img src="./images/avatar-michelle.jpg" alt="" />
                </div>
                <div class="info">
                    <p class="info-name">Michelle Appleton</p>
                    <p class="info-date">28 Jun 2020</p>
                </div>
                <div class="share" on:click={openFooter}>
                    <img src="./images/icon-share.svg" alt="" />
                </div>
            </div>
            <div
                class={footerToggle === true ? 'showHiddenFooter' : 'hideFooter'}>
                <div class="share-icons">
                    <p>SHARE</p>
                    <div class="icon mr-16">
                        <img src="./images/icon-facebook.svg" alt="" />
                    </div>
                    <div class="icon mr-16">
                        <img src="./images/icon-twitter.svg" alt="" />
                    </div>
                    <div class="icon">
                        <img src="./images/icon-pinterest.svg" alt="" />
                    </div>
                </div>
                <div class="share " on:click={closeFooter}>
                    <svg
                        version="1.1"
                        id="Layer_1"
                        xmlns="http://www.w3.org/2000/svg"
                        xmlns:xlink="http://www.w3.org/1999/xlink"
                        x="0px"
                        y="0px"
                        width="15px"
                        height="15px"
                        viewBox="0 0 121.31 122.876"
                        enable-background="new 0 0 121.31 122.876"
                        xml:space="preserve">
                        <g>
                            <path
                                fill="#fff"
                                d="M90.914,5.296c6.927-7.034,18.188-7.065,25.154-0.068
                                c6.961,6.995,6.991,18.369,0.068,25.397L85.743,61.452l30.425,30.855c6.866,6.978,6.773,18.28-0.208,25.247
                                c-6.983,6.964-18.21,6.946-25.074-0.031L60.669,86.881L30.395,117.58c-6.927,7.034-18.188,7.065-25.154,0.068
                                c-6.961-6.995-6.992-18.369-0.068-25.397l30.393-30.827L5.142,30.568c-6.867-6.978-6.773-18.28,0.208-25.247
                                c6.983-6.963,18.21-6.946,25.074,0.031l30.217,30.643L90.914,5.296L90.914,5.296z" />
                        </g>
                    </svg>
                </div>
            </div>
        </div>
    </article>
</main>

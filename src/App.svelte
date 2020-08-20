<script>
    let footerToggle = false;
    function toogleFooter() {
        footerToggle = !footerToggle;
        console.log("footerToggle: ", footerToggle);
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
    }
    .showHiddenFooter {
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
            svg{
                transform: translateY(-1px);
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
                <div class="share" on:click={toogleFooter}>
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
                <div class="share">
                    <svg
                        xmlns="http://www.w3.org/2000/svg"
                        width="15"
                        height="13">
                        <path
                            fill="#fff"
                            d="M15 6.495L8.766.014V3.88H7.441C3.33 3.88 0 7.039
                            0 10.936v2.049l.589-.612C2.59 10.294 5.422 9.11 8.39
                            9.11h.375v3.867L15 6.495z" />
                    </svg>
                </div>
            </div>
        </div>
    </article>
</main>

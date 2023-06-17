<script>
    const COUNTDOWN_DAYS = 14;

    // initialize the counter object
    let counterObject = {
        days: 14,
        hours: 24,
        minutes: 60,
        seconds: 60,
    };

    let targetDate = new Date();

    targetDate.setDate(targetDate.getDate() + COUNTDOWN_DAYS);

    // update the countdown every second

    let countdown = setInterval(updateCountdown, 1000);

    function updateCountdown() {
        let currentDate = new Date();

        let timeDifference = targetDate.getTime() - currentDate.getTime();

        if (timeDifference <= 0) {
            clearInterval(countdown); // stop the countdown when the target date is reached
            return;
        } else {
            let remainingDays = Math.floor(
                timeDifference / (1000 * 60 * 60 * 24)
            );
            let remainingHours = Math.floor(
                (timeDifference % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60)
            );
            let remainingMinutes = Math.floor(
                (timeDifference % (1000 * 60 * 60)) / (1000 * 60)
            );
            let remainingSeconds = Math.floor(
                (timeDifference % (1000 * 60)) / 1000
            );

            // Display the results in the UI

            counterObject.days = remainingDays;
            counterObject.hours = remainingHours;
            counterObject.minutes = remainingMinutes;
            counterObject.seconds = remainingSeconds;
        }
    }
</script>

<main>
    <section class="container">
        <h1>WE'RE LAUNCHING SOON</h1>
        <div class="counter">
            <div class="counter__item">
                <h2>{counterObject.days}</h2>
                <p>days</p>
            </div>
            <div class="counter__item">
                <h2>{counterObject.hours}</h2>
                <p>hours</p>
            </div>
            <div class="counter__item">
                <h2>{counterObject.minutes}</h2>
                <p>minutes</p>
            </div>
            <div class="counter__item">
                <h2>{counterObject.seconds}</h2>
                <p>seconds</p>
            </div>
        </div>
    </section>
    <div class="socials">
        <div class="social-icons">
            <a href="/facebook">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24"
                    ><path
                        fill="#8385A9"
                        d="M22.675 0H1.325C.593 0 0 .593 0 1.325v21.351C0 23.407.593 24 1.325 24H12.82v-9.294H9.692v-3.622h3.128V8.413c0-3.1 1.893-4.788 4.659-4.788 1.325 0 2.463.099 2.795.143v3.24l-1.918.001c-1.504 0-1.795.715-1.795 1.763v2.313h3.587l-.467 3.622h-3.12V24h6.116c.73 0 1.323-.593 1.323-1.325V1.325C24 .593 23.407 0 22.675 0z"
                    /></svg
                >
            </a>
            <a href="/instagram">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24"
                    ><path
                        fill="#8385A9"
                        d="M12 2.163c3.204 0 3.584.012 4.85.07 3.252.148 4.771 1.691 4.919 4.919.058 1.265.069 1.645.069 4.849 0 3.205-.012 3.584-.069 4.849-.149 3.225-1.664 4.771-4.919 4.919-1.266.058-1.644.07-4.85.07-3.204 0-3.584-.012-4.849-.07-3.26-.149-4.771-1.699-4.919-4.92-.058-1.265-.07-1.644-.07-4.849 0-3.204.013-3.583.07-4.849.149-3.227 1.664-4.771 4.919-4.919 1.266-.057 1.645-.069 4.849-.069zM12 0C8.741 0 8.333.014 7.053.072 2.695.272.273 2.69.073 7.052.014 8.333 0 8.741 0 12c0 3.259.014 3.668.072 4.948.2 4.358 2.618 6.78 6.98 6.98C8.333 23.986 8.741 24 12 24c3.259 0 3.668-.014 4.948-.072 4.354-.2 6.782-2.618 6.979-6.98.059-1.28.073-1.689.073-4.948 0-3.259-.014-3.667-.072-4.947-.196-4.354-2.617-6.78-6.979-6.98C15.668.014 15.259 0 12 0zm0 5.838a6.162 6.162 0 100 12.324 6.162 6.162 0 000-12.324zM12 16a4 4 0 110-8 4 4 0 010 8zm6.406-11.845a1.44 1.44 0 100 2.881 1.44 1.44 0 000-2.881z"
                    /></svg
                >
            </a>
            <a href="/pinterest">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24"
                    ><path
                        fill="#8385A9"
                        d="M12 0C5.373 0 0 5.372 0 12c0 5.084 3.163 9.426 7.627 11.174-.105-.949-.2-2.405.042-3.441.218-.937 1.407-5.965 1.407-5.965s-.359-.719-.359-1.782c0-1.668.967-2.914 2.171-2.914 1.023 0 1.518.769 1.518 1.69 0 1.029-.655 2.568-.994 3.995-.283 1.194.599 2.169 1.777 2.169 2.133 0 3.772-2.249 3.772-5.495 0-2.873-2.064-4.882-5.012-4.882-3.414 0-5.418 2.561-5.418 5.207 0 1.031.397 2.138.893 2.738a.36.36 0 01.083.345l-.333 1.36c-.053.22-.174.267-.402.161-1.499-.698-2.436-2.889-2.436-4.649 0-3.785 2.75-7.262 7.929-7.262 4.163 0 7.398 2.967 7.398 6.931 0 4.136-2.607 7.464-6.227 7.464-1.216 0-2.359-.631-2.75-1.378l-.748 2.853c-.271 1.043-1.002 2.35-1.492 3.146C9.57 23.812 10.763 24 12 24c6.627 0 12-5.373 12-12 0-6.628-5.373-12-12-12z"
                    /></svg
                >
            </a>
        </div>
    </div>
</main>

<style lang="scss">
    @import "./variables.scss";

    // media queries mixin

    @mixin desktop {
        @media (min-width: 768px) {
            @content;
        }
    }

    main {
        width: 100%;
        height: 100%;
        background: url(/bg-stars.svg) no-repeat top center fixed,
            $very-dark-blue;
        display: flex;
        align-items: center;
        flex-direction: column;
        justify-content: center;
        position: relative;

        .container {
            margin-inline: auto;
            h1 {
                color: $white;
                letter-spacing: 0.5rem;
                font-size: 1.2rem;
                margin-bottom: 3rem;

                @include desktop {
                    font-size: 2.5rem;
                    margin-bottom: 5rem;
                }
            }

            div.counter {
                display: flex;
                gap: 1rem;
                justify-content: center;
                margin-bottom: 10rem;

                @include desktop {
                    gap: 2rem;
                }

                h2 {
                    color: $soft-red;
                    font-size: 1.5rem;
                    position: relative;

                    background: $dark-desaturated-blue;
                    padding: 1rem 0rem;
                    width: 4rem;
                    margin-bottom: 1rem;

                    border-radius: 0.5rem;

                    @include desktop {
                        font-size: 6rem;
                        width: 9rem;
                        padding: 0.2rem 0;
                    }

                    &::before,
                    &::after {
                        content: "";
                        display: block;
                        width: 0.8rem;
                        height: 5px;
                        top: 50%;

                        border-radius: 0.5rem;
                        position: absolute;
                        background-color: $very-dark-blue;
                        border-radius: 5px;
                    }
                    &::after {
                        left: -0.5rem;
                    }
                    &::before {
                        content: "";
                        right: -0.5rem;
                    }
                }

                p {
                    color: $grayish-blue;
                    font-weight: 400;
                    text-transform: uppercase;
                    font-size: 0.5rem;
                    letter-spacing: 0.2rem;

                    @include desktop {
                        font-size: 0.8rem;
                    }
                }
            }
        }

        .socials {
            display: flex;
            justify-content: center;
            align-items: end;
            width: 100%;

            position: absolute;
            bottom: 0;
            height: 10rem;
            background: url(/pattern-hills.svg) no-repeat;
            background-size: 25rem 10rem;

            @include desktop {
                background-size: 100% 10rem;
            }

            .social-icons {
                display: flex;
                gap: 2rem;
                height: 48%;
                a {
                    transition: all 0.3s ease-in-out;
                    svg {
                        path {
                            fill: $grayish-blue;
                            transition: all 0.3s ease-in-out;
                        }
                    }
                    &:hover {
                        svg {
                            path {
                                fill: $soft-red;
                            }
                        }
                    }
                }
            }
        }
    }
</style>

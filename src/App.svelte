<script>
</script>

<main>
    <section class="container">
        <h1>WE'RE LAUNCHING SOON</h1>
        <div class="counter">
            <div class="counter__item">
                <h2>00</h2>
                <p>days</p>
            </div>
            <div class="counter__item">
                <h2>00</h2>
                <p>hours</p>
            </div>
            <div class="counter__item">
                <h2>00</h2>
                <p>minutes</p>
            </div>
            <div class="counter__item">
                <h2>00</h2>
                <p>seconds</p>
            </div>
        </div>
    </section>
</main>

<style lang="scss">
    @import "./variables.scss";

    main {
        width: 100%;
        height: 100%;
        background: url(/bg-stars.svg) no-repeat top center fixed,
            $very-dark-blue;
        display: flex;
        align-items: center;

        .container {
          margin-inline: auto;
            h1 {
                color: $white;
                letter-spacing: 0.5rem;
                font-size: 1.2rem;
                margin-bottom: 3rem;
            }

            div.counter {
              display: flex;
              gap: 1rem;
              justify-content: center;

              h2 {
                color: $soft-red;
                font-size: 1.5rem;
                position: relative;

                background: $dark-desaturated-blue;
                padding: 1rem 1.1rem;
                margin-bottom: 1rem;

                border-radius: 0.5rem;
                
                &::before,
                &::after {
                  content: "";
                  display: block;
                  width: .8rem;
                  height: 5px;
                  top: 50%;

                  border-radius: 0.5rem;
                  position: absolute;
                  background-color: $very-dark-blue;
                  border-radius:5px;
                }
                &::after {
                  left: -.5rem;
                }
                &::before {
                  content: "";
                  right: -.5rem;
                }
              }

              p {
                color: $grayish-blue;
                font-weight: 400;
                text-transform: uppercase;
                font-size: 0.5rem;
                letter-spacing: 0.2rem;
              }
            }
        }
    }
</style>

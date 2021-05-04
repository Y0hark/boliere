<template>
  <div>
    <div class="card-content-site">
      <div class="card-component-site">
        <div class="content-card-site">
          <h4 class="title-card">
            {{ title }}
          </h4>
          <p class="copy">
            {{ description }}
          </p>
          <a class="btn btn-link" :href="buttonLink" target="_blank"> {{ buttonTitle }} </a>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    title: { type: String, default: 'Title Card Site' },
    description: { type: String, default: 'Card description' },
    buttonTitle: { type: String, default: 'Button Name' },
    buttonLink: { type: String, default: 'https://google.com' }
  }
}
</script>
<style lang="scss">

:root {
  --d: 700ms;
  --e: cubic-bezier(0.19, 1, 0.22, 1);
  --font-sans: 'Noto Serif TC';
  --font-serif: 'Noto Serif';
}

.btn-link {
    text-decoration: none;
    font-weight: normal;
}

.card-content-site {
  position: relative;
  font-family: var(--font-sans);
}

.card-component-site {
  min-height: 60vh;
  max-width: 50vw;
  min-width: 50vw;
  display: flex;
  align-items: flex-end;
  overflow: hidden;
  padding: 1rem;
  text-align: center;
  color: rgb(255, 255, 255);
  background-color: whitesmoke;

  &:before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 110%;
    background-size: cover;
    background-position: 0 0;
    transition: transform calc(var(--d) * 1.5) var(--e);
    pointer-events: none;
  }

  &:after {
    content: '';
    display: block;
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 200%;
    pointer-events: none;
    background-image: linear-gradient(
      to bottom,
      hsla(0, 0%, 0%, 0) 0%,
      hsla(0, 0%, 0%, 0.009) 11.7%,
      hsla(0, 0%, 0%, 0.034) 22.1%,
      hsla(0, 0%, 0%, 0.072) 31.2%,
      hsla(0, 0%, 0%, 0.123) 39.4%,
      hsla(0, 0%, 0%, 0.182) 46.6%,
      hsla(0, 0%, 0%, 0.250) 48.6%,
      hsla(0, 0%, 0%, 0.450) 50.6%,
      hsla(0, 0%, 0%, 0.950) 53.1%,
      hsla(0, 0%, 0%, 0.950) 58.9%,
      hsla(0, 0%, 0%, 0.950) 64.3%,
      hsla(0, 0%, 0%, 0.950) 69.3%,
      hsla(0, 0%, 0%, 0.950) 74.1%,
      hsla(0, 0%, 0%, 0.950) 78.8%,
      hsla(0, 0%, 0%, 0.950) 83.6%,
      hsla(0, 0%, 0%, 0.950) 88.7%,
      hsla(0, 0%, 0%, 0.950) 94.1%,
      rgba(0, 0, 0, 1) 100%
    );
    transform: translateY(-50%);
    transition: transform calc(var(--d) * 2) var(--e);
  }
    background-size: cover;
    background-repeat: no-repeat;
    }
  @media screen and (min-width: 768px) {
    .card-component-site {
      min-width: 40vw;
      max-width: 40vw;
  }
  }
  @media screen and (min-width: 850px) {
    .card-component-site {
      min-height: 60vh;
      max-width: 40vw;
      min-width: 40vw;
    }
  }

  @media screen and (min-width: 1000px) {
    .card-component-site {
      max-width: 35vw;
      min-width: 35vw;
    }
  }

  @media screen and (min-width: 1150px) {
    .card-component-site {
      max-width: 50vw;
      min-width: 50vw;
    }
  }

.content-card-site {
  position: relative;
  display: flex;
  flex-direction: column;
  align-items: center;
  width: 100%;
  padding: 1rem;
  transition: transform var(--d) var(--e);
  z-index: 1;

  > * + * {
    margin-top: 1rem;
  }
}
.title-card {
    font-size: 1.3rem;
    font-weight: bold;
    line-height: 1.2;
}

.copy {
  font-family: var(--font-serif);
  font-size: 0.6rem;
  font-style: italic;
  line-height: 1.35;
  word-break: break-word;
}

.btn {
  cursor: pointer;
  margin-top: 1.5rem;
  padding: 0.75rem 1.5rem;
  font-size: 0.65rem;
  letter-spacing: 0.025rem;
  text-transform: uppercase;
  color: white;
  background-color: rgb(44, 44, 44);
  border: none;

  &:hover {
    background-color: lighten(rgb(27, 27, 27), 5%);
  }

  &:focus {
    outline-offset: 3px;
  }
}

@media (hover: hover) {
  .card-component-site:after {
    transform: translateY(0);
  }

  .content-card-site {
    transform: translateY(calc(100% - 4.5rem));

    > * {
      opacity: 0;
      transform: translateY(1rem);
      transition:
        transform var(--d) var(--e),
        opacity var(--d) var(--e);
    }
  }

  .card-component-site:hover,
  .card-component-site:focus-within {
    align-items: center;

    &:before { transform: translateY(-4%); }
    &:after { transform: translateY(-50%); }

    .content-card-site {
      transform: translateY(0);

      > * {
        opacity: 1;
        transform: translateY(0);
        transition-delay: calc(var(--d) / 8);
      }
    }
  }

  .card-component-site:focus-within {
    &:before,
    &:after,
    .content-card-site,
    .content-card-site > * {
      transition-duration: 0s;
    }
  }
}

</style>

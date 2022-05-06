<script setup>
import BookingButton from "./Button/BookingButton.vue";
</script>
<template>
  <section class="location relative">
    <div class="title absolute text-center top-0">
      <TitleRibbon title="Standorte" />
    </div>
    <div class="grid">
      <!--Store selection-->
      <div class="selection"></div>
      <!--Map-->
      <div class="flex">
        <div id="accordion" class="flex-1">
          <div id="accordion-bg">
            <details open>
              <summary>WIESBADEN 1</summary>
              <div class="content">
                <strong>Glammy Nails im Globus EKZ Wiesbaden</strong>
                <span>Ostring 2</span>
                <span> 65205 Wiesbaden </span>
                <strong>Telefonnummer</strong>
                <span>061227077423</span>
                <span>01797693582</span>
                <strong>E-Mail:</strong>

                <a href="mailto:info@glammy-nails.de">info@glammy-nails.de</a>
              </div>
              <h1>
                <a href="#">
                  Pricelist
                  <svg
                    class="ml-6 inline-block"
                    width="16"
                    height="16"
                    viewBox="0 0 16 16"
                    fill="none"
                    xmlns="http://www.w3.org/2000/svg"
                  >
                    <path
                      d="M0.5 8.5H15.5"
                      stroke="#E6007E"
                      stroke-miterlimit="10"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      data-darkreader-inline-stroke=""
                      style="--darkreader-inline-stroke: #ff2b9f"
                    ></path>
                    <path
                      d="M10.5 3.5L15.5 8.5L10.5 13.5"
                      stroke="#E6007E"
                      stroke-miterlimit="10"
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      data-darkreader-inline-stroke=""
                      style="--darkreader-inline-stroke: #ff2b9f"
                    ></path></svg
                ></a>
              </h1>
              <BookingButton title="Book a date" />
            </details>
          </div>
        </div>
        <Map id="map" class="flex-1" />
      </div>
    </div>
  </section>
</template>
<script>
import Map from "./Map/Map.vue";
import TitleRibbon from "./Ribbon/TitleRibbon.vue";
export default {
  name: "Location",
  components: {
    Map,
    TitleRibbon,
  },
};
</script>
<style lang="scss" scoped>
.title {
  left: 50%;
  transform: translateX(-50%);
}
#accordion {
  flex: 0 0 50%;
  text-align: left;
  font-family: "system-ui";
  padding: 4rem;

  details {
    width: 300px;
    position: relative;
    padding: 0;
    margin: 0;

    &::after {
      all: unset;
      content: "+";
      position: absolute;
      right: 0;
      top: 0.25rem;
      font-size: 1.75rem;
      background: #e6007e;
      color: #fff;
      padding-bottom: 0.875rem;
      padding-inline: 0.4375rem;
      height: 2rem;
      width: 2rem;
      border-radius: 0.25rem;
      text-align: center;
      transform: scale(0.6) translate(5px, -5px);
    }

    &[open] {
      padding-bottom: 1rem;
      &::after {
        content: "-";
        padding-bottom: 0.75rem;
        padding-inline: 0.375rem;
        transform: scale(0.625) translate(2px, -3.5px);
      }
    }

    summary {
      cursor: pointer;
      text-align: left;
      list-style: none;
      color: #e6007e;
      text-transform: uppercase;
      font-size: 2rem;
      font-family: "Architecture", sans-serif;
      letter-spacing: 2px;
      border-bottom: 1px solid rgba(0, 0, 0, 0.1);
      position: relative;
      padding: 0;
      margin: 0;

      &::-webkit-details-marker {
        display: none;
      }
    }

    .content {
      display: flex;
      flex-flow: column;
      gap: 1.5rem;
      margin-top: 1.25rem;
      color: #967871;
      font-size: 1.0625rem;
      font-weight: 500;
      strong {
        color: #6b433b;
        font-size: 1.125rem;
      }
    }

    h1 {
      font-family: "Architecture", sans-serif;
      margin: 1rem 0 1.5rem 0;
      text-transform: uppercase;
      font-size: 2rem;
      font-weight: unset;
      letter-spacing: 2px;

      & > a {
        color: #e6007e !important;
        display: flex;
        gap: 0.5rem;
        align-items: center;
      }
    }
  }
}
#accordion-bg {
  width: max-content;
  border-radius: 0.75rem;
  padding: 1.25rem 1.5rem;
  background: #fffbf5;
}
#map {
  flex: 0 0 50%;
}
.location {
  background-image: url("/src/assets/images/bg-standorte.jpg");
}
</style>

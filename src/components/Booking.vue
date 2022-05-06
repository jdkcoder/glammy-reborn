<template>
  <section class="" id="booking">
    <div class="relative">
      <div class="h-9 bg-brown-2 shadow-1"></div>
      <!--Title ribbon-->
      <div class="absolute left-1/2 text-center -translate-x-1/2 top-0">
        <TitleRibbon title="Booking" />
      </div>

      <div class="booking-form-wrapper bg-no-repeat bg-center">
        <form action="" id="booking-form">
          <!--First input row-->
          <div class="input-row grid">
            <label class="font-heading text-pink-1 uppercase w-full">
              <div class="text-align-left">Name*</div>
              <input
                id="name"
                required
                type="text"
                class="
                  booking-input
                  border border-transparent
                  font-body
                  mt-8
                  px-16
                  py-12
                  w-full
                "
                placeholder="John Doe"
              />
            </label>
            <label class="font-heading text-pink-1 uppercase w-full">
              <div class="text-align-left">Telefon*</div>
              <input
                required
                type="text"
                class="
                  booking-input
                  border border-transparent
                  font-body
                  mt-8
                  px-16
                  py-12
                  w-full
                "
                placeholder="0123456789"
              />
            </label>
            <label class="font-heading text-pink-1 uppercase w-full">
              <div class="text-align-left">Email*</div>
              <input
                required
                type="text"
                class="
                  booking-input
                  border border-transparent
                  font-body
                  mt-8
                  px-16
                  py-12
                  w-full
                "
                placeholder="johndoe@gmail.com"
              />
            </label>
          </div>
          <!--Break line -->
          <div></div>
          <!--Second input row-->
          <div class="input-row grid">
            <label class="font-heading text-pink-1 uppercase w-full">
              <div class="text-align-left">Store</div>
              <input
                type="text"
                class="
                  booking-input
                  border border-transparent
                  font-body
                  mt-8
                  px-16
                  py-12
                  w-full
                "
              />
            </label>
            <label class="font-heading text-pink-1 uppercase w-full">
              <div class="text-align-left">Datum</div>
              <input
                id="date-input"
                class="
                  booking-input
                  date-input
                  border border-transparent
                  font-body
                  mt-8
                  px-16
                  py-12
                  w-full
                "
                type="date"
              />
            </label>
            <label class="font-heading text-pink-1 uppercase w-full">
              <div class="text-align-left">Service</div>
              <select
                name=""
                id=""
                class="
                  booking-input
                  border border-transparent
                  font-body
                  mt-8
                  px-16
                  py-12
                  w-full
                "
              >
                <option value="">New</option>
                <option value="">Repair</option>
              </select>
            </label>
          </div>
          <div class="time-picker">
            <!--Third input row-->
            <h5 class="font-heading text-pink-1 text-align-left uppercase">
              Zeitrahmen
            </h5>
            <!--Time Picker Row 1-->
            <div class="time-picker-row grid">
              <label>
                <input type="radio" name="time" />
                <span class="flex">9:00-9:45</span>
              </label>
              <label>
                <input type="radio" name="time" />
                <span class="flex">9:45-10:30</span>
              </label>
              <label>
                <input type="radio" name="time" />
                <span class="flex">10:30-11:15</span>
              </label>
              <label>
                <input type="radio" name="time" />
                <span class="flex">11:15-12:00</span>
              </label>
              <label>
                <input type="radio" name="time" />
                <span class="flex">12:00-12:45</span>
              </label>
              <label>
                <input type="radio" name="time" />
                <span class="flex">12:45-13:30</span>
              </label>
              <label>
                <input type="radio" name="time" />
                <span class="flex">13:30-14:15</span>
              </label>
              <label>
                <input type="radio" name="time" />
                <span class="flex">14:15-15:00</span>
              </label>
              <label>
                <input type="radio" name="time" />
                <span class="flex">15:00-15:45</span>
              </label>
              <label>
                <input type="radio" name="time" />
                <span class="flex">15:45-16:30</span>
              </label>
              <label>
                <input type="radio" name="time" />
                <span class="flex">16:30-17:15</span>
              </label>
              <label>
                <input type="radio" name="time" />
                <span class="flex">17:15-18:00</span>
              </label>
            </div>
          </div>

          <div class="consent-checkbox text-align-left">
            <label
              for="
        "
            >
              <input type="checkbox" />Bei Klärung weiterer Informationen bin
              ich mit einem Telefongespräch einverstanden.
            </label>
          </div>

          <div id="booking-form-submit" class="text-center">
            <BookingButton title="Termin Buchen" />
          </div>
        </form>
      </div>
    </div>
  </section>
</template>

<!--Script part-->
<script>
import $ from "jquery";
import BookingButton from "./Button/BookingButton.vue";
import TitleRibbon from "./Ribbon/TitleRibbon.vue";
export default {
  name: "Booking",
  components: {
    BookingButton,
    TitleRibbon,
  },
};
</script>
<!--End script part-->
<style lang="scss" scoped>
//white-space:nowrap;
.absolute {
  z-index: 1;
}
.consent-checkbox {
  padding-left: 5rem;
}

.booking-form-wrapper {
  background-image: url("../assets/images/bg-book.png");
  background-size: 100% 100%;
  height: 750px;
}
#booking-form {
  transform: translateY(20%);
  /*Booking Form Submit */
  #booking-form-submit {
    margin-top: 2%;
    padding: 17px 40px;
    // transform: translateY(35%);
    /*Text*/
    letter-spacing: 0.1em;
    font-size: 16px;
    line-height: 24px;
  }
  /*input row*/
  .input-row {
    row-gap: 0px;
    column-gap: 30px;
    margin-bottom: 30px;
    margin-left: 5rem;
    margin-right: 5rem;
    grid-template-columns: 1fr 1fr 1fr;
    column-gap: 130px;

    .booking-input {
      border-width: 1px;
      border-color: transparent;

      &:focus {
        outline: none !important;
        border-color: #e6007e;
        transition: all 0.4s ease;
      }
    }
    & > label {
      font-size: 20px;
      line-height: 1.4;
      letter-spacing: 0.04em;
      div {
        width: inherit;
      }
    }
  }
  /*Time picker row*/
  .time-picker {
    margin-left: 5rem;
    margin-right: 5rem;
  }
  .time-picker-row {
    gap: 20px;
    margin-bottom: 30px;

    grid-template-columns: 1fr 1fr 1fr 1fr 1fr 1fr;

    input:checked ~ span {
      background-color: rgba(230, 0, 126, 1);
      color: rgba(255, 255, 255, 1);
      transition: all 0.4s ease-in-out;
    }

    span {
      font-size: 1.125rem;
      transition: all 0.4s ease-in-out;
    }

    label {
      box-sizing: border-box;
      cursor: pointer;
      input {
        display: none;
      }
    }
    span {
      background-color: rgba(255, 255, 255, 1);
      box-sizing: border-box;
      align-items: center;
      justify-content: center;
      height: 100%;
      padding-left: 10px;
      padding-right: 10px;
      padding-top: 12px;
      padding-bottom: 12px;
      --tw-shadow: 0px 4px 4px rgba(0, 0, 0, 0.1);
      box-shadow: var(--tw-ring-offset-shadow, 0 0 #0000),
        var(--tw-ring-shadow, 0 0 #0000), var(--tw-shadow);
      text-align: center;
      color: rgba(107, 67, 59, 0.4);
    }
  }
}
.date-input {
  background-image: url(../assets/svg/calendar-icon.svg);
  background-repeat: no-repeat;
  background-position: 96% center;
  color: rgba(107, 67, 59, 0.4);
}

.page-title {
  background-image: url("../assets/images/bg-title.png");
}
</style>

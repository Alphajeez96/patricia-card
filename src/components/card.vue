<template>
  <div>
    <div class="card-holder" :class="{ switch: !isVisible }">
      <!-- Logo - display icon here-->
      <div class="flex items-center">
        <!-- Logo here-->
        <div>
          <img
            src="@/assets/img/logo.svg"
            height="16.63"
            width="95.34"
            alt="logo"
          />
        </div>

        <!-- Visibility Toggler here-->
        <div class="ml-auto">
          <a @click="isVisible = !isVisible">
            <img
              :src="isVisible ? vector.mask1 : vector.mask2"
              height="17.92"
              width="25.59"
              alt="Mask"
            />
          </a>
        </div>
      </div>

      <!-- Card digits display here-->
      <div class="flex justify-between digits">
        <input
          :type="toggleType(i)"
          value="9784"
          disabled
          class="primary-gray"
          v-for="i in 4"
          :key="i"
        />
      </div>

      <!-- bottom contents here-->
      <div class="flex justify-between placeholders">
        <div class="primary-gray font-14 card-holder-name">
          <p>Cardholder Name</p>
        </div>

        <!-- Validity here-->
        <div class="flex items-center validity">
          <p class="font-7 sec-gray">
            VALID <br />
            THRU
          </p>
          <p class="primary-gray">10/12</p>
        </div>

        <!-- Cvv here-->
        <div class="flex items-center cvv">
          <p class="font-7 sec-gray" v-if="!isVisible">CVV</p>
          <input
            :type="isVisible ? 'text' : 'password'"
            value="455"
            class="primary-gray"
            disabled
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "card",

  data: () => ({
    isVisible: true,
    vector: {
      mask1: require("@/assets/img/vectors/Mask.svg"),
      mask2: require("@/assets/img/vectors/Mask-1.svg"),
    },
  }),

  methods: {
    toggleType(i) {
      if (this.isVisible || i == 4) {
        return "text";
      }
      return "password";
    },
  },
};
</script>

<style scoped>
.card-holder {
  background-image: url("../assets/img/patricia-icon-2.svg");
  background-repeat: no-repeat;
  background-size: contain;
  background-color: var(--primary-black);
  padding: 39px 30px 0px 30px;
  border-radius: 20px;
  width: inherit;
}

.card-holder.switch {
  background-image: url("../assets/img/patricia-icon.png");
}

a {
  cursor: pointer;
}

.card-holder > .digits {
  margin-top: 90px;
}

.card-holder > .digits input {
  width: 12%;
  background: inherit;
  border: none;
  font-size: 1.438rem;
}

.card-holder > .placeholders {
  margin-top: 65px;
}

.card-holder-name {
  width: 60%;
}

.validity {
  width: 30%;
}

.validity :first-child {
  margin-right: 15px;
}

.cvv > input {
  width: 30px;
  background: inherit;
  border: none;
  font-size: 1rem;
  margin-left: 10px;
}
</style>

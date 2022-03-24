<template>
  <div class="order">
    <h1>Order</h1>
    <main class="form-order">
      <div class="card">
        <div class="card-body">
          <form @submit.prevent="getFormValues">
            <div class="input-container">
              <input id="1" type="checkbox" name="1" value="Salade" v-model="checkedNames">
              <label for="1"><span>Salade</span></label>
            </div>
            <div class="input-container">
              <input id="2" type="checkbox" name="2" value="Tomates" v-model="checkedNames">
              <label for="2"><span>Tomates</span></label>
            </div>
            <div class="input-container">
              <input id="3" type="checkbox" name="3" value="Oignons" v-model="checkedNames">
              <label for="3"><span>Oignons</span></label>
            </div>
            <div class="input-container">
              <input id="4" type="checkbox" name="4" value="Concombre" v-model="checkedNames">
              <label for="4"><span>Concombre</span></label>
            </div>
            <div class="input-container">
              <input id="5" type="checkbox" name="5" value="Ail" v-model="checkedNames">
              <label for="5"><span>Ail</span></label>
            </div>
            <div class="input-container">
              <input id="6" type="checkbox" name="6" value="Merguez" v-model="checkedNames">
              <label for="6"><span>Merguez</span></label>
            </div>
            <div class="input-container">
              <input id="7" type="checkbox" name="7" value="Nuggets" v-model="checkedNames">
              <label for="7"><span>Nuggets</span></label>
            </div>
            <div class="input-container">
              <input id="8" type="checkbox" name="8" value="Frites" v-model="checkedNames">
              <label for="8"><span>Frites</span></label>
            </div>
            <div class="slidecontainer">
              Petit <input type="range" min="1" max="3" value="1" class="slider" id="myRange"> Grand
            </div>
            <div class="row">
              <div class="col">
                <label for="name">Name : </label>
                <input id="name" type="text" name="name" placeholder="Clément"><br>
                <label for="surname">Surname : </label>
                <input id="surname" type="text" name="surname" placeholder="Dauvois"><br>
                <label for="mail">Mail : </label>
                <input id="mail" type="email" name="mail" placeholder="turbo@kebab.com"><br>
                <label for="collect">Collect option : </label>
                <select id="collect" name="collect">
                  <option value="pickup">Pick up at restaurant</option>
                  <option value="delivery">Home delivery</option>
                </select>
              </div>
              <div class="col">
                <label for="address">Address : </label>
                <input id="address" type="text" name="address" placeholder="777 boulevard Robert-Bourassa"><br>
                <label for="city">City : </label>
                <input id="city" type="text" name="city" placeholder="Montréal"><br>
                <label for="postalcode">Postal code : </label>
                <input id="postalcode" type="text" name="postalcode" placeholder="H3C3Z7"><br>
                <label for="country">Country : </label>
                <input id="country" type="text" name="country" placeholder="Canada">
              </div>
            </div>
            <input type="submit" value="Order now !">
          </form>
        </div>
        <table class="table">
          <thead>
          <tr>
            <th scope="col">Food</th>
            <th scope="col">Name</th>
            <th scope="col">Surname</th>
            <th scope="col">Mail</th>
            <th scope="col">Collect option</th>
          </tr>
          </thead>
          <tbody>
          <tr>
            <td>{{checkedNames}}</td>
            <td>{{name}}</td>
            <td>{{surname}}</td>
            <td>{{mail}}</td>
            <td>{{collect}}</td>
          </tr>
          </tbody>
        </table>
      </div>
    </main>
  </div>
</template>

<script>
export default {
  name: 'OrderView',
  data: function(){
    return {
      name: "",
      surname: "",
      mail: "",
      collect: "",
      checkedNames: []
    }
  },
  methods: {
    getFormValues(submitEvent) {
      this.name = submitEvent.target.elements.name.value
      this.surname = submitEvent.target.elements.surname.value
      this.mail = submitEvent.target.elements.mail.value
      this.collect = submitEvent.target.elements.collect.value
      this.checkedName = submitEvent.target.elements.checkedNames.value
    }
  }
}
</script>

<style>

.form-order {
  width: 100%;
  max-width: 805px;
  margin: auto;
  align-items: center;
}

.order {
  padding: 2%;
  text-align: center;
  align-items: center;
}

.slider {
  width: 50%;
}

.col label, .col input, .slidecontainer {
  margin: 10px;
}

.input-container {
  position: relative;
  display: inline-block;
  width: 190px;
  height: 80px;
}

.input-container input[type="checkbox"] {
  display: none;
}

input[type="checkbox"]:checked + label {
  background-color: #888;
}

.input-container label {
  position: absolute;
  display: block;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  margin: 5px;
  padding: 0 10px;
  color: #fff;
  text-align: center;
  line-height: 70px;
  background-color: #ccc;
  border-radius: 4px;
  font-family: Algerian;
  font-size: large;
}

.input-container label:hover {
  cursor: pointer;
  -webkit-transition: background-color .3s ease;
  -moz-transition: background-color .3s ease;
  -ms-transition: background-color .3s ease;
  -o-transition: background-color .3s ease;
  transition: background-color .3s ease;
}

.input-container label:hover, input[type="checkbox"]:checked + label:hover {
  background-color: #555;
}

label span {
  display: inline-block;
  vertical-align: middle;
  line-height: normal;
}

input[type="submit"] {
  font-family: Algerian;
}
</style>

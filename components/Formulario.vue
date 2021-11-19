<template>
  <div id="contactanos" class="form-section">
    <div class="form-container relative m-auto">
      <div class="tag-wrap">
        <div class="tag flex">ESPECIALÍZATE,<br />TRANSFORMA<br />Y LIDERA</div>
      </div>
      <div class="form-content m-auto">
        <h3 class="form-title uppercase">{{ titleForm }}</h3>
        <form @submit="enviarForm" @submit.prevent>
          <div class="flex flex-wrap -mx-3 mb-6">
            <div class="w-full md:w-1/2 md:px-3 mb-6 md:mb-0">
              <input
                v-model="form.nombre"
                class="
                  appearance-none
                  block
                  w-full
                  text-gray-700
                  border border-gray-200
                  rounded
                  leading-tight
                  focus:outline-none focus:bg-white focus:border-red-500
                "
                type="text"
                placeholder="Nombres"
                required
              />
            </div>
            <div class="w-full md:w-1/2 md:px-3">
              <input
                v-model="form.apellidos"
                class="
                  appearance-none
                  block
                  w-full
                  text-gray-700
                  border border-gray-200
                  rounded
                  leading-tight
                  focus:outline-none focus:bg-white focus:border-red-500
                "
                type="text"
                placeholder="Apellidos"
                required
              />
            </div>
          </div>
          <div class="flex flex-wrap -mx-3 mb-6">
            <div class="w-full md:w-1/2 md:px-3 mb-6 md:mb-0 relative">
              <select
                class="
                  appearance-none
                  block
                  w-full
                  text-gray-700
                  border border-gray-200
                  rounded
                  form-select
                  block
                  w-full
                  focus:outline-none focus:bg-white focus:border-red-500
                "
                required
              >
                <option selected>Seleccionar</option>
                <option value="DNI">DNI</option>
                <option value="CE">C.E</option>
              </select>
              <div
                class="
                  pointer-events-none
                  absolute
                  inset-y-0
                  right-10
                  md:bottom-4
                  bottom-0
                  flex
                  items-center
                  px-1
                  text-gray-700
                "
              >
                <svg
                  class="fill-current h-4 w-4"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 20 20"
                >
                  <path
                    d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z"
                  />
                </svg>
              </div>
            </div>
            <div class="w-full md:w-1/2 md:px-3">
              <input
                v-model="form.documento"
                required
                min="11111111"
                class="
                  appearance-none
                  block
                  w-full
                  text-gray-700
                  border border-gray-200
                  rounded
                  leading-tight
                  focus:outline-none focus:bg-white focus:border-red-500
                "
                type="number"
                placeholder="Documento"
              />
            </div>
          </div>
          <div class="flex flex-wrap -mx-3 mb-6">
            <div class="w-full md:w-1/2 md:px-3 mb-6 md:mb-0">
              <input
                class="
                  appearance-none
                  block
                  w-full
                  text-gray-700
                  border border-gray-200
                  rounded
                  leading-tight
                  focus:outline-none focus:bg-white focus:border-red-500
                "
                type="email"
                placeholder="Email"
                required
              />
            </div>
            <div class="w-full md:w-1/2 md:px-3">
              <input
                v-model="form.telefono"
                class="
                  appearance-none
                  block
                  w-full
                  text-gray-700
                  border border-gray-200
                  rounded
                  leading-tight
                  focus:outline-none focus:bg-white focus:border-red-500
                "
                type="number"
                min="9999"
                placeholder="Teléfono"
                required
              />
            </div>
          </div>
          <div class="flex flex-wrap -mx-3 mb-6">
            <div
              class="
                w-full
                md:w-1/2 md:px-3
                lg:mb-6
                md:mb-0
                px-2
                md:text-right md:py-2
              "
            >
              <span class="label-form">Grado Académico*</span>
            </div>
            <div class="w-full md:w-1/2 md:px-3 relative">
              <select
                v-model="form.gradoAcademico"
                class="
                  appearance-none
                  block
                  w-full
                  text-gray-700
                  border border-gray-200
                  rounded
                  form-select
                  block
                  w-full
                  focus:outline-none focus:bg-white focus:border-red-500
                "
                required
              >
                <option selected>Seleccionar</option>
                <option value="universidad">Univesitario</option>
                <option value="instituto">Instituto</option>
                <option value="postgrado">Postgrado</option>
              </select>
              <div
                class="
                  pointer-events-none
                  absolute
                  inset-y-0
                  right-10
                  md:bottom-4
                  bottom-0
                  flex
                  items-center
                  px-1
                  text-gray-700
                "
              >
                <svg
                  class="fill-current h-4 w-4"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 20 20"
                >
                  <path
                    d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z"
                  />
                </svg>
              </div>
            </div>
          </div>
          <div class="flex flex-wrap -mx-3 mb-6">
            <div
              class="
                w-full
                md:w-1/2 md:px-3 md:mb-6 md:mb-0 md:text-right
                py-2
                px-2
              "
            >
              <span class="label-form">Años de Experiencia Laboral</span>
            </div>
            <div class="w-full md:w-1/2 md:px-3 relative">
              <select
                v-model="form.experiencia"
                class="
                  appearance-none
                  block
                  w-full
                  text-gray-700
                  border border-gray-200
                  rounded
                  form-select
                  block
                  w-full
                  focus:outline-none focus:bg-white focus:border-red-500
                "
                required
              >
                <option selected disabled hidden>Seleccionar</option>
                <option value="1-3years">1-3 años</option>
                <option value="3-5years">3-5 años</option>
                <option value="5+years">5+ años</option>
              </select>
              <div
                class="
                  pointer-events-none
                  absolute
                  inset-y-0
                  right-10
                  md:bottom-4
                  bottom-0
                  flex
                  items-center
                  px-1
                  text-gray-700
                "
              >
                <svg
                  class="fill-current h-4 w-4"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 20 20"
                >
                  <path
                    d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z"
                  />
                </svg>
              </div>
            </div>
          </div>
          <div class="flex flex-wrap -mx-3 mb-6">
            <div
              class="
                w-full
                md:w-1/2 md:px-3 md:mb-6 md:mb-0 md:text-right
                py-2
                px-2
              "
            >
              <span class="label-form">Campo de Maestria de Elección</span>
            </div>
            <div class="w-full md:w-1/2 md:px-3 relative">
              <select
                v-model="form.maestria"
                class="
                  appearance-none
                  block
                  w-full
                  text-gray-700
                  border border-gray-200
                  rounded
                  form-select
                  block
                  w-full
                  focus:outline-none focus:bg-white focus:border-red-500
                "
                required
              >
                <option selected disabled hidden>Seleccionar</option>
                <option value="Direccion de Marketing">
                  Dirección de Marketing
                </option>
                <option value="Supply ChainManagement">
                  Supply Chain Management
                </option>
                <option value="Tecnología de la Información">
                  Tecnología de la Información
                </option>
                <option value="Administración de la Energía">
                  Administración de la Energía
                </option>
                <option value="Gerencia del Desarrollo Competitivo Regional">
                  Gerencia del Desarrollo Competitivo Regional
                </option>
              </select>
              <div
                class="
                  pointer-events-none
                  absolute
                  inset-y-0
                  right-10
                  md:bottom-4
                  bottom-0
                  flex
                  items-center
                  px-1
                  text-gray-700
                "
              >
                <svg
                  class="fill-current h-4 w-4"
                  xmlns="http://www.w3.org/2000/svg"
                  viewBox="0 0 20 20"
                >
                  <path
                    d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z"
                  />
                </svg>
              </div>
            </div>
          </div>
          <div class="checkbox-form text-center form-section-2">
            <label class="text-center flex check-section">
              <input
                v-model="form.check1"
                type="checkbox"
                class="form-checkbox"
              />
              <div class="conditions text-left">
                <span class="check-title"
                  >Autorización para el uso de datos personales* </span
                ><br />
                <span class="check-txt">
                  Autorizo a la Pontificia Universidad Católica del Perú a
                  utilizar mis datos<br />
                  personales para los fines mencionados.</span
                >
              </div>
            </label>
          </div>
          <div class="checkbox-form text-center">
            <label class="text-center flex check-section">
              <input
                v-model="form.check2"
                type="checkbox"
                checked
                class="form-checkbox"
              />
              <div class="conditions text-left">
                <span class="check-title"
                  >Autorización para el envío de información </span
                ><br />
                <span class="check-txt"
                  >Autorizo a la Pontificia Universidad Católica del Perú a
                  enviarme información sobre<br />sus programas
                  académicos.</span
                >
              </div>
            </label>
          </div>
          <div class="flex justify-center btn-wrap">
            <button class="text-white btn-form">ENVIAR</button>
          </div>
        </form>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      titleForm: 'Solicita más información AQUÍ',
      form: {
        nombre: '',
        apellidos: '',
        document: '',
        telefono: '',
        gradoAcademico: 'Seleccionar',
        experiencia: 'Seleccionar',
        maestria: 'Seleccionar',
        check1: false,
        check2: true,
      },
    }
  },
  methods: {
    enviarForm() {
      console.log(this.form)
    },
  },
}
</script>
<style scoped>
.btn-wrap {
  filter: drop-shadow(0px 4px 4px rgba(0, 0, 0, 0.25));
}
.tag-wrap {
  filter: drop-shadow(3px 11px 54px rgba(0, 0, 0, 0.35));
  position: absolute;
  top: -12%;
}
.tag {
  width: 576px;
  background: #3b69fa;
  color: white;
  padding: 34px 60px 34px 83px;
  clip-path: polygon(0 0, 100% 0, 67% 100%, 0% 100%);
  font-weight: 600;
  font-size: 50px;
  line-height: 50px;
  position: absolute;
  top: -8%;
}
@media (min-width: 900px) {
  .btn-wrap {
    margin-top: 75px;
  }
}
@media (max-width: 1000px) {
  .tag-wrap {
    filter: none !important;
    position: absolute;
    top: -30px;
  }
  .tag {
    width: 227px !important;
    font-size: 18px !important;
    line-height: 18px !important;
    padding: 10px 40px 3px 16px !important;
  }
}
@media (max-width: 850px) {
  .form-select {
    padding-right: 1rem !important;
  }
  .check-txt {
    font-size: 12px !important;
    line-height: 14.4px !important;
    padding-right: 25px !important;
  }
  .btn-form {
    margin-top: 30px !important;
    box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25) !important;
  }
  .check-section {
    margin-left: 0px !important;
  }
  .label-form {
    padding-top: 0px !important;
  }
  .form-content input {
    padding: 11px 26px 7px 20px !important;
  }
  .form-select {
    padding: 11px 26px 7px 20px !important;
  }
  .form-section {
    padding: 60px 28px 80px 28px;
  }
  .form-title {
    font-size: 18px !important;
    text-transform: uppercase;
    margin-left: -10px !important;
    padding-bottom: 10px !important;
    font-weight: 400;
  }
  .form-content {
    padding: 51px 29px 24px 29px !important;
    box-shadow: -2px -3px 45px 20px rgba(0, 0, 0, 0.1) !important;
  }
}
.btn-form {
  clip-path: polygon(0 0, 100% 0, 87% 100%, 0% 100%);
  background: #ff6400;
  box-shadow: 0px 4px 4px rgba(0, 0, 0, 0.25);
  padding: 15px 120px 13px 80px;
  text-align: center;
  font-size: 24px;
  font-weight: 600;
}
.check-section {
  margin-left: 8rem;
}
.form-section-2 {
  padding-top: 3.6rem;
}
.form-checkbox {
  margin-right: 24px;
}
.check-title {
  font-weight: 600;
  font-size: 16px;
}
.check-txt {
  font-size: 16px;
  line-height: 19px;
}
.label-form {
  font-size: 20px;
  font-weight: 500;
  color: #363661;
  padding-top: 10px;
}
.form-content {
  max-width: 825px;
  padding-top: 10rem;
  padding-bottom: 4.4rem;
}
.form-content h3 {
  font-weight: 400;
  font-size: 1.8rem;
  color: #363661;
}

.form-content input {
  border-radius: 41px !important;
  background: #e8ebf0;
  padding: 17px 22px 16px 54px;
}
.form-select {
  border-radius: 41px;
  background: #e8ebf0;
  color: #a4a4bf !important;
  padding: 12px 22px 16px 54px;
  border-radius: 41px !important;
}
::placeholder {
  color: #a4a4bf;
  font-size: 1.11rem;
}
.form-section {
  background: #e8ebf0;
  padding-top: 10.8rem;
}
.form-container {
  max-width: 1464px;
  background: #ffffff;
}
option {
  background: white;
  border: none;
}
</style>

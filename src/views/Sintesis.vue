<template lang="pug">
.curso-main-container.creditos-vista
  BannerInterno.text-uppercase(:titulo="'unidad 1. Introducción al trabajo en modalidad virtual'" :subTitulo="'SÍNTESIS'")
  .container.tarjeta.tarjeta--blanca.p-4.p-md-5
    p.fs-18px.mb-4.mb-md-5 En esta unidad 1: Introducción al trabajo en modalidad virtual, se exploran tres temas clave para el éxito en el aprendizaje virtual, alineados con el objetivo de desarrollar competencias digitales y habilidades de autoformación. El aprendizaje en línea ha revolucionado el acceso a la educación, superando limitaciones geográficas y de tiempo mediante el uso de tecnologías digitales. Sin embargo, presenta retos como la gestión eficaz del tiempo y la interacción constante entre estudiantes y docentes.
    figure
      img(src='@/assets/componentes/sintesis.png', alt='Texto que describa la imagen')
    

</template>
<script>
import BannerInterno from '../components/plantilla/BannerInterno'
import Footer from '../components/plantilla/Footer'
export default {
  name: 'Creditos',
  components: {
    BannerInterno,
    Footer,
  },
  data: () => ({
    configTitulos: {
      liderEquipo: 'ECOSISTEMA DE RECURSOS EDUCATIVOS DIGITALES',
      contenidoInstruccional: 'CONTENIDO INSTRUCCIONAL',
      desarrolloProducto:
        'DISEÑO Y DESARROLLO DE RECURSOS EDUCATIVOS DIGITALES',
      gestoresRepositorio: 'GESTORES DE REPOSITORIO',
    },
  }),
  computed: {
    creditosData() {
      return this.$config.creditos
    },
    creditosAdicionales() {
      return this.$config.creditosAdicionales
    },
  },
  methods: {
    renderText(textObj) {
      let newText = ''
      if (Array.isArray(textObj)) {
        textObj.forEach((texto, index) => {
          newText += (index ? '<br/>' : '') + texto
        })
      } else {
        newText += textObj
      }
      return newText
    },
  },
}
</script>

<style lang="sass">
.creditos-vista
  .tarjeta.credito
    background-color: $color-sistema-d

.creditos
  color: $color-sistema-b
  overflow-x: auto

  &__item
    min-width: 490px

  p
    line-height: 1.3em
    margin-bottom: 0
    color: $color-sistema-b

  &__titulo
    font-weight: $base-bold-font-weight
    background-color: $color-sistema-d
    padding: 5px 10px
    border-top-radius: $base-border-radius
    border-top-left-radius: $base-border-radius
    border-top-right-radius: $base-border-radius
  table
    td, th
      border-color: $color-sistema-d
</style>

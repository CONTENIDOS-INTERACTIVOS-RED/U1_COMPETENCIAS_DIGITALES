<template lang="pug">
  .curso-main-container.pb-3
    BannerInterno(icono="far fa-question-circle" titulo="Actividad didáctica")
    .container.tarjeta.tarjeta--blanca.p-4.p-md-5
  
      #Actividad                
        <Actividad :cuestionario="cuestionario"/>
  
  </template>

<script>
import Actividad from '@/components/actividad/Actividad.vue'
export default {
  name: 'ActividadDidactica',
  components: {
    Actividad,
  },
  data: () => ({
    cuestionario: {
      tema: 'Aprendizaje Virtual y Herramientas Digitales',
      titulo: 'Ponte a prueba',
      introduccion:
        'Demuestra lo que aprendiste en esta unidad y pon a prueba tus conocimientos.',
      barajarPreguntas: true,
      preguntas: [
        {
          id: 1,
          texto:
            '¿Cuál de los siguientes factores es crítico para el éxito en el aprendizaje en línea?',
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Memorizar todo el contenido',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Planificación y organización',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Asistencia física a una institución',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Cumplir con los encuentros sincrónicos',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 2,
          texto:
            '¿Cuál de estas herramientas es útil para almacenar y compartir documentos en línea?',
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Microsoft Word', esCorrecta: false },
            { id: 'b', texto: 'Google Drive', esCorrecta: true },
            { id: 'c', texto: 'Bloc de notas', esCorrecta: false },
            { id: 'd', texto: 'Google Meet', esCorrecta: false },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 3,
          texto:
            '¿Qué función cumple un "chat" en un entorno virtual de aprendizaje?',
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Descargar archivos', esCorrecta: false },
            {
              id: 'b',
              texto: 'Comunicación rápida entre estudiantes y docentes',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Organizar el perfil del usuario',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Subir las evidencias del curso',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 4,
          texto:
            '¿Cuál de estas herramientas permite crear encuestas o cuestionarios en línea?',
          barajarRespuestas: true,
          opciones: [
            { id: 'a', texto: 'Canva', esCorrecta: false },
            { id: 'b', texto: 'Google Forms', esCorrecta: true },
            { id: 'c', texto: 'Excel', esCorrecta: false },
            { id: 'd', texto: 'Microsoft Word', esCorrecta: false },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
        {
          id: 5,
          texto: '¿Qué técnica es efectiva para mejorar la gestión del tiempo?',
          barajarRespuestas: true,
          opciones: [
            {
              id: 'a',
              texto: 'Estudiar sin descanso hasta terminar',
              esCorrecta: false,
            },
            {
              id: 'b',
              texto: 'Utilizar la técnica Pomodoro',
              esCorrecta: true,
            },
            {
              id: 'c',
              texto: 'Trabajar en múltiples actividades al mismo tiempo',
              esCorrecta: false,
            },
            {
              id: 'd',
              texto: 'Estudiar siempre los fines de semana',
              esCorrecta: false,
            },
          ],
          mensaje_correcto: '¡Muy bien! Ha acertado la respuesta.',
          mensaje_incorrecto: 'Lo sentimos, su respuesta no es la correcta.',
        },
      ],
      mensaje_final_aprobado: '¡Excelente! Ha superado la actividad.',
      mensaje_final_reprobado:
        'Le recomendamos volver a revisar el componente formativo e intentar nuevamente la actividad didáctica.',
    },
  }),
}
</script>

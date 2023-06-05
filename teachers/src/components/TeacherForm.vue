<script lang="ts" setup>
import { type Ref, ref } from 'vue'

interface ITeacher {
  teacherName: string,
  surname: string,
  dni: string,
  subjects: Array<string>,
  docs: boolean
}

let teacher:Ref<ITeacher> = ref({
  teacherName: '',
  surname: '',
  dni: '',
  subjects: [],
  docs: false
})

let teachers:Ref<Array<ITeacher>> = ref([]);

let subject:Ref<string> = ref('')

const handleSubject = () => {
  teacher.value.subjects.push(subject.value)
  subject.value =  ''
}

const handleTeachers = () => {
  teachers.value.push({
    teacherName: teacher.value.teacherName,
    surname: teacher.value.surname,
    dni: teacher.value.dni,
    subjects: teacher.value.subjects,
    docs: teacher.value.docs
  })
  teacher.value.teacherName = ''
  teacher.value.surname = ''
  teacher.value.dni = ''
  teacher.value.subjects = []
  teacher.value.docs = false
}
</script>

<template>
  <section>
    <h3>Añadir Profesor</h3>
    <div><label>Nombre: <input type="text" v-model="teacher.teacherName" /></label></div>
    <div><label>Apellido: <input type="text" v-model="teacher.surname" /></label></div>
    <div><label>DNI / NIF: <input type="text" v-model="teacher.dni" /></label></div>
    <div><label>Materias: <input type="text" v-model="subject" /></label> <button @click="handleSubject()" >Agregar</button></div>
    <div>
      <ul>
        <li v-for="(subj, index) in teacher.subjects" :key="index" >{{ subj }}</li>
      </ul>
    </div>
    <input type="checkbox" v-model="teacher.docs" />Documentación Entregada
    <button @click="handleTeachers()">Agregar</button>
  </section>
  <section>
    <h2>Listado de Profesores:</h2>
    <table>
      <tr>
        <th>Nombres</th>
        <th>Apellidos</th>
        <th>DNI</th>
        <th>Materias</th>
        <th>Documentación Entregada</th>
      </tr>
      <tr v-for="t in teachers" :key="t.dni">
        <th>{{ t.teacherName }}</th>
        <th>{{ t.surname }}</th>
        <th>{{ t.dni }}</th>
        <th>
          <ul>
            <li v-for="(m, index) in t.subjects" :key="index">{{ m }}</li>
          </ul>
        </th>
        <th v-if="t.docs">Entregado</th>
        <th v-else>No entregado</th>
      </tr>
    </table>
  </section>
</template>

<style scoped></style>
<template>
	<div class="row planes">
		<div
			class="col-12 col-sm-6 col-md-6 col-lg-3 my-3"
			v-for="(item, index) of planes"
			v-bind:key="index"
		>
			<Plan v-bind:nombre="item" @selection="seleccionado"/>
		</div>
	</div>
</template>
<script>
  import Plan from './Plan'
	export default {
    name: 'Planes',
    components: {
      Plan
    },
    data() {
			return {
				planes: [
					'Plan 1 - Principiante',
					'Plan 2 - Intermedio',
					'Plan 3 - Avanzado',
					'Plan 4 - Experto',
				],
        planSeleccionado: null
			}
		},
    methods: {
      seleccionado: function( plan ){
        this.planSeleccionado = plan;
      }
    }
  }
</script>
<style scoped>
  .planes .plan.seleccionado{
    background-color: lightgreen;
    transition: background-color 0.3s ease-in-out;
  }
</style>

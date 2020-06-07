<template>
	<div class="plan" @click="aumentar();seleccionarPlan()" :class="{'seleccionado':seleccionado}">
		<span class="nombre">{{ nombre }}</span>
		<span class="cantidad ml-4 font-weight-bold">{{ cantidad }}</span>
	</div>
</template>
<script>
	export default {
		name: 'Plan',
		data() {
			return {
				cantidad: 0,
        seleccionado: false
			}
		},
		methods: {
			aumentar: function() {
				this.cantidad += 1
			},
      seleccionarPlan: function() {
        this.$emit('selection', this.nombre);
        this.seleccionado = true;
      }
		},
		props: {
			nombre: {
				type: String,
				default: 'Plan 1 - Principiante',
				required: true,
			},
		},
	}
</script>
<style scoped>
	.plan {
		background-color: #f2f2f2;
		padding: 10px 5px;
		margin: 2px;
		border-radius: 5px;
		box-shadow: 0px 1px 2px 0px #b2b2b2;
		transition: box-shadow 0.3s ease-in-out;
	}
	.plan:hover {
		box-shadow: 0px 3px 5px 0px #b2b2b2;
		cursor: pointer;
	}
	.nombre::after {
		content: ':';
	}
</style>

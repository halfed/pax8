<template>
	<div>
		<ul v-for="company in companyList" :key="company.id">
			<li>{{ company.id }}</li>
			<li>{{ company.name }}</li>
			<li><router-link :to="'/edit-company/'+company.id">Edit</router-link></li>
		</ul>
	</div>
</template>

<script>
export default {
	name: 'DisplayList',
	props: ['companyList'],
	data() {
		return {
			company: ''
		}
	}
}
</script>

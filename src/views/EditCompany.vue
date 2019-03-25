<template>
	<div>
		<h2>Edit Company</h2>
		<form>
			<div>
				<label>Name: </label>
				<input name="name" type="text" />
			</div>
			<div>
				<label>Domain: </label>
				<input name="domain" type="text" />
			</div>
			<div>
				<label>Number of Employees: </label>
				<input name="number-of-employees" type="text" />
			</div>
			<div>
				<label>Subscriptions Per Employee</label>
				<input name="subscriptions-per-employee" type="text" />
			</div>
		</form>
	</div>
</template>

<script>
import GetById from '../services/CompanyService';
export default {
	name: 'edit-company',
	data() {
		return {
			routeParam: this.$route.params.company_id,
			companys: []
		}
	},
	methods: {
		getCompanyDetails(companyId) {
			const promise = GetById.getById(parseInt(companyId))
  			.then(company => {
  			return company;
  			});
		}
	},
	created() {
		this.getCompanyDetails(this.$route.params.company_id);
	},
	watch: {
		'$route.params.company_id': function(companyId) {
			this.getCompanyDetails(companyId)
		}
	}

}
</script>

<style>
</style>

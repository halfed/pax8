<template>
	<div>
		<h1>This is the home page</h1>
  		<div>
  			<display-list :companyList="companies"/>
  			
  		</div>
	</div>
  
  
</template>

<script>
import DisplayList from '../components/DisplayList.vue';
import GetAll from '../services/CompanyService';
export default {
  name: 'home',
  components: {
  	DisplayList
  },
  data() {
  	return {
  		companies: []
  	}
  },
  created() {
  	this.getCompanies();
  },
  methods: {
  	getCompanies() {
  		const promise = GetAll.getAll()
  		.then(companies => {
  			this.companies = companies;
  		});
  	}
  }
};
</script>

<template>
	<section>

			<el-steps :space="300" :active="active" :align-center='true' finish-status="success">
			  <el-step title="步骤 1111"></el-step>
			  <el-step title="步骤 2"></el-step>
			  <el-step title="步骤 3"></el-step>
			</el-steps>
			<el-button style="margin-top: 12px;" @click="next">下一步</el-button>

	</section>

  </template>

  <script>
    export default {
    data() {
      return {
        active: 1
      };
    },

    methods: {
      next() {
        if (this.active++ > 2) this.active = 0;
        console.log(this.active)
      }
    }
  }
  </script>
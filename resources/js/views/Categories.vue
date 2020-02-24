<template>
  <div class="container-fluid">
    <h1 class="mt-4">Dashboard</h1>
    <ol class="breadcrumb mb-4">
      <router-link to="/">Dashboardd</router-link>
    </ol>

    <div class="row">
      <div class="col-xl-12">
        <div class="card mb-4">
          <div class="card-header d-flex">
            <span>
              <i class="fas fa-chart-area mr-1"></i>
              Categories Menagemen
            </span>
            <button class="btn btn-primary btn-sm ml-auto" v-on:click="showNewCategoryModal">
              <span class="fa fa-plus"></span>Create New
            </button>
          </div>
          <div class="card-body">
            <table class="table">
              <thead>
                <tr>
                  <td>ID</td>
                  <td>Name</td>
                  <td>Image</td>
                  <td>Action</td>
                </tr>
              </thead>
              <tbody>
                <td>1</td>
                <td>shirt</td>
                <td>image</td>
                <td>
                  <button class="btn btn-primary btn-sm">
                    <span class="fa fa-edit"></span>
                  </button>
                  <button class="btn btn-denger btn-sm">
                    <span class="fa fa-trash"></span>
                  </button>
                </td>
              </tbody>
            </table>
          </div>
        </div>
      </div>
    </div>

    <b-modal ref="NewCategoryModal" hide-footer title="Add New Category">
      <div class="d-block">
        <form v-on:submit.prevent="createCategory">
          <div class="form-group">
            <label for="name">Enter Name</label>
            <input
              type="text"
              v-model="categoryData.name"
              class="form-control"
              id="name"
              placeholder="Enter category name"
            />
          </div>

          <div class="form-group">
            <label for="image">Choose an image</label>
            <input type="file" v-on:change="attachImage" class="form-control" id="image" />
          </div>

          <hr />

          <div class="text-right">
            <button type="button" class="btn btn-default" v-on:cllck="hideNewCategoryModal">Cancel</button>
            <button type="submit" class="btn btn-primary">
              <span class="fa fa-check">Save</span>
            </button>
          </div>
        </form>
      </div>
    </b-modal>
  </div>
</template>

<script>
export default {
  name: "category",
  data() {
    return {
      categoryData: {
        name: "",
        image: ""
      }
    };
  },
  methods: {
    attachImage() {},
    hideNewCategoryModal() {
      this.$refs.NewCategoryModal.hide();
    },
    showNewCategoryModal() {
      this.$refs.NewCategoryModal.show();
    },
    createCategory() {
      console.log("form submitted");
    }
  }
};
</script>

<style>
</style>

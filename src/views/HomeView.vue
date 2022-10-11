<template>
  <div class="container" style="padding-top: 25px;">
        <div class="row">
            <div class="col-12 text-center">
                <h3 class="pt-3">Lütfen Sidebardan gitmek istediğiniz bölümü seçiniz.</h3>
                <h3 class="pt-3">Sol alt kısımdaki ok işaretine tıklayarak, sidebar'ı açabilirsiniz.</h3>
            </div>
            <div>{{ categories }}</div>
        </div>
        <div class="row">
            <div v-for="category of categories" :key="category.id" class="col-12 pt-3 col-xl-4 col-md-6 d-flex">
                <CategoryBox :category="category"></CategoryBox>
            </div>
        </div>
    </div>
</template>

<script>
import { collapsed, toggleSidebar} from '@/components/sidebar/state'

export default {
  name: 'HomeView',
  components: {
  },
  setup() {
    return { collapsed, toggleSidebar}
  }
};
</script>

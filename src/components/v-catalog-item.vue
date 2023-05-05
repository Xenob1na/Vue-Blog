<template>
    <div class='v-catalog-item-wrapper'>
        <div class="gap">
            <div class="card">
                <img class="card-img-top" src="../assets/images/placeholder-blue.png" alt="placeholder">
                <div class="card-body">
                    <p class="card-text">
                        <small class="text-muted">{{ product_data.date }}</small>
                    </p>

                    <h5 class="card-title">{{ product_data.name }}</h5>
                    <p class="card-text">{{ product_data.description }}</p>
                    

                    <!-- <RouterLink :to="'/post/' + product_data.name" class="btn btn-primary">Читать</RouterLink> -->
                    <RouterLink :to="{path: `/post/${product_data.id}`}"    class="btn btn-primary">Читать</RouterLink>
                </div>
            </div>
        </div>
    
    </div>
</template>


<script>
export default {
    name: 'v-catalog-item',
    components: {

    },
    props: {
        product_data: {
            type: Object,
            default() {
                return {

                }
            }
        }
    },
    data() {
        return {
            
        }
    },
}
</script>


<style >

.gap {
    margin-right: 20px;
}
</style>
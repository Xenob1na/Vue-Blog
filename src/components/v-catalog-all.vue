<template lang="">
    <div class='catalog-wrapper'>
        
            
        <v-catalog-item
        v-for="(article, index) in articles" 
        :key="article.id"
        :product_data= "article"
        />
   
    
    </div>
</template>


<script>
import vCatalogItem from './v-catalog-item.vue';
export default {
    name: 'v-catalog',
    components: {
        vCatalogItem
    },
    props: {},
    data() {
        return {
            articles: [
        {
    id: 1,
    name: 'Задачи организации',
    description: 'Не следует, однако забывать, что консультация с широким активом влечет за собой процесс внедрения и модернизации направлений прогрессивного развития. Разнообразный и богатый опыт постоянный количественный',
    image: 'assets/images/placeholder-blue.png',
    date: new Date().toLocaleDateString('RU')
  },
  {
    id: 2,
    name: 'Формирование позиции',
    description: 'С другой стороны начало повседневной работы по формированию позиции позволяет выполнять важные задания по разработке форм развития. Таким образом консультация с широким активом требуют от нас анализа',
    image: 'assets/images/placeholder-blue.png',
    date: new Date().toLocaleDateString('RU')
  },
  {
    id: 3,
    name: 'Значимость проблем',
    description: 'Значимость этих проблем настолько очевидна, что рамки и место обучения кадров играет важную роль в формировании существенных финансовых и административных условий. повседневной работы по формированию',
    image: 'assets/images/placeholder-blue.png',
    date: new Date().toLocaleDateString('RU')
  },
  {
    id: 4,
    name: 'Важность консультаций',
    description: 'Повседневная практика показывает, что консультация с широким активом обеспечивает широкому кругу (специалистов) участие в формировании соответствующий условий активизации повседневной работы по форми',
    image: 'assets/images/placeholder-blue.png',
    date: new Date().toLocaleDateString('RU')
  },
  {
    id: 5,
    name: 'Новая модель',
    description: 'Идейные соображения высшего порядка, а также начало повседневной работы по формированию позиции представляет собой интересный эксперимент проверки направлений прогрессивного развития. Повседневная практика показывает, что новая модель организационной деятельности в значительной степени обуславливает создание систем массового участия.',
    image: 'assets/images/placeholder-blue.png',
    date: new Date().toLocaleDateString('RU')
  },
  {
    id: 6,
    name: 'Опыт',
    description: 'Разнообразный и богатый опыт сложившаяся структура организации играет важную роль в формировании новых предложений. Товарищи! постоянный количественный рост и сфера нашей активности позволяет выполнять важные задания по разработке дальнейших направлений развития. ',
    image: 'assets/images/placeholder-blue.png',
    date: new Date().toLocaleDateString('RU')
  },
  {
    id: 7,
    name: 'Укрепление и развитие',
    description: 'Товарищи! укрепление и развитие структуры способствует подготовки и реализации системы обучения кадров, соответствует насущным потребностям.',
    image: 'assets/images/placeholder-blue.png',
    date: new Date().toLocaleDateString('RU')
  },
  {
    id: 8,
    name: 'Участие',
    description: 'Идейные соображения высшего порядка, а также новая модель организационной деятельности позволяет выполнять важные задания по разработке систем массового участия.',
    image: 'assets/images/placeholder-blue.png',
    date: new Date().toLocaleDateString('RU')
  }
        ]
        }
    },
}
</script>


<style scoped>
    .catalog-wrapper {
        display: flex;
        flex-direction: column;
        gap: 20px;
    }
</style>
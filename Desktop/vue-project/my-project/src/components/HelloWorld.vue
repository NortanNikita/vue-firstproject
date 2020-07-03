<template>
  <div class="table-container">
    <!--КОД Шапки таблицы-->
      <div class="table-header">
        <Ul class="table__list_choose">
          <li  v-for="(item, i) in items" :key="i">{{item.title}}</li>
        </Ul>
        <Ul class="table__list_values">
          <li  v-for="(value, i) in values" :key="i">{{value.title}}</li>
        </Ul>
      </div>
        <!--/КОД Шапки таблицы-->
      <div class="table-body">
        <!--КОД ПРОДУКТА-->
          <div class="table-body__item" v-for="(product, i) in products" :key="i">
            <ul class="table_item__left-side">
              <li>
                  <ul class="table_item__name">
                          <li>{{product.name}}</li>
                  </ul>
              </li>
              <li>
                  <Ul class="table_item__info">
                          <li class="table_info__type"><h4>{{product.type}}</h4></li>
                          <li class="table_info__name"><h2>{{product.name}}</h2></li>
                          <li class="table_info__percents">{{product.percents}}</li>
                  </Ul>
              </li>
            </ul>
            <ul class="table_item__right-side">
              <li v-for="(figure, i) in figures" :key="i">
                  <ul class="table_item_figures">
                    <li>{{figure.info}}</li>
                    <li>-</li>
                  </ul>
              </li>
            </ul>
          </div>
          <!--/КОД ПРОДУКТА-->
      </div>
  </div>
</template>

<script>
export default {
    data: () => ({
        items: [
            {
                title: 'Sativa'
            },
            {
                title: 'Hybrid'
            },
            {
                title: 'Indica'
            },
        ], 
        values: [
            {
                title: '1 gram'
            },
            {
                title: '2 gram'
            },
            {
                title: '1/8 oz'
            },
            {
                title: '1/4 oz'
            },
            {
                title: '1/2 oz'
            },
            {
                title: '1 oz'
            },
        ],
        products: [
            {
                name: 'Artem',
                type: 'Indica',
                percents: 'THC 10% CBD 5%',

            },
            {
                name: 'Artem',
                type: 'Indica',
                percents: 'THC 10% CBD 5%',

            },
            {
                name: 'Artem',
                type: 'Indica',
                percents: 'THC 10% CBD 5%',

            },
            {
                name: 'Artem',
                type: 'Indica',
                percents: 'THC 10% CBD 5%',

            }
        ],
        figures: [
            {
                info: '1 gram'
            },
            {
                info: '2 gram'
            },
            {
                info: '1/8 oz'
            },
            {
                info: '1/4 oz'
            },
            {
                info: '1/2 oz'
            },
            {
                info: '1 oz'
            },
        ]
    })
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1,h2,h3,h4,h5,h6{
  padding: 0;margin:0;
}
.table-container{
  padding: 50px;
}
.table-header{
  background: rgb(242,242,242);
  height: 50px;
  border:1px solid rgb(229,229,229);
  border-bottom: none;
  display: flex;
  justify-content: space-between;
  padding-left: 20px;
  padding-right: 20px;
}
.table__list_choose{
  display:flex;
}
.table__list_values{
  display:flex;
  
}
.table-body__item{
  display: flex;
  justify-content: space-between;
  border:1px solid rgb(229,229,229);
  border-top: none;
}
.table_item__left-side{
  display: flex;
}
.table_item__name{
    text-align: center;
    font-weight: bold;
    padding-top: 20px;
}
.table_item__info{
  display:grid;
}
.table_item_figures{
  display: grid;
}

ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}

</style>

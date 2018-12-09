<template>
    <div>
        <div class="BarChart"></div>
    </div>
</template>


<script>
import bb from 'billboard.js'
export default{
	name: "BarChart",
	components:{},
	props:['rest-s'],
	data: function(){
		return{
			columns: [
              ["data1", 30, 200, 100, 170, 150, 250],
              ["data2", 130, 100, 140, 35, 110, 50]
          ],
	}

    },
    mounted: function(){
        bb.generate(
            {
                bindto: ".BarChart",
                data: {
                    type: "bar",
                    columns: this.data()
          
      }
            }
        );
    }
   
}

</script>

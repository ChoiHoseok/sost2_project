<template>
    <div>
        <slot></slot>
            <div class="BarChart"></div>
    </div>
</template>


<script>
import bb from 'billboard.js'
export default{
	name: "BarChart",
	components:{},
	props:['columns'],
    mounted: function(){
        let rS = this.columns
        bb.generate(
            {
                bindto: ".BarChart",
                data: {
                    type: "bar",
                    columns: rS
          
      }
            }
        );
    }
   
}

</script>

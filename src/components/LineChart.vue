<template>
    <div>
        <slot></slot>
            <div class="LineChart"></div>
    </div>
</template>


<script>
import bb from 'billboard.js'
import "billboard.js/dist/billboard.css"
export default{
	name: "LineChart",
	components:{},
	props:['columns'],
    mounted: function(){
        let rS = this.columns
        bb.generate(
            {
                bindto: ".LineChart",
                data: {
                    type: "line",
                    columns: rS
          
      }
            }
        );
    }
   
}

</script>

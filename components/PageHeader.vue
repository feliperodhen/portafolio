<template>
  <i-header fullscreen id="header" :cover="true" class="_text-center _text-white background-hero">
  
          <i-row end-xs>
      <i-column xs="6">
            <h1>Aca va un titulo fantastico</h1>
    <p>Aca va un relleno de texto expectacular</p>
    
      </i-column>
      <i-column xs="6">
         
      </i-column>
      </i-row>
 
  
    
</i-header>

</template>

<script>

export default {
    name: "PageHeader",

}
</script>

<style scoped>
#header{
      
  background: url(../assets/fondo-hero-full.png);
  background-repeat: no-repeat;
  background-position: right bottom;
  height: 718px;

}
.face-img{
    width: 518px;
    

}
</style>


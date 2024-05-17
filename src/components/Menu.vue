<template>
    <div class="menu" :class="{ 'small-menu': smallMenu }">
      <MenuItem
        v-for="(item, index) in menuTree"
        :key="index"
        :data="item.children"
        :label="item.label"
        :icon="item.icon"
        :depth="0"
       
         />
      
   
  
  </div> 
  
  </template>
  
  <script>
  import MenuItem from './MenuItem.vue';
  
  
  export default {
    name: 'recursive-menu',
    data() {
      return {
        smallMenu: false,
        menuTree: [
          {
            


            label: "ANASAYFA ",
            
            children: [
              
              {
                label: " CRM",
                
              },
              {
                label: "E-ticaret",
                
              },
              
              {
                label: "Lojistik",
                
              }
            ]
          },
          {
                label: "Analizler",
               
              },
          

          {
            label: "SAYFALAR",
           
           children: [
              {
                label: "Son Eklenenler",
               
                children: [
                  {
                    label: "Analiz Sayfaları",
                    
                    children: [
                      {
                        label: "Kullanıcı analizi",
                        
                      }
                    ]
                  }
                ]
              },
              
            ]
          },
          
          {
            label: "Ayarlar",
            
          },
          {
            label: "Çıkış",
          
          }


        ]
      };
    },
    components: {
      MenuItem,
      
    }
   
  
  };</script>
  
  <style lang="scss" scoped>
  .menu {
    
    top:20;
    position: fixed;
    height: 100vh;
    width: 240px;
    left:0 ;
    top: 0;
    border-right: 2px solid #400000;
    transition: all .3s ease;
    overflow: auto;
    background: linear-gradient(to top, #2d0134, #34011c, #130303);
    
    i {
      position: fixed;
      left: 250px;
      font-size: 20px;
      top: 15px;
      user-select: none;
      cursor: pointer;
      transition: all .3s ease;
    }
    
  
    
      }
   </style>
  
  
<template >
  <ion-grid>
  <ion-page>
    <ion-content :fullscreen="false">   
      <ion-col align-self-center>               
        <div id='imagen'><ion-img src="./assets/20945495.png" style="width: 350px; height: 350px;"></ion-img>     </div>     
            <ion-item>        
                      <ion-label position="floating"> <ion-icon :src="person"  size="medium" color="primary"> </ion-icon>
                        Usuario</ion-label>
                      <ion-input placeholder="username123"></ion-input>
                    </ion-item>
                              
            <ion-item>
          <ion-label position="floating"> <ion-icon :src="lockClosed"  size="medium" color="primary"> </ion-icon>
            Contraseña</ion-label>
          <ion-input type="password" placeholder="Ingrese contraseña"></ion-input>
        </ion-item>

          <div id="ingresar">
            <ion-button>Ingresar</ion-button>
          </div>
          
          <div id="espacio"> </div>

       

      <ion-row> 
        <div id="cuenta">
        <ion-text color="azulito" style="font-size: 15px"> <p>¿No tienes una cuenta?</p></ion-text> 
      </div>
      <div id="registrate"><ion-button @click="() => router.push('/paginaRegistro')" fill="clear" color="azulo" style="font-size: ;15px ">Regístrate</ion-button>
       </div>
        
      </ion-row>
    </ion-col>    
    </ion-content>
  </ion-page>
  </ion-grid>
</template>

<script lang="ts">
import { IonContent, IonPage, IonImg, IonText, IonGrid, IonRow, IonCol, IonIcon } from '@ionic/vue';
import { lockClosed, person } from "ionicons/icons";
import { defineComponent } from 'vue';
import registro from '@/views/paginaRegistro.vue';
import {useRouter } from 'vue-router';

export default defineComponent({
  name: 'HomePage',
  components: {
    IonContent,
    IonPage,
    IonImg,
    IonText,
    IonGrid,
    IonRow,
    IonCol,
    IonIcon

    
  },
  setup() {
      const router = useRouter();
      return {person,lockClosed, router}
    
  }
});
</script>

<style scoped>

#imagen{transform: translateX(1%);}

#espacio{
  margin: 30%;
}

#ingresar {
text-align: end;
  left: 50px;
  right: 50px;
margin: 5%;
    /*transform: translateY(90%);
  transform: translateX(30%);*/

}

#cuenta {
text-align: center;
  left: 50px;
  right: 50px;
  top: 50%;

  /*transform: translateY(90%);*/
  transform: translateX(30%);

}

#registrate {
  
  text-align: center;
  left: 50px;
  right: 50px;
  top: 50%;

   /*transform: translateY(90%);*/
  transform: translateX(30%);
}


#container {
  

  display: flex;
  align-content: flex-start;
  text-align: center;
  left: 50px;
  right: 50px;
  top: 50%;
  transform: translateY(-50%);
}

#container strong {
  font-size: 20px;
  line-height: 26px;
}

#container p {
  
  font-size: 16px;
  line-height: 22px;
  
  color: #8c8c8c;
  
  margin: 0;
}

#container a {
  text-decoration: none;
}
</style>
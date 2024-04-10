<script>
// const router = useIonRouter();
// const goBack = router.back();

export default {
  data() {
    return {
      featuredContent: [
        /* Array of featured movies or TV shows */
      ],
      trendingContent: [
        /* Array of trending movies or TV shows */
      ],
      categories: ["Action", "Comedy", "Drama", "Sci-Fi", "Horror"], // Example categories
      // methods: {
      //   navigateToProfilePage() {
      //     // Example: Navigate to the profile page
      //     router.push("/profile");
      //   },
      // },
    };
  },
  // Fetch data when the component is mounted
  mounted() {
    // Example: Fetch featuredContent, trendingContent, and categories from API
    // Once data is fetched, update the respective data properties
  },
};
</script>

<template>
  <IonPage>
    <!-- Header -->
    <IonHeader>
      <IonToolbar color="primary">
        <IonButtons class="justify-center object-left">
          <IonButton onclick="navigateToProfilePage">
            <IonIcon :icon="ioniconsPersonCircleOutline"></IonIcon>
          </IonButton>
        </IonButtons>
        <IonTitle>Home</IonTitle>
      </IonToolbar>
    </IonHeader>

    <!-- Content -->
    <IonContent class="ion-padding">
      <!-- Featured Content -->
      <IonCard>
        <IonCardHeader> Featured Content </IonCardHeader>
        <IonCardContent>
          <!-- Display featured movies or TV shows -->
          <IonList>
            <IonItem v-for="(item, index) in featuredContent" :key="index">
              <IonLabel>{{ item.title }}</IonLabel>
            </IonItem>
          </IonList>
        </IonCardContent>
      </IonCard>

      <!-- Trending Content -->
      <IonCard>
        <IonCardHeader> Trending </IonCardHeader>
        <IonCardContent>
          <!-- Display trending movies or TV shows -->
          <IonList>
            <IonItem v-for="(item, index) in trendingContent" :key="index">
              <IonLabel>{{ item.title }}</IonLabel>
            </IonItem>
          </IonList>
        </IonCardContent>
      </IonCard>

      <!-- Categories -->
      <IonCard>
        <IonCardHeader> Categories </IonCardHeader>
        <IonCardContent>
          <!-- Display categories such as Action, Comedy, Drama, etc. -->
          <IonList>
            <IonItem v-for="(category, index) in categories" :key="index">
              <IonLabel>{{ category }}</IonLabel>
            </IonItem>
          </IonList>
        </IonCardContent>
      </IonCard>
    </IonContent>
  </IonPage>
</template>

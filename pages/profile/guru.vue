<!-- <script setup>
useHead({
  title: "Data Pendidik",
  meta: [
    {
      name: "description",
      content: "Halaman Data Pendidik",
    },
  ],
});

const supabase = useSupabaseClient();

const dataGuru = ref([]);

const getData = async () => {
  const { data } = await supabase
    .from("data_guru")
    .select(`*`)
    .order("id", { ascending: true });
  if (data) dataGuru.value = data;
};

onMounted(() => {
  getData();
});
</script> -->

<template>
  <div class="container">
    <h4 class="text-center pt-3" style="color: #00467d !important">
      Guru & Staf SMK Negeri 4 Tasikmalaya
    </h4>
    <div class="row justify-content-center">
      <div class="col-lg-4">
        <div class="zoom-card">
          <img src="/assets/img/kepsekk.png" alt="img" />
          <div class="overlay">
            <h5 class="card-title">Kurniawan S.pd M.pd</h5>
          </div>
        </div>
      </div>
      <!-- <div class="col-lg-4" v-for="(card, index) in dataGuru" :key="index">
        <div class="zoom-card">
          <img :src="card.poto" class="card-img" alt="Card Image" />
          <div class="overlay">
            <h5 class="card-title">{{ card.nama }}</h5>
          </div>
        </div>
      </div> -->
    </div>
  </div>
</template>

<style scoped>
.zoom-card {
  width: 100%;
  max-width: 18rem;
  height: 250px;
  margin: 20px auto;
  overflow: hidden;
  border-radius: 5px;
  position: relative;
  cursor: pointer;
  transition: transform 0.4s ease-in-out;
}
.card-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: opacity 0.4s ease-in-out;
}
.overlay {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0, 0, 0, 0.6);
  color: white;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  opacity: 0;
  transform: translateY(20px);
  transition: opacity 0.4s ease-in-out, transform 0.4s ease-in-out;
}
.overlay h5 {
  font-size: 1.5rem;
  margin-bottom: 10px;
}

.overlay p {
  font-size: 1rem;
}

.zoom-card:hover .overlay {
  opacity: 1;
  transform: translateY(0);
}
</style>

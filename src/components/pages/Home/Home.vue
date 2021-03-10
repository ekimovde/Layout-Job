<template>
  <div class="home">
    <div class="container">
      <div class="sections">
        <section class="wrapp">
          <Sidebar />

          <Info />
        </section>

        <section class="footer">
          <Footer />
        </section>
      </div>
    </div>
  </div>
</template>

<script>
import "./Home.scss";
import Sidebar from "@/components/UI/Sidebar/Sidebar";
import Info from "@/components/commons/Info/Info";
import Footer from "@/components/commons/Footer/Footer";

export default {
  name: "Home",
  components: {
    Sidebar,
    Info,
    Footer,
  },
};
</script>

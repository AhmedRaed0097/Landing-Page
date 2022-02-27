<template>
  <div class="pricing-tables-container" id="pricing-tables-section">
    <h2 class="pricing-tables-title section-title mt-16 mb-16">
      PRICING TABLES
    </h2>
    <v-row class="tables-row">
      <v-col md="3" v-for="(table, index) in tables" :key="index">
        <section
          class="table-section"
          :class="{ personal: table.title === 'PERSONAL' }"
        >
          <p class="table-title">
            {{ table.title }}
          </p>
          <div class="pricing">
            <span>${{ table.pricing }}/m</span>
          </div>
          <div class="details">
            <p>
              <span>
                {{ table.storage }}
              </span>
              Storage
            </p>
            <p>
              <span>
                {{ table.clients }}
              </span>
              Clients
            </p>
            <p>
              <span>
                {{ table.activate_project }}
              </span>
              Active Projects
            </p>
            <p>Free Goodies</p>
            <p>
              <span> 24/7 </span>
              Email support
            </p>
          </div>
          <div class="btn-container">
            <v-btn class="more-btn">Purchase</v-btn>
          </div>
        </section>
      </v-col>
    </v-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      tables: [
        {
          title: "ECONOMY",
          pricing: 10,
          storage: "1GB",
          clients: "2",
          activate_project: "5",
        },
        {
          title: "PERSONAL",
          pricing: 20,
          storage: "5GB",
          clients: "10",
          activate_project: "10",
        },
        {
          title: "BUSINESS",
          pricing: 30,
          storage: "15GB",
          clients: "15",
          activate_project: "15",
        },
        {
          title: "PROFESIONAL",
          pricing: 40,
          storage: "Unlimited ",
          clients: "Unlimited ",
          activate_project: "",
        },
      ],
    };
  },
};
</script>

<style lang="scss" scoped>
.table-section {
  border: 3px solid #dee3e4;
  border-radius: 7px;
  height: 600px;
}
.table-section {
  position: relative;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  padding: 10px 26px 29px 26px;

  &:hover {
    .pricing {
      span {
        width: 120px;
        height: 120px;
      }
    }
  }

  .table-title {
    font-size: 2rem;
    color: #1abc9c;
    position: absolute;
    top: 0;
    width: 100%;
    text-align: center;
    padding: 5px 0;
  }

  .pricing {
    height: 250px;
    span {
      border: 2px solid #1abc9c;
      border-radius: 50%;
      width: 110px;
      height: 110px;
      display: flex;
      justify-content: center;
      align-items: center;
      margin-top: 70px !important;
      transition: all 0.2s ease-out;
    }
  }
  .details {
    display: flex;
    flex-direction: column;
    gap: 30px;
    p {
      color: #979797;
      span {
        color: #000;
      }
    }
      margin-bottom: 20px !important;
  }
  .btn-container {
    width: 100%;
    .v-btn {
      width: 100%;
    }
  }
}
.tables-row {
  .col {
    padding-left: 3px;
  }
}
.personal {
  border-color: #484f58;
  .table-title {
    position: absolute;
    top: 0;
    width: 100%;
    text-align: center;
    padding: 5px 0;
    color: #fff;
    background: #484f58;
    p {
    }
  }
  .pricing {
    span {
      border-color: #484f58;
      background: #484f58;
      color: #fff;
      font-weight: bold;
    }
  }
  .btn-container {
    .v-btn {
      background: #484f58 !important;
      color: #fff;
    }
  }
}
</style>

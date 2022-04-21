<template>
  <section class="home">
    <div class="home__content">
      <div class="hprofile">
        <div class="hprofile__content">
          <div class="hprofile__image">
            <img src="https://images.unsplash.com/photo-1463453091185-61582044d556?ixlib=rb-1.2.1&ixid=MnwxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8&auto=format&fit=crop&w=2670&q=80" alt="" class="image" />
          </div>
          <div class="hprofile__meta">
            <h1 class="h1">Hello! <span>Dennis</span></h1>
            <div class="hprofile__status">
              <span>You're on track</span>
              <span class="dot-indicator"></span>
            </div>
            <div class="hprofile__link">
              <span>Tap to see balance</span>
            </div>
          </div>
        </div>
      </div>
      <div class="add-budget">
        <span>add new budget</span>
      </div>
      <div>services</div>
      <BudgetLists />
      <TransactionLists />
    </div>
  </section>
</template>

<script>
import BudgetLists from '@/components/budget/BudgetLists.vue'
import TransactionLists from '@/components/transaction/TransactionLists.vue'

export default {
  name: "HomeView",
  components: { 
    BudgetLists,
    TransactionLists
  },
}
</script>

<style lang="scss">
  //mixins
  @mixin border-radius($num){
    border-radius: $num;
  }

  .home{
    background: #fff;
    &__content{
      padding: 30px 20px 20px;
    }
  }

  .hprofile{

    &__content{
      display: flex;
    }

    &__image{
      width: 100px;
      height: 100px;
      margin-right: 20px;
      border: 1px solid rgba(0,0,0,0.1);
      @include border-radius(15px);
      padding: 4px;

      .image{
        width: 100%;
        height: 100%;
        object-fit: cover;
        @include border-radius(15px);
      }

    }

    &__link{
      background: #151515;
      color: #fff;
      margin-top: 10px;
      padding: 10px 20px;
      border-radius: 10px;
      font-weight: 500;
      cursor: pointer;
    }
  }

  .add-budget{
    margin-top: 20px;
    margin-bottom: 20px;
    border: 1px solid #dae2e4;
    padding: 15px 20px;
    font-weight: 500;
    color: #949494;
    @include border-radius(15px);
  }
</style>
<template>
  <div id="my-account">
    <SfBreadcrumbs
      class="breadcrumbs desktop-only"
      :breadcrumbs="breadcrumbs"
    />
    <SfContentPages
      title="My Account"
      :active="activePage"
      class="my-account"
      @click:change="changeActivePage"
    >
      <SfContentCategory title="Personal Details">
        <SfContentPage title="My profile">
          <MyProfile
            :account="account"
            @update:personal="account = { ...account, ...$event }"
          />
        </SfContentPage>
        <SfContentPage title="Shipping details">
          <ShippingDetails
            :account="account"
            @update:shipping="account = { ...account, ...$event }"
          />
        </SfContentPage>
        <SfContentPage title="Loyalty card">
          <LoyaltyCard />
        </SfContentPage>
        <SfContentPage title="My newsletter">
          <MyNewsletter />
        </SfContentPage>
      </SfContentCategory>
      <SfContentCategory title="Order details">
        <SfContentPage title="Order history">
          <OrderHistory />
        </SfContentPage>
        <SfContentPage title="My reviews">
          <MyReviews />
        </SfContentPage>
      </SfContentCategory>
      <SfContentPage title="Log out" />
    </SfContentPages>
  </div>
</template>
<script>
import { SfBreadcrumbs, SfContentPages } from '@storefront-ui/vue';
import MyProfile from './MyAccount/MyProfile';
import ShippingDetails from './MyAccount/ShippingDetails';
import LoyaltyCard from './MyAccount/LoyaltyCard';
import MyNewsletter from './MyAccount/MyNewsletter';
import OrderHistory from './MyAccount/OrderHistory';
import MyReviews from './MyAccount/MyReviews';

// TODO: protect this route: https://github.com/SalvadorLtd/next/issues/379
export default {
  name: 'MyAccount',
  components: {
    SfBreadcrumbs,
    SfContentPages,
    MyProfile,
    ShippingDetails,
    LoyaltyCard,
    MyNewsletter,
    OrderHistory,
    MyReviews
  },
  data() {
    return {
      breadcrumbs: [
        {
          text: 'Home',
          route: {
            link: '#'
          }
        },
        {
          text: 'My Account',
          route: {
            link: '#'
          }
        }
      ],
      account: {
        firstName: 'Sviatlana',
        lastName: 'Havaka',
        email: 'example@email.com',
        password: 'a*23Et',
        shipping: [
          {
            firstName: 'Sviatlana',
            lastName: 'Havaka',
            streetName: 'Zielinskiego',
            apartment: '24/193A',
            city: 'Wroclaw',
            state: 'Lower Silesia',
            zipCode: '53-540',
            country: 'Poland',
            phoneNumber: '(00)560 123 456'
          },
          {
            firstName: 'Sviatlana',
            lastName: 'Havaka',
            streetName: 'Zielinskiego',
            apartment: '20/193A',
            city: 'Wroclaw',
            state: 'Lower Silesia',
            zipCode: '53-603',
            country: 'Poland',
            phoneNumber: '(00)560 123 456'
          }
        ],
        orders: [
          ['#35765', '4th Nov, 2019', 'Visa card', '$12.00', 'In process'],
          ['#35766', '4th Nov, 2019', 'Paypal', '$12.00', 'Finalised'],
          ['#35768', '4th Nov, 2019', 'Mastercard', '$12.00', 'Finalised'],
          ['#35769', '4th Nov, 2019', 'Paypal', '$12.00', 'Finalised']
        ]
      }
    };
  },
  computed: {
    activePage() {
      const { pageName } = this.$route.params;

      if (pageName) {
        return (pageName.charAt(0).toUpperCase() + pageName.slice(1)).replace('-', ' ');
      }

      return 'My profile';
    }
  },
  methods: {
    changeActivePage(title) {
      if (title === 'Log out') {
        return;
      }

      this.$router.push(`/my-account/${title.toLowerCase().replace(' ', '-')}`);
    }
  }
};
</script>
<style lang='scss' scoped>
@import "~@storefront-ui/vue/styles";

#my-account {
  box-sizing: border-box;
  @include for-desktop {
    max-width: 1240px;
    margin: 0 auto;
  }
}
.breadcrumbs {
  padding: var(--spacer-big) var(--spacer-extra-big) var(--spacer-extra-big)
    var(--spacer-extra-big);
}
</style>

<template>
  <div id="category">
    <SfBreadcrumbs
      class="breadcrumbs desktop-only"
      :breadcrumbs="breadcrumbs"
    />
    <div class="navbar section">
      <div class="navbar__aside desktop-only">
        <h1 class="navbar__title">Categories</h1>
      </div>
      <div class="navbar__main">
        <SfButton
          class="sf-button--text navbar__filters-button"
          @click="isFilterSidebarOpen = true"
        >
          <SfIcon size="15px" style="margin-right: 10px;">
            <svg viewBox="0 0 18 18" xmlns="http://www.w3.org/2000/svg">
              <g clip-icon="url(#clip0)">
                <path
                  d="m2.461 6.9416e-6h-0.1786c-1.113 0.0021094-2.0151 0.90421-2.0173 2.018v0.17859c-0.001406 0.53649 0.21024 1.0512 0.58851 1.4316 0.37829 0.38039 0.89226 0.59414 1.4287 0.59555h0.1786c0.53859 0.0014 1.0547-0.21165 1.4358-0.59204 0.38039-0.38039 0.59344-0.89719 0.59203-1.4351v-0.17859c-0.0014-0.53649-0.21585-1.0505-0.59554-1.4295-0.3804-0.37829-0.89581-0.58991-1.4323-0.58851zm1.452 2.1965c0.00141 0.38531-0.15047 0.75585-0.42329 1.028-0.27281 0.27281-0.64265 0.42539-1.0287 0.42329h-0.1786c-0.3839-7.1e-4 -0.75164-0.15399-1.0223-0.4261-0.27-0.27281-0.42117-0.64125-0.41906-1.0252v-0.1786c7.03e-4 -0.79594 0.64616-1.4407 1.4414-1.4421h0.1786c0.3839-0.00211 0.75305 0.14906 1.0252 0.41976 0.27281 0.27 0.4261 0.63844 0.4268 1.0223v0.1786z"
                />
                <path
                  d="m9.0959 0h-0.19265c-1.1109 0.005625-2.0095 0.90634-2.0117 2.018v0.17859c-0.00281 1.1145 0.89719 2.0214 2.0117 2.0272h0.19265c1.1145-0.00562 2.0144-0.91265 2.0117-2.0272v-0.17859c-0.0021-1.1116-0.9007-2.0124-2.0117-2.018zm1.4421 2.1965h-7e-4c0.0022 0.3839-0.149 0.75235-0.4197 1.0252-0.27001 0.27211-0.63846 0.4254-1.0217 0.4261h-0.19265c-0.79524-0.00141-1.4407-0.64616-1.4414-1.4421v-0.17859c-0.00211-0.3839 0.14907-0.75235 0.41976-1.0252 0.27-0.27211 0.63845-0.4254 1.0216-0.4261h0.19265c0.79524 0.001406 1.4407 0.64616 1.4414 1.4421l7e-4 0.17859z"
                />
                <path
                  d="m15.718 6.9631e-6h-0.1786c-0.5364-0.0014063-1.0518 0.21024-1.4322 0.58851-0.3797 0.37899-0.5942 0.89296-0.5956 1.4295v0.17859c-0.0014 0.5379 0.2117 1.0547 0.5921 1.4351 0.3811 0.38039 0.8972 0.59344 1.4358 0.59204h0.1786c0.5364-0.00141 1.0504-0.21516 1.4287-0.59555s0.5899-0.89509 0.5885-1.4316v-0.17859c-0.0021-1.1138-0.9042-2.0158-2.0172-2.018h-1e-4zm1.4414 2.1965c0.0022 0.3839-0.149 0.75234-0.419 1.0252-0.2707 0.27211-0.6385 0.42539-1.0224 0.4261h-0.1786c-0.386 0.00211-0.7558-0.15047-1.0286-0.42329-0.2728-0.27211-0.4247-0.64265-0.4233-1.028v-0.1786c7e-4 -0.3839 0.154-0.75234 0.4268-1.0223 0.2721-0.2707 0.6412-0.42188 1.0251-0.41976h0.1786c0.7953 0.001406 1.4407 0.64616 1.4414 1.4421v0.1786z"
                />
                <path
                  d="m2.461 6.8921h-0.17859c-1.1138 0.00211-2.0165 0.90562-2.0173 2.0194v0.17859c0.002109 1.1138 0.90421 2.0158 2.0173 2.018h0.17859c0.53719 0.0014 1.0526-0.2103 1.433-0.5892 0.3804-0.379 0.59415-0.89369 0.59485-1.4302v-0.1786c-0.00141-0.53649-0.21586-1.0505-0.59555-1.4294-0.38039-0.37829-0.89579-0.58991-1.4323-0.58851v-7e-5zm1.452 2.1965c-0.0014 0.79524-0.64616 1.4407-1.4421 1.4414h-0.1786c-0.3839 0.0021-0.75305-0.149-1.0252-0.419-0.27211-0.27073-0.4254-0.63847-0.4261-1.0224v-0.1786c7.03e-4 -0.79594 0.64617-1.4407 1.4414-1.4421h0.17859c0.38461-0.00211 0.75375 0.14906 1.0259 0.42046 0.2728 0.2707 0.42609 0.63915 0.42609 1.023v0.17719z"
                />
                <path
                  d="m9.0959 6.8921h-0.19266c-1.1116 0.00562-2.0102 0.90774-2.0117 2.0194v0.17859c0.00211 1.1116 0.9007 2.0124 2.0117 2.018h0.19266c1.1117-0.0056 2.0103-0.9078 2.0117-2.0194v-0.17859c-0.0021-1.1116-0.9007-2.0124-2.0117-2.018zm1.4421 2.1965h-7e-4c0 0.79664-0.64542 1.4421-1.4414 1.4435h-0.19266c-0.79524-0.0014-1.4407-0.64612-1.4414-1.4421v-0.17859c0-0.79664 0.64546-1.4421 1.4414-1.4435h0.19266c0.79524 0.00141 1.4407 0.64616 1.4414 1.4421l7e-4 0.1786z"
                />
                <path
                  d="m15.717 6.8922h-0.1786c-0.5371-0.0014-1.0525 0.21024-1.4329 0.58921-0.3804 0.37899-0.5942 0.89367-0.5949 1.4302v0.17859c0.0014 0.53649 0.2159 1.0505 0.5956 1.4295 0.3804 0.3783 0.8958 0.5899 1.4322 0.5885h0.1786c1.1138-0.0021 2.0166-0.9056 2.0173-2.0194v-0.17859c-0.0021-1.1138-0.9042-2.0158-2.0173-2.018v7e-5zm1.4414 2.1965c-7e-4 0.79524-0.6461 1.4407-1.4414 1.4414h-0.1786c-0.3839 0.0021-0.753-0.1491-1.0251-0.4191-0.2728-0.27065-0.4261-0.63839-0.4268-1.0223v-0.17859c0.0014-0.79594 0.6462-1.4407 1.4421-1.4421h0.1786c0.3839-0.00211 0.753 0.14906 1.0259 0.42046 0.2721 0.27071 0.4253 0.63915 0.4253 1.023v0.17719z"
                />
                <path
                  d="m9.0959 13.786h-0.19266c-1.1109 5e-3 -2.0095 0.9064-2.0117 2.0173v0.1786c0.00211 1.1116 0.9007 2.0124 2.0117 2.018h0.19266c1.111-0.0057 2.0096-0.9064 2.0117-2.018v-0.1786c-0.0021-1.1109-0.9007-2.0124-2.0117-2.0173zm1.4421 2.1966l-7e-4 -7e-4c-7e-4 0.7959-0.64612 1.4407-1.4414 1.4421h-0.19266c-0.79524-0.0014-1.4407-0.6462-1.4414-1.4421v-0.1786c7e-4 -0.7953 0.64616-1.4407 1.4414-1.4414h0.19266c0.79524 7e-4 1.4407 0.6461 1.4414 1.4414l7e-4 0.1793z"
                />
              </g>
            </svg>
          </SfIcon>
          Filters
        </SfButton>
        <div class="navbar__sort desktop-only">
          <span class="navbar__label">Sort by:</span>
          <SfSelect class="sort-by" v-model="sortBy">
            <SfSelectOption
              v-for="option in sortByOptions"
              :key="option.value"
              :value="option.value"
              class="sort-by__option"
              >{{ option.label }}</SfSelectOption
            >
          </SfSelect>
        </div>
        <div class="navbar__counter">
          <span class="navbar__label desktop-only">Products found: </span>
          <strong class="desktop-only">{{ totalProducts }}</strong>
          <span class="navbar__label mobile-only">{{ totalProducts }} Items</span>
        </div>
        <div class="navbar__view desktop-only">
          <span>View </span>
          <SfIcon
            class="navbar__view-icon"
            :color="isGridView ? '#1D1F22' : '#BEBFC4'"
            size="10px"
            role="button"
            aria-label="Change to grid view"
            :aria-pressed="isGridView"
            @click="isGridView = true"
          >
            <svg viewBox="0 0 10 10">
              <rect width="2" height="2" />
              <rect y="4" width="2" height="2" />
              <rect y="8" width="2" height="2" />
              <rect x="4" width="2" height="2" />
              <rect x="4" y="4" width="2" height="2" />
              <rect x="4" y="8" width="2" height="2" />
              <rect x="8" width="2" height="2" />
              <rect x="8" y="4" width="2" height="2" />
              <rect x="8" y="8" width="2" height="2" />
            </svg>
          </SfIcon>
          <SfIcon
            class="navbar__view-icon"
            :color="!isGridView ? '#1D1F22' : '#BEBFC4'"
            size="11px"
            role="button"
            aria-label="Change to list view"
            :aria-pressed="!isGridView"
            @click="isGridView = false"
          >
            <svg viewBox="0 0 11 10">
              <rect width="11" height="2" />
              <rect y="8" width="11" height="2" />
              <rect y="4" width="7" height="2" />
            </svg>
          </SfIcon>
        </div>
        <SfButton
          class="sf-button--text navbar__filters-button mobile-only"
          @click="isFilterSidebarOpen = true"
        >
          Sort by
          <SfIcon size="15px" style="margin-left: 10px;">
            <svg viewBox="0 0 12 16" xmlns="http://www.w3.org/2000/svg">
              <path
                d="M8.32809 15.2897L12 11.7644V12.2892L8.13547 16L4.27094 12.2892V11.7644L7.94285 15.2897V6.83165H8.32809L8.32809 15.2897ZM3.67191 0.710288L0 4.23556V3.71082L3.86453 0L7.72906 3.71082V4.23556L4.05715 0.710288V9.16835H3.67191L3.67191 0.710288Z"
              />
            </svg>
          </SfIcon>
        </SfButton>
      </div>
    </div>
    <div class="main section">
      <div class="sidebar desktop-only">
        <SfLoader :class="{ loading }" :loading="loading">
          <SfAccordion :firstOpen="true" :showChevron="false">
            <SfAccordionItem
              v-for="(cat, i) in categoryTree && categoryTree.items"
              :key="i"
              :header="cat.label"
            >
              <template>
                <SfList>
                  <SfListItem>
                    <SfMenuItem :label="cat.label">
                      <template #label>
                        <nuxt-link :to="getCategoryUrl(cat.slug)" :class="isCategorySelected(cat.slug) ? 'sidebar--cat-selected' : ''">All</nuxt-link>
                      </template>
                    </SfMenuItem>
                  </SfListItem>
                  <SfListItem v-for="(subCat, j) in cat.items" :key="j">
                    <SfMenuItem :label="subCat.label">
                      <template #label="{ label }">
                        <nuxt-link :to="getCategoryUrl(subCat.slug)" :class="isCategorySelected(subCat.slug) ? 'sidebar--cat-selected' : ''">{{ label }}</nuxt-link>
                      </template>
                    </SfMenuItem>
                  </SfListItem>
                </SfList>
              </template>
            </SfAccordionItem>
          </SfAccordion>
        </SfLoader>
      </div>
      <div class="products">
        <transition-group
          v-if="isGridView"
          appear
          name="products__slide"
          tag="div"
          class="products__grid"
        >
          <SfProductCard
            v-for="(product, i) in products"
            :key="productGetters.getSlug(product)"
            :style="{ '--index': i }"
            :title="productGetters.getName(product)"
            :image="productGetters.getCoverImage(product)"
            :regular-price="productGetters.getFormattedPrice(productGetters.getPrice(product).regular)"
            :special-price="productGetters.getFormattedPrice(productGetters.getPrice(product).special)"
            :max-rating="5"
            :score-rating="3"
            :isOnWishlist="false"
            @click:wishlist="toggleWishlist(i)"
            :link="`/p/${productGetters.getId(product)}/${productGetters.getSlug(product)}`"
            class="products__product-card"
          />
        </transition-group>
        <transition-group
          v-else
          appear
          name="products__slide"
          tag="div"
          class="products__list"
        >
          <SfProductCardHorizontal
            v-for="(product, i) in products"
            :key="productGetters.getSlug(product)"
            :style="{ '--index': i }"
            :title="productGetters.getName(product)"
            :description="productGetters.getDescription(product)"
            :image="productGetters.getCoverImage(product)"
            :regular-price="productGetters.getFormattedPrice(productGetters.getPrice(product).regular)"
            :special-price="productGetters.getFormattedPrice(productGetters.getPrice(product).special)"
            :max-rating="5"
            :score-rating="3"
            :is-on-wishlist="false"
            class="products__product-card-horizontal"
            @click:wishlist="toggleWishlist(i)"
            :link="`/p/${productGetters.getId(product)}/${productGetters.getSlug(product)}`"
          />
        </transition-group>
        <SfPagination
          v-show="totalPages > 1"
          class="products__pagination"
          :current="currentPage"
          @click="goToPage"
          :total="totalPages"
          :visible="5"
        />
        <!-- TODO: change accordingly when designed by UI team: https://github.com/SalvadorLtd/storefront-ui/issues/941 -->
        <div
          v-show="totalPages > 1"
          class="products__pagination__options"
        >
          <span class="products__pagination__label">Items per page:</span>
          <SfSelect class="items-per-page" v-model="itemsPerPage">
            <SfSelectOption
              v-for="option in perPageOptions"
              :key="option"
              :value="option"
              class="items-per-page__option"
              >{{ option }}</SfSelectOption
            >
          </SfSelect>
        </div>
        <!-- end of TODO -->
      </div>
    </div>
    <SfSidebar
      :visible="isFilterSidebarOpen"
      title="Filters"
      @close="isFilterSidebarOpen = false"
    >
      <div class="filters">
        <h3 class="filters__title">Collection</h3>
        <SfFilter
          v-for="filter in filters.collection"
          :key="filter.value"
          :label="filter.label"
          :count="filter.count"
          :selected="filter.selected"
          class="filters__item"
          @change="filter.selected = !filter.selected"
        />
        <h3 class="filters__title">Color</h3>
        <div class="filters__colors">
          <SfColor
            v-for="filter in filters.color"
            :key="filter.value"
            :color="filter.color"
            :selected="filter.selected"
            class="filters__color"
            @click="filter.selected = !filter.selected"
          />
        </div>
        <h3 class="filters__title">Size</h3>
        <SfFilter
          v-for="filter in filters.size"
          :key="filter.value"
          :label="filter.label"
          :count="filter.count"
          :selected="filter.selected"
          class="filters__item"
          @change="filter.selected = !filter.selected"
        />
        <h3 class="filters__title">Price</h3>
        <SfFilter
          v-for="filter in filters.price"
          :key="filter.value"
          :label="filter.label"
          :count="filter.count"
          :selected="filter.selected"
          class="filters__item"
          @change="filter.selected = !filter.selected"
        />
        <h3 class="filters__title">Material</h3>
        <SfFilter
          v-for="filter in filters.material"
          :key="filter.value"
          :value="filter.value"
          :label="filter.label"
          :selected="filter.selected"
          class="filters__item"
          @change="filter.selected = !filter.selected"
        />
        <div class="filters__buttons">
          <SfButton
            @click="isFilterSidebarOpen = false"
            class="sf-button--full-width"
            >Done</SfButton
          >
          <SfButton
            @click="clearAllFilters"
            class="sf-button--full-width filters__button-clear"
            >Clear all</SfButton
          >
        </div>
      </div>
    </SfSidebar>
  </div>
</template>

<script>
import {
  SfSidebar,
  SfButton,
  SfList,
  SfIcon,
  SfMenuItem,
  SfFilter,
  SfProductCard,
  SfProductCardHorizontal,
  SfPagination,
  SfAccordion,
  SfSelect,
  SfBreadcrumbs,
  SfLoader,
  SfColor
} from '@storefront-ui/vue';
import { computed, ref, watch } from '@vue/composition-api';
import { useCategory, useProduct, productGetters, categoryGetters } from '<%= options.composables %>';
import { getCategorySearchParameters } from '~/helpers/category/getCategorySearchParameters';
import { onSSR } from '@vue-storefront/core';

const perPageOptions = [20, 40, 100];

const sortByOptions = [
  { value: 'latest', label: 'Latest' },
  { value: 'price-up', label: 'Price from low to high' },
  { value: 'price-down', label: 'Price from high to low' }
];

// TODO: to be implemented in https://github.com/SalvadorLtd/next/issues/200
const filters = {
  collection: [
    { label: 'Summer fly', value: 'summer-fly', count: '10', selected: false },
    { label: 'Best 2018', value: 'best-2018', count: '23', selected: false },
    { label: 'Your choice', value: 'your-choice', count: '54', selected: false }
  ],
  color: [
    { label: 'Red', value: 'red', color: '#990611', selected: false },
    { label: 'Black', value: 'black', color: '#000000', selected: false },
    { label: 'Yellow', value: 'yellow', color: '#DCA742', selected: false },
    { label: 'Blue', value: 'blue', color: '#004F97', selected: false },
    { label: 'Navy', value: 'navy', color: '#656466', selected: false }
  ],
  size: [
    { label: 'Size 2 (XXS)', value: 'xxs', count: '10', selected: false },
    { label: 'Size 4-6 (XS)', value: 'xs', count: '23', selected: false },
    { label: 'Size 8-10 (S)', value: 's', count: '54', selected: false },
    { label: 'Size 12-14 (M)', value: 'm', count: '109', selected: false },
    { label: 'Size 16-18 (L)', value: 'l', count: '23', selected: false },
    { label: 'Size 20-22(XL)', value: 'xl', count: '12', selected: false },
    { label: 'Size 24-26 (XXL)', value: 'xxl', count: '2', selected: false }
  ],
  price: [
    { label: 'Under $200', value: 'under-200', count: '23', selected: false },
    { label: 'Under $300', value: 'under-300', count: '54', selected: false }
  ],
  material: [
    { label: 'Cotton', value: 'coton', count: '33', selected: false },
    { label: 'Silk', value: 'silk', count: '73', selected: false }
  ]
};

// TODO: to be implemented in https://github.com/SalvadorLtd/next/issues/211
const breadcrumbs = [
  { text: 'Home', route: { link: '#' } },
  { text: 'Women', route: { link: '#' } }
];

function updateFilter() {}

function clearAllFilters() {
  const filtersNames = Object.keys(filters);
  filtersNames.forEach((name) => {
    filters[name].forEach((value) => {
      value.selected = false;
    });
  });
}

export default {
  transition: 'fade',
  setup(props, context) {
    const { params, query } = context.root.$route;

    const { categories, search, loading } = useCategory('categories');
    const { products: categoryProducts, totalProducts, search: productsSearch, loading: productsLoading } = useProduct('categoryProducts');
    const currentPage = ref(parseInt(query.page, 10) || 1);
    const itemsPerPage = ref(parseInt(query.items, 10) || perPageOptions[0]);

    onSSR(async () => {
      await search(getCategorySearchParameters(context));
      await productsSearch({
        catId: (categories.value[0] || {}).id,
        page: currentPage.value,
        perPage: itemsPerPage.value
      });
    });

    watch([currentPage, itemsPerPage], () => {
      if (categories.value.length) {
        productsSearch({
          catId: categories.value[0].id,
          page: currentPage.value,
          perPage: itemsPerPage.value
        });
        context.root.$router.push({ query: {
          items: itemsPerPage.value !== perPageOptions[0] ? itemsPerPage.value : undefined,
          page: currentPage.value !== 1 ? currentPage.value : undefined
        }});
      }
    });

    const products = computed(() => productGetters.getFiltered(categoryProducts.value, { master: true}));
    const categoryTree = computed(() => categoryGetters.getTree(categories.value[0]));

    const getCategoryUrl = (slug) => `/c/${params.slug_1}/${slug}`;
    const isCategorySelected = (slug) => slug === (categories.value && categories.value[0].slug);

    const sortBy = ref('price-up');
    const isGridView = ref(true);
    const isFilterSidebarOpen = ref(false);

    function toggleWishlist(index) {
      products.value[index].isOnWishlist = !this.products.value[index].isOnWishlist;
    }

    const goToPage = (pageNumber) => {
      currentPage.value = pageNumber;
      context.root.$scrollTo(context.root.$el, 2000);
    };

    return {
      products,
      productsLoading,
      categoryTree,
      getCategoryUrl,
      isCategorySelected,
      loading,
      productGetters,
      totalProducts,
      totalPages: computed(() => Math.ceil(totalProducts.value / itemsPerPage.value)),
      currentPage,
      itemsPerPage,
      perPageOptions: computed(() => perPageOptions),
      sortBy,
      isFilterSidebarOpen,
      sortByOptions: computed(() => sortByOptions),
      filters: ref(filters),
      breadcrumbs: computed(() => breadcrumbs),
      updateFilter,
      clearAllFilters,
      toggleWishlist,
      isGridView,
      goToPage
    };
  },
  components: {
    SfButton,
    SfSidebar,
    SfIcon,
    SfList,
    SfFilter,
    SfProductCard,
    SfProductCardHorizontal,
    SfPagination,
    SfMenuItem,
    SfAccordion,
    SfSelect,
    SfBreadcrumbs,
    SfLoader,
    SfColor
  }
};
</script>

<style lang="scss">
@import "~@storefront-ui/vue/styles";
#category {
  box-sizing: border-box;
  @include for-desktop {
    max-width: 1240px;
    margin: 0 auto;
  }
}
.section {
  padding: 0 var(--spacer-big);
  @include for-desktop {
    padding: 0;
  }
}
.breadcrumbs {
  padding: var(--spacer-big) var(--spacer-extra-big) var(--spacer-extra-big)
    var(--spacer-extra-big);
}
.navbar {
  position: relative;
  display: flex;
  font: 300 var(--font-size-small) / 1.6 var(--body-font-family-primary);
  @include for-desktop {
    border: 1px solid var(--c-light);
    border-width: 1px 0 1px 0;
  }
  &::after {
    position: absolute;
    bottom: 0;
    left: var(--spacer-big);
    width: calc(100% - calc(var(--spacer-big) * 2));
    height: 1px;
    background: var(--c-light);
    content: "";
    @include for-desktop {
      content: none;
    }
  }
  &__aside,
  &__main {
    display: flex;
    align-items: center;
    padding: var(--spacer-medium) 0;
    font-size: var(--font-size-small);
    line-height: 1.6;
    @include for-desktop {
      padding: var(--spacer-big) 0;
    }
  }
  &__aside {
    flex: 0 0 15%;
    padding: var(--spacer-big) var(--spacer-extra-big);
    border: 1px solid var(--c-light);
    border-width: 0 1px 0 0;
  }
  &__main {
    flex: 1;
  }
  &__title {
    padding: 0;
    font-size: var(--font-size-big);
    font-family: var(--body-font-family-secondary);
    font-weight: 500;
    line-height: 1.6;
  }
  &__filters-button {
    --button-text-decoration: none;
    --button-font-weight: var(--body-font-weight-secondary);
    --button-color: var(--c-text);
    --button-transition: all 150ms linear;
    display: flex;
    align-items: center;
    @include for-desktop {
      margin: 0 0 0 var(--spacer-extra-big);
    }
    svg {
      fill: var(--c-text-muted);
    }
    &:hover {
      --button-color: var(--c-primary);
      svg {
        fill: var(--c-primary);
      }
    }
  }
  &__label {
    color: var(--c-text-muted);
  }
  &__sort {
    display: flex;
    align-items: center;
    margin: 0 auto 0 var(--spacer-extra-big);
    --select-font-size: var(--font-size-small);
  }
  &__counter {
    margin: auto;
    @include for-desktop {
      margin: auto 0 auto auto;
    }
  }
  &__view {
    display: flex;
    align-items: center;
    margin: 0 var(--spacer-extra-big);
    @include for-desktop {
      margin: var(--spacer-big);
    }
    &-icon {
      margin: 0 0 0 0.625rem;
      cursor: pointer;
    }
  }
}
.sort-by {
  /*--select-padding: 0 0.625rem;*/
  flex: unset;
  width: 11.875rem;
  --select-dropdown-z-index: 10;
}
.main {
  display: flex;
}
.sidebar {
  flex: 0 0 15%;
  padding: var(--spacer-extra-big);
  border: 1px solid var(--c-light);
  border-width: 0 1px 0 0;
}
.products {
  box-sizing: border-box;
  flex: 1;
  margin: 0 calc(var(--spacer) * -1);
  @include for-desktop {
    margin: var(--spacer-big);
  }
  @include for-mobile {
    display: flex;
    flex-direction: column;
    justify-items: center;

    &__pagination {
      display: inline-block;
      margin-left: auto;
      margin-right: auto;
    }
  }
  &__grid,
  &__list {
    display: flex;
    flex-wrap: wrap;
  }
  &__product-card {
    --product-card-padding: var(--spacer);
    flex: 1 1 50%;
    @include for-desktop {
      --product-card-padding: var(--spacer-big);
      flex: 1 1 25%;
    }
  }
  // TODO: change accordingly when designed by UI team: https://github.com/SalvadorLtd/storefront-ui/issues/941, https://github.com/SalvadorLtd/storefront-ui/issues/1001
  &__pagination__options {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: row;

    .items-per-page {
      min-width: 3rem;
    }
  }

  &__pagination__label {
    color: var(--c-text-muted);
  }
  // end of TODO
  &__product-card-horizontal {
    --product-card-horizontal-padding: var(--spacer);
    flex: 0 0 100%;
    @include for-desktop {
      --product-card-horizontal-padding: var(--spacer-big);
    }
  }
  &__slide-enter {
    opacity: 0;
    transform: scale(0.5);
  }
  &__slide-enter-active {
    transition: all 0.2s ease;
    transition-delay: calc(0.1s * var(--index));
  }
  &__pagination {
    @include for-desktop {
      display: flex;
      justify-content: center;
      margin: var(--spacer-extra-big) 0 0 0;
    }
  }
}
.filters {
  padding: var(--spacer-big);
  &__title {
    margin: calc(var(--spacer-big) * 3) 0 var(--spacer-big) 0;
    font: 400 var(--font-size-extra-big) / 1.6 var(--body-font-family-secondary);
    line-height: 1.6;
    &:first-child {
      margin: 0 0 var(--spacer-big) 0;
    }
  }
  &__colors {
    margin: calc(var(--spacer) * -1);
  }
  &__color {
    margin: var(--spacer);
  }
  &__item {
    margin: var(--spacer) 0;
  }
  &__buttons {
    margin: calc(var(--spacer-big) * 3) 0 0 0;
  }
  &__button-clear {
    --button-background: var(--c-light);
    --button-color: var(--c-dark-variant);
    margin: 0.625rem 0 0 0;
  }
}
</style>

<template>
    <div id="base-order-detail">
        <!-- Container -->
        <div id="order-detail-container">
            <!-- Area 1 -->
            <div class="area-1 t-flex t-between">
                <div class="t-flex">
                    <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" class="injected-svg" data-src="/assets/images/icons/bag_filled.svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                        <path d="M12.0002 0.75C10.8067 0.75 9.66209 1.22411 8.81817 2.06802C7.97426 2.91193 7.50015 4.05653 7.50015 5.25V6H6.87765C6.24624 5.99934 5.6389 6.24222 5.18207 6.6781C4.72523 7.11398 4.45412 7.70925 4.42515 8.34L3.83265 20.6775C3.81746 21.0093 3.86961 21.3407 3.98595 21.6517C4.10228 21.9628 4.2804 22.2471 4.50956 22.4875C4.73873 22.7278 5.01419 22.9193 5.31935 23.0504C5.62451 23.1814 5.95304 23.2493 6.28515 23.25H17.7152C18.0473 23.2493 18.3758 23.1814 18.681 23.0504C18.9861 22.9193 19.2616 22.7278 19.4907 22.4875C19.7199 22.2471 19.898 21.9628 20.0144 21.6517C20.1307 21.3407 20.1828 21.0093 20.1677 20.6775L19.5752 8.34C19.5462 7.70925 19.2751 7.11398 18.8182 6.6781C18.3614 6.24222 17.7541 5.99934 17.1227 6H16.5002V5.25C16.5002 4.05653 16.026 2.91193 15.1821 2.06802C14.3382 1.22411 13.1936 0.75 12.0002 0.75ZM9.00015 5.25C9.00015 4.45435 9.31622 3.69129 9.87883 3.12868C10.4414 2.56607 11.2045 2.25 12.0002 2.25C12.7958 2.25 13.5589 2.56607 14.1215 3.12868C14.6841 3.69129 15.0002 4.45435 15.0002 5.25V6H9.00015V5.25ZM7.77015 9.1425C7.77015 8.99416 7.81414 8.84916 7.89655 8.72582C7.97896 8.60249 8.0961 8.50636 8.23314 8.44959C8.37018 8.39283 8.52098 8.37797 8.66647 8.40691C8.81196 8.43585 8.94559 8.50728 9.05048 8.61217C9.15537 8.71706 9.2268 8.8507 9.25574 8.99618C9.28468 9.14167 9.26983 9.29247 9.21306 9.42951C9.1563 9.56656 9.06017 9.68369 8.93683 9.7661C8.81349 9.84851 8.66849 9.8925 8.52015 9.8925C8.32124 9.8925 8.13047 9.81348 7.98982 9.67283C7.84917 9.53218 7.77015 9.34141 7.77015 9.1425ZM14.7302 9.1425C14.7302 8.99416 14.7741 8.84916 14.8566 8.72582C14.939 8.60249 15.0561 8.50636 15.1931 8.44959C15.3302 8.39283 15.481 8.37797 15.6265 8.40691C15.772 8.43585 15.9056 8.50728 16.0105 8.61217C16.1154 8.71706 16.1868 8.8507 16.2157 8.99618C16.2447 9.14167 16.2298 9.29247 16.1731 9.42951C16.1163 9.56656 16.0202 9.68369 15.8968 9.7661C15.7735 9.84851 15.6285 9.8925 15.4802 9.8925C15.2812 9.8925 15.0905 9.81348 14.9498 9.67283C14.8092 9.53218 14.7302 9.34141 14.7302 9.1425Z" fill="#4a4d51"></path>
                    </svg>
                    <h2 style="font-size: 25px; font-weight: bold; margin-left: 8px;">Order Details</h2>
                </div>
                <div>
                    <router-link v-if="this.role != 'ADMIN'" :to="{ name: 'profile', params: { isOrderList: 1 }}">
                        <base-button :buttonName="'Order List'"></base-button>
                    </router-link>

                    <router-link v-if="this.role == 'ADMIN'" :to="{ name: 'adminHone', params: { isOrderList: 1 }}">
                        <base-button :buttonName="'Order List'"></base-button>
                    </router-link>
                </div>
            </div>
            <!-- End Area 1 -->

            <!-- Area 2 -->
            <div class="area-2 t-flex t-align-center">
                <div 
                    class="t-process-common t-order-color-common t-color-order-status"
                >
                    <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 32 32" fill="none" class="injected-svg" data-src="/assets/images/icons/package-box.svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                        <path d="M7.40692 11.3465L20.5779 4.304L16.0004 2L2.41992 8.836L7.40692 11.3465Z" fill="white"></path>
                        <path d="M24.5773 6.3175L11.4062 13.36L15.9998 15.6725L29.5803 8.83601L24.5773 6.3175Z" fill="white"></path>
                        <path d="M15.625 16.3275L11 13.9995V19.1145L9 17.101H7V11.986L2 9.46948V23.1415L15.625 30V16.3275Z" fill="white"></path>
                        <path d="M16.375 16.3275V30L30 23.1415V9.46948L16.375 16.3275Z" fill="white"></path>
                    </svg>
                </div>
                <div 
                    class="t-line-1 t-order-color-common"
                    :class="orderDetail.status != 2 ? 't-color-order-status' : ''"
                ></div>
                <div 
                    class="t-process-common t-order-color-common"
                    :class="orderDetail.status != 2 ? 't-color-order-status' : ''"
                >
                    <svg xmlns="http://www.w3.org/2000/svg" width="36" height="36" viewBox="0 0 36 36" fill="none" class="injected-svg" data-src="/assets/images/icons/truck-1.svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                        <path :fill="orderDetail.status != 2 ? 'white' : '#D23F57'" fill-rule="evenodd" clip-rule="evenodd" d="M5.1302 7.5H22.4118C22.8992 7.5 23.2941 7.89504 23.2941 8.38236V10.1471H28.322C28.8735 10.1471 29.3583 10.5127 29.5098 11.043L31.0223 16.3368C31.1997 16.368 31.3647 16.4529 31.4937 16.5819L32.7416 17.8298C32.907 17.9952 33 18.2198 33 18.4538V24.2648C33 24.752 32.6049 25.1471 32.1177 25.1471H29.4707C29.4707 27.0963 27.8904 28.6764 25.9412 28.6764C23.9919 28.6764 22.4118 27.0963 22.4118 25.1471H13.5882C13.5882 27.0963 12.0081 28.6764 10.0588 28.6764C8.10959 28.6764 6.52941 27.0963 6.52941 25.1471H3.88236C3.39504 25.1471 3 24.752 3 24.2648V9.63019C3 9.39618 3.09296 9.17175 3.25844 9.00627L4.50627 7.75843C4.67175 7.59295 4.89618 7.5 5.1302 7.5ZM29.1833 16.3236L27.9227 11.9118H23.2941V15.4412C23.2941 15.9285 23.6892 16.3236 24.1764 16.3236H29.1833ZM25.9412 23.3823C26.9159 23.3823 27.7059 24.1725 27.7059 25.1471C27.7059 26.1218 26.9159 26.9118 25.9412 26.9118C24.9666 26.9118 24.1764 26.1218 24.1764 25.1471C24.1764 24.1725 24.9666 23.3823 25.9412 23.3823ZM8.29412 25.1471C8.29412 26.1218 9.08421 26.9118 10.0588 26.9118C11.0334 26.9118 11.8235 26.1218 11.8235 25.1471C11.8235 24.1725 11.0334 23.3823 10.0588 23.3823C9.08421 23.3823 8.29412 24.1725 8.29412 25.1471Z"></path>
                    </svg>
                </div>
                <div 
                    class="t-line-2 t-order-color-common"
                    :class="orderDetail.status == 1 ? 't-color-order-status' : ''"
                ></div>
                <div 
                    class="t-process-common t-order-color-common"
                    :class="orderDetail.status == 1 ? 't-color-order-status' : ''"
                >
                    <svg xmlns="http://www.w3.org/2000/svg" width="32" height="32" viewBox="0 0 32 32" fill="none" class="injected-svg" data-src="/assets/images/icons/delivery.svg" xmlns:xlink="http://www.w3.org/1999/xlink">
                        <path :fill="orderDetail.status == 1 ? 'white' : '#D23F57'" d="M24.0531 1.69349L23.7031 2.33374C23.5704 2.57647 23.3708 2.77603 23.1281 2.90874L22.4878 3.25874C22.4584 3.27482 22.4339 3.29852 22.4167 3.32735C22.3996 3.35619 22.3906 3.38909 22.3906 3.42262C22.3906 3.45614 22.3996 3.48905 22.4167 3.51788C22.4339 3.54671 22.4584 3.57041 22.4878 3.58649L23.1281 3.93649C23.3708 4.0692 23.5704 4.26876 23.7031 4.51149L24.0531 5.15174C24.0691 5.18122 24.0928 5.20583 24.1217 5.22297C24.1506 5.24011 24.1835 5.24916 24.2171 5.24916C24.2506 5.24916 24.2836 5.24011 24.3124 5.22297C24.3413 5.20583 24.365 5.18122 24.3811 5.15174L24.7311 4.51149C24.8639 4.26884 25.0634 4.0693 25.3061 3.93649L25.9463 3.58649C25.9757 3.57041 26.0003 3.54671 26.0174 3.51788C26.0345 3.48905 26.0435 3.45614 26.0435 3.42262C26.0435 3.38909 26.0345 3.35619 26.0174 3.32735C26.0003 3.29852 25.9757 3.27482 25.9463 3.25874L25.3061 2.90874C25.0634 2.77593 24.8639 2.5764 24.7311 2.33374L24.3811 1.69349C24.365 1.66401 24.3413 1.63941 24.3124 1.62226C24.2836 1.60512 24.2506 1.59607 24.2171 1.59607C24.1835 1.59607 24.1506 1.60512 24.1217 1.62226C24.0928 1.63941 24.0691 1.66401 24.0531 1.69349Z"></path>
                        <path :fill="orderDetail.status == 1 ? 'white' : '#D23F57'" d="M27.4868 6.42496L27.2408 6.87496C27.1475 7.04555 27.0072 7.18577 26.8366 7.27896L26.3866 7.52496C26.3659 7.53626 26.3487 7.55292 26.3367 7.57317C26.3247 7.59343 26.3184 7.61654 26.3184 7.64008C26.3184 7.66363 26.3247 7.68674 26.3367 7.70699C26.3487 7.72725 26.3659 7.7439 26.3866 7.75521L26.8366 8.00121C27.0072 8.0944 27.1475 8.23462 27.2408 8.40521L27.4868 8.85521C27.4981 8.87593 27.5147 8.89323 27.535 8.90528C27.5552 8.91733 27.5784 8.9237 27.602 8.9237C27.6255 8.9237 27.6487 8.91733 27.6689 8.90528C27.6892 8.89323 27.7058 8.87593 27.7171 8.85521L27.9631 8.40521C28.0562 8.23422 28.1964 8.09357 28.3671 7.99996L28.8171 7.75396C28.8377 7.74265 28.855 7.726 28.867 7.70574C28.879 7.68549 28.8853 7.66238 28.8853 7.63883C28.8853 7.61529 28.879 7.59218 28.867 7.57192C28.855 7.55167 28.8377 7.53501 28.8171 7.52371L28.3671 7.27771C28.1966 7.18443 28.0564 7.04423 27.9631 6.87371L27.7171 6.42371C27.7057 6.40305 27.689 6.38584 27.6687 6.37389C27.6483 6.36195 27.6252 6.35571 27.6016 6.35584C27.578 6.35596 27.5549 6.36245 27.5347 6.37462C27.5145 6.38678 27.498 6.40417 27.4868 6.42496Z"></path>
                        <path :fill="orderDetail.status == 1 ? 'white' : '#D23F57'" d="M22.72 27.117C22.2155 26.7778 21.395 26.9463 20.616 27.144C20.3484 27.2145 20.0852 27.3007 19.8278 27.402C19.3339 27.6067 18.806 27.717 18.2715 27.727C17.6673 27.717 16.961 27.5575 16.5123 27.8078C16.4668 27.8331 16.4165 27.8487 16.3647 27.8536C16.3129 27.8584 16.2606 27.8524 16.2112 27.8359C16.1618 27.8195 16.1164 27.7929 16.0779 27.7579C16.0393 27.723 16.0084 27.6803 15.9873 27.6328C15.951 27.541 15.9505 27.439 15.9859 27.3469C16.0214 27.2548 16.0901 27.1794 16.1785 27.1355C16.8433 26.7855 17.6623 27.0173 18.3395 27.1148C18.742 27.1795 19.1513 27.1907 19.5568 27.1483C19.6799 27.1304 19.7915 27.066 19.8685 26.9684C19.9456 26.8707 19.9823 26.7472 19.971 26.6233C19.9497 26.5028 19.8999 26.3892 19.8257 26.2919C19.7515 26.1946 19.6551 26.1165 19.5445 26.064C19.1475 25.8553 17.709 25.464 16.7735 25.273C15.285 24.9739 13.739 25.1859 12.386 25.8748C11.6408 26.2278 9.50876 27.6795 8.98101 28.504C8.90689 28.6092 8.8747 28.7382 8.89076 28.8658C8.94426 29.3465 10.3875 30.7326 10.8303 30.8761C10.9111 30.9062 10.9981 30.9159 11.0836 30.9044C11.1692 30.8929 11.2505 30.8605 11.3205 30.8101C11.5873 30.6386 12.174 30.0625 12.765 29.855C13.8595 29.47 15.6748 29.8025 16.5585 29.7815C17.8585 29.7503 22.201 28.6373 22.8718 28.0315C23.1388 27.7913 23.0415 27.333 22.72 27.117Z"></path>
                        <path :fill="orderDetail.status == 1 ? 'white' : '#D23F57'" d="M13.1345 8.16596L13.8048 5.48721H17.1298L17.799 8.16596H24.5925L21.679 5.69996C21.5161 5.56197 21.3095 5.48623 21.096 5.48621H9.8383C9.62479 5.48623 9.41822 5.56197 9.2553 5.69996L6.3418 8.16596H13.1345Z"></path>
                        <path :fill="orderDetail.status == 1 ? 'white' : '#D23F57'" d="M17.8989 8.91602V14.55C17.899 14.6265 17.8796 14.7017 17.8426 14.7686C17.8056 14.8355 17.7523 14.8919 17.6875 14.9325C17.6228 14.9731 17.5488 14.9967 17.4725 15.0009C17.3961 15.0051 17.32 14.9898 17.2512 14.9565L15.7702 14.13C15.6883 14.0597 15.584 14.0211 15.476 14.0211C15.3681 14.0211 15.2638 14.0597 15.1819 14.13L13.6854 14.9598C13.6166 14.9926 13.5406 15.0075 13.4645 15.003C13.3884 14.9986 13.3146 14.9749 13.2501 14.9342C13.1856 14.8936 13.1325 14.8373 13.0956 14.7705C13.0588 14.7038 13.0395 14.6288 13.0394 14.5525V8.91602H5.95117V22.7145C5.95117 22.9143 6.03052 23.1059 6.17178 23.2472C6.31303 23.3885 6.50462 23.468 6.70442 23.468H24.2347C24.4345 23.468 24.6262 23.3886 24.7675 23.2473C24.9088 23.106 24.9882 22.9144 24.9882 22.7145V8.91602H17.8989Z"></path>
                    </svg>
                </div>
            </div>
            <!-- End Area 2 -->

            <!-- Area 3 -->
            <div class="area-3">
                <div class="t-flex t-between">
                    <div>
                        <span style="color: rgb(125, 135, 156); font-weight: 500;">Order: </span> {{ orderDetail.code }}
                    </div>

                    <div>
                        <span style="color: rgb(125, 135, 156); font-weight: 500;">Placed on: </span> {{ formatDate(orderDetail.orderDate) }}
                    </div>
                </div>

                <base-order-product-row
                    v-for="(product, index) in orderProducts"
                    :key="index"
                    :id="product.id"
                    :imgSrc="product.photos"
                    :name="product.name"
                    :price="product.price"
                    :quantity="product.quantitySelected"
                    :category="product.category.name"
                    :categoryId="product.category.id"
                    :discount="product.discount"
                ></base-order-product-row>
            </div>
            <!-- End Area 3 -->

            <!-- Area 4 -->
            <div class="area-4 t-flex t-between" style="margin-top: 32px;">
                <!-- Left -->
                <div class="area-4-left" style="background-color: #fff; padding: 12px; 
                    border-radius: 8px; box-shadow: rgba(0, 0, 0, 0.05) 0px 6px 26px; width: 50%; margin-right: 12px;">
                    <h5 style="font-size: 16px; font-weight: 600;">Shipping Address</h5>
                    <p style="font-size: 16px; margin-bottom: 0;">{{ orderDetail.detailAddress + ", " + orderDetail.district + ", " +  orderDetail.city }}</p>
                </div>

                <!-- Right -->
                <div class="area-4-right" style="background-color: #fff; padding: 12px; 
                    border-radius: 8px; box-shadow: rgba(0, 0, 0, 0.05) 0px 6px 26px; width: 50% ; margin-left: 12px;">
                    <h5 style="font-size: 16px; font-weight: 600;">Total Summary</h5>
                    <h5 style="font-size: 16px; font-weight: 600; margin-bottom: 0;">{{ formatPrice(orderDetail.total) }} VND</h5>
                </div>
            </div>
            <!-- End Area 4 -->
        </div>
        <!-- End container -->
    </div>
</template>

<script>
import axios from 'axios';
import BaseButton from './BaseButton.vue';
import BaseOrderProductRow from './BaseOrderProductRow.vue';

export default {
    name: 'base-order-detail',
    components: {
        BaseButton,
        BaseOrderProductRow,
    },
    beforeCreate() {
        // Get order id from router link
        let orderId = this.$route.params.orderId
        let me = this;
        // Get order details
        const token = localStorage.getItem('token');
        // header
        const headers = {
            Authorization: `Bearer ${token}`
        }

        // call api:
        axios
            .get(`http://localhost:8080/api/v1/order/${orderId}`, {headers})
            .then((response) => {
                console.log(response);
                me.orderDetail = response.data;
                me.orderProducts = response.data.products;
            })
            .catch((reject) => {
                console.log(reject);
                alert("Fail load product list in order!");
            });
    },
    mounted () {
        window.scrollTo(0, 0)
    },
    data() {
        return {
            // Order
            orderDetail: {},

            // List product in order
            orderProducts: [],

            role: localStorage.getItem("role"),
        }
    },
    methods: {
        formatDate(dateTimeString) {
            let date = new Date(dateTimeString);
            let day = date.getDate();
            let month = date.getMonth() + 1;
            let year = date.getFullYear();
            return (day < 10 ? '0' : '') + day + '/' + (month < 10 ? '0' : '') + month + '/' + year;
        },

        // Format price:
        formatPrice(value) {
            let val = (value/1).toFixed(0).replace('.', ',')
            return val.toString().replace(/\B(?=(\d{3})+(?!\d))/g, ".")
        },

        // Go back
        // backLastPage() {
        //     window.history.back();
        // },
    },

}
</script>

<style>
@import url('../../styles/base/orderDetail.css');
</style>
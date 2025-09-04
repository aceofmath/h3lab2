<script setup>
// import { ref } from 'vue';
// import { supabase } from '../../supabase/supabaseClient';
const ports = [
    {
        seq: 5,
        title: '2025 ~ 2026',
        img: '2025-01.png',
        period: '2025.03 ~ 2026.02',
        name: '현대백화점 NEW 커머스 플랫폼 프로젝트 참여',
        role: '정산, 배치',
        ing: '진행중'
    },
    {
        seq: 4,
        title: '2023 ~ 2025',
        img: '2023-01.png',
        period: '2023.06 ~ 2025.03',
        name: 'NH농협 디지털금융 플랫폼 전환 프로젝트 참여',
        role: '금융상품몰(앱,웹,모바일웹)',
        ing: '완료'
    },
    {
        seq: 3,
        title: '2023',
        img: '2022-01.png',
        period: '2023.01 ~ 2023.12',
        name: 'SBI저축은행 수신 통합·여신 비대면 채널 구축 프로젝트 참여',
        role: '채널(앱,웹,모바일웹)',
        ing: '완료'
    },
    {
        seq: 2,
        title: '2022',
        img: '2022-02.jpg',
        period: '2022.07 ~ 2023.02',
        name: 'NH농협 마이데이터 고도화 프로젝트 참여',
        role: '관리자(웹), 배치',
        ing: '완료'
    },
    {
        seq: 1,
        title: '2021',
        img: '2021-01.jpg',
        period: '2021.01 ~ 2021.12',
        name: 'KB국민은행 리브 Reboot구축 프로젝트 참여',
        role: '채널(백엔드)',
        ing: '완료'
    }
];

const baseUrl = '/demo/images/landing/';

const productImage = (img) => {
    return '/demo/images/landing/' + img;
};

// const ports = ref([]);
// const getPortfolios = async () => {
//     const { data } = await supabase.from('portfolio').select();
//     ports.value = data;
// };
// onMounted(() => {
//     getPortfolios();
// });
</script>
<template>
    <div id="pricing" class="py-6 px-6 lg:px-20 my-2 md:my-6">
        <div class="text-center mb-6">
            <div class="text-surface-900 dark:text-surface-0 font-normal mb-2 text-4xl">Portfolio</div>
            <!-- <span class="text-muted-color text-2xl">Amet consectetur adipiscing elit...</span> -->
        </div>

        <div class="grid grid-cols-12 gap-4 justify-between mt-20 md:mt-0">
            <div v-for="port in ports" :key="port.seq" class="col-span-12 lg:col-span-4 p-0 md:p-4 mt-6 md:mt-0">
                <div class="p-4 flex flex-col border-surface-200 dark:border-surface-600 pricing-card cursor-pointer border-2 hover:border-primary duration-300 transition-all" style="border-radius: 10px">
                    <div class="text-surface-900 dark:text-surface-0 text-center my-8 text-3xl">{{ port.title }}</div>
                    <img :src="baseUrl + port.img" class="w-10/12 mx-auto" alt="enterprise" />
                    <!-- <div class="my-8 flex flex-col items-center gap-4">
                        <div class="flex items-center">
                            <span class="text-5xl font-bold mr-2 text-surface-900 dark:text-surface-0">$5</span>
                            <span class="text-surface-600 dark:text-surface-200">per month</span>
                        </div>
                        <Button label="Get Started" class="p-button-rounded border-0 ml-4 font-light leading-tight bg-blue-500 text-white"></Button>
                    </div> -->
                    <Divider class="w-full bg-surface-200"></Divider>
                    <ul class="my-8 list-none p-0 flex text-surface-900 dark:text-surface-0 flex-col px-8">
                        <li class="py-2">
                            <i class="pi pi-fw pi-check text-xl text-cyan-500 mr-2"></i>
                            <span class="text-xl leading-normal">{{ port.period }}</span>
                        </li>
                        <li class="py-2">
                            <i class="pi pi-fw pi-check text-xl text-cyan-500 mr-2"></i>
                            <span class="text-xl leading-normal">{{ port.name }}</span>
                        </li>
                        <li class="py-2">
                            <i class="pi pi-fw pi-check text-xl text-cyan-500 mr-2"></i>
                            <span class="text-xl leading-normal">{{ port.role }}</span>
                        </li>
                        <li class="py-2">
                            <i class="pi pi-fw pi-check text-xl text-cyan-500 mr-2"></i>
                            <span class="text-xl leading-normal">{{ port.ing }}</span>
                        </li>
                    </ul>
                </div>
            </div>
        </div>
    </div>
</template>

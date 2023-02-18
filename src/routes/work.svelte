<!-- <script context="module">
    /* TODO Loading error creates a memory hog */
    import { image_list } from "../stores/images_api";

    export async function load() {
        return {
            props: {image_list}
        };
    }
</script> -->

<script>
    import { onMount } from "svelte";
    import { underline_value } from "../stores/underline_value";

    import WorkCard from "../components/Work/WorkCard.svelte";

    onMount(() => $underline_value = 3);

    export const image_list = [
        /* Tall */
        {
            id: 1,
            src: "/img/tall/Boat in the Sunset.jpg",
            details: ["/img/tall/details/Boat in the Sunset detail.jpg"],
            title: "Boat in the Sunset",
            size: "tall",
            price: 80,
            dimensions: "60 x 100",
            type: "Acrilic",
        },
        {
            id: 2,
            src: "/img/tall/Dali.jpg",
            details: ["/img/tall/details/Dali detail.jpg"],
            size: "tall",
            title: "Dali",
            price: 100,
            dimensions: "60 x 80",
            type: "Acrilic",
        },
        {
            id: 3,
            src: "/img/tall/Lighthouse.jpg",
            details: [],
            size: "tall",
            title: "Lighthouse",
            price: 70,
            dimensions: "60 x 100",
            type: "Acrilic",
        },
        {
            id: 4,
            src: "/img/tall/Old House.jpg",
            details: ["/img/tall/details/Old House detail.jpg"],
            size: "tall",
            title: "Old House",
            price: 80,
            dimensions: "60 x 100",
            type: "Acrilic",
        },
        {
            id: 5,
            src: "/img/tall/Pencil.jpg",
            details: ["/img/tall/details/Pencil detail.jpg"],
            size: "tall",
            title: "Pencil",
            price: 80,
            dimensions: "60 x 100",
            type: "Acrilic",
        },
        {
            id: 6,
            src: "/img/tall/Poppies.jpg",
            details: [],
            size: "tall",
            title: "Poppies",
            price: 120,
            dimensions: "60 x 90",
            type: "Acrilic",
        },
        {
            id: 7,
            src: "/img/tall/River.jpg",
            details: [],
            size: "tall",
            title: "River",
            price: 100,
            dimensions: "60 x 100",
            type: "Acrilic",
        },
        {
            id: 8,
            src: "/img/tall/Rose.jpg",
            details: ["/img/tall/details/Rose detail.jpg"],
            size: "tall",
            title: "Rose",
            price: 100,
            dimensions: "60 x 100",
            type: "Acrilic",
        },
        {
            id: 9,
            src: "/img/tall/Salt Shaker.jpg",
            details: ["/img/tall/details/Salt Shaker detail.jpg"],
            size: "tall",
            title: "Salt Shaker",
            price: 100,
            dimensions: "60 x 100",
            type: "Acrilic",
        },
        {
            id: 10,
            src: "/img/tall/Sunny Snow.jpg",
            details: [],
            size: "tall",
            title: "Sunny Snow",
            price: 100,
            dimensions: "60 x 100",
            type: "Acrilic",
        },
        {
            id: 11,
            src: "/img/tall/Ver Meer.jpg",
            details: [],
            size: "tall",
            title: "Ver Meer",
            price: 100,
            dimensions: "60 x 100",
            type: "Acrilic",
        },

        /* Wide */
        {
            id: 100,
            src: "/img/wide/Figs.jpg",
            details: ["/img/wide/details/Figs detail.jpg"],
            size: "wide",
            title: "Figs",
            price: 100,
            dimensions: "90 x 60",
            type: "Acrilic",
        },
        {
            id: 101,
            src: "/img/wide/Fruit.jpg",
            details: [
                "/img/wide/details/Fruit detail1.jpg",
                "/img/wide/details/Fruit detail2.jpg",
            ],
            size: "wide",
            title: "Fruit",
            price: 100,
            dimensions: "90 x 60",
            type: "Acrilic",
        },
        {
            id: 102,
            src: "/img/wide/Leaves.jpg",
            details: [
                "/img/wide/details/Leaves detail1.jpg",
                "/img/wide/details/Leaves detail2.jpg",
                "/img/wide/details/Leaves detail3.jpg",
            ],
            size: "wide",
            title: "Leaves",
            price: 100,
            dimensions: "90 x 60",
            type: "Acrilic",
        },
        {
            id: 103,
            src: "/img/wide/Night Waves.jpg",
            details: [],
            size: "wide",
            title: "Night Waves",
            price: 100,
            dimensions: "90 x 60",
            type: "Acrilic",
        },
        {
            id: 104,
            src: "/img/wide/Peaches.jpg",
            details: [],
            size: "wide",
            title: "Peaches",
            price: 100,
            dimensions: "90 x 60",
            type: "Acrilic",
        },
        {
            id: 105,
            src: "/img/wide/River Boat.jpg",
            details: ["/img/wide/details/River Boat detail.jpg"],
            size: "wide",
            title: "River Boat",
            price: 100,
            dimensions: "90 x 60",
            type: "Acrilic",
        },
        {
            id: 106,
            src: "/img/wide/Rocks.jpg",
            details: [],
            size: "wide",
            title: "Rocks",
            price: 100,
            dimensions: "90 x 60",
            type: "Acrilic",
        },
        {
            id: 107,
            src: "/img/wide/Snowy Village.jpg",
            details: [
                "/img/wide/details/Snowy Village detail1.jpg",
                "/img/wide/details/Snowy Village detail2.jpg",
            ],
            size: "wide",
            title: "Snowy Village",
            price: 100,
            dimensions: "90 x 60",
            type: "Acrilic",
        },
        {
            id: 108,
            src: "/img/wide/Vase.jpg",
            details: [],
            size: "wide",
            title: "Vase",
            price: 100,
            dimensions: "90 x 60",
            type: "Acrilic",
        },
        {
            id: 109,
            src: "/img/wide/Waves.jpg",
            details: [],
            size: "wide",
            title: "Waves",
            price: 100,
            dimensions: "90 x 60",
            type: "Acrilic",
        },

        /* Ultra Wide */
        {
            id: 10000,
            src: "/img/ultra-wide/Cactus.jpg",
            details: [],
            size: "ultra-wide",
            title: "Cactus",
            price: 150,
            dimensions: "120 x 50",
            type: "Acrilic",
        },
        {
            id: 10001,
            src: "/img/ultra-wide/Naxos.jpg",
            details: [],
            size: "ultra-wide",
            title: "Naxos",
            price: 150,
            dimensions: "120 x 50",
            type: "Acrilic",
        },
        {
            id: 10002,
            src: "/img/ultra-wide/Pumkin.jpg",
            details: [
                "/img/ultra-wide/details/Pumkin detail1.jpg",
                "/img/ultra-wide/details/Pumkin detail2.jpg",
            ],
            size: "ultra-wide",
            title: "Pumkin",
            price: 150,
            dimensions: "120 x 50",
            type: "Acrilic",
        },
        {
            id: 10003,
            src: "/img/ultra-wide/Quay.jpg",
            details: [
                "/img/ultra-wide/details/Quay detail1.jpg",
                "/img/ultra-wide/details/Quay detail2.jpg",
            ],
            size: "ultra-wide",
            title: "Quay",
            price: 150,
            dimensions: "120 x 50",
            type: "Acrilic",
        },
        {
            id: 10004,
            src: "/img/ultra-wide/Quince.jpg",
            size: "ultra-wide",
            details: [],
            title: "Quince",
            price: 150,
            dimensions: "120 x 50",
            type: "Acrilic",
        },
    ];

</script>

<h1>My Work</h1>

<div class="wrapper">
    {#each image_list as image}
        <WorkCard {image}/>
    {/each}
</div>

<style>
    h1 {
        margin-top: 6.5rem;
        text-align: center;
        font-size: 4rem;
        font-style: italic;
    }

    .wrapper {
        display: grid;
        grid-template-columns: 23.4% 23.4% 23.4% 23.4%;
        gap: 1.5rem;
        margin: 4.5rem auto;
        width: 75%;
        align-items: center;
    }

    @media (max-width: 1280px) {
        .wrapper {
            grid-template-columns: 31.5% 31.5% 31.5%;
        }
    }

    @media (max-width: 1024px) {
        .wrapper {
            grid-template-columns: 47.5% 47.5%;
        }
    }

    @media (max-width: 769px) {
        .wrapper {
            grid-template-columns: 100%;
        }
    }
</style>

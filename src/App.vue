<template>
    <div class="btn">
        <div class="container">
            <div class="box">
                <div id="bot" v-for="(davlat, ind) in davlatlar" :key="davlat.name" :class="{ active: activeBtn === ind }"
                    @click="activeBtn = ind">
                    {{ davlat.name }}
                </div>
            </div>
            <div class="block">
                <div class="block_left">
                    <div class="card">
                        <img :src="davlatlar[activeBtn].flag" alt="flag" />
                    </div>
                    <div class="card">
                        <h1>Address</h1>
                        <a href="">{{ davlatlar[activeBtn]["address"].text }}</a>
                    </div>
                    <div class="card">
                        <h1>Phone</h1>
                        <a href="">{{ davlatlar[activeBtn]["phone"].text }}</a>
                    </div>
                    <div class="card">
                        <h1>Email</h1>
                        <a href="">{{ davlatlar[activeBtn].email }}</a>
                    </div>
                    <div class="card">
                        <h1>Website</h1>
                        <a :href="davlatlar[activeBtn].website.link"
                        >{{ davlatlar[activeBtn]["website"].text }}</a>
                    </div>
                </div>
                <div class="block_right">
                    <iframe :src="davlatlar[activeBtn].map" width="600" height="450" style="border:0;" allowfullscreen=""
                        loading="lazy" referrerpolicy="no-referrer-when-downgrade"></iframe>
                </div>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            activeBtn: '0',
            davlatlar: [
                {
                    name: 'Uzbekistan',
                    address: {
                        text: 'Toshkent Gold City Uzbekiston',
                        link: '',
                    },
                    phone: {
                        text: '+998 97 192 0323',
                        link: '+998 97 192 0323',
                    },
                    email: 'toshkent@gmail.com',
                    website: {
                        text: 'City.ai',
                        link: 'https://www.youtube.com/',
                    },
                    flag: require('@/assets/img/uzb.jpg'),
                    map: 'https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d6139265.145829016!2d60.085215273010995!3d41.29389303410847!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x38ae8b20a5d676b1%3A0xca0a6dad7e841e20!2z0KPQt9Cx0LXQutC40YHRgtCw0L0!5e0!3m2!1sru!2s!4v1677929419988!5m2!1sru!2s',
                },
                {
                    name: 'India',
                    address: {
                        text: 'India Gold City Bangldesh',
                        link: '',
                    },
                    phone: {
                        text: '+998 97 4545 4545 ',
                        link: '+998 97 192 0323',
                    },
                    email: 'India@gmail.com',
                    website: {
                        text: 'India.ai',
                        link: 'https://google.com',
                    },
                    flag: require('@/assets/img/india.png'),
                    map: 'https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d3452785.0286841136!2d77.86804669067516!3d22.838019139139238!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x30635ff06b92b791%3A0xd78c4fa1854213a6!2z0JjQvdC00LjRjw!5e0!3m2!1sru!2s!4v1677954847151!5m2!1sru!2s',
                },
                {
                    name: 'Russia',
                    address: {
                        text: 'Mascova Gold City Russia',
                        link: '',
                    },
                    phone: {
                        text: '+7 990 4545 4545 ',
                        link: '+998 97 192 0323',
                    },
                    email: 'Mascova@gmail.com',
                    website: {
                        text: 'Mascove.ai',
                        link: 'https://google.com',
                    },
                    flag: 'https://upload.wikimedia.org/wikipedia/en/thumb/f/f3/Flag_of_Russia.svg/1200px-Flag_of_Russia.svg.png',
                    map: 'https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d577336.7641068471!2d36.82512728226207!3d55.58074806785123!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x46b54afc73d4b0c9%3A0x3d44d6cc5757cf4c!2z0JzQvtGB0LrQstCwLCDQoNC-0YHRgdC40Y8!5e0!3m2!1sru!2s!4v1677955896157!5m2!1sru!2s',
                },
                {
                    name: 'USA',
                    address: {
                        text: 'washington Gold City USA',
                        link: '',
                    },
                    phone: {
                        text: '+34 4534 4545 4545 ',
                        link: '+998 97 192 0323',
                    },
                    email: 'USA@gmail.com',
                    website: {
                        text: 'ChatGpt',
                        link: 'https://google.com',
                    },
                    flag: 'https://upload.wikimedia.org/wikipedia/en/a/a4/Flag_of_the_United_States.svg',
                    map: 'https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d26371377.07903099!2d-113.71816877210625!3d36.211251316091385!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x54eab584e432360b%3A0x1c3bb99243deb742!2z0KHQvtC10LTQuNC90LXQvdC90YvQtSDQqNGC0LDRgtGLINCQ0LzQtdGA0LjQutC4!5e0!3m2!1sru!2s!4v1677956051763!5m2!1sru!2s',

                },
                {
                    name: 'Turkiya',
                    address: {
                        text: 'Anqara Gold City Turkiya',
                        link: '',
                    },
                    phone: {
                        text: '+998 932 12 7 4545 4545 ',
                        link: '+998 97 192 0323',
                    },
                    email: '121212@gmail.com',
                    website: {
                        text: 'Alisa',
                        link: 'https://google.com',
                    },
                    flag: 'http://geografiya.uz/uploads/posts/2015-07/thumbs/1437159683_turkiya.png',
                    map: 'https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d195884.9609039456!2d32.62268038214896!3d39.90329227715166!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x14d347d520732db1%3A0xbdc57b0c0842b8d!2z0JDQvdC60LDRgNCwLCDQotGD0YDRhtC40Y8!5e0!3m2!1sru!2s!4v1677956281017!5m2!1sru!2s',
                },
            ],
        };
    },
};
</script>
<style>
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    background-color: rgba(0, 0, 0, 0.8) !important;
}

.container {
    margin: 0 auto;
    padding: 20px 0;
    width: 100%;
    max-width: 1140px;
}

.btn {
    margin-top: 100px;
}

.box {
    display: flex;
}

.box #bot {
    padding: 5px 25px;
    border: 2px solid white;
    margin-left: 10px;
    border-radius: 20px;
    color: white;
    font-size: 20px;
    cursor: pointer;
}

.box #bot.active {
    border-color: aqua;
    color: aqua;
}

.block {
    display: flex;
    margin-top: 100px !important;
    justify-content: space-between;
}

.card h1 {
    color: aqua;
    font-size: 35px;
    margin-bottom: 10px;
}

.card a {
    text-decoration: none;
    color: white;
    font-size: 20px;
}

.card img {
    width: 300px;
    height: 150px;
    margin-bottom: 20px;
}

.block_right {
    width: 500px;
    height: 400px;
    background-color: gray;
}</style>

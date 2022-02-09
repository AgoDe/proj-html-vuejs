<template>
    <footer>
        <img src="../assets/maps.png" alt="mappa">
        <div class="contacts container">

            <h2>Contact Us</h2>
            <div class="subtitle">Our postal address and contact details</div>
            <img class="divider" src="../assets/header_divider.png" alt="">

            <div class="contacts-box">
                <div
                class="info-box"
                v-for="(item, index) in contactsItems"
                :key="index"
                >
                    <img :src="`/images/${item.path}`" :alt="item.path">
                    <h3> {{ item.item }} </h3>
                    <div class="info"> {{item.info1}} </div>
                    <div class="info"> {{item.info2}} </div>
                    <div class="info"> {{item.info3}} </div>
                    
                </div>
            </div>

            <div class="input-container">
                <div>
                    <input placeholder="Your Name *" type="text">
                    <input placeholder="Your E-mail *" type="text">
                    <input placeholder="Subject *" type="text">
                </div>

                <div>
                    <input placeholder="Your Message *" type="textarea">
                </div>
            </div>
            <div class="button">send message</div>



        </div>
    </footer>
</template>

<script>
export default {
    data() {
        return {
            contactsItems: [
                {
                    path:'envelope(1).png',
                    item: 'Postal Address',
                    info1:'Fable Care Center',
                    info2:'85 Fentiman Ave' ,
                    info3:'Ottawa, ON K1S 0T7',  
                },
                {
                    path:'mobile.png',
                    item: 'Phone & E-mail',
                    info1:'Phone: 1-800-64-38',
                    info2:'Fax: 1-800-64-39',
                    info3:'office@fable.com',  
                },
                {
                    path:'clock.png',
                    item: 'Business Hours',
                    info1:'Monday - Friday',
                    info2:'8.00 am - 5.00 pm',
                    info3:'Weekend Closed', 
                },
                {
                    path:'document(1).png',
                    item: 'Session',
                    info1:'Mornings, 8am - 12 noon',
                    info2:'Afternoons, 1 pm - 5 pm',
                    info3:'Full Day, 8 am - 5 pm',  
                },
            ]
        }
    }
    
}
</script>

<style lang="scss" scoped>
@import '@/styles/main.scss';

footer {
    

    .contacts {
        padding: $container-pad 0;

        .contacts-box {
            display: flex;
            justify-content: space-between;

            .info-box {
                img {
                    height: 25px;
                    margin: 10px 0;
                }
                h3 {
                    color: $purple;
                    margin: 10px 0;
                }
                .info {
                    color: $grey;
                    font-size: 11px;
                    margin: 3px;
                }
            }
        } // end of contacts-box

        .input-container {
            display: flex;

            div {
                width: 50%;
                padding: 15px;
                display: flex;
                flex-direction: column;
            } 
        } // end of input-container

        .button {
            margin-top: 14px;
            background: $orange;
            color: $sugar;
            
                
            &:hover {
                background-color: $purple;
            }
        }

    } // end of contacts
} // end of footer

</style>
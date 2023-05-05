<script>

</script>


<template>
<div class="area">
<div class="bar">
        <nav>
            <div class="nav nav-tabs" id="nav-tab" role="tablist">
                <button class="nav-link active" id="nav-home-tab" data-bs-toggle="tab" data-bs-target="#nav-home" type="button" role="tab" aria-controls="nav-home" aria-selected="true">
                    商品上架
                </button>

                <button class="nav-link" id="nav-profile-tab" data-bs-toggle="tab" data-bs-target="#nav-profile" type="button" role="tab" aria-controls="nav-profile" aria-selected="false">
                    我的商品
                </button>

                <button class="nav-link" id="nav-contact-tab" data-bs-toggle="tab" data-bs-target="#nav-contact" type="button" role="tab" aria-controls="nav-contact" aria-selected="false">
                    訂單
                </button>
            </div>
        </nav>
</div>


<div class="content">
    
        <div class="sellSystem tab-content" id="nav-tabContent">
            <div class="add tab-pane fade show active" id="nav-home" role="tabpanel" aria-labelledby="nav-home-tab">
            Want to sell

            </div>

            <div class="products tab-pane fade" id="nav-profile" role="tabpanel" aria-labelledby="nav-profile-tab">
                <div class="input">
                    My products
                </div>
                <div class="ans">
                    ~~~
                </div>

            </div>

            <div class="order tab-pane fade" id="nav-contact" role="tabpanel" aria-labelledby="nav-contact-tab">
            My order

            </div>
        </div>

    

<!-- content尾巴 -->
</div>





<!-- area尾巴 -->
</div>

</template>

<style lang="scss" scoped>
.area{
    width:70%;
    height:60%;



    .bar{
        width:100%;
        height: 10%;
        background-color: white;
    }
    .content{
        width: 100%;
        height: 90%;
        background-color: rgba(138, 173, 238, 0.6);
        // border: 1px solid black;
        
        

        .tab-pane{
            width: 100%;
            height: 383.725px;
        }
        .products{
            // border: 5px solid black;
            
            .input{
                width: 100%;
                height: 10%;
                // border: 1px solid black;
            }

            .ans{
                width:100%;
                height: 90%;
                border: 1px solid white;
            }

        }
    }



    
}

</style>
<template>
    <div>
        <b-button id="show-btn" variant="primary" @click="showModal">Abrir Modal</b-button>
<!--        <b-button id="toggle-btn" @click="toggleModal">Toggle Modal</b-button>-->

        <b-modal ref="my-modal" size="xl" centered hide-footer title="Paquetes de Lifecoins"
                 :header-bg-variant="headerBgVariant"
                 :header-text-variant="headerTextVariant"
        >
            <div class="card" style="box-shadow: 2px 2px 6px rgba(0 ,0 , 0, 0.25)">
                <div class="card-header text-uppercase">
                    <span class="text-danger">Paquetes de lifecoins</span>
                </div>
                <div class="card-body row">
                    <div class="row col-md-6">
                        <div class="col-md-3 border border-danger text-danger text-center m-2 pt-2 rounded-lg">
                            <b-icon icon="server" scale="1.5"></b-icon>
                            <br>
                            <span class="mt-2">1000 Lifecoins</span>
                            <br>
                            <span class="mb-1">190 EUR</span>
                            <br>
                            <span>Cantidad {{ counter1 }}</span>
                            <br>
                            <div class="mb-2">
                                <b-icon v-on:click="counter1 += 1, checkValue()" icon="plus" scale="1"></b-icon>
                                <b-icon v-on:click="counter1 -= 1, checkValue()" v-if="counter1 > 0" icon="dash" scale="1"></b-icon>
                            </div>
                        </div>
                        <div class="col-md-3 border border-danger text-danger text-center m-2 pt-2 rounded-lg">
                            <b-icon icon="server" scale="1.5"></b-icon>
                            <br>
                            <span class="mt-2">1500 Lifecoins</span>
                            <br>
                            <span class="mb-1">270 EUR</span>
                            <br>
                            <span>Cantidad {{ counter2 }}</span>
                            <br>
                            <div class="mb-2">
                                <b-icon v-on:click="counter2 += 1, checkValue()" icon="plus" scale="1"></b-icon>
                                <b-icon v-on:click="counter2 -= 1, checkValue()" v-if="counter2 > 0" icon="dash" scale="1"></b-icon>
                            </div>
                        </div>
                        <div class="col-md-3 border border-danger text-danger text-center m-2 pt-2 rounded-lg">
                            <b-icon icon="server" scale="1.5"></b-icon>
                            <br>
                            <span class="mt-2">3000 Lifecoins</span>
                            <br>
                            <span class="mb-1">510 EUR</span>
                            <br>
                            <span>Cantidad {{ counter3 }}</span>
                            <br>
                            <div class="mb-2">
                                <b-icon v-on:click="counter3 += 1, checkValue()" icon="plus" scale="1"></b-icon>
                                <b-icon v-on:click="counter3 -= 1, checkValue()" v-if="counter3 > 0" icon="dash" scale="1"></b-icon>
                            </div>
                        </div>
                        <div class="col-md-3 border border-danger text-danger text-center m-2 pt-2 rounded-lg">
                            <b-icon icon="server" scale="1.5"></b-icon>
                            <br>
                            <span class="mt-2">5000 Lifecoins</span>
                            <br>
                            <span class="mb-1">800 EUR</span>
                            <br>
                            <span>Cantidad {{ counter4 }}</span>
                            <br>
                            <div class="mb-2">
                                <b-icon v-on:click="counter4 += 1, checkValue()" icon="plus" scale="1"></b-icon>
                                <b-icon v-on:click="counter4 -= 1, checkValue()" v-if="counter4 > 0" icon="dash" scale="1"></b-icon>
                            </div>
                        </div>
                        <div class="col-md-3 border border-danger text-danger text-center m-2 pt-2 rounded-lg">
                            <b-icon icon="server" scale="1.5"></b-icon>
                            <br>
                            <span class="mt-2">10000 Lifecoins</span>
                            <br>
                            <span class="mb-1">1500 EUR</span>
                            <br>
                            <span>Cantidad {{ counter5 }}</span>
                            <br>
                            <div class="mb-2">
                                <b-icon v-on:click="counter5 += 1, checkValue()" icon="plus" scale="1"></b-icon>
                                <b-icon v-on:click="counter5 -= 1, checkValue()" v-if="counter5 > 0" icon="dash" scale="1"></b-icon>
                            </div>
                        </div>
                        <div class="col-md-3 border border-danger text-danger text-center m-2 pt-2 rounded-lg">
                            <b-icon icon="server" scale="1.5"></b-icon>
                            <br>
                            <span class="mt-2">20000 Lifecoins</span>
                            <br>
                            <span class="mb-1">2800 EUR</span>
                            <br>
                            <span>Cantidad {{ counter6 }}</span>
                            <br>
                            <div class="mb-2">
                                <b-icon v-on:click="counter6 += 1, checkValue()" icon="plus" scale="1"></b-icon>
                                <b-icon v-on:click="counter6 -= 1, checkValue()" v-if="counter6 > 0" icon="dash" scale="1"></b-icon>
                            </div>
                        </div>
                    </div>
                    <div class="col-md-6">
                        <b-card class="text-center" header="Resumen del pedido" style="box-shadow: 2px 2px 6px rgba(0 ,0 , 0, 0.25)">
                            <blockquote class="blockquote mb-0" style="font-size:0.6rem;">
                                <div class="col-md-12 text-sm-center">
                                    <table class="table table-responsive rounded-lg" style="box-shadow: 2px 2px 6px rgba(0 ,0 , 0, 0.25)">
                                        <thead class="table-active">
                                        <tr>
                                            <th>Paquetes(Total de Lifecoins)</th>
                                            <th>Precio(EUR)</th>
                                            <th>Cantidad(Unidades)</th>
                                            <th>Descuento 5%</th>
                                            <th>Total(EUR)</th>
                                        </tr>
                                        </thead>
                                        <tbody id="example_body">
                                            <!--body here-->
                                        </tbody>
                                        <tfoot id="example_footer" class="table-active font-weight-bold">
                                            <!--footer here-->
                                        </tfoot>
                                    </table>
                                </div>
                                <div>
                                    <b-form @submit="onSubmit" v-if="show">
                                        <b-button type="submit" variant="danger" class="text-uppercase float-right mr-3">Generar pedido</b-button>
                                    </b-form>
                                </div>
                            </blockquote>
                        </b-card>
                    </div>
                </div>
            </div>
        </b-modal>
    </div>
</template>

<script>
    export default {
        methods: {
            showModal() {
                this.$refs['my-modal'].show()
            },
            hideModal() {
                this.$refs['my-modal'].hide()
            },
            toggleModal() {
                // We pass the ID of the button that we want to return focus to
                // when the modal has hidden
                this.$refs['my-modal'].toggle('#toggle-btn')
            },
            onSubmit(event) {
                event.preventDefault();
                let packs = [{
                    pack01:this.counter1,
                    pack02:this.counter2,
                    pack03:this.counter3,
                    pack04:this.counter4,
                    pack05:this.counter5,
                    pack06:this.counter6,
                }];
                console.log(packs);
            },
            checkValue: function () {
                $('#example_body').html('');
                $('#example_footer').html('');
                let total1, total2, total3, total4, total5, total6 = 0;
                let percent1, percent2, percent3, percent4, percent5, percent6 = 0;
                if ((this.counter6 + this.counter5 + this.counter4 + this.counter3 + this.counter2 + this.counter1) > 0){
                    this.show = true;
                }else{
                    this.show = false;
                }
                if (this.counter6 >= 1){
                    total6 = (2800*this.counter6);
                    percent6 = total6*0.05;
                    $('#example_body').append('<tr>\n' +
                        '                                            <td>20000</td>\n' +
                        '                                            <td>2800</td>\n' +
                        '                                            <td>'+this.counter6+'</td>\n' +
                        '                                            <td>'+percent6+'</td>\n' +
                        '                                            <td>'+(total6-percent6)+'</td>\n' +
                        '                                        </tr>');
                }
                if (this.counter5 >= 1){
                    total5 = (1500*this.counter5);
                    percent5 = total5*0.05;
                    $('#example_body').append('<tr>\n' +
                        '                                            <td>10000</td>\n' +
                        '                                            <td>1500</td>\n' +
                        '                                            <td>'+this.counter5+'</td>\n' +
                        '                                            <td>'+percent5+'</td>\n' +
                        '                                            <td>'+(total5-percent5)+'</td>\n' +
                        '                                        </tr>');
                }
                if (this.counter4 >= 1){
                    total4 = (800*this.counter4);
                    percent4 = total4*0.05;
                    $('#example_body').append('<tr>\n' +
                        '                                            <td>5000</td>\n' +
                        '                                            <td>800</td>\n' +
                        '                                            <td>'+this.counter4+'</td>\n' +
                        '                                            <td>'+percent4+'</td>\n' +
                        '                                            <td>'+(total4-percent4)+'</td>\n' +
                        '                                        </tr>');
                }
                if (this.counter3 >= 1){
                    total3 = (510*this.counter3);
                    percent3 = total3*0.05;
                    $('#example_body').append('<tr>\n' +
                        '                                            <td>3000</td>\n' +
                        '                                            <td>510</td>\n' +
                        '                                            <td>'+this.counter3+'</td>\n' +
                        '                                            <td>'+percent3+'</td>\n' +
                        '                                            <td>'+(total3-percent3)+'</td>\n' +
                        '                                        </tr>');
                }
                if (this.counter2 >= 1){
                    total2 = (270*this.counter2);
                    percent2 = total2*0.05;
                    $('#example_body').append('<tr>\n' +
                        '                                            <td>1500</td>\n' +
                        '                                            <td>270</td>\n' +
                        '                                            <td>'+this.counter2+'</td>\n' +
                        '                                            <td>'+percent2+'</td>\n' +
                        '                                            <td>'+(total2-percent2)+'</td>\n' +
                        '                                        </tr>');
                }
                if (this.counter1 >= 1){
                    total1 = (190*this.counter1);
                    percent1 = total1*0.05;
                    $('#example_body').append('<tr>\n' +
                        '                                            <td>1000</td>\n' +
                        '                                            <td>190</td>\n' +
                        '                                            <td>'+this.counter1+'</td>\n' +
                        '                                            <td>'+percent1+'</td>\n' +
                        '                                            <td>'+(total1-percent1)+'</td>\n' +
                        '                                        </tr>');
                }
                let total_package = (this.counter6*2000) + (this.counter5*10000) + (this.counter4*5000) + (this.counter3*3000) + (this.counter2*1500) + (this.counter1*1000);
                let total_price = (this.counter6*2800) + (this.counter5*1500) + (this.counter4*800) + (this.counter3*510) + (this.counter2*270) + (this.counter1*190);
                let total_qty = this.counter6 + this.counter5 + this.counter4 + this.counter3 + this.counter2 + this.counter1;
                let total_percent = total_price*0.05;
                let total = total_price - total_percent;
                $('#example_footer').html('<tr>\n' +
                    '                                            <td>'+total_package+'</td>\n' +
                    '                                            <td>'+total_price+'</td>\n' +
                    '                                            <td>'+total_qty+'</td>\n' +
                    '                                            <td>'+total_percent+'</td>\n' +
                    '                                            <td>'+total+'</td>\n' +
                    '                                        </tr>');

            }
        },
        data() {
            return{
                headerBgVariant: 'danger',
                headerTextVariant: 'light',
                counter1: 0,
                counter2: 0,
                counter3: 0,
                counter4: 0,
                counter5: 0,
                counter6: 0,
                show: false,
            }
        }
    }
</script>

<template>
    <canvas @mousemove="draw" @mousedown="drawing = true" @mouseup="drawing = false"
            ref="canSign" class="signature" width="380" height="200">
    </canvas>
</template>

<script>
    export default {
        data() {
            return {
                ctx: null,
                x_0: -1,
                y_0: -1,
                drawing: false
            }
        },
        methods: {
            draw( event ){
                if ( !this.drawing ) {
                    this.x_0 = -1;
                    this.y_0 = -1;
                    return;
                }
                if ( this.x_0 < 0 || this.y_0 < 0 ){
                    this.x_0 = event.offsetX;
                    this.y_0 = event.offsetY;
                    return;
                }
                const x_1 = event.offsetX;
                const y_1 = event.offsetY;
                this.ctx.beginPath();
                this.ctx.moveTo(this.x_0, this.y_0);
                this.ctx.lineTo(x_1, y_1);
                this.ctx.stroke();

                this.x_0 = x_1;
                this.y_0 = y_1;
            }
        },
        mounted(){
            this.ctx = this.$refs.canSign.getContext('2d');
            this.ctx.strokeStyle = '#303030';
            this.ctx.lineWidth = 5;
            this.ctx.lineCap = 'round';
        }
    }
</script>

<style>
    .signature {
        cursor: pointer;
        background-color: white;
        border-radius: 5px;
        box-shadow: inset 0 0 15px rgba(0,0,0,0.9);
    }
</style>
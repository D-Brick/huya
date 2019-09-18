<template>
    <div class="nav">
        <ul class="nav-list">
            <li :class="item.nid === currentNid ? 'nav-list-item-activity' : 'nav-list-item'"
                v-for="item in navList"
                :key="item.nid"
                @click="selectNav(item.nid)"
            >{{item.content}}
            </li>
        </ul>
    </div>
</template>

<script lang="ts">
import { Component, Prop, Vue } from 'vue-property-decorator'

@Component
export default class Navigator extends Vue {
    data() {
        return {
            currentNid: 0
        }
    }

    @Prop({
        type: Array,
        default() {
            return [
                {
                    nid: 0,
                    content: '首页'
                },
                {
                    nid: 1,
                    content: '王者荣耀'
                },
                {
                    nid: 2,
                    content: '绝地求生'
                },
                {
                    nid: 3,
                    content: '英雄联盟'
                },
                {
                    nid: 4,
                    content: '星秀'
                }
            ]
        }
    }) 
    navList!: Array<any>

    selectNav(nid: number) {
        this.currentNid = nid
    }
}

</script>

<style lang="stylus" scoped>
    .nav
        display flex
        justify-content center

        width 100%
        height 46px
        .nav-list
            display flex
            flex-direction row
            align-items: center

            padding-left 10px

            font-size 15px
            font-weight 280
            color #151515
            .nav-list-item
                margin-right 25px
                padding-bottom 3px

            .nav-list-item-activity
                margin-right 25px
                padding-bottom 3px
                border-bottom 2px solid #FFA200
                
                color #FFA200
</style>
<template>
<div id="firstcomponent">
    <h1>I am a title.</h1>
    <img src="../assets/logo.png">
    <!-- <a> written by {{ author }} </a> -->
    <div id="list" v-for="(item,index) in items" :key="index" @click="myClick(item)">
        <div class="item-left">
            <div class="item-title">{{item.title}}</div>
            <div class="item-content">{{item.content}}</div>
        </div>
        <div class="item-right">
            <img src="../assets/logo.png" class="item-image">
      </div>

            <div class="item-line"></div>
            <!-- <br> -->
        </div>
    </div>
</template>

<script>
// var items = ["first", "second", "third", "fourth"];

var items = [{
        title: "firs",
        content: "first content"
    },
    {
        title: "second",
        content: "second content"
    },
    {
        title: "third",
        content: "third content"
    },
    {
        title: "fourth",
        content: "fourth content"
    },
    {
        title: "fifth",
        content: "fifth content"
    }
];

export default {
    data() {
        return {
            items: items
        };
    },
    methods: {
        myClick(item) {
            console.log(item);
            switch (item.title) {
                case "first":
                    this.$router.push({
                        path: "HelloWorld"
                    });
                    break;
                case "second":
                    this.$router.push({
                        path: "Second"
                    });
                    break;
                case "third":
                    break;
                case "fourth":
                    break;
            }
        }
    }
};
</script>

<style>
* {
    margin: 0 auto;
    padding: 0;
}

#list {
    color: rgb(30, 30, 122);
    width: auto;
    height: 120px;
    list-style-type: none;
    background-color: bisque;
    margin-bottom: 1px;
}

#list .item-title {
    height: 50%;
    /* begin 设置最大行数，超过折行显示... */
    word-break: break-all;
    display: -webkit-box;
    -webkit-line-clamp: 2;
    -webkit-box-orient: vertical;
    overflow: hidden;
    /* end */
    font-size: 20px;
    background-color: gold;
    text-align: left;
    padding-left: 10px;
    padding-top: 10px;
}

#list .item-content {
    font-size: 18px;
    text-align: left;
    padding-left: 10px;
    padding-top: 10px;
    background-color: dodgerblue;
}

#list .item-image {
    width: 60px;
    height: 60px;
    margin-top: 30px;
    border-radius: 5px;
    background-clip: content-box;
}

#list .item-left {
    height: 100%;
    width: 60%;
    text-align: center;
    float: left;
    background-color: aqua;
}

#list .item-right {
    height: 100%;
    width: 40%;
    float: right;
}

#list .item-line {
    height: 1px;
    width: 100%;
    background-color: rgb(134, 9, 9);
    clear: both;
}
</style>

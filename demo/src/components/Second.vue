<template>
<div id="vue_det">
    <ul class="tab-head">
        <li class="tab-head-item">兴趣爱好1</li>
        <li class="tab-head-item">兴趣爱好2</li>
        <li class="tab-head-item">兴趣爱好3</li>
        <li class="tab-head-item">兴趣爱好4</li>
        <li class="tab-head-item">兴趣爱好5</li>
        <li class="tab-head-item">兴趣爱好6</li>
        <li class="tab-head-item">兴趣爱好7</li>
        <li class="tab-head-item">兴趣爱好8</li>
        <li class="tab-head-item">兴趣爱好9</li>
        <li class="tab-head-item">兴趣爱好10</li>
        <li class="tab-head-item">兴趣爱好11</li>
    </ul>
    <h1>site : {{site}}</h1>
    <h1>url : {{url}}</h1>
    <h1>{{details()}}</h1>
    <div v-bind:disabled='idButtonDisable' id="button">学习</div>
    <div class="parent">
        <div class="children"></div>
    </div>

    <br>
    <div class="absoulte-parent">
        <div class="Absolute-Center"></div>
    </div>
    <br>
    <div id="ex3_container">
        <div id="ex3_content">Hello World</div>
    </div>
</div>
</template>

<script>
var data = {
    site: "菜鸟教程",
    url: "www.runoob.com",
    alexa: "10000",
    idButtonDisable: true,
};
export default {
    data() {
        return data;
    },
    methods: {
        details: function () {
            return this.site + " - 学的不仅是技术，更是梦想！加油";
        }
    }
}

// document.write('<p>data '+data.site +' addd</p>');
</script>

<style>
#button {
    color: blue;
    font-size: 20px;
    background-color: bisque;
    width: 40px;
    padding: 3px 10px 3px 10px;
    text-align: center;
    margin: 0 auto;
}

.parent {
    margin: 0 auto;
    width: 200px;
    height: 200px;
    background-color: red;
}

.children {
    width: 100px;
    height: 100px;
    padding: 50px;
    background-color: black;
    background-clip: content-box;
    /*居中的关键*/
}

.absoulte-parent {
    margin: 0 auto;
    width: 200px;
    height: 200px;
    background-color: red;
    position: relative;
}

.Absolute-Center {
    width: 50%;
    height: 50%;
    overflow: auto;
    margin: auto;
    position: absolute;
    background-color: wheat;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
}

#ex3_container {
    margin: 0 auto;
    width: 200px;
    height: 200px;
    background-color: yellow;
    position: relative;
}

#ex3_content {
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    -webkit-transform: translate(-50%, -50%);
    background-color: gray;
    color: white;
    position: absolute;
}

.tab-head {
    list-style-type: none;
    display: -webkit-box;
    display: -webkit-flex;
    display: -ms-flexbox;
    display: flex;
    -webkit-flex-wrap: nowrap;
    -ms-flex-wrap: nowrap;
    flex-wrap: nowrap;
    -webkit-box-pack: justify;
    -webkit-justify-content: space-between;
    -ms-flex-pack: justify;
    justify-content: space-between;
    background: #FF4878;
    padding: 0;
    overflow: auto;
}

.tab-head-item {
    background-color: green;
    -webkit-box-flex: 1;
    -webkit-flex: 1 0 auto;
    -ms-flex: 1 0 auto;
    flex: 1 0 auto;
    color: white;
    padding: 10px 5px;
}
</style>

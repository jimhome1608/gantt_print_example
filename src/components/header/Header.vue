<!-- 
/**
 * @author Saki
 * @date 2019-03-28 13:15:02
 * @Last Modified by: Saki
 * @Last Modified time: 2019-04-28 21:01:28
 *
 * Header with title and buttons
 */ 
-->
<!--
/* <remove-on-release> */
/* cSpell: ignore toggleable */
/* </remove-on-release> */
-->
<template>
    <header class="app-header">
        <h1><a :href="link">{{ $props.title }}</a></h1>
        <fullscreen-button></fullscreen-button>
    </header>
</template>

<script>
    import FullscreenButton from './FullscreenButton.vue';

    export default {
        name  : 'app-header',
        props : {
            link  : { type : String, default : '..' },
            title : { type : String, default : 'Example Header' }
        },
        components : {
            FullscreenButton
        }
    } // exports the header components
</script>

<style lang="scss">
    .app-header {
        padding             : 2.1em .5em 2.1em 5em;
        background          : url(~bryntum-resources/images/logo_bryntum_bw.png) #2667c8;
        background-repeat   : no-repeat;
        background-size     : 40px;
        background-position : center left 1.5em;
        display             : flex;
        align-items         : center;        
    }

    .app-header h1 {
        margin      : 0;
        font-size   : 1.8em;
        color       : #fff;
        font-weight : normal;
        flex        : 1;
        align-self  : center;
    }

    .app-header a {
        color           : inherit;
        text-decoration : none;
    }

</style>

<!-- eof -->

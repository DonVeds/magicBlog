<script>
    export let name='daily frontend';
    export let text='the development world\'s beguiling broadsheet of choice';
    export let ad = ['21.4% OFF', 'RITA SKEETER\'S HIT SENASTION'];
    export let weather = ['REACT.JS - 141k stars','ANGULAR.JS - 59.6k stars','VUE.JS - 154k stars','SVELTE.JS - 27.4 stars'];
</script>

<header>
    <div class="header-the">
        <hr class="header-the-line">
        <p class="header-the-p">The</p>
        <hr class="header-the-line">
    </div>
    <h1 class="header-name">{name}</h1>
    <p class="header-text">&#10038{text}&#10038</p>
    <hr class="header-line"> 
    <div class="header-ad">
        <p class="header-ad-sale">{ad[0]}</p>
        <p class="header-ad-descr">{ad[1]}</p>
    </div>
    <div class="header-info">
        <div class="header-info-weather">
            <p class="header-info-weather-title">NATIONAL WEATHER</p>
            <p class="header-info-weather-text">{weather[0]}<br>{weather[1]}<br>{weather[2]}<br>{weather[3]}</p>
        </div>
    </div>
    <img class="header-gif" src="https://lh3.googleusercontent.com/Ug1d5vabk0yuIcmboUU5gHhr2jl8queOt0lhQALi0uB_qKF7YrgUpd8NNX9hK_SSwIhUFHBk3zPUeml7qssNgmn49WwoDKD8jh1XkJKKC6kpy8L8gIn3LeBAHwND2bo_PetP8Z-vXxfiYPOUjVOaaq9xcZ8dYnayrMPtdY9hH883LtQbNeqSaO38NPdSuH1Jg6Et4MvQP_Rjwjced377A6tHkUMM67ZKbs1XHwzGzuGy4KEIuA0Xih6eW9o3GVJCK1FrhIH2rjb96ErWHJ5t3BNtDQCVQVyGlryKumVYAMCj77Gl9o4Jxql8jxdNyh_ExmwezBE1Ix2KEySb5pn33QGhJUURAmUyTWifjC3B70ZYs2FTku-60Pc_Uwscy12wN282BBmoLyEO60mwhnq2XZi2HfkR-5Fapv4jHhWjRY9yFDvEjo1dacChbKnPe4abAah1wTNXvtfA9_QCqygXQQsXvCCAo9J0kj_OYeOT34j0y2FJgO5dNe31bshulU-IFpI38fnaBv5g8NFFp6xDTjDHYdKZuNcQ14l4vHfdPidOW2HBg1X1l90tif6C0tpmwrP3hSnxoid7dh3hOkoclJipydyklh7F3saCD_Mv8j--8-o9owxf9iLRwz6vMQLnj9m4YncStTayhWfohF9YJdiB2gYuEtCDUeppCvx9U5hm5lxnALINzcmL=w500-h212-no" alt="">
</header>

<style>
    header{
        display: grid;
        grid-template-columns: 30% auto 30%;
        grid-template-rows: auto ;
        grid-template-areas: 
            "the the the"
            "name name name"
            "text text text"
            "line line line"
            "ad info gif";
    }

    .header-the { 
        grid-area: the;
        display: flex;
        justify-content: center;
        align-items: center;
        height: 2.5em;
    }
    .header-the-line{
        margin-left: 0;
        margin-right: 0;
        flex-grow: 20; 
        height: 1px;
        background-color: black;
    }
    .header-the-p{
        flex-grow: 1;
        font-family: 'Marck Script', cursive;
        font-weight: 600;
        font-size: 2em;
    }

    .header-name {
        grid-area: name;
        text-transform: uppercase;
        font-size: 4em;
        font-weight: 100;
        font-family: 'Ruslan Display', cursive;
        margin: 0;
        overflow: hidden; /* Ensures the content is not revealed until the animation */
        white-space: nowrap; /* Keeps the content on a single line */
        margin: 0 auto; /* Gives that scrolling effect as the typing happens */
        letter-spacing: .15em; /* Adjust as needed */
        animation: 
            typing 3.5s steps(40, end);
        animation-iteration-count: infinite;
    }
    @keyframes typing {
        from { width: 0 }
        to { width: 100% }
    }

    .header-text {
        font-family: 'Kelly Slab', cursive;
        grid-area: text;
        margin: 0;
        font-weight: bold;
        text-transform: uppercase;
    }

    .header-line {
        grid-area: line;
        width: 100%;
        height: 1px;
        background-color: black;
    }

    .header-ad {
        grid-area: ad;
        display: flex;
        align-items: center;
        border: 2px solid #555555;
        font-family: 'Kelly Slab', cursive;
        padding: 5px;
    }

    .header-ad-sale {
        flex-grow: 1;
        margin: 0;
        font-weight: bold;
        font-size: 1em
    }

    
    .header-ad-descr {
        flex-grow: 2;
        margin: 0;
    }

    .header-info{
        grid-area: info;
        margin: 0px 10px;
    }

    .header-info-weather-title {
        margin: 0;
        font-family: 'Kelly Slab', cursive;
        font-weight: bold;
    }
    .header-info-weather-text {
        font-size: 12px;
        margin: 0;
        /* text-align: left; */
    }

    .header-gif {
        height: 80px;
    }

</style>
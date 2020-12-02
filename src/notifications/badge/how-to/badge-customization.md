# Badge Customization

## Colour customization

Even though badges come with `8 predefined colors`, you can also customize the colour of the badge as desired.

{% tab template="badge/color", isDefaultActive=true %}

```html
<template>
    <div id='element'>
        <h1>Color Customization <span class="e-badge e-badge-primary e-badge-pill green">New</span></h1>
        <h1>Color Customization <span class="e-badge e-badge-primary e-badge-pill bue">New</span></h1>
        <h1>Color Customization <span class="e-badge e-badge-primary e-badge-pill purple">New</span></h1>
        <h1>Color Customization <span class="e-badge e-badge-primary e-badge-pill gradient">New</span></h1>
    </div>
</template>
<script>
import Vue from "vue";

export default {
  data() {
    return {};
  }
}
</script>
<style>
    @import "../node_modules/@syncfusion/ej2-base/styles/material.css";
    @import "../node_modules/@syncfusion/ej2-vue-notifications/styles/material.css";

    #element {
    display: table;
    width: 560px;
    margin: auto;
    height: 200px;
    border: 1px solid #dddddd;
    border-radius: 3px;
    justify-content: center;
    position: relative;
    top: 55px;
    }

    h1 {
    text-align: center;
    }

    #element .e-badge.green {
    background: #329378;
    color: #fff;
    }

    #element .e-badge.blue {
    background: #5f65b8;
    color: #fff;
    }

    #element .e-badge.gradient {
    background: #4776E6;
    /* fallback for old browsers */
    background: -webkit-linear-gradient(to top, #8E54E9, #4776E6);
    /* Chrome 10-25, Safari 5.1-6 */
    background: linear-gradient(to top, #8E54E9, #4776E6);
    /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
    color: #fff;
    }

    #element .e-badge.purple {
    background: #9a428f;
    color: #fff;
    }


</style>

```

{% endtab %}

## Customize badge size

Badges are designed to change its size based on the content. To change the size of a badge, adjust the `font size` of the badge.

{% tab template="badge/size", isDefaultActive=true %}

```html
<template>
    <div id='element'>
        <h1>Badge Component <span class="e-badge e-badge-primary size_1">New</span></h1>
        <h1>Badge Component <span class="e-badge e-badge-primary size_2">New</span></h1>
        <h1>Badge Component <span class="e-badge e-badge-primary size_3">New</span></h1>
    </div>
</template>
<script>
import Vue from "vue";

export default {
  data() {
    return {};
  }
}
</script>
<style>
@import "../node_modules/@syncfusion/ej2-base/styles/material.css";
    @import "../node_modules/@syncfusion/ej2-vue-notifications/styles/material.css";

    #element {
        display: block;
        width: 400px;
        margin: auto;
        border: 1px solid #dddddd;
        border-radius: 3px;
        justify-content: center;
    }

    h1 {
        text-align: center;
    }

    .e-badge.size_1 {
        font-size: 12px;
    }

    .e-badge.size_2 {
        font-size: 16px;
    }

    .e-badge.size_3 {
        font-size: 18px;
    }

</style>

```

{% endtab %}

## Custom position

Even though the badges support the conventional `top` and `bottom` positions, the position of the badges can be changed as desired.
This can be done by adding a custom class to the badge element to override the default position applied from the source.

{% tab template="badge/custom-position", isDefaultActive=true %}

```html
<template>
    <div id='element'>
        <div style="width: 200px;margin: 10px auto;">
            <div class="badge-block">
                <div class="whatsapp svg_icons"></div>
                <!-- Warning Colored Notification Badge -->
                <span class="e-badge e-badge-warning e-badge-notification e-badge-overlap leftTop">99+</span>
            </div>

            <div class="badge-block">
                <div class="facebook svg_icons"></div>
                <!-- Danger Colored Notification Badge -->
                <span class="e-badge e-badge-danger e-badge-notification e-badge-overlap leftTop">99+</span>
            </div>

            <div class="badge-block">
                <div class="skype svg_icons"></div>
                <!-- Secondary Colored Notification Badge -->
                <span class="e-badge e-badge-secondary e-badge-notification e-badge-overlap leftTop">18</span>
            </div>
        </div>
        <div style="width: 200px;margin: 10px auto;">
            <div class="badge-block">
                <div class="whatsapp svg_icons"></div>
                <!-- Warning Colored Notification Badge -->
                <span class="e-badge e-badge-warning e-badge-notification e-badge-overlap leftBottom">99+</span>
            </div>

            <div class="badge-block">
                <div class="facebook svg_icons"></div>
                <!-- Danger Colored Notification Badge -->
                <span class="e-badge e-badge-danger e-badge-notification e-badge-overlap leftBottom">99+</span>
            </div>

            <div class="badge-block">
                <div class="skype svg_icons"></div>
                <!-- Secondary Colored Notification Badge -->
                <span class="e-badge e-badge-secondary e-badge-notification e-badge-overlap leftBottom">18</span>
            </div>
        </div>
    </div>
</template>
<script>
import Vue from "vue";

export default {
  data() {
    return {};
  }
}
</script>
<style>
@import "../node_modules/@syncfusion/ej2-base/styles/material.css";
    @import "../node_modules/@syncfusion/ej2-vue-notifications/styles/material.css";

    #element {
        display: flex;
        width: 500px;
        margin: auto;
        border: 1px solid #dddddd;
        border-radius: 3px;
        justify-content: center;
        position: relative;
        top: 130px;
        }

        .badge-block {
        position: relative;
        display: inline-block;
        margin: 10px 13px 10px 10px;
        }

        .badge-block .e-badge.leftBottom {
        transform: translateX(-150%) translateY(200%);
        }

        .badge-block .e-badge.leftTop {
        transform: translateX(-150%);
        }

        /* SVG Icons */

        .facebook {
        background: transparent url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32'%3E%3Cpath fill='#3b5998' d='M1.82 0h28.36c.908 0 1.645.819 1.645 1.829v28.342c0 1.011-.737 1.829-1.645 1.829h-8.188V18.852h3.934v-4.271h-3.934V13.15c0-1.04.828-1.883 1.853-1.883h2.081V6.998h-4.505c-2.737 0-4.955 2.251-4.955 5.029v2.554h-3.55v4.271h3.55V32H1.82c-.908 0-1.645-.818-1.645-1.829V1.829C.175.819.912 0 1.82 0z'/%3E%3C/svg%3E") no-repeat 100% 100%;
        }

        .skype {
        background: transparent url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32'%3E%3Cpath fill='#00aff0' d='M16.067 5.579c-1.68 0-3.166.234-4.416.696-1.265.468-2.247 1.15-2.92 2.028a4.893 4.893 0 0 0-1.022 3.046c0 1.192.328 2.207.974 3.016.636.796 1.505 1.433 2.585 1.891 1.056.449 2.383.847 3.944 1.181 1.148.24 2.077.471 2.76.684.657.204 1.198.502 1.606.885.392.367.582.833.582 1.428 0 .752-.364 1.366-1.114 1.878-.767.523-1.787.789-3.031.789-.905 0-1.64-.131-2.187-.389-.541-.257-.965-.585-1.261-.976-.308-.406-.599-.922-.864-1.533-.24-.56-.537-.995-.883-1.288-.363-.307-.809-.462-1.326-.462-.63 0-1.157.196-1.57.584a1.89 1.89 0 0 0-.628 1.421c0 .882.325 1.797.964 2.719a7.062 7.062 0 0 0 2.478 2.199c1.413.75 3.226 1.131 5.388 1.131 1.8 0 3.383-.278 4.702-.827 1.333-.554 2.362-1.335 3.058-2.32a5.711 5.711 0 0 0 1.053-3.358c0-1.037-.206-1.928-.612-2.65a5.125 5.125 0 0 0-1.697-1.792c-.706-.46-1.572-.856-2.574-1.176-.99-.317-2.11-.61-3.327-.871a55.674 55.674 0 0 1-2.082-.51 6.642 6.642 0 0 1-1.211-.47c-.382-.191-.683-.42-.897-.681a1.328 1.328 0 0 1-.301-.876c0-.559.306-1.031.933-1.443.652-.427 1.529-.643 2.608-.643 1.16 0 2.006.195 2.512.579.52.397.976.959 1.35 1.672.325.558.617.946.898 1.195.302.268.74.404 1.297.404.613 0 1.133-.217 1.545-.646.41-.425.617-.914.617-1.452 0-.559-.158-1.136-.47-1.717-.31-.574-.801-1.127-1.463-1.644-.657-.514-1.493-.931-2.485-1.24-.987-.306-2.168-.462-3.513-.462zM8.95 0c1.708 0 3.298.492 4.643 1.339.836-.144 1.696-.22 2.575-.22 8.31 0 15.049 6.738 15.049 15.049 0 1.109-.121 2.189-.35 3.229a8.728 8.728 0 0 1-11.945 11.567c-.892.166-1.814.253-2.754.253-8.311 0-15.05-6.738-15.05-15.049 0-1.037.105-2.049.304-3.026A8.727 8.727 0 0 1 8.95 0z'/%3E%3C/svg%3E") no-repeat 100% 100%;
        }

        .twitter {
        background: transparent url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32'%3E%3Cpath fill='#1da1f2' d='M22.155 5.26c1.888 0 3.594.658 4.792 1.712a14.9 14.9 0 0 0 4.169-1.316c-.49 1.267-1.531 2.33-2.887 3A15.3 15.3 0 0 0 32 7.802a12.298 12.298 0 0 1-3.276 2.807c.013.233.019.467.019.703 0 7.164-6.604 15.427-18.679 15.427-3.708 0-7.158-.897-10.064-2.436.514.05 1.037.076 1.566.076 3.076 0 5.907-.867 8.153-2.322-2.872-.043-5.297-1.612-6.132-3.766a7.864 7.864 0 0 0 2.964-.093c-3.003-.498-5.266-2.688-5.266-5.316l.001-.067a7.637 7.637 0 0 0 2.974.678c-1.762-.974-2.921-2.633-2.921-4.514 0-.994.324-1.925.889-2.726 3.238 3.28 8.075 5.438 13.532 5.666a4.542 4.542 0 0 1-.17-1.237c0-2.994 2.939-5.421 6.565-5.421z'/%3E%3C/svg%3E") no-repeat 100% 100%;
        }

        .whatsapp {
        background: transparent url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32'%3E%3Cpath fill='#25D366' d='M11.863 8.305c-.444-.011-.813.335-1.18.677-.12.11-.235.228-.344.35-.489.552-.798 1.186-.703 1.935.103.807.187 1.63.423 2.402.65 2.13 1.962 3.843 3.605 5.309 1.51 1.346 3.162 2.47 5.151 2.977a9.847 9.847 0 0 0 1.966.268c.984.044 2.378-.942 2.728-1.86a.37.37 0 0 0 .022-.158c-.028-.435-.052-.87-.097-1.303-.009-.088-.083-.212-.158-.242a276.61 276.61 0 0 0-3.316-1.281c-.277-.105-.526-.057-.749.159-.337.325-.707.617-1.029.956-.207.217-.384.257-.617.078-.619-.48-1.26-.933-1.853-1.443-.93-.8-1.7-1.744-2.38-2.763-.19-.284-.199-.483.077-.724.294-.256.517-.592.804-.856.366-.336.37-.69.192-1.12a85.3 85.3 0 0 1-.964-2.46c-.3-.792-.294-.795-1.258-.833a.894.894 0 0 0-.32-.068zm4.016-5.566c5.806-.062 10.95 3.973 12.154 9.89 1.123 5.523-1.825 11.269-6.975 13.536-3.56 1.568-7.1 1.477-10.606-.216-.13-.063-.337-.05-.479.004-1.39.532-2.777 1.08-4.164 1.625-.069.027-.14.049-.266.093.412-1.455.8-2.847 1.205-4.235.064-.216.03-.357-.112-.526-2.056-2.454-3.018-5.292-2.889-8.483.226-5.636 4.415-10.442 9.968-11.475.727-.136 1.45-.205 2.164-.213zm.203-2.086a14.416 14.416 0 0 0-4.595.74c-5.636 1.87-9.435 6.872-9.764 12.803-.189 3.43.773 6.54 2.82 9.307.133.182.178.333.12.563-.576 2.266-1.137 4.535-1.718 6.866.178-.065.31-.111.438-.162 2.147-.838 4.297-1.67 6.44-2.521.324-.128.598-.141.925-.005 1.091.452 2.228.737 3.4.883 3.548.44 6.831-.306 9.797-2.291 5.426-3.631 7.685-10.342 5.562-16.54A14.243 14.243 0 0 0 16.082.654zM16.032 0c.494.004.992.03 1.492.078 6.504.613 12.026 5.686 13.158 12.108.805 4.565-.231 8.687-3.16 12.275-2.333 2.857-5.366 4.599-9.012 5.227a14.618 14.618 0 0 1-7.895-.793.818.818 0 0 0-.649 0c-2.55 1.005-5.105 1.999-7.659 2.996-.08.031-.162.058-.305.108l.783-3.13c.393-1.573.791-3.144 1.172-4.72a.617.617 0 0 0-.089-.442c-1.92-2.71-2.94-5.725-2.8-9.04.26-6.171 3.233-10.635 8.781-13.33C11.81.386 13.89-.017 16.032 0z'/%3E%3C/svg%3E") no-repeat 100% 100%;
        }

        .firefox {
        background: transparent url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32'%3E%3Cpath fill='#e66000' d='M27.579 8.902l.048.09a.54.54 0 0 1-.045-.082zm-7.06-4.054c-.351.003-.712.024-1.081.067 1.2.192 2.284.501 2.729 1.457-.625-.005-1.3-.054-1.58.291 2.275 1.189 5.035 1.886 5.315 5.096-.36-.17-.48-.58-1.005-.582.23 1.595.78 3.799.145 5.388-.35-.422-.365-1.185-.865-1.457.105 2.68-.025 5.119-1.29 6.407-.035-.572.405-1.424 0-1.892-1.15 3.86-8.29 5.12-10.2 1.746 3.016.292 3.73-1.751 6.176-2.038-.125-.937-.915-1.676-2.01-1.748-1.19-.076-2.215 1.096-3.305 1.02-.56-.04-1.18-.554-1.725-1.02-1.77-1.514-.894-2.931 1.58-1.892.325-.797-.145-1.698-.43-2.33.64-.954 2.245-.928 2.3-2.475-1.76-.012-2.745-.81-3.45-1.894.33-1.317 1.165-2.124 2.015-2.912-1.65.172-2.605 1.05-3.734 1.748-1.075-.346-2.275.005-3.16.29-1-.539-1.15-1.941-1.58-3.057-1.1 1.167-1.445 3.102-1.44 5.388-.765 1.018-1.57 1.998-1.575 3.786.42.168.53-.698.715-.292-2.335 8.76 5.49 16.323 13.644 16.018 8.354-.313 13.649-8.231 13.219-17.182-.65-.12.03 1.098-.575 1.019.025-2.797-.825-5.474-2.155-6.407.31.28.204.983.35 1.428l.032.083-.083-.157c-1.265-2.286-3.702-3.923-6.977-3.897zM16.103 0c2.763-.007 5.09.615 6.784 1.421 4.995 2.381 9.719 7.97 9.049 16.162-.73 8.88-8.514 14.467-16.088 14.417C6.794 31.937-.645 24.6.045 14.816.32 10.992 1.724 8.529 2.634 7.1 4.599 3.998 8.959.67 14.123.111a18.887 18.887 0 0 1 1.98-.11z'/%3E%3C/svg%3E") no-repeat 100% 100%;
        }

        .contact {
        background: transparent url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32'%3E%3Cellipse cx='16' cy='16' fill='#4285f4' rx='16' ry='16'/%3E%3Cpath fill='#FFF' d='M13.55 16.95h4.9c2.7 0 4.85 2.05 4.85 4.6 0 .9-.25 1.75-.75 2.45H9.45c-.5-.7-.75-1.55-.75-2.45 0-2.55 2.15-4.6 4.85-4.6zM16.05 8c2.05 0 3.7 1.65 3.7 3.7 0 2.05-1.65 3.7-3.7 3.7-2.05 0-3.7-1.65-3.7-3.7.05-2.05 1.7-3.7 3.7-3.7z'/%3E%3C/svg%3E") no-repeat 100% 100%;
        }

        .chrome {
        background: transparent url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32'%3E%3Cpath fill='#ffffff' d='M16.033 11.049a5.155 5.155 0 1 1 0 10.312 5.156 5.156 0 0 1 0-10.312zM16.124 0c1.281-.003 9.659.318 14.268 9.043h-.016l.01.018c.33.578 3.745 6.94-.485 14.969 0 0-4.215 8.107-14.565 7.968l-.452-.012-.004.007-.004.007.02-.037c.564-.98 5.112-8.884 6.357-11.067l.016-.028.007-.008.04-.069.11-.127a7.085 7.085 0 0 0 1.457-2.967l.01-.046.035-.151c.088-.424.148-.944.128-1.549l-.006-.117v-.004l-.007-.143-.006-.07-.005-.079-.012-.116v-.01l-.001-.008-.016-.158a7.2 7.2 0 0 0-.096-.572l-.018-.081-.013-.064a9.801 9.801 0 0 0-.692-2.016c-.165-.243-.332-.489-.512-.733l-.142-.187 8.728-2.554s-10.538-.01-13.018-.001l.021.005H16.642l-.14-.013a7.034 7.034 0 0 0-1.132-.003l-.167.016h-.047l-.034-.001c-.193.002-1.213.045-2.492.764l-.005.003-.033.016a7.158 7.158 0 0 0-3.25 3.533l-.059.148-6.485-6.404s4.74 8.311 6.165 10.779l.065.113.023.088a7.14 7.14 0 0 0 7.777 5.118l.144-.02L14.854 32h-.027c-.667-.005-7.894-.234-12.744-7.906 0 0-4.925-7.698.37-16.573l.252-.411.001-.002C2.822 6.904 6.58.374 15.958.003c0 0 .057-.003.166-.003z'/%3E%3C/svg%3E") no-repeat 100% 100%;
        }

        .pinterest {
        background: transparent url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 32 32'%3E%3Cellipse cx='16' cy='16' fill='#bd081c' rx='16' ry='16'/%3E%3Cpath fill='#FFF' d='M16.22 6.458c4.807-.009 9.028 1.888 9.663 5.307.787 4.256-2.438 8.866-8.213 8.535-1.565-.09-2.222-.666-3.448-1.22-.675 2.628-1.5 5.147-3.942 6.463-.754-3.972 1.107-6.954 1.971-10.12-1.474-1.842.177-5.547 3.284-4.634 3.824 1.123-3.31 6.845 1.48 7.56 5 .746 7.04-6.441 3.94-8.779-4.48-3.376-13.042-.077-11.989 4.755.256 1.181 1.9 1.54.657 3.17-2.868-.471-3.724-2.15-3.614-4.39.178-3.664 4.435-6.229 8.705-6.583.506-.043 1.01-.064 1.507-.064z'/%3E%3C/svg%3E") no-repeat 100% 100%;
        }

        .svg_icons {
        width: 32px;
        height: 32px;
        display: inline-block;
        }

</style>

```

{% endtab %}
<template>
    <div class="sidebar-menu">
        <div class="logo"> <a href="#" class="sidebar-icon"> <span class="fa fa-bars"></span> </a> <a href="#"> <span id="logo" ></span>
            <!--<img id="logo" src="" alt="Logo"/>-->
        </a> </div>
        <div class="menu">
            <ul id="menu" >
                <li id="menu-home" ><router-link to="/"><i class="fa fa-tachometer"></i><span>Dashboard</span></router-link></li>
                <li><a href="#"><i class="fa fa-cogs"></i><span>Components</span><span class="fa fa-angle-right" style="float: right"></span></a>
                    <ul>
                        <li><a href="grids.html">Grids</a></li>
                        <li><a href="portlet.html">Portlets</a></li>
                    </ul>
                </li>
                <li id="menu-comunicacao" ><a href="#"><i class="fa fa-book nav_icon"></i><span>Element</span><span class="fa fa-angle-right" style="float: right"></span></a>
                    <ul id="menu-comunicacao-sub" >
                        <li id="menu-mensagens" style="width: 120px" ><a href="buttons.html">Buttons</a>
                        </li>
                        <li id="menu-arquivos" ><a href="typography.html">Typography</a></li>
                        <li id="menu-arquivos" ><a href="icons.html">Icons</a></li>
                    </ul>
                </li>
                <li><a href="maps.html"><i class="fa fa-map-marker"></i><span>Maps</span></a></li>
                <li id="menu-academico" ><a href="#"><i class="fa fa-file-text"></i><span>Pages</span><span class="fa fa-angle-right" style="float: right"></span></a>
                    <ul id="menu-academico-sub" >
                        <li id="menu-academico-boletim" ><a href="login.html">Login</a></li>
                        <li id="menu-academico-avaliacoes" ><a href="signup.html">Sign Up</a></li>
                    </ul>
                </li>

                <li><a href="charts.html"><i class="fa fa-bar-chart"></i><span>Charts</span></a></li>
                <li><a href="#"><i class="fa fa-envelope"></i><span>Mailbox</span><span class="fa fa-angle-right" style="float: right"></span></a>
                    <ul id="menu-academico-sub" >
                        <li id="menu-academico-avaliacoes" ><a href="inbox.html">Inbox</a></li>
                        <li id="menu-academico-boletim" ><a href="inbox-details.html">Compose email</a></li>
                    </ul>
                </li>
                <li><a href="#"><i class="fa fa-cog"></i><span>System</span><span class="fa fa-angle-right" style="float: right"></span></a>
                    <ul id="menu-academico-sub" >
                        <li id="menu-academico-avaliacoes" ><a href="404.html">404</a></li>
                        <li id="menu-academico-boletim" ><a href="blank.html">Blank</a></li>
                    </ul>
                </li>
                <li><a href="#"><i class="fa fa-shopping-cart"></i><span>E-Commerce</span><span class="fa fa-angle-right" style="float: right"></span></a>
                    <ul id="menu-academico-sub" >
                        <li id="menu-academico-avaliacoes" ><a href="product.html">Product</a></li>
                        <li id="menu-academico-boletim" ><a href="price.html">Price</a></li>
                    </ul>
                </li>
            </ul>
        </div>
    </div>
</template>

<script>
    export default {
        name: "Sidebar",

        mounted() {

            var toggle = true;

            $(".sidebar-icon").click(function() {
                if (toggle)
                {
                    $(".page-container").addClass("sidebar-collapsed").removeClass("sidebar-collapsed-back");
                    $("#menu span").css({"position":"absolute"});
                }
                else
                {
                    $(".page-container").removeClass("sidebar-collapsed").addClass("sidebar-collapsed-back");
                    setTimeout(function() {
                        $("#menu span").css({"position":"relative"});
                    }, 400);
                }
                toggle = !toggle;
            });




            $("html").niceScroll({styler:"fb",cursorcolor:"#68ae00", cursorwidth: '6', cursorborderradius: '10px', background: '#FFFFFF', spacebarenabled:false, cursorborder: '0',  zindex: '1000'});

            $(".scrollbar1").niceScroll({styler:"fb",cursorcolor:"#68ae00", cursorwidth: '6', cursorborderradius: '0',autohidemode: 'false', background: '#FFFFFF', spacebarenabled:false, cursorborder: '0'});



            $(".scrollbar1").getNiceScroll();
            if ($('body').hasClass('scrollbar1-collapsed')) {
                $(".scrollbar1").getNiceScroll().hide();
            }
        }
    }
</script>

<style scoped>

</style>
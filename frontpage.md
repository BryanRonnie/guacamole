<!DOCTYPE html>
<html lang="en-US" class="no-deferjs">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <link rel="preload" as="style" href="styles.css">
        <link rel="preload" as="style" href="https://www.thegradsplace.com/wp-content/plugins/gdpr-banner/css/gdpr-banner.css">
        <link rel="preload" as="style" href="https://www.thegradsplace.com/wp-includes/css/dist/block-library/style.min.css">
        <link rel="preload" as="style" href="https://www.thegradsplace.com/wp-content/plugins/enlighter/cache/EnlighterJS.custom.css">
        <link rel="preload" as="script" href="https://www.thegradsplace.com/wp-includes/js/jquery/jquery.js">
        <link rel="preload" as="script" href="https://www.thegradsplace.com/wp-includes/js/jquery/jquery-migrate.min.js">
        <link rel="preload" as="script" href="https://www.thegradsplace.com/wp-content/plugins/gdpr-banner/js/gdpr-banner.js">
        <link rel="preload" as="script" href="https://www.thegradsplace.com/wp-content/plugins/google-analytics-dashboard-for-wp/front/js/tracking-analytics-events.js">
        <link rel="preload" as="script" href="https://www.thegradsplace.com/wp-content/themes/zakra/assets/js/navigation.min.js">
        <link rel="preload" as="script" href="https://www.thegradsplace.com/wp-content/themes/zakra/assets/js/skip-link-focus-fix.min.js">
        <link rel="preload" as="script" href="https://www.thegradsplace.com/wp-content/themes/zakra/assets/js/zakra-custom.min.js">
        <link rel="preload" as="script" href="https://ajax.googleapis.com/ajax/libs/mootools/1.6.0/mootools.min.js">
        <link rel="preload" as="script" href="https://www.thegradsplace.com/wp-content/plugins/enlighter/resources/EnlighterJS.min.js">

        <script id="defer-script">


            !function(e, o, t, n, i, r) {
                function c(e, t) {
                    r ? n(e, t || 32) : i.push(e, t)
                }
                function f(e, t, n, i) {
                    return t && o.getElementById(t) || (i = o.createElement(e || 'SCRIPT'),
                    t && (i.id = t),
                    n && (i.onload = n),
                    o.head.appendChild(i)),
                    i || {}
                }
                r = /p/.test(o.readyState),
                e.addEventListener('on' + t in e ? t : 'load', function() {
                    for (r = t; i[0]; )
                        c(i.shift(), i.shift())
                }),
                c._ = f,
                e.defer = c,
                e.deferscript = function(t, n, e, i) {
                    c(function(e) {
                        f(0, n, i).src = t
                    }, e)
                }
            }(this, document, 'pageshow', setTimeout, []),
            function(u, n) {
                var a = 'IntersectionObserver'
                  , d = 'src'
                  , l = 'lazied'
                  , h = 'data-'
                  , p = h + l
                  , y = 'load'
                  , m = 'forEach'
                  , r = 'appendChild'
                  , b = 'getAttribute'
                  , c = n.head
                  , g = Function()
                  , v = u.defer || g
                  , f = v._ || g;
                function I(e, t) {
                    return [].slice.call((t || n).querySelectorAll(e))
                }
                function e(s) {
                    return function(e, t, o, r, c, f) {
                        v(function(n, t) {
                            function i(n) {
                                !1 !== (r || g).call(n, n) && (I('SOURCE', n)[m](i),
                                (f || ['srcset', d, 'style'])[m](function(e, t) {
                                    (t = n[b](h + e)) && (n[e] = t)
                                }),
                                y in n && n[y]()),
                                n.className += ' ' + (o || l)
                            }
                            t = a in u ? (n = new u[a](function(e) {
                                e[m](function(e, t) {
                                    e.isIntersecting && (t = e.target) && (n.unobserve(t),
                                    i(t))
                                })
                            }
                            ,c)).observe.bind(n) : i,
                            I(e || s + '[' + h + d + ']:not([' + p + '])')[m](function(e) {
                                e[b](p) || (e.setAttribute(p, s),
                                t(e))
                            })
                        }, t)
                    }
                }
                function t() {
                    v(function(t, n, i, o) {
                        t = [].concat(I((i = 'script[type=deferjs]') + ':not(' + (o = '[async]') + ')'), I(i + o)),
                        function e() {
                            if (0 != t) {
                                for (o in n = f(),
                                (i = t.shift()).parentNode.removeChild(i),
                                i.removeAttribute('type'),
                                i)
                                    'string' == typeof i[o] && n[o] != i[o] && (n[o] = i[o]);
                                n[d] && !n.hasAttribute('async') ? (n.onload = n.onerror = e,
                                c[r](n)) : (c[r](n),
                                v(e, .1))
                            }
                        }()
                    }, 4)
                }
                t(),
                u.deferstyle = function(t, n, e, i) {
                    v(function(e) {
                        (e = f('LINK', n, i)).rel = 'stylesheet',
                        e.href = t
                    }, e)
                }
                ,
                u.deferimg = e('IMG'),
                u.deferiframe = e('IFRAME'),
                v.all = t
            }(this, document);
            ;"IntersectionObserver"in window || deferscript("https://polyfill.io/v3/polyfill.min.js?features=IntersectionObserver", "polyfill-js", 1);
            !function(e, n, t, i) {
                var o, r = '', a = 'defer.js', u = 'defer-', c = 'deferjs', d = 'jQuery', s = Function(), f = 'data-', l = 'getAttribute', m = 'object' == typeof e.chrome && -1 == e.navigator.userAgent.indexOf('Trident/'), h = ':not([' + f + 'lazied]):not([' + f + 'ignore])', p = '[' + f + 'src]' + h, g = 'addEventListener', b = 'load', y = ['img' + p, 'picture' + h, '[data-style]' + h].join(','), v = ['iframe' + p, 'frame' + p, 'audio' + h, 'video' + h].join(','), j = {
                    c: u + 'lazied',
                    l: u + 'loading',
                    d: u + 'loaded',
                    h: n.getElementsByTagName('html').item(0),
                    t: 10
                }, T = (t.log || s).bind(t), N = e.defer || s, x = e.deferimg || s, z = e.deferiframe || s;
                function A() {
                    m && T('%defer.js ')
                }
                function k(e, n) {
                    return e.split(' ').filter(function(e) {
                        return '' != e && e != n
                    })
                }
                function M(e, n) {
                    var t = k(e.className, n);
                    t.push(n),
                    e.className = t.join(' ')
                }
                function C(e, n) {
                    e.className = k(e.className, n).join(' ')
                }
                function E(e) {
                    var n, t, i = e[l](f + 'src');
                    function o() {
                        n && (clearTimeout(n),
                        n = null),
                        C(e, j.l),
                        M(e, j.d)
                    }
                    M(e, j.l),
                    null !== (t = /(?:youtube(?:-nocookie)?\.com\/(?:[^/\n\s]+\/\S+\/|(?:v|e(?:mbed)?)\/|\S*?[?&]v=)|youtu\.be\/)([a-zA-Z0-9_-]{11})/.exec(i)) && (e.style.background = 'transparent url(https://img.youtube.com/vi/' + t[1] + '/hqdefault.jpg) 50% 50% / cover no-repeat'),
                    e.hasAttribute(f + 'ignore') || i && e.src == i || !i && e[l](f + 'style') ? o() : (e[g](b, o),
                    n = setTimeout(o, 3e3))
                }
                function O() {
                    x(y, j.t, j.c, E, {
                        rootMargin: '150%'
                    }),
                    z(v, j.t, j.c, E, {
                        rootMargin: '200%'
                    })
                }
                j.copyright = A,
                j.debounce = function(t, i, o, r) {
                    return function() {
                        var e = this
                          , n = arguments;
                        o || clearTimeout(r),
                        o && r || (r = setTimeout(function() {
                            r = null,
                            t.apply(e, n)
                        }, i))
                    }
                }
                ,
                j.defermedia = O,
                j.addClass = M,
                (j.removeClass = C)(j.h, 'no-' + c),
                M(j.h, c),
                e.defer_helper = j,
                e[g](b, function() {
                    !o && d in e && 'fn'in e[d] && (o = e[d].fn.ready,
                    e[d].fn.ready = function(e) {
                        return N(function() {
                            o(e)
                        }),
                        this
                    }
                    )
                }),
                O(),
                A()
            }(this, document, console);
        </script>
        <style id="defer-css">
            .no-deferjs .has-noscript {
                display: none!important
            }

            audio,embed,frame,iframe,img,picture,source,video {
                min-width: 1px;
                min-height: 1px;
                visibility: visible
            }

            .defer-lazied {
                transition: opacity .1s linear
            }

            .defer-lazied.defer-loaded {
                background-color: transparent!important
            }

            .defer-lazied.defer-loading:not([data-style]):not([data-ignore]) {
                opacity: .5!important
            }
        </style>
        <title>Data Structures-TheGradsPlace</title>
        <meta name="description" content="A data structure is a model where data is organized, managed and stored in a format that enables efficient access. Read a brief introduction.">
        <meta property="og:locale" content="en_US">
        <meta property="og:type" content="website">
        <meta property="og:title" content="Introduction to Data Structures - Data Structures Handbook">
        <meta property="og:description" content="A data structure is a model where data is organized, managed and stored in a format that enables efficient access. Read a brief introduction.">
        <meta property="og:url" content="https://www.thegradsplace.com/">
        <meta property="og:site_name" content="Data Structures Handbook">
        <meta name="twitter:card" content="summary_large_image">
        <meta name="twitter:description" content="A data structure is a model where data is organized, managed and stored in a format that enables efficient access. Read a brief introduction.">
        <meta name="twitter:title" content="Introduction to Data Structures - Data Structures Handbook">
        <script type="application/ld+json" class="yoast-schema-graph yoast-schema-graph--main">
            {
    
        </script>
        <link rel="dns-prefetch" href="https://ajax.googleapis.com">
        <link rel="dns-prefetch" href="https://fonts.googleapis.com">
        <link rel="dns-prefetch" href="https://s.w.org">
        <link rel="stylesheet" id="gdpr_css-css" href="https://www.thegradsplace.com/wp-content/plugins/gdpr-banner/css/gdpr-banner.css">
        <link rel="stylesheet" id="wp-block-library-css" href="https://www.thegradsplace.com/wp-includes/css/dist/block-library/style.min.css">
        <link rel="stylesheet" id="font-awesome-css" href="https://www.thegradsplace.com/wp-content/themes/zakra/assets/lib/font-awesome/css/font-awesome.min.css">
        <link rel="stylesheet" id="zakra-style-css" href="styles.css">
        <style id="zakra-style-inline-css">

            .tg-site-header {
                border-bottom-width: 0px
            }

            .tg-site-header {
                border-bottom-color: #ff3535
            }

            .main-navigation.tg-primary-menu>div ul li.tg-header-button-wrap a {
                color: #0a0a0a
            }

            .main-navigation.tg-primary-menu>div ul li.tg-header-button-wrap a {
                background-color: rgba(219,219,219,0.75)
            }

            .main-navigation.tg-primary-menu>div ul li.tg-header-button-wrap a:hover {
                background-color: #dd9933
            }

            .main-navigation.tg-primary-menu>div ul li.tg-header-button-wrap a {
                border-radius: 1px
            }

            .tg-primary-menu>div>ul li:not(.tg-header-button-wrap) a {
                color: black
            }

            .tg-primary-menu>div>ul li:not(.tg-header-button-wrap):hover>a {
                color: #dd3333
            }

            .tg-primary-menu>div ul li:active>a,.tg-primary-menu>div ul>li:not(.tg-header-button-wrap).current_page_item>a,.tg-primary-menu>div ul>li:not(.tg-header-button-wrap).current-menu-item>a {
                color: #dd8500
            }

            .tg-primary-menu.tg-primary-menu--style-underline>div ul>li:not(.tg-header-button-wrap).current_page_item>a::before,.tg-primary-menu.tg-primary-menu--style-underline>div ul>li:not(.tg-header-button-wrap).current-menu-item>a::before,.tg-primary-menu.tg-primary-menu--style-left-border>div ul>li:not(.tg-header-button-wrap).current_page_item>a::before,.tg-primary-menu.tg-primary-menu--style-left-border>div ul>li:not(.tg-header-button-wrap).current-menu-item>a::before,.tg-primary-menu.tg-primary-menu--style-right-border>div ul>li:not(.tg-header-button-wrap).current_page_item>a::before,.tg-primary-menu.tg-primary-menu--style-right-border>div ul>li:not(.tg-header-button-wrap).current-menu-item>a::before {
                background-color: #dd8500
            }

            .tg-site-header .main-navigation {
                border-bottom-width: 0px
            }

            @media (min-width: 1200px) {
                .tg-container {
                    max-width:1000px
                }
            }

            #primary {
                width: 75%
            }

            #secondary {
                width: 25%
            }

            .tg-page-header .tg-page-header__title {
                font-size: 50px
            }

            .tg-page-header {
                padding: 14px 0px 15px 0px
            }

            .tg-page-header {
                background-color: #ffa000;
                background-image: ;
                background-repeat: repeat;
                background-position: center center;
                background-size: contain;
                background-attachment: scroll
            }

            .tg-page-header .breadcrumb-trail ul li {
                font-size: 18px
            }

            a:hover,a:focus,.tg-primary-menu>div ul li:hover>a,.tg-primary-menu>div>ul>li.current_page_item>a,.tg-primary-menu>div>ul>li.current-menu-item>a,.entry-content a,.tg-meta-style-two .entry-meta span,.tg-meta-style-two .entry-meta a {
                color: #1e73be
            }

            .tg-primary-menu.tg-primary-menu--style-underline>div>ul>li.current_page_item>a::before,.tg-primary-menu.tg-primary-menu--style-underline>div>ul>li.current-menu-item>a::before,.tg-primary-menu.tg-primary-menu--style-left-border>div>ul>li.current_page_item>a::before,.tg-primary-menu.tg-primary-menu--style-left-border>div>ul>li.current-menu-item>a::before,.tg-primary-menu.tg-primary-menu--style-right-border>div>ul>li.current_page_item>a::before,.tg-primary-menu.tg-primary-menu--style-right-border>div>ul>li.current-menu-item>a::before,.tg-scroll-to-top.tg-scroll-to-top--show:hover,button,input[type="button"],input[type="reset"],input[type="submit"] {
                background-color: #1e73be
            }

            .tg-site-footer .tg-site-footer-bar {
                color: #002a5e
            }

            .tg-site-footer .tg-site-footer-bar .tg-container {
                border-top-width: 0px
            }

            .tg-site-footer .tg-site-footer-bar {
                background-color: #ffa000;
                background-image: ;
                background-repeat: repeat;
                background-position: center center;
                background-size: contain;
                background-attachment: scroll
            }

            .tg-scroll-to-top.tg-scroll-to-top--show:hover {
                background-color: #ff2d2d
            }

            body {
                font-family: Cairo;
                font-size: 19px;
                line-height: 1.6;
                font-weight: 400;
                font-style: normal
            }


            h1,h2,h3,h4,h5,h6 {
                font-family: Cairo;
                line-height: 1.3;
                font-weight: 400;
                font-style: normal
            }

            .site-branding .site-title {
                font-family: Gugi;
                font-size: 3.313rem;
                line-height: 1.0;
                font-weight: 400;
                font-style: normal
            }

            .site-branding .site-description {
                font-family: Cairo;
                font-size: 1.2em;
                line-height: 1.8;
                font-weight: 400;
                font-style: normal
            }

            .tg-primary-menu>div ul li a {
                font-family: -apple-system,blinkmacsystemfont,segoe ui,roboto,oxygen-sans,ubuntu,cantarell,helvetica neue,helvetica,arial,sans-serif;
                font-size: 1.2rem;
                line-height: 1.8;
                font-weight: 400;
                font-style: normal
            }

            .tg-page-header .tg-page-header__title,.tg-page-content__title {
                font-family: Cairo;
                line-height: 1.1;
                font-weight: 400;
                font-style: normal
            }

            .widget .widget-title {
                font-family: -apple-system,blinkmacsystemfont,segoe ui,roboto,oxygen-sans,ubuntu,cantarell,helvetica neue,helvetica,arial,sans-serif;
                font-size: 1.2rem;
                line-height: 1.3;
                font-weight: 400;
                font-style: normal
            }

            .widget {
                font-family: Cairo;
                font-size: 15px;
                line-height: 1.8;
                font-weight: 400;
                font-style: normal
            }
        </style>
        <link href="https://fonts.googleapis.com/css2?family=Cairo&family=Gugi&display=swap" rel="stylesheet">
        
        <style>
            .recentcomments a {
                display: inline!important;
                padding: 0!important;
                margin: 0!important;
            }
        </style>
        <style id="custom-background-css">
            body.custom-background {
                background-color: #c7c7c7
            }
        </style>

        <style id="wp-custom-css">
            .tg-primary-menu>div>ul li a {
                font-size: 21px
            }

            .tg-primary-menu>div>ul li {
                margin: 2px 16px
            }

            .widget ul li {
                padding: 0.2rem 0
            }

            .site-content {
                margin-top: 40px;
                margin-bottom: 80px
            }

            .site-branding {
                margin-bottom: 20px
            }

            .tg-primary-menu>div>ul {
                justify-content: center
            }

            .EnlighterJS {
                width: auto;
                overflow-x: auto;
                word-wrap: normal
            }

            ol.EnlighterJS,ul.EnlighterJS {
                display: grid
            }

            .EnlighterJS li {
                white-space: pre
            }
        </style>
    </head>
    <body class="home page-template-default page page-id-38 custom-background tg-site-layout--right tg-container--wide has-page-header has-breadcrumbs">
        <div id="page" class="site tg-site">
            <a class="skip-link screen-reader-text" href="#content">Skip to content</a>
            <header id="masthead" class="site-header tg-site-header tg-site-header--center">
                <div class="tg-site-header-bottom" style="background-color: black">
                    <div class="tg-header-container tg-container tg-container--flex tg-container--flex-center tg-container--flex-space-between">
                        <div class="site-branding">
                            <div class="site-info-wrap">
                                <p class="site-title">
                                    <a href="https://www.thegradsplace.com/" rel="home" style="background: -webkit-linear-gradient(black, white,grey,white,black);-webkit-background-clip: text;-webkit-text-fill-color: transparent;">TheGrad'sPlace</a>
                                </p>
                                <p class="site-description">Keep it simple.</p>
                            </div>
                        </div>
                        <nav id="site-navigation" class="main-navigation tg-primary-menu tg-primary-menu--style-underline">
                            <div class="menu">
                                <ul id="primary-menu" class="menu-primary">
                                    <li id="menu-item-327" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-327" style="background-color: grey; border-radius: 15px ;padding: 0px 5px 0px 5px" >
                                        <a href="https://www.thegradsplace.com\arrays/">Data Structures</a>
                                    </li>
                                    <li id="menu-item-26" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-26" style="background-color: grey ; border-radius: 15px; padding: 0px 5px 0px 5px">
                                        <a href="https://www.thegradsplace.com/linked-lists/">Algorithms</a>
                                    </li>
                                </ul>
                            </div>
                        </nav>
                        <nav id="header-action" class="tg-header-action">
                            <ul class="tg-header-action-list">
                                <li class="tg-header-action__item tg-mobile-toggle">
                                    <i class="tg-icon tg-icon-bars"></i>
                                </li>
                            </ul>
                        </nav>
                    </div>
                </div>
            </header>
            <main id="main" class="site-main">
                <div id="content" class="site-content">
                    <div class="tg-container tg-container--flex tg-container--flex-space-between">
                        <div id="primary" class="content-area">
                            <article id="post-38" class="post-38 page type-page status-publish hentry zakra-article-page">
                                <header class="entry-header">
                                    <h1 class="entry-title tg-page-content__title">What is a Data Structure?</h1>
                                </header>
                                <div class="entry-content">
                                    <p>Data structure  is  a  particular  way  of  storing  and organizing data in a computer so that it can be used efficiently. A data structure is a special format for organizing and storing data.</p>
                                    <p>A good data structure must have the following properties:</p>
									<ol>
									    <li>It must be able to process the data efficiently when necessary.</li>
									    <li>It must be able to represent the inherent relationship of the data in the real world.</li>
									</ol>
									                                    

                                    <h2 id="why-study-data-structures">Why learn Data Structures?</h2>
                                    <p>It is necessary to have a good knowledge of data structures and understand where to use the best one. The study includes the description, implementation and quantitative performance analysis of the data structure.A program built using improper data structures will be therefore inefficient or unnecessarily complex. </p>

 									<h2 id="real-world-example">One simple example!</h2>

                                    
                                    	<img src="https://th.bing.com/th/id/OIP.SSeVpoxHmQ85GeY2n9Zt_wHaLW?w=201&h=309&c=7&o=5&dpr=1.1&pid=1.7" style="float:left; width:130px; height:180px; margin:5px;" />
                                    		<p>You never eat icecream from the bottom, right? Why? Because if you do, it'll take much time. Moreover, you're only complicating the process.</p><p>Why not add scoops from the top, eat from the top? Simple right?</p>This is a perfect example of <strong>stack</strong>.
                                    
                                     
                              
                                    <h2 id="types-of-data-type">Types of Data Types</h2>
                                    <h3 id="primitive-data-types">Primitive Data Types</h3>
                                    <p>A primitive data type is one that is inbuilt into the programming language for defining the most basic types of data. These may be different for the various programming languages available. </p>
                                    <blockquote><strong>Example</strong> : int, float ,double ,boolean</blockquote>
                                    <h3 id="user-defined-data-type">User-Defined Data Type</h3>
                                    <p>User-defined data type, as the name suggests is the one that the user defines as per the requirements of the data to be stored. Most programming languages provide support for creating user-defined data types. 
                                    <blockquote><strong>Example</strong> : struct, enum, union</blockquote>
                                    <h3 id="abstract-data-type-adt">Abstract Data Type (ADT)</h3>
                                    <p>Abstract Data Types are defined by its behaviour from the point of view of the user of the data. It defines it in terms of possible values, operations on data, and the behaviour of these operations.</p>
                                    <p>The definition of ADT only mentions what operations are to be performed but not how these operations will be implemented. That is, it does not specify how the data is being handled under the hood. This concept is known as abstraction.</p>
                                    
                                    <blockquote><strong>Example</strong> : The user of the stack data structure only knows about the push and pop operations in a stack. They don't care what happens inside. They just want the job done in their format.</blockquote>
                                    <h2 id="common-operations-in-a-data-structure">Common Operations in a Data Structure</h2>
                                    <p>A data structure is only useful when you can perform operations on it, right? These are the basic operations that should be able to be performed on every data structure.</p>
                                   
                                    <h4 id="search">Search</h4>
                                    <p>This operation handles finding the location of a given element of a given structure.</p>
                                    <h4 id="insertion">Insert</h4>
                                    <p>This operation specifies how new elements are to be added to the structure.</p>
                                    <h4 id="deletion">Delete</h4>
                                    <p>This operation specifies how existing elements can be removed from the structure.</p>
                                    <h2 id="classification-of-data-structure">Classification of data structure</h2>
                                    <h4 id="access">Display</h4>
                                    <p>This operation handles displaying the elements currently stored in the data structure.</p>

                                    <p>A data structure can be broadly classified into 2 types:</p>
                                    <h3 id="linear-data-structures">Linear Data Structures</h3>
                                    <p>A linear data structure’s elements form a sequence. Every element in the structure has some element before and after it. Examples of linear structures are:</p>
                                    <h4>Arrays</h4>
                                    <p>
                                        An array holds a fixed number of similar elements that are stored under <strong>one name</strong>
                                        . These elements are stored in <strong>continuous memory locations</strong>
                                        . The elements of an array can be accessed using one identifier.
                                    </p>
                                    <h4>Linked Lists</h4>
                                    <p>
                                        A linked list is a linear data structure where each element is a separate object, known as a <strong>node</strong>
                                        . Each node contains some data and points to the next node in the structure, forming a <strong>sequence</strong>
                                        . 
                                    </p>
                                    <h4>Stacks</h4>
                                    <p>
                                        Stacks are a type of linear data structures that store data in an order known as the <strong>Last In First Out (LIFO)</strong>
                                        order. This property is helpful in certain programming cases where the data needs to be ordered. 
                                    </p>
                                    <h4>Queues</h4>
                                    <p>
                                        Queues are a type of linear data structures that store data in an order known as the <strong>First In First Out (FIFO)</strong>
                                        order. This property is helpful in certain programming cases where the data needs to be ordered. 
                                    </p>
                                    <h3 id="non-linear-data-structures">Non-Linear Data Structures</h3>
                                    <p>A non-linear data structure’s elements do not form a sequence. Every element may not have a unique element before and after it.</p>
                                    <h4>Trees</h4>
                                    <p>
                                        A tree is a data structure that simulates a hierarchical tree, with a root value and the children as the subtrees, represented by a set of linked nodes. 
                                    </p>
                                    <h4>Heaps</h4>
                                    <p>
                                        A heap is a specialized tree-based data structure that satisfies the <strong>heap</strong>
                                        property. 
                                    </p>
                                    <h4>Graphs</h4>
                                    <p>
                                        A graph data structure is used to represent relations between pairs of objects. It consists of <strong>nodes</strong>
                                        (known as vertices) that are connected through <strong>links</strong>
                                        (known as edges). The relationship between the nodes can be used to model the relation between the objects in the graph. 
                                    </p>
                                    <h4 id="hash-tables">Hash Tables</h4>
                                    <p>
                                        A Hash Table is a data structure where data is stored in an associative manner. The data is mapped to array positions by a hash function that generates a unique value from each key. The value stored in a hash table can then be searched in <strong>O(1)</strong>
                                        time using the same hash function which generates an address from the key.
                                        
                                    </p>
                                </div>
                            </article>
                        </div>
                        <aside id="secondary" class="widget-area ">

                            <section id="nav_menu-10" class="widget widget_nav_menu">
                                <h2 class="widget-title" style="background-color: #dac0ff ; text-align: center; border-radius: 10px">Arrays</h2>
                                <div class="menu-arrays-container">
                                    <ul id="menu-arrays" class="menu">
                                        <li id="menu-item-328" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-328">
                                            <a href="https://www.thegradsplace.com\arrays\">Arrays</a>
                                        </li>
                                        <li id="menu-item-167" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-167">
                                            <a href="https://www.thegradsplace.com/searching-in-arrays/">Searching in Arrays</a>
                                        </li>
                                        <li id="menu-item-166" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-166">
                                            <a href="https://www.thegradsplace.com/sorting-in-arrays/">Sorting in Arrays</a>
                                        </li>
                                        <li id="menu-item-168" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-168">
                                            <a href="https://www.thegradsplace.com/sparse-matrices/">Sparse Matrices</a>
                                        </li>
                                    </ul>
                                </div>
                            </section>
                            <section id="nav_menu-5" class="widget widget_nav_menu">
                                <h2 class="widget-title" style="background-color: #dac0ff ; text-align: center; border-radius: 10px">Linked Lists</h2>
                                <div class="menu-linked-lists-container">
                                    <ul id="menu-linked-lists" class="menu">
                                        <li id="menu-item-121" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-121">
                                            <a href="https://www.thegradsplace.com/linked-lists/">Linked Lists</a>
                                        </li>
                                        <li id="menu-item-119" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-119">
                                            <a href="https://www.thegradsplace.com/doubly-linked-list/">Doubly Linked List</a>
                                        </li>
                                        <li id="menu-item-120" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-120">
                                            <a href="https://www.thegradsplace.com/circular-linked-lists/">Circular Linked Lists</a>
                                        </li>
                                    </ul>
                                </div>
                            </section>
                            <section id="nav_menu-6" class="widget widget_nav_menu">
                                <h2 class="widget-title" style="background-color: #dac0ff ; text-align: center; border-radius: 10px">Stacks</h2>
                                <div class="menu-stacks-container">
                                    <ul id="menu-stacks" class="menu">
                                        <li id="menu-item-122" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-122">
                                            <a href="https://www.thegradsplace.com/stacks/">Stacks</a>
                                        </li>
                                        <li id="menu-item-123" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-123">
                                            <a href="https://www.thegradsplace.com/stacks-using-linked-lists/">Stacks Using Linked Lists</a>
                                        </li>
                                        <li id="menu-item-124" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-124">
                                            <a href="https://www.thegradsplace.com/expression-parsing/">Expression Parsing</a>
                                        </li>
                                    </ul>
                                </div>
                            </section>
                            <section id="nav_menu-7" class="widget widget_nav_menu">
                                <h2 class="widget-title" style="background-color: #dac0ff ; text-align: center; border-radius: 10px">Queues</h2>
                                <div class="menu-queues-container">
                                    <ul id="menu-queues" class="menu">
                                        <li id="menu-item-127" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-127">
                                            <a href="https://www.thegradsplace.com/queues/">Queues</a>
                                        </li>
                                        <li id="menu-item-126" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-126">
                                            <a href="https://www.thegradsplace.com/queues-using-linked-list/">Queues Using Linked List</a>
                                        </li>
                                        <li id="menu-item-125" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-125">
                                            <a href="https://www.thegradsplace.com/double-ended-queue-deque/">Double Ended Queue (Deque)</a>
                                        </li>
                                    </ul>
                                </div>
                            </section>
                            <section id="nav_menu-8" class="widget widget_nav_menu">
                                <h2 class="widget-title" style="background-color: #dac0ff ; text-align: center; border-radius: 10px">Trees</h2>
                                <div class="menu-trees-container">
                                    <ul id="menu-trees" class="menu">
                                        <li id="menu-item-133" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-133">
                                            <a href="https://www.thegradsplace.com/trees/">Trees</a>
                                        </li>
                                        <li id="menu-item-132" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-132">
                                            <a href="https://www.thegradsplace.com/tree-traversals/">Tree Traversals</a>
                                        </li>
                                        <li id="menu-item-131" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-131">
                                            <a href="https://www.thegradsplace.com/binary-trees/">Binary Trees</a>
                                        </li>
                                        <li id="menu-item-130" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-130">
                                            <a href="https://www.thegradsplace.com/binary-search-trees/">Binary Search Trees</a>
                                        </li>
                                        <li id="menu-item-129" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-129">
                                            <a href="https://www.thegradsplace.com/multiway-trees/">Multiway Trees</a>
                                        </li>
                                        <li id="menu-item-128" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-128">
                                            <a href="https://www.thegradsplace.com/avl-trees/">AVL Trees</a>
                                        </li>
                                    </ul>
                                </div>
                            </section>
                            <section id="nav_menu-12" class="widget widget_nav_menu">
                                <h2 class="widget-title" style="background-color: #dac0ff ; text-align: center; border-radius: 10px">Heaps</h2>
                                <div class="menu-heaps-container">
                                    <ul id="menu-heaps" class="menu">
                                        <li id="menu-item-436" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-436">
                                            <a href="https://www.thegradsplace.com/heaps/">Heaps</a>
                                        </li>
                                    </ul>
                                </div>
                            </section>
                            <section id="nav_menu-9" class="widget widget_nav_menu">
                                <h2 class="widget-title" style="background-color: #dac0ff ; text-align: center; border-radius: 10px">Graphs</h2>
                                <div class="menu-graphs-container">
                                    <ul id="menu-graphs" class="menu">
                                        <li id="menu-item-136" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-136">
                                            <a href="https://www.thegradsplace.com/graphs/">Graphs</a>
                                        </li>
                                        <li id="menu-item-135" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-135">
                                            <a href="https://www.thegradsplace.com/breadth-first-search/">Breadth First Search</a>
                                        </li>
                                        <li id="menu-item-134" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-134">
                                            <a href="https://www.thegradsplace.com/depth-first-search/">Depth First Search</a>
                                        </li>
                                    </ul>
                                </div>
                            </section>
                            <section id="nav_menu-13" class="widget widget_nav_menu">
                                <h2 class="widget-title" style="background-color: #dac0ff ; text-align: center; border-radius: 10px">Hash Tables</h2>
                                <div class="menu-hash-tables-container">
                                    <ul id="menu-hash-tables" class="menu">
                                        <li id="menu-item-437" class="menu-item menu-item-type-post_type menu-item-object-page menu-item-437">
                                            <a href="https://www.thegradsplace.com/hash-tables/">Hash Tables</a>
                                        </li>
                                    </ul>
                                </div>
                            </section>
                        </aside>
                    </div>
                </div>
            </main>
            <footer id="colophon" class="site-footer tg-site-footer" >
                <div class="tg-site-footer-bar tg-site-footer-bar--center" style="background-color : black">
                    <div class="tg-container tg-container--flex tg-container--flex-top" >
                        <div class="tg-site-footer-section-1">
                            <p>
                                Copyright © 2020   |  <strong>     TheGradsPlace    |  </strong>
                                 
                                <strong>
                                    <a href="https://www.thegradsplace.com/privacy-policy/" data-wplink-url-error="true">View Privacy Policy</a>
                                </strong>
                               
                            </p>
                        </div>
                        <div class="tg-site-footer-section-2"></div>
                    </div>
                </div>
            </footer>
        </div>
        <nav id="mobile-navigation" class="tg-mobile-navigation">
            <div class="menu-all-data-structures-container">
                <ul id="primary-menu" class="menu">
                    <li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-327">
                        <a href="https://www.thegradsplace.com\arrays/">Arrays</a>
                    </li>
                    <li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-26">
                        <a href="https://www.thegradsplace.com/linked-lists/">Linked Lists</a>
                    </li>
                    <li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-28">
                        <a href="https://www.thegradsplace.com/stacks/">Stacks</a>
                    </li>
                    <li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-27">
                        <a href="https://www.thegradsplace.com/queues/">Queues</a>
                    </li>
                    <li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-113">
                        <a href="https://www.thegradsplace.com/trees/">Trees</a>
                    </li>
                    <li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-114">
                        <a href="https://www.thegradsplace.com/heaps/">Heaps</a>
                    </li>
                    <li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-115">
                        <a href="https://www.thegradsplace.com/graphs/">Graphs</a>
                    </li>
                    <li class="menu-item menu-item-type-post_type menu-item-object-page menu-item-25">
                        <a href="https://www.thegradsplace.com/hash-tables/">Hash Tables</a>
                    </li>
                </ul>
            </div>
        </nav>
        <a href="" id="tg-scroll-to-top" class="tg-scroll-to-top">
            <i class="tg-icon tg-icon-arrow-up">
                <span class="screen-reader-text">Scroll to top</span>
            </i>
        </a>

        <div class="tg-overlay-wrapper"></div>
        <div id="gdpr_banner">
            <p>
                By using this website you agree to accept our <a href="https://www.thegradsplace.com/privacy-policy/">Privacy Policy</a>
                and <a href="https://www.thegradsplace.com/privacy-policy/">Terms and Conditions</a>
                <button id="gdpr_accept">Accept</button>
            </p>
        </div>
        <script src="https://www.thegradsplace.com/wp-includes/js/jquery/jquery.js"></script>
        <script src="https://www.thegradsplace.com/wp-includes/js/jquery/jquery-migrate.min.js"></script>
        <script src="https://www.thegradsplace.com/wp-content/plugins/gdpr-banner/js/gdpr-banner.js"></script>
        <script>
            var gadwpUAEventsData = {
                "options": {
                    "event_tracking": "1",
                    "event_downloads": "zip|mp3*|mpe*g|pdf|docx*|pptx*|xlsx*|rar*",
                    "event_bouncerate": 0,
                    "aff_tracking": 1,
                    "event_affiliates": "\/out\/",
                    "hash_tracking": "1",
                    "root_domain": "",
                    "event_timeout": 100,
                    "event_precision": 0,
                    "event_formsubmit": 0,
                    "ga_pagescrolldepth_tracking": 0,
                    "ga_with_gtag": 0
                }
            };
        </script>
        <script src="https://www.thegradsplace.com/wp-content/plugins/google-analytics-dashboard-for-wp/front/js/tracking-analytics-events.js"></script>
        <script>
            (function(i, s, o, g, r, a, m) {
                i['GoogleAnalyticsObject'] = r;
                i[r] = i[r] || function() {
                    (i[r].q = i[r].q || []).push(arguments)
                }
                ,
                i[r].l = 1 * new Date();
                a = s.createElement(o),
                m = s.getElementsByTagName(o)[0];
                a.async = 1;
                a.src = g;
                m.parentNode.insertBefore(a, m)
            }
            )(window, document, 'script', 'https://www.google-analytics.com/analytics.js', 'ga');
            ga('create', 'UA-147218841-1', 'auto');
            ga('send', 'pageview');
        </script>
        <script>
            jQuery(function() {
                var gaProperty = '';
                var disableStr = 'ga-disable-' + gaProperty;
                if (document.cookie.indexOf(disableStr + '=true') > -1) {
                    window[disableStr] = true;
                    jQuery('#analytics_opt_out_link').text("You have opted out of Google Analytics tracking");
                }
            });
            function analytics_opt_out() {
                var gaProperty = '';
                var disableStr = 'ga-disable-' + gaProperty;
                document.cookie = disableStr + '=true; expires=Thu, 31 Dec 2099 23:59:59 UTC; path=/';
                window[disableStr] = true;
                jQuery('#analytics_opt_out_link').text("You have opted out of Google Analytics tracking");
            }
        </script>

        <script src="https://ajax.googleapis.com/ajax/libs/mootools/1.6.0/mootools.min.js"></script>
        <script src="https://www.thegradsplace.com/wp-content/plugins/enlighter/resources/EnlighterJS.min.js"></script>
        <script>
            EnlighterJS_Config = {
                "selector": {
                    "block": "pre.EnlighterJSRAW",
                    "inline": "code.EnlighterJSRAW"
                },
                "language": "c",
                "theme": "wpcustom",
                "indent": 2,
                "hover": "hoverEnabled",
                "showLinenumbers": true,
                "rawButton": true,
                "infoButton": false,
                "windowButton": true,
                "rawcodeDoubleclick": true,
                "grouping": true,
                "cryptex": {
                    "enabled": false,
                    "email": "mail@example.tld"
                }
            };
            !function() {
                var a = function(a) {
                    var b = "Enlighter Error: ";
                    console.error ? console.error(b + a) : console.log && console.log(b + a)
                };
                return window.addEvent ? "undefined" == typeof EnlighterJS ? void a("Javascript Resources not loaded yet!") : "undefined" == typeof EnlighterJS_Config ? void a("Configuration not loaded yet!") : void window.addEvent("domready", function() {
                    EnlighterJS.Util.Init(EnlighterJS_Config.selector.block, EnlighterJS_Config.selector.inline, EnlighterJS_Config)
                }) : void a("MooTools Framework not loaded yet!")
            }();
            ;</script>
    </body>
</html>

# JQuery-concepts
All Jquery concepts

# Starts here...

$(document).ready(function () {


    // The below two sentences are same so we can say that $ and jQuery are same

    // console.log($);
    // console.log(jQuery);

    // Syntax of jQuery
    // $('selector').action();

    // There are three types of selections are in jQuery
    // 1.Element Selection
    // 2.ID Selection
    // 3.Class Selection

    // 1.Element
    //click handled at p.......
    $('p').click(function(){
        console.log('This is Awanish.....')
        $('p').hide();
    });

    //If we click any paragraph then all the paragraph gets hide so we will use different syntax for handling each and every para separately...
    $('p').click(function () {
        console.log('This is Awanish.....')
        $(this).hide();
    });

    // $('#id').action()
    // $('.class').action

    // 2.ID Selection

    $('#header').click(function(){
        console.log('You clicked on p', this);
    });

    // 3. Class Selection

    $('.aks').click(function () {

        console.log('This is awanish....')

    });

    $('p').dblclick(function () {
        console.log('you double clicked on p', this);
        //  $('#id').hide();
        //  $('.class').hide();
    });

    $('p').hover(function () {
        console.log('you hoverd on: ', this);
        //  $('#id').hide();
        //  $('.class').hide();
    },
    function (){

        console.log('Thanks for coming')
    });


    // other selectors
    // $('*').click() // clicks on all the elements
    // $('p.odd').click() // clicks on all the elements having class name odd.
    // $('p:first').click() // clicks on all the elements having id as first.

    // Events in jQuery
    // Mouse events = click, dblclick, mouseenter, mouseleave
    // KeyboardEvent = keypress, keydown, MediaKeyStatusMap
    // form events = submit, change, focus, blur
    // document/window events = load, resize, scroll, unload

    // demoing the on method
    $('p').on(
        {
            click: function () {
                console.log('Thanks for clicking', this);
            },
            mouseleave: function () {
                console.log("mouseleave");

            }



        })

    $('#wiki').hide(1000, function () {
        console.log("hidden");
    })   
    $('#wiki').show(1000, function () {
        console.log("show");
    })  
    $('#but').click(function () {
        $('#wiki').fadeOut(5000);
    })

    //fadeIn()
    // fadeOut()
    // fadeToggle()
    // fadeTo()

    // Slide methods - speed and callback parameters are optional
    $('#wiki').slideUp(1000, function(){
        console.log('done');
    })
    $('#wiki').slideDown(1000)
    $('#wiki').slideToggle(1000)

    // Animate function in jQuery
    $('#wiki').animate({
        opacity:0.3,
        height: '150px',
        width:'350px'

    }, "fast")
    $('#wiki').animate({ opacity: 0.3 }, 4000);
    $('#wiki').animate({ opacity: 0.9 }, 1000);
    $('#wiki').animate({ width: '350px' }, 12000);

    $('#ta').val('setting it to harry');
    $('#ta').html('setting it to harry');
    $('#ta').html('setting it to harry3');
    $('#inp').html('setting it to harry3');
    $('#inp').val('setting it to harry3');
    $('#inp').empty()
    $('#wiki').empty()
    $('#wiki').text('you are good')
    $('#wiki').remove()

        $('#wiki').addClass('myclass')
    $('#wiki').addClass('myclass2')
    $('#wiki').removeClass('myclass2')
    $('#wiki').css('background-color', 'red')
    $('#wiki').css('background-color')

    // AJAX Using jQuery
    $.get('https://code.jquery.com/jquery-3.3.1.js', function (data, status) { alert(data); })

    $.get('https://code.jquery.com/jquery-3.3.1.js', function (data, status) { alert(status); })

    $.post('https://code.jquery.com/jquery-3.3.1.js',
        { name: 'harry', channel: 'code with harry' },
        function (data, status) { alert(status) });




});

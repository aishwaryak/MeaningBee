var socket = io.connect("/echo"),
    $log = $("#log"),
    $input = $("#input-echo");

socket.on('msg', function (msg) {
    $log.append($("<p>" + msg + "</p>"));
});

$("#form-echo").on("submit", function(event){
    event.preventDefault();
    var msg = $input.val();
    $input.val("");
    socket.emit("msg", msg);
});

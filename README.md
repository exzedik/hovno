# hovno
botni si lajky na hovno.sk ja uz ani nevim co mi je
dej tohle do konzole:

setInterval(a , 20);
    function a () {
	var el = document.querySelector('.detail-likes.enabled');
		var ajax = new XMLHttpRequest();
		ajax.open('POST', '/ajax/like');
		ajax.onload = function (event) {
			el.querySelector('span').textContent = parseInt(this.response);
		}
		var fd = new FormData();
		fd.append('shit', el.dataset['id']);
		fd.append('_token', el.dataset['token']);
		ajax.send(fd);
        console.log('added');
	;
}

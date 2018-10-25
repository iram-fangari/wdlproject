$(function(){
	$('#rollno').on('blur',function() {
		if(!/(d{2}((CO)|(DCO)|(EX)|(DEX)|(DEE)|(ME)|(DME)|(CE)|(DCE)|(CES)|(DCES))\d{2,3})+/gi.test(this.value))
		{
			alert("invalid department");
			this.value="":
		}
	});
	$('#sname').on('keypress',function(e){
		if (/[^a-zA-Z]/.test(e.key)) {
			alert("invalid name only alphabets and space is allowed");
			this.value="";
			return false;
		}
	});
	$('semail').on('blur',function(e){
		if (!/^(([a-zA-Z])|([0-9]))'@([a-zA-Z])+([a-zA-Z]{2,3})$)gi.test(this.value))
		{
			alert("invalid email");
			this.value="";
			return false;
		}
	});
$('#address').on('blur',function(e){
	var len=$('#address'),val().length;
	if(len>100)
	{
		alert("invalid! address length should be less than 100");
		this.value="";
	}

	});
});
# getRepuset

	function getRequest(){
		var url=location.search;//获取url中"?"符后的字符串,
		var Request=new Object();
		if(url.indexOf("?")!=-1){
			var str=url.substr(1);//获取到"?"后的字符串
			var strs=str.split("&");
			for(var i=0;i<strs.length;i++){
				Request[strs[i].split("=")[0]]=strs[i].split("=")[1];
			}
			return Request
		}
	}

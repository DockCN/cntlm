# cntlm
cntlm running in ubuntu

生成认证信息：
	docker run -it --rm --dns=8.8.8.8 -v ${PWD}/cntlm.conf:/etc/cntlm.conf custa/cntlm -c /etc/cntlm.conf -M https://www.google.com

运行：
	docker run -d --restart=always --name cntlm --dns=8.8.8.8 -v ${PWD}/cntlm.conf:/etc/cntlm.conf:ro -p 8080:8080 custa/cntlm

---
layout: post
---

When Developing Pyverge i was looking for a way to  generate public addresses so i found a interest python libary called
pyqrcode. Here is a little code snippit showing how to generate qrcodes in the terminal on Ubuntu 18-03.





{% highlight python %}

  import pyqrcode
  verge_address = "DQkwDpRYUyNNnoEZDf5Cb3QVazh4FuPRs9"
  
  def get_Balance():
		url = "https://verge-blockchain.info/ext/getbalance/%s"%verge_address
		request_To_verge = requests.get(url,verify = False)
		return request_To_verge.text
    
  
  def get_Qrcode(qr_Size=None):
		try:
			check = float(get_Balance())
		except Exception as err:
			raise QrcodeGenerationError("cant generate qr code")
		if(qr_Size!=None):
			wallet=pyqrcode.create(verge_address,size=qr_Size)
			wallet_To_terminal = wallet.terminal()
			print(wallet_To_terminal)
		else:
			wallet=pyqrcode.create(verge_address)
			wallet_To_terminal = wallet.terminal()
      print(wallet_To_terminal)#Prints qrcode to terminal
  
{% endhighlight %}

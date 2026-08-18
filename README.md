# upi-qr-code-generator
The UPI QR Code Generator 
<br>
Author - Vipul Choudhary

import qrcode

upi_id = input("Enter your UPI ID:")

googlepay_url=f"upi://pay?pa={upi_id}&pn=Recipient%20Name&mc=1234"
phonepay_url=f"upi://pay?pa={upi_id}&pn=Recipient%20Name&mc=1234"
paytm_url=f"upi://pay?pa={upi_id}&pn=Recipient%20Name&mc=1234"

googlepay_qr=qrcode.make(googlepay_url)
phonepay_qr=qrcode.make(phonepay_url)
paytm_qr=qrcode.make(paytm_url)

googlepay_qr.save("google_pay.png")
phonepay_qr.save("phone_pay.png")
paytm_qr.save("paytm.png")

googlepay_qr.show()
phonepay_qr.show()
paytm_qr.show()


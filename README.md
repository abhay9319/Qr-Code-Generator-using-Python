# Qr-Code-Generator-using-Python
Import necessary modules:
import qrcode
from PIL import Image
Create a QRCode instance with specific parameters:

qr = qrcode.QRCode(
    version=1,
    error_correction=qrcode.constants.ERROR_CORRECT_H,
    box_size=20,
    border=4
)
Add the data (URL in this case) to the QRCode instance:

qr.add_data("https://www.youtube.com/")
Make the QRCode fit the data:

qr.make(fit=True)
Generate the QR code image with specified fill and background colors:

img = qr.make_image(fill_color="red", back_color="white")
Save the generated QR code image as "youtubeadv.png":

img.save("youtubeadv.png")
Make sure you have the required libraries installed before running the script. You can install them using the following commands:

pip install qrcode[pil]

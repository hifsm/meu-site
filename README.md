pip install pillow
from PIL import Image, ImageDraw, ImageFont

largura, altura = 400, 100  # Defina o tamanho da imagem
imagem = Image.new('RGB', (largura, altura), color=(255, 255, 255))

desenhista = ImageDraw.Draw(imagem)

try:
    fonte = ImageFont.truetype("arial.ttf", 30)  # Você pode ajustar o tamanho da fonte aqui
except IOError:
    fonte = ImageFont.load_default()  # Se a fonte não for encontrada, usa uma padrão

texto = "FLAG{CR1pt0grafia}"

largura_texto, altura_texto = desenhista.textsize(texto, font=fonte)
posicao = ((largura - largura_texto) // 2, (altura - altura_texto) // 2)

desenhista.text(posicao, texto, fill=(0, 0, 0), font=fonte)  # Cor do texto: preto

imagem.save('flag_imagem.png')

imagem.show()

pip install pillow
from PIL import Image, ImageDraw, ImageFont

# Cria uma imagem branca (com fundo branco)
largura, altura = 400, 100  # Defina o tamanho da imagem
imagem = Image.new('RGB', (largura, altura), color=(255, 255, 255))

# Cria um objeto para desenhar na imagem
desenhista = ImageDraw.Draw(imagem)

# Definindo a fonte (se não tiver a fonte 'arial.ttf', pode usar uma disponível no seu sistema)
try:
    fonte = ImageFont.truetype("arial.ttf", 30)  # Você pode ajustar o tamanho da fonte aqui
except IOError:
    fonte = ImageFont.load_default()  # Se a fonte não for encontrada, usa uma padrão

# Texto a ser adicionado
texto = "FLAG{CR1pt0grafia}"

# Calcula o tamanho do texto para centralizá-lo
largura_texto, altura_texto = desenhista.textsize(texto, font=fonte)
posicao = ((largura - largura_texto) // 2, (altura - altura_texto) // 2)

# Adiciona o texto na imagem
desenhista.text(posicao, texto, fill=(0, 0, 0), font=fonte)  # Cor do texto: preto

# Salva a imagem
imagem.save('flag_imagem.png')

# Mostra a imagem gerada
imagem.show()

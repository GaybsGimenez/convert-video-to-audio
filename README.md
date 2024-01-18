# Conversor de Vídeo para Áudio

Este script Python utiliza a biblioteca `moviepy` para converter vídeos no formato MKV para arquivos de áudio WAV. Ele oferece a funcionalidade de converter um único arquivo MKV em um arquivo WAV ou realizar a conversão para todos os arquivos MKV ou MP4 em uma determinada pasta.

## Pré-requisitos
Certifique-se de ter as seguintes bibliotecas instaladas antes de executar o script:
- moviepy

Você pode instalá-las usando o seguinte comando:
```bash
pip install moviepy
```

## Uso

### Função `convert_mkv_to_wav`

Esta função converte um arquivo MKV para um arquivo WAV.

```python
convert_mkv_to_wav(input_file, output_file)
```

- `input_file`: Caminho para o arquivo MKV de entrada.
- `output_file`: Caminho para salvar o arquivo WAV de saída.

### Função `convert_videos_in_folder`

Esta função percorre todos os arquivos MKV ou MP4 em uma pasta e os converte para arquivos WAV.

```python
convert_videos_in_folder(input_folder, output_folder)
```

- `input_folder`: Caminho da pasta contendo os arquivos MKV ou MP4.
- `output_folder`: Caminho da pasta onde os arquivos WAV serão salvos.

### Exemplo de Uso

```python
# Defina os caminhos das pastas de vídeos e áudios
videos_folder_path = "videos"
audios_folder_path = "audios"

# Converta todos os vídeos na pasta de vídeos para áudios na pasta de áudios
convert_videos_in_folder(videos_folder_path, audios_folder_path)
```

Certifique-se de ajustar os caminhos das pastas de entrada e saída de acordo com suas necessidades.

**Observação**: Este script assume que os vídeos de entrada têm a extensão MKV ou MP4. Certifique-se de ajustar a lista de extensões na função `convert_videos_in_folder` se estiver usando outros formatos.

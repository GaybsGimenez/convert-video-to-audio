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

Claro, aqui está a adição ao seu README:

```markdown
## Cálculo do Tempo Total dos Áudios

Para calcular o tempo total dos áudios na pasta, você pode usar a função `calculate_total_audio_duration`. Esta função percorre todos os arquivos de áudio no formato WAV na pasta especificada e calcula o tempo total em segundos. Em seguida, converte esse tempo para horas, minutos e segundos.

```python
from moviepy.audio.io.AudioFileClip import AudioFileClip

def calculate_total_audio_duration(audio_folder):
    audio_files = [f for f in os.listdir(audio_folder) if f.endswith('.wav')]

    total_duration = 0

    for audio_file in audio_files:
        audio_path = os.path.join(audio_folder, audio_file)
        audio_clip = AudioFileClip(audio_path)
        total_duration += audio_clip.duration

    return total_duration

# Exemplo de Uso
audios_folder_path = "audios"
total_audio_duration_seconds = calculate_total_audio_duration(audios_folder_path)

# Convertendo para horas, minutos e segundos
hours, remainder = divmod(total_audio_duration_seconds, 3600)
minutes, seconds = divmod(remainder, 60)

print(f"Tempo total dos áudios na pasta: {int(hours)} horas, {int(minutes)} minutos, {int(seconds)} segundos")
```

Certifique-se de ajustar o caminho da pasta de áudio de acordo com a sua estrutura de diretórios. Isso fornecerá uma visão rápida do tempo total dos áudios disponíveis na pasta.

Certifique-se de ajustar os caminhos das pastas de entrada e saída de acordo com suas necessidades.

**Observação**: Este script assume que os vídeos de entrada têm a extensão MKV ou MP4. Certifique-se de ajustar a lista de extensões na função `convert_videos_in_folder` se estiver usando outros formatos.

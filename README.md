# Conversor Vídeo para Áudio

Este script Python utiliza a biblioteca `moviepy` para converter vídeos no formato MKV para arquivos de áudio WAV. Além disso, oferece uma funcionalidade para calcular o tempo total dos áudios gerados na pasta.

## Pré-requisitos
Certifique-se de ter a biblioteca `moviepy` instalada antes de executar o script:

```bash
pip install moviepy
```

## Conversão de Vídeo para Áudio

### Função `convert_mkv_to_wav`

Converte um arquivo MKV para um arquivo WAV.

### Função `convert_videos_in_folder`

Percorre arquivos MKV ou MP4 em uma pasta, convertendo-os para arquivos WAV.

```python
videos_folder_path = "videos"
audios_folder_path = "audios"
convert_videos_in_folder(videos_folder_path, audios_folder_path)
```

## Cálculo do Tempo Total dos Áudios

Função `calculate_total_audio_duration` calcula o tempo total dos áudios na pasta e imprime em horas, minutos e segundos.

```python
audios_folder_path = "audios"
total_audio_duration_seconds = calculate_total_audio_duration(audios_folder_path)
print(f"Tempo total dos áudios na pasta: {int(hours)} horas, {int(minutes)} minutos, {int(seconds)} segundos")
```

Ajuste os caminhos das pastas conforme necessário. Este README fornece uma visão geral concisa do script e suas principais funcionalidades.

Certifique-se de ajustar os caminhos das pastas de entrada e saída de acordo com suas necessidades.

**Observação**: Este script assume que os vídeos de entrada têm a extensão MKV ou MP4. Certifique-se de ajustar a lista de extensões na função `convert_videos_in_folder` se estiver usando outros formatos.

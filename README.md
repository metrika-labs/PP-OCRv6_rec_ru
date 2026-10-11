<div align="center">
  <img src="media/logo.png" alt="Logo" width="100%"/>
  <br>
  <a href="https://huggingface.co/collections/vladlinv/ru-ocr"><img src="https://img.shields.io/badge/🤗_Hugging_Face-RU_OCR-FFD21E" alt="Hugging Face"></a>
  <a href="https://github.com/vladlinv/PP-OCRv6_rec_ru"><img src="https://img.shields.io/badge/GitHub-PP--OCRv6__rec__ru-181717?logo=github" alt="GitHub"></a>
</div>

## Быстрые OCR-модели PP-OCRv6, дообученные для распознавания текста на русском языке, включая рукописный.

Результаты на [ru-ocr-benchmark-hard](https://huggingface.co/datasets/vladlinv/ru-ocr-benchmark-hard) — бенчмарке со сложными примерами, включая искажения, дефекты печати и изображения низкого качества.

### Full pages — complete OCR pipeline (155 images)

<table>
  <thead>
    <tr><th align="left">Model</th><th>1-NED</th><th>SER</th><th>WER</th><th>Accuracy</th></tr>
  </thead>
  <tbody>
    <tr><td>Yandex Vision OCR</td><td align="center">0.967687</td><td align="center">20.21%</td><td align="center">6.74%</td><td align="center">18.06%</td></tr>
    <tr><td><a href="https://huggingface.co/vladlinv/PP-OCRv6_medium_rec_ru"><b>PP-OCRv6 Medium RU</b></a> (<a href="https://huggingface.co/vladlinv/PP-OCRv6_medium_rec_ru_onnx">For RapidOCR</a>)<br><sub>DET: PP-OCRv6 Medium</sub></td><td align="center">0.977348</td><td align="center">16.14%</td><td align="center">5.59%</td><td align="center">13.55%</td></tr>
    <tr><td><a href="https://huggingface.co/vladlinv/PP-OCRv6_tiny_rec_ru"><b>PP-OCRv6 Tiny RU</b></a> (<a href="https://huggingface.co/vladlinv/PP-OCRv6_tiny_rec_ru_onnx">For RapidOCR</a>)<br><sub>DET: PP-OCRv6 Small</sub></td><td align="center">0.973302</td><td align="center">25.01%</td><td align="center">7.93%</td><td align="center">5.81%</td></tr>
    <tr><td>Occular-OCR (SVTR-T)</td><td align="center">0.958628</td><td align="center">42.07%</td><td align="center">12.34%</td><td align="center">0.00%</td></tr>
    <tr><td>PP-OCRv5 Cyrillic (RapidOCR)<br><sub>DET: PP-OCRv5 Server</sub></td><td align="center">0.841356</td><td align="center">50.28%</td><td align="center">27.10%</td><td align="center">0.00%</td></tr>
    <tr><td>PP-OCRv5 ESlav (RapidOCR)<br><sub>DET: PP-OCRv5 Server</sub></td><td align="center">0.833810</td><td align="center">57.50%</td><td align="center">30.78%</td><td align="center">0.00%</td></tr>
    <tr><td>Tesseract 5 Best</td><td align="center">0.761598</td><td align="center">61.68%</td><td align="center">36.37%</td><td align="center">0.00%</td></tr>
  </tbody>
</table>

### Crops — text recognition (3182 images)

<table>
  <thead>
    <tr><th align="left">Model</th><th>1-NED</th><th>SER</th><th>WER</th><th>Accuracy</th></tr>
  </thead>
  <tbody>
    <tr><td><a href="https://huggingface.co/vladlinv/PP-OCRv6_medium_rec_ru"><b>PP-OCRv6 Medium RU</b></a> (<a href="https://huggingface.co/vladlinv/PP-OCRv6_medium_rec_ru_onnx">For RapidOCR</a>)</td><td align="center">0.951576</td><td align="center">28.16%</td><td align="center">16.05%</td><td align="center">71.84%</td></tr>
    <tr><td>Yandex Vision OCR</td><td align="center">0.845650</td><td align="center">39.25%</td><td align="center">22.29%</td><td align="center">60.75%</td></tr>
    <tr><td><a href="https://huggingface.co/vladlinv/PP-OCRv6_tiny_rec_ru"><b>PP-OCRv6 Tiny RU</b></a> (<a href="https://huggingface.co/vladlinv/PP-OCRv6_tiny_rec_ru_onnx">For RapidOCR</a>)</td><td align="center">0.908217</td><td align="center">48.18%</td><td align="center">27.71%</td><td align="center">51.82%</td></tr>
    <tr><td>Occular-OCR (SVTR-T)</td><td align="center">0.884307</td><td align="center">50.97%</td><td align="center">29.24%</td><td align="center">49.03%</td></tr>
    <tr><td>PP-OCRv5 Cyrillic (RapidOCR)</td><td align="center">0.803864</td><td align="center">67.13%</td><td align="center">46.66%</td><td align="center">32.87%</td></tr>
    <tr><td>PP-OCRv5 ESlav (RapidOCR)</td><td align="center">0.790004</td><td align="center">69.58%</td><td align="center">50.21%</td><td align="center">30.42%</td></tr>
    <tr><td>Tesseract 5 Best</td><td align="center">0.659237</td><td align="center">78.13%</td><td align="center">60.65%</td><td align="center">21.87%</td></tr>
  </tbody>
</table>

## Использование

### 🚀 Рекомендуемые для CPU (RapidOCR / ONNX)
* [**RapidOCR (PP-OCRv6 Medium RU)**](https://huggingface.co/vladlinv/PP-OCRv6_medium_rec_ru_onnx)
* [**RapidOCR (PP-OCRv6 Tiny RU)**](https://huggingface.co/vladlinv/PP-OCRv6_tiny_rec_ru_onnx)

### 🚀 Рекомендуемые для GPU (PaddlePaddle)
* [**PP-OCRv6 Medium RU**](https://huggingface.co/vladlinv/PP-OCRv6_medium_rec_ru)
* [**PP-OCRv6 Tiny RU**](https://huggingface.co/vladlinv/PP-OCRv6_tiny_rec_ru)

## Детали
PP-OCRv6 — линейка легковесных распознавателей текста PaddlePaddle. Модели дообучены для русского языка на 2 млн изображений текстовых строк из реальных сканов документов, рукописных образцов и синтетических данных. Доступны для PaddleOCR, а также в формате ONNX для быстрого инференса на CPU через RapidOCR.

Текущая версия уверенно распознаёт разборчивый рукописный текст, однако при работе со скорописью и менее чётким почерком возможны неточности. В следующем релизе будут устранены характерные для архитектуры PP-OCR ограничения. Данных для обучения станет в разы больше, а качество распознавания рукописного текста заметно улучшится.


<img src="https://raw.githubusercontent.com/vladlinv/PP-OCRv6_rec_ru/master/media/sample1.png" alt="Пример 1" width="50%"/><br>
PP-OCRv6 Medium: Мир меняется быстро (score: 0.9765)<br>
PP-OCRv6 Tiny: чир меняется быстро (score: 0.9082)<br>

## Ссылки

Стандартные аугментации при обучении модели дополнялись собственным пайплайном.<br>

Бенчмарк для проверки качества моделей: [vladlinv/ru-ocr-benchmark-hard](https://huggingface.co/datasets/vladlinv/ru-ocr-benchmark-hard)

Часть примеров рукописи из [AntiplagiatCompany/HWR200](https://huggingface.co/datasets/AntiplagiatCompany/HWR200)

Оригинальный репозиторий PaddleOCR: [PaddlePaddle/PaddleOCR](https://github.com/PaddlePaddle/PaddleOCR)<br>
Фреймворк RapidOCR: [RapidAI/RapidOCR](https://github.com/RapidAI/RapidOCR)

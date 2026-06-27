# TranscribeAudioOutput

## EN

A GNU/Linux bash script that allows to transcribe system audio output via whisper.cpp and copy the result to clipboard.

### Dependencies:

- Configured [whisper.cpp](https://github.com/ggml-org/whisper.cpp).
- Downloaded main model and voice activity detection model.
- xclip (on X11) or wl-clipboard (on Wayland) for clipboard copy.
- PipeWire audio subsystem for sound recording via pw-record.
- curl for making requests to whisper-server.

### Preparation Guide:

1. Copy the transcribe_audio_output script into a directory under [PATH](https://www.digitalocean.com/community/tutorials/how-to-view-and-update-the-linux-path-environment-variable).
2. Change lang and dir parameters in the script to match your target language for transcribing (a two-letter [ISO-639-1](https://en.wikipedia.org/wiki/List_of_ISO_639_language_codes) format) and whisper.cpp directory location.
3. If models other than ggml-large-v3.bin and ggml-silero-v6.2.0.bin are supposed to be used, update model and vad parameters respectively.
4. Mark the script as executable via file manager or terminal (e.g. `chmod +x ./transcribe_audio_output`).
5. Assign a certain shortcut (e.g. Super+X) to transcribe audio with the script in your system settings or configuration. For example:

   <img width="644" height="212" alt="image" src="https://github.com/user-attachments/assets/bb055f5b-36ee-4fd2-ad2c-0d614d9240ac" />

6. Optionally assign another shortcut (e.g. Shift+Super+X) to unload the whisper-server process from RAM, in your system settings or configuration. For example:

   <img width="644" height="220" alt="image" src="https://github.com/user-attachments/assets/5e8b21da-60dc-4bef-a512-14e738d4d8f9" />


### Use Guide:

1. Press the assigned shortcut for transcribing in order to start recording system audio.
2. Play your audio.
3. Press the shorcut again to stop the recording, get it transcribed and copy the transcription to clipboard.
4. Paste the transcribed text where it's needed.
5. [Optional] Press the shortcut for unloading the whisper-server process to save RAM when the transcribing session is over.


## UA

GNU/Linux bash-скрипт, який дозволяє транскрибувати системний аудіовихід за допомогою whisper.cpp та копіювати результат у буфер обміну.

### Залежності:

- Налаштований [whisper.cpp](https://github.com/ggml-org/whisper.cpp) ([приклад](https://t.me/RefoldUA/165)).
- Завантажена основна модель та модель виявлення голосової активності.
- xclip (на X11) чи wl-clipboard (на Wayland) для копіювання в буфер обміну.
- Аудіо підсистема PipeWire для запису звуку через pw-record.
- curl для надсилання запитів до whisper-server.

### Інструкція з підготовки:

1. Скопіюйте скрипт transcribe_audio_output у директорію, що входить до [PATH](https://itmaster.biz.ua/programming/linux/path-in-linux.html).
2. Змініть параметри lang і dir у скрипті відповідно до потрібної мови транскрибування (дволітерний формат [ISO-639-1](https://en.wikipedia.org/wiki/List_of_ISO_639_language_codes)) та розташування каталогу whisper.cpp.
3. Якщо планується використання інших моделей, ніж ggml-large-v3.bin та ggml-silero-v6.2.0.bin, оновіть параметри model та vad відповідно.
4. Зробіть скрипт виконуваним через файловий менеджер або термінал (наприклад, `chmod +x ./transcribe_audio_output`).
5. Призначте певну комбінацію клавіш (наприклад, Super+X) для запуску транскрибування в налаштуваннях сабо конфігурації системи. Наприклад:

   <img width="644" height="212" alt="image" src="https://github.com/user-attachments/assets/bb055f5b-36ee-4fd2-ad2c-0d614d9240ac" />

6. За бажанням призначте іншу комбінацію клавіш (наприклад, Shift+Super+X) для вивантаження процесу whisper-server з оперативної пам’яті у налаштуваннях або конфігурації системи. Наприклад:

   <img width="644" height="220" alt="image" src="https://github.com/user-attachments/assets/5e8b21da-60dc-4bef-a512-14e738d4d8f9" />

### Інструкція з використання:

1. Натисніть призначену комбінацію клавіш для транскрибування, щоб почати запис системного аудіо.
2. Запустіть відтворення аудіо.
3. Натисніть комбінацію клавіш ще раз, щоб зупинити запис, отримати транскрипцію та скопіювати її в буфер обміну.
4. Вставте транскрибований текст у потрібне місце.
5. [Опціонально] Натисніть комбінацію клавіш для вивантаження процесу whisper-server, щоб звільнити оперативну пам’ять після завершення сесії транскрибування.

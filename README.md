# Сегментация аорты и ее 3D моделирование

В [windowing_and_png_saving.ipynb](../main/windowing_and_png_saving.ipynb) осуществляется предобработка датасета SegTHOR, а также его сохранение
в .png формате.

В [resnet_and_thresholding.ipynb](../main/resnet_and_thresholding.ipynb) обучается классификатор ResNet-18, а также подбирается такой порог, что количество ложно отрицательных (False Negative) прогнозов равно нулю. Это нужно для того, чтобы исключить ошибочный пропуск снимка, содержащего аорту.

Следующие ноутбуки включают в себя инициализацию,
обучение и измерение метрик сегментации моделей U-Net, TransUNet, Swin-Unet соответственно:

* [unet_training.ipynb](../main/unet_training.ipynb)
* [transunet_training.ipynb](../main/unet_training.ipynb)
* [swinunet_training.ipynb](../main/unet_training.ipynb)


В ноутбуке [3d_render_using_segmentation.ipynb](../main/3d_render_using_segmentation.ipynb) производится 3D моделирование аорты с помощью библиотеки SimpleITK. 3D модель сохраняется в формат .nii.gz (NIfTI).

# Segmentación de columna
Realizar esta segmentación fue un reto, sobretodo por
<img width="1336" height="857" alt="Captura de pantalla 2026-06-14 215636" src="https://github.com/user-attachments/assets/1f372a07-4cb4-4f73-a5d7-fdc15f0b16fd" />

## Resolución de imagen
Usé el archivo .nrrd proporcionado para esta práctica.
* Tamaño vóxel: 0.7617 mm x 0.7617 mm
* Espesor de corte: 2.5000 mm
<img width="586" height="403" alt="Captura de pantalla 2026-06-14 212145" src="https://github.com/user-attachments/assets/8e1df519-6f37-4ab9-83ca-57102bad7cc4" />

##   Protocolo de segmentación
Usé Segment Editor para el proceso de segmentación del modelo:
* Threshold principalmente para **segmentar por densidades la vértebra**:
<img width="580" height="572" alt="Captura de pantalla 2026-06-14 221816" src="https://github.com/user-attachments/assets/5faae406-1fc0-4019-91b9-a641007947ab" />

Después, para solo quedarme con dos vértebras de mi interés, usé la herramienta de Scissors con Erase Outside en la vista 3D para aislarlas, y Erase Inside para eliminar los pequeños restos que quedaban.
* Paint principalmente para los **discos: "manual"**
<img width="1918" height="1005" alt="Captura de pantalla 2026-06-14 213457" src="https://github.com/user-attachments/assets/4c517c61-462a-4196-8849-832f00b03de1" />

Para los discos fue diferente debido a que es un tejido blando y no tiene un contraste útil definido. El método que usé fue manual ya que elegí la herramienta de Paint.
Después de definirlos con ayuda de los planos, apliqué la herramienta de Fill between slices para el volumen
## Filtros aplicados
Apliqué de manera individual la herramienta de Smoothing utilizando el filtro Median para ambos segmentos, para eliminar el ruido y definir mejor los bordes de ambos.
<img width="1918" height="828" alt="Captura de pantalla 2026-06-14 214012" src="https://github.com/user-attachments/assets/c8247602-41a0-4e62-bea6-9e2954ec1992" />

## Datos cuantitativos
Los siguientes datos los saqué de la herramienta de Segment Statistics a partir del resultadonfinal:
* Vértebras (Hueso)  
V:83,542.4 mm³, Área de superficie: 28,968.6 mm²
* Discos  
V: 11,083.6 mm³, área de superficie: 3,277.17 mm²
<img width="1347" height="192" alt="Captura de pantalla 2026-06-14 214544" src="https://github.com/user-attachments/assets/0bb620f6-a97a-438f-9e2a-977989d964a1" />
<img width="486" height="192" alt="Captura de pantalla 2026-06-14 214553" src="https://github.com/user-attachments/assets/7a257743-9e50-463d-87bf-18fdbe937237" />

## Archivos STL
* [Descargar Modelo del Hueso (Vértebras)](./Segmentation_Hueso.stl)
* [Descargar Modelo del Disco Intervertebral](./Segmentation_Disco.stl)

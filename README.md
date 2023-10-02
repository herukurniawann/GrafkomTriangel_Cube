## Tugas 3 Grafika Komputer

Nama : Heru Dwi Kurniawan

NRP : 5025211055

Kelas : Grafika Komputer A

**SIMPLE WEB-GL 2D AND 3D**

## 2D Square from Two Triangle

**Before**

![WhatsApp Image 2023-10-03 at 06 03 38](https://github.com/herukurniawann/GrafkomTriangel_Cube/assets/93961310/f1e1c24b-4f99-404b-8ec4-8b688667cf7c)


**After**

![WhatsApp Image 2023-10-03 at 05 58 11](https://github.com/herukurniawann/Pweb-tugas-1-Healthy-Food/assets/93961310/1329898e-bf35-4fbd-bebb-3d7ed61d67cd)

```bash
 function draw() {
        gl.clearColor(0, 0, 0, 1); // specify the color to be used for clearing
        gl.clear(gl.COLOR_BUFFER_BIT); // clear the canvas (to black)

        /* SEGITIGA KE-1 */

        /* Koordinat segitiga ke-1 : */
        /* Set up values for the "coords" attribute */

        let coords1 = new Float32Array([-0.5, -0.5, 0.5, 0.5, -0.5, 0.5]);

        gl.bindBuffer(gl.ARRAY_BUFFER, bufferCoords);
        gl.bufferData(gl.ARRAY_BUFFER, coords1, gl.STREAM_DRAW);
        gl.vertexAttribPointer(attributeCoords, 2, gl.FLOAT, false, 0, 0);
        gl.enableVertexAttribArray(attributeCoords);

        /* Warna segitiga ke-1 : */
        /* Set up values for the "color" attribute */

        let color = new Float32Array([0, 1, 0, 1, 0, 0, 0, 0, 1]);

        gl.bindBuffer(gl.ARRAY_BUFFER, bufferColor);
        gl.bufferData(gl.ARRAY_BUFFER, color, gl.STREAM_DRAW);
        gl.vertexAttribPointer(attributeColor, 3, gl.FLOAT, false, 0, 0);
        gl.enableVertexAttribArray(attributeColor);

        /* Gambar segitiga ke-1 :*/
        /* Draw the triangle. */

        gl.drawArrays(gl.TRIANGLES, 0, 3);

        /* Set Up Coords triangel ke-2*/

        let coords2 = new Float32Array([-0.5, -0.5, 0.5, 0.5, 0.5, -0.5]);

        gl.bindBuffer(gl.ARRAY_BUFFER, bufferCoords);
        gl.bufferData(gl.ARRAY_BUFFER, coords2, gl.STREAM_DRAW);
        gl.vertexAttribPointer(attributeCoords, 2, gl.FLOAT, false, 0, 0);
        gl.enableVertexAttribArray(attributeCoords);

        /* Set Up Color triangel ke-2 : */

        let color2 = new Float32Array([0, 1, 0, 1, 0, 0, 1, 1, 1]);

        gl.bindBuffer(gl.ARRAY_BUFFER, bufferColor);
        gl.bufferData(gl.ARRAY_BUFFER, color2, gl.STREAM_DRAW);
        gl.vertexAttribPointer(attributeColor, 3, gl.FLOAT, false, 0, 0);
        gl.enableVertexAttribArray(attributeColor);

        /* Draw the triangle. */
        /*  Triangel ke-2 :*/

        gl.drawArrays(gl.TRIANGLES, 0, 3);
      }
```

## 3D Cube


**Before**

![WhatsApp Image 2023-10-03 at 06 11 46](https://github.com/fathinmputra/assignment3_webgl/assets/93961310/9d4670a6-d4c2-4ad3-8ea0-722a071ab45f)

**After**

![WhatsApp Image 2023-10-03 at 06 10 23](https://github.com/fathinmputra/assignment3_webgl/assets/93961310/c69c636e-b97a-4016-be09-9a8fff41b0a5)

## Warna Biru Bagian Depan 

![WhatsApp Image 2023-10-02 at 22 17 50 (1)](https://github.com/fathinmputra/assignment3_webgl/assets/93961310/13359cbf-be17-4d56-8ca2-2a0b05d7f49b)

```bash
 drawPrimitive(
          gl.TRIANGLE_FAN,
          [0, 0, 1, 1],
          [-0.5, -0.3, -0.4, -0.5, 0.3, -0.5, 0.2, 0.3, -0.5, 0.2, -0.3, -0.5]
        ); // Warna Biru Depan
```
## Warna Hijau Bagian Belakang

![WhatsApp Image 2023-10-02 at 22 19 36 (1)](https://github.com/fathinmputra/assignment3_webgl/assets/93961310/e9cfe40e-b040-4a8a-8a52-dbb5a1a90e45)

``` bash
  drawPrimitive(
          gl.TRIANGLE_FAN,
          [0, 1, 0, 1],
          [-0.2, -0.1, 0.4, 0.4, -0.1, 0.4, 0.4, 0.5, 0.4, -0.2, 0.5, 0.4]
        ); // Warna Hijau Belakang
```

## Warna Cyan Bagian Atas

![WhatsApp Image 2023-10-02 at 22 20 24 (1)](https://github.com/fathinmputra/assignment3_webgl/assets/93961310/4c368fa5-d956-43ca-ae91-3a09cfcdee60)

``` bash
 drawPrimitive(
          gl.TRIANGLE_FAN,
          [0, 1, 1, 1],
          [-0.2, 0.5, -0.4, -0.5, 0.3, 0.4, 0.2, 0.3, 0.4, 0.4, 0.5, -0.5]
        ); // Warna Cyan Bagian Atas
```

## Warna Fuchsia Bagian Bawah

![WhatsApp Image 2023-10-02 at 22 21 08 (1)](https://github.com/fathinmputra/assignment3_webgl/assets/93961310/3a40bb2c-e8e7-43fb-993f-c1331880a861)

``` bash
drawPrimitive(
          gl.TRIANGLE_FAN,
          [1, 0, 1, 1],
          [-0.2, -0.1, -0.4, 0.4, -0.1, -0.4, 0.2, -0.3, 0.4, -0.5, -0.3, 0.4]
        ); // Warna Fuchsia Bagian Bawah
```

## Warna Kuning Bagian Sisi Kanan

![WhatsApp Image 2023-10-02 at 22 22 28 (1)](https://github.com/fathinmputra/assignment3_webgl/assets/93961310/1acd85e7-2029-4852-bf5c-c95597901ed1)

``` bash drawPrimitive(
          gl.TRIANGLE_FAN,
          [1, 1, 0, 1],
          [0.4, -0.1, -0.4, 0.4, 0.5, -0.5, 0.2, 0.3, 0.4, 0.2, -0.3, 0.4]
        ); // Warna Kuning Bagian Sisi kanan
```

## Warna Merah Bagian Sisi Kiri

![WhatsApp Image 2023-10-02 at 22 23 46 (1)](https://github.com/fathinmputra/assignment3_webgl/assets/93961310/f495b1dc-7ac5-41db-857c-9ebf1e51a796)

``` bash
 drawPrimitive(
          gl.TRIANGLE_FAN,
          [1, 0, 0, 1],
          [-0.2, -0.1, -0.4, -0.5, -0.3, 0.4, -0.5, 0.3, 0.4, -0.2, 0.5, -0.5]
        ); // Warna Merah Bagian Sisi Kiri
```








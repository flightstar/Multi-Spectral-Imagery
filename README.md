# Multi-Spectral Imagery
Research solved problems as Military Target Tracking, Land Mine Detection, Ballistic Missile Detection, Space-based imaging, Documents and artworks,...

![](https://i.ytimg.com/vi/icjvpOWijRo/maxresdefault.jpg)

Khi bạn xem bài này, đôi mắt bạn nhìn thấy đó là những sự phản xạ năng lượng của ánh sáng nhưng máy tính thì chỉ nhìn thấy 3 kênh màu: đỏ, xanh lục, xanh lam.

Nếu bạn là chú cá vàng thì có lẻ bạn có thể nhìn thấy nhiều loại ánh sáng khác nhau. một chú cá vàng có thể nhìn thấy các bức xạ hồng ngoại, cái mà mắt thường của con người không thể nhìn thấy được.

Một chú ong có thể nhìn thấy ánh sáng cực tím, là cái mà mắt thường của con người không thể nhìn thấy được.

Còn bây giờ, bạn hãy tưởng tượng rằng mình đang ở trong thế giới của loài ong, cá, người để có thể nhìn thấy nhiều loại ánh sáng khác nhau. Liệu chúng ta có thể biến điều này thành hiện thực không? Chúng ta có thể áp dụng các bộ cảm biến và các thuật toán đa hướng Multispectral và Hyperspectral để thực hiện điều đó để quan sát sóng (mọi loại sóng đều có thể truyền năng lượng) và ánh sáng.

### Vậy sự khác nhau của Multispectral và Hyperspectral là gì?
+ Phổ điện từ (Electromagnetic Spectrum)
  Kênh màu (đỏ, lục và lam), hồng ngoại và cực tím là các [vùng mô tả trong phổ điện từ](https://earthobservatory.nasa.gov/Features/RemoteSensing/remote_03.php). Mỗi vùng được phân loại dựa trên độ dài bước sóng:
  
  + Vùng ánh sáng con người nhìn thấy là từ **380 nm đến 700 nm**
  + Vùng cá vàng nhìn thấy tia hồng ngoại là từ **700 nm đến 1mm**
  + Vùng ong nhìn thấy các bức xạ cực tím là từ **10 nm đến 380 nm**
   
  Trên thực tế ta có thể nhìn nhiều hơn như thế này từ các phản xạ của các bức xạ điện từ truyền tới các cảm biến.
  
  Sự khác nhau lớn nhất giữa multispectral và hyperspectral là số lượng các dải bước sóng
  
  + Hình ảnh multispectral thường đề cập đến 3 đến 10 dải. Để rõ ràng, mỗi dải thu được bằng cách sử dụng một máy đo bức xạ viễn thám.
  
  ![](https://gisgeography.com/wp-content/uploads/2014/07/multi.png)
  
  + Hình ảnh hyperspectral gồm rất nhiều các dải nhỏ (10-20 nm). Một hình ảnh hyperspectral có thể có hàng trăm hoặc hàng ngàn dải nhỏ. Nó lấy từ các quang phổ hình ảnh.
  
  ![](https://gisgeography.com/wp-content/uploads/2014/07/hyper.png)
  
  **Các ví dụ về cảm biến đa hướng [Landsat-8](https://landsat.usgs.gov/landsat-8)**. Landsat-8 tạo ra 11 hình ảnh với các băng tần sau:
  
  + Coastal aerosol trong dải 1 (0.43-0.45 um)
  + Blue trong dải 2 (0.45-0.51 um)
  + Green trong dải 3 (0.53-0.59 um)
  + Red trong dải 4 (0.64-0.67 um)
  + Near infrared NIR trong dải 5 (0.85-0.88 um)
  + Short-wave Infrared SWIR 1 trong dải 6 (1.57-1.65 um)
  + Short-wave Infrared SWIR 2 trong dải 7 (2.11-2.29 um)
  + Panchromatic trong dải 8 (0.50-0.68 um)
  + Cirrus trong dải 9 (1.36-1.38 um)
  + Thermal Infrared TIRS 1 trong dải 10 (10.60-11.19 um)
  + Thermal Infrared TIRS 2 trong dải 11 (11.50-12.51 um)
  
  Mỗi dải băng tần có độ phân giải không gian 30 m (tức là thu được và phân tích tốt dải sóng trong 30m) ngoại trừ băng tần 8, 10 và 11. Trong khi băng tần 8 có độ phân giải không gian là 15 m, băng tần 10 và 11 có kích thước pixel là 100m.

  Nếu bạn tự hỏi tại sao không có dải 0.88 đến 1.36, sự hấp thụ khí quyển là động lực chính tại sao không có cảm biến nào phát hiện các bước sóng này.
  
  **Ví dụ về hyperspectral image:**
  
  Vệ tinh TRW Lewis là hệ thống vệ tinh siêu âm đầu tiên vào năm 1997. Thật không may, [NASA đã mất liên lạc với nó](https://www.nasa.gov/home/hqnews/1997/97-182.txt).
  
  Nhưng sau đó NASA đã có [máy đo quang phổ Hyperion](https://archive.usgs.gov/archive/sites/eo1.usgs.gov/index.html) (một phần của vệ tinh EO-1) là một ví dụ về cảm biến siêu âm. Ví dụ, Hyperion tạo ra hình ảnh có độ phân giải không gian 30 mét trong 220 băng tần phổ (0.4-2.5 um).

  Kính hiển vi hình ảnh hồng ngoại của NASA [(AVIRIS)](https://aviris.jpl.nasa.gov/) là một ví dụ về cảm biến các băng tần trên không. Ví dụ, AVIRIS cung cấp 224 kênh liền kề với bước sóng từ 0,4-2,5 um.
  
  **Note**: um = micrometer
  
  Tóm lại sự khác nhau giữa multispectral image và hyperspectral image là
  + Multispectral image: Từ 3 đến 10 dải rộng
  + Hyperspectral image: Hàng trăn thậm chí hàng nghìn dải hẹp
  
  ### Một số chủ đề nghiên cứu thuật toán Multispectral:
  
  @algorithm image processing
  
  @algorithm hardware
  
  @analysis of algorithms videos
  
  [![Discover house, building from aerial image](https://i.ytimg.com/vi/jA5FM3tBfgw/maxresdefault.jpg)](https://youtu.be/jA5FM3tBfgw)

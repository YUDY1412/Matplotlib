Khi vẽ biểu đồ với Matplotlib trong Python, bạn có thể cấu hình rất nhiều thuộc tính của biểu đồ để tùy chỉnh giao diện và hành vi của nó. Dưới đây là danh sách các lệnh cấu hình chính mà bạn có thể sử dụng:

### 1. **Tiêu đề và nhãn**
- **`plt.title('Tiêu đề')`**: Đặt tiêu đề cho biểu đồ.
- **`plt.xlabel('Nhãn trục X')`**: Đặt nhãn cho trục X.
- **`plt.ylabel('Nhãn trục Y')`**: Đặt nhãn cho trục Y.

### 2. **Giới hạn trục**
- **`plt.xlim([xmin, xmax])`**: Đặt giới hạn cho trục X.
- **`plt.ylim([ymin, ymax])`**: Đặt giới hạn cho trục Y.
- **`plt.axis([xmin, xmax, ymin, ymax])`**: Đặt giới hạn cho cả hai trục cùng lúc.

### 3. **Định dạng trục**
- **`plt.xticks(ticks, labels)`**: Tùy chỉnh các giá trị và nhãn trên trục X.
- **`plt.yticks(ticks, labels)`**: Tùy chỉnh các giá trị và nhãn trên trục Y.
- **`plt.grid(True)`**: Bật/tắt lưới cho biểu đồ.

### 4. **Định dạng đường**
- **`plt.plot(x, y, linestyle='-', linewidth=2, color='blue', marker='o')`**: Tùy chỉnh kiểu đường, độ dày, màu sắc và kiểu marker.
- **`plt.set_linestyle('--')`**: Đặt kiểu đường (solid, dashed, dash-dot, dotted).
- **`plt.set_marker('o')`**: Đặt kiểu marker (chấm, tròn, vuông, dấu cộng, dấu sao, v.v.).

### 5. **Chú thích (Legend)**
- **`plt.legend()`**: Hiển thị chú thích cho các đường trên biểu đồ.
- **`plt.legend(loc='upper right')`**: Đặt vị trí của chú thích (có thể chọn 'upper right', 'upper left', 'lower right', 'lower left', 'center', v.v.).

### 6. **Định dạng văn bản**
- **`plt.text(x, y, 'Văn bản')`**: Thêm văn bản vào vị trí `(x, y)` trên biểu đồ.
- **`plt.annotate('Chú thích', xy=(x, y), xytext=(x2, y2), arrowprops=dict(facecolor='black', shrink=0.05))`**: Thêm chú thích với mũi tên.

### 7. **Chỉnh sửa kích thước và tỉ lệ**
- **`plt.figure(figsize=(width, height))`**: Đặt kích thước của biểu đồ (đơn vị inch).
- **`plt.subplots_adjust(left=0.1, right=0.9, top=0.9, bottom=0.1)`**: Điều chỉnh lề của biểu đồ.

### 8. **Màu sắc**
- **`plt.set_facecolor('color')`**: Đặt màu nền cho toàn bộ vùng đồ thị.
- **`plt.set_edgecolor('color')`**: Đặt màu viền cho vùng đồ thị.

### 9. **Định dạng đường viền và khung**
- **`plt.spines['top'].set_visible(False)`**: Ẩn/hiện các đường viền trên đồ thị (có thể là 'top', 'bottom', 'left', 'right').
- **`plt.spines['left'].set_position(('outward', 10))`**: Đặt vị trí cho đường viền (có thể là 'outward', 'inward', 'data').

### 10. **Hiển thị màu sắc và màu sắc gradient**
- **`plt.imshow()`**: Hiển thị dữ liệu dưới dạng ảnh (thường dùng cho ma trận).
- **`plt.colorbar()`**: Thêm thanh màu (color bar) cho các biểu đồ nhiệt (heatmap).

### 11. **Định dạng hình ảnh**
- **`plt.savefig('filename.png', dpi=300)`**: Lưu biểu đồ dưới dạng tệp hình ảnh với độ phân giải tùy chọn.
- **`plt.tight_layout()`**: Điều chỉnh các phần tử trên biểu đồ để tránh chồng chéo.

### 12. **Subplots**
- **`plt.subplot(nrows, ncols, index)`**: Tạo một lưới con trong một biểu đồ (ví dụ: `plt.subplot(2, 1, 1)`).
- **`plt.subplots(nrows, ncols)`**: Tạo một lưới subplots và trả về các đối tượng Figure và Axes.
- **`plt.subplot2grid((nrows, ncols), (row, col), rowspan=1, colspan=1)`**: Tạo subplots với cách bố trí grid tùy chỉnh.

### 13. **Tương tác**
- **`plt.ion()`**: Bật chế độ tương tác.
- **`plt.ioff()`**: Tắt chế độ tương tác.
- **`plt.pause(interval)`**: Tạm dừng biểu đồ trong khoảng thời gian `interval` (giây).

### 14. **Kiểu trục (Logarithmic, Symlog, Logit)**
- **`plt.xscale('log')`**: Đặt trục X theo thang đo logarit.
- **`plt.yscale('log')`**: Đặt trục Y theo thang đo logarit.
- **`plt.yscale('symlog', linthreshy=0.01)`**: Sử dụng thang đo `symlog` với ngưỡng tuyến tính.

### 15. **Cấu hình toàn cục**
- **`plt.rcParams['font.size'] = 14`**: Thay đổi kích thước phông chữ mặc định cho toàn bộ biểu đồ.
- **`plt.rcParams['figure.figsize'] = [10, 6]`**: Đặt kích thước mặc định cho tất cả các biểu đồ.

### 16. **Các loại biểu đồ khác**
- **`plt.bar(x, height)`**: Tạo biểu đồ cột.
- **`plt.hist(data, bins=20)`**: Tạo biểu đồ histogram.
- **`plt.scatter(x, y)`**: Tạo biểu đồ phân tán (scatter plot).
- **`plt.pie(sizes, labels=labels)`**: Tạo biểu đồ tròn.

Các lệnh trên cho phép bạn tùy chỉnh và điều chỉnh chi tiết biểu đồ để phù hợp với nhu cầu của mình khi sử dụng Matplotlib.


 
	https://matplotlib.org/stable/gallery/ticks/index.html

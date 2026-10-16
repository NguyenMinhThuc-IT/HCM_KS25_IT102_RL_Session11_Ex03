Dòng code bị lỗi: if (nhiet_do_bao_quan >= NHIET_DO_MIN || nhiet_do_bao_quan <= NHIET_DO_MAX)

Nguyên nhân kỹ thuật: Sử dụng toán tử logic HOẶC (||) thay vì VÀ (&&).

Mọi giá trị nhiệt độ $> 5.0^\circ\text{C}$ (như $25.0^\circ\text{C}$) đều thỏa mãn điều kiện nhiet_do_bao_quan >= -18.0.
Mọi giá trị nhiệt độ $< -18.0^\circ\text{C}$ (như $-25.0^\circ\text{C}$) đều thỏa mãn điều kiện nhiet_do_bao_quan <= 5.0.
Biểu thức này luôn luôn trả về true với mọi giá trị số thực, làm vô hiệu hóa hàng rào kiểm định nhiệt độ.

Biểu thức sửa lại: Sử dụng toán tử && để bắt buộc giá trị nhiệt độ phải nằm đồng thời trong cả hai mốc biên $[-18.0^\circ\text{C}, 5.0^\circ\text{C}]$:
if (nhiet_do_bao_quan >= NHIET_DO_MIN && nhiet_do_bao_quan <= NHIET_DO_MAX)

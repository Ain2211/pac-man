# pac-man
pac man project

Họ tên: Nguyễn Tú Anh
MSSV : 18020146

cách làm
Bài 1 : DFS
sử dụng 1 stack để duyệt các trạng thái theo chiều sâu cho đến khi nếu hết stack (stack trống) => duyệt thất bại
mỗi trạng thái sẽ thêm 1 mảng ( đường đi từ điểm xuất phát đến trạng thái đó )
mỗi phần tử được lấy ra khỏi stack sẽ check xem đó có phải trạng thái đích không ,
nếu có thì return về kết quả đường đi từ điểm đầu đến vị trí đó
nếu không lấy tiếp đến các trạng thái kế vị và thêm vào stack ( công thêm vị trí của trạng thái đó vào mảng kết quả đường đi của mỗi chính trạng thái đó)

Bài 2: BFS
tương tự bài 1 nhưng duyệt theo chiều rộng nên dùng Queue thay cho stack

Bài 3: UCS
tương tự bài 2 nhưng duyệt theo ưu tiên chi phí nên dùng PriotityQueue với trọng số là chi phí của mỗi trạng thái

Bài 4: A*
tương tự bài 3 nhưng PriotityQueue lấy trọng số là tổng của chi phí và hàm ước lượng (manhattan) từ trạng thái đó đến đích  

Bài 5: CornersProblem
tạo một list mới có 4 điểm góc đã cho và lấy trạng thái đầu là vị trí hiện tại và thêm list đã tạo
mỗi lần duyệt đến trạng thái nào check xem có trùng với 4 điểm góc không
nếu trùng thì lấy trạng thái đó là vị trí hiện tại và list những điểm góc còn lại (bỏ qua điểm góc trùng)
duyệt cho đến khi không còn điểm góc nào chưa đi qua (list check góc của mỗi trạng thái lúc đó sẽ rỗng)
=> hoàn thành

Bài 6: cornersHeuristic
chọn H là khoảng cách nhỏ nhất từ vị trí hiện tại khi đi qua cả 4 điểm góc theo tất cả cách đi qua 4 điểm góc theo thứ tự nào
dùng hàm permutations để trả về tất cả hoán vị của 4 điểm góc
tiếp theo với mỗi hoán vị tính khoảng cách mahattan của vị trí hiện tại đến điểm góc đầu tiên rồi tiếp túc lặp cho đến điểm cuối cùng 
ta có tổng khoảng cách
đến cuối cùng chọn khoảng cách nhỏ nhất trong các khoảng cách ứng với mỗi hoán vị 4 góc
= H

Bài 7: foodHeuristic
chọn H là khoảng cách lớn nhất từ vị trí hiện tại đến tất cả các dot ( dot xa nhất )

Bài 8: AnyFoodSearchProblem
dùng BFS để tìm node gần nhất
Một số yếu tố của luật server (2026.04.2)

# Giải thích một số khái niệm
**Khu vực trung lập**: những khu vực đặc biệt trong server, thuộc về mọi người chơi. Những khu vực trung lập bao gồm:
- Khu vực base chính trong phạm vi hình chữ nhật với 2 mốc tại tọa độ (-218; -49) và (326; -199) (tính cả đường biên);
- Khu vực spawn;
- Máy farm Enderman;
- Mapart được xác nhận;
- Mộ của Happy Ghast.

**Mapart được xác nhận**: một khu vực dùng để xây dựng mapart có những yêu cầu sau:
- Được xây ở The End;
- Có tọa độ khu vực xây dựng được tiết lộ.

**Nghị viện**: một nhóm đảm nhận công việc thông qua và bãi bỏ các luật được đề xuất, xét xử những người được cho là sử dụng các công cụ gian lận, v.v. (xem phần [Nghị viện](#nghị-viện) để biết thêm).

# Nghị viện
Nghị viện là một nhóm gồm 3 thành viên chính và 1 thành viên phụ, được bầu cử 1 lần mỗi 2 tuần. Nghị viện có quyền thông qua và bãi bỏ các luật do người chơi đề xuất, đồng thời xét xử một người chơi bị cho là phạm luật.

## Quy trình bầu cử
Nghị viện sẽ tổ chức bầu cử 1 lần mỗi 2 tuần. Một ứng cử viên phải có đủ các yêu cầu sau:
- Đã tham gia server ít nhất 1 lần trong vòng 1 tuần trước kì bầu cử;
- Đã tham gia máy chủ Discord;
- Không vi phạm bất cứ điều luật nào của server trong 1 tháng.

Khi tổ chức bầu cử, các thành viên (trừ chủ server) đáp ứng đủ các yêu cầu ở trên sẽ được thêm vào một cuộc khảo sát trên máy chủ Discord. Trải qua các vòng bầu cử, 3 thành viên cuối cùng có số phiếu bầu cao nhất sẽ là thành viên chính của Nghị viện, trong khi người thứ 4 sẽ là thành viên phụ.

Trong quá trình bầu cử, nếu mọi ứng cử viên đều có số phiếu bầu như nhau, thì một người sẽ được chọn ngẫu nhiên để bị loại thông qua lệnh Python bên dưới:
```py
import random

print(random.choice(danh_sách_ứng_viên))
input()
```

Ngoài bầu cử 1 lần mỗi 2 tuần, nếu như Nghị viện chỉ còn 2 thành viên (do 2 thành viên còn lại bị đình chỉ), bầu cử cũng sẽ được tổ chức để bầu lại thành viên của Nghị viện.

## Quy trình biểu quyết
Các thành viên chính có thể tiến hành một cuộc biểu quyết để thực hiện một hành động (ví dụ như thông qua một luật mà một người chơi đề xuất).

Khi biểu quyết được thực hiện, yêu cầu phải có từ 2 đến 3 lựa chọn: một lựa chọn đồng ý với hành động, một lựa chọn phản đối hành động, và (nếu biểu quyết có 3 lựa chọn) một lựa chọn khác thực hiện một hành động trung gian nào đó. Ví dụ: khi một người đề xuất luật cấm đánh cắp đồ của người khác, họ có thể tạo biểu quyết với 3 lựa chọn: đồng ý thêm luật, phản đối thêm luật, đồng ý thêm luật nhưng chỉ giới hạn ở một số lại đồ nhất định.

Trong trường hợp cả 3 lựa chọn đều có một người chọn, thành viên phụ của Nghị viện có thể tham gia biểu quyết để giải quyết.

## Đình chỉ thành viên
Một thành viên chính của Nghị viện nếu vi phạm luật server với hình phạt bị ban cũng sẽ bị đình chỉ khỏi việc biểu quyết trong 2 ngày. Khi đó, thành viên phụ cùa Nghị viện sẽ tạm thời thay thế vị trí của thành viên bị đình chỉ.

## Quyền lực của Nghị viện
Nghị viện có thể thực hiện các hành động sau:
- Thông qua và bãi bỏ điều luật do người chơi đề xuất cùng với hình phạt cho việc vi phạm;
- Biến điều luật do người chơi đề xuất thành điều luật cứng (lưu ý rằng hành động đó sẽ không thể đảo ngược);
- Xét xử một thành viên bị cho là đã gian lận (vi phạm điều 3.1.);
    - Việc xét xử yêu cầu phải có ít nhất 2 bằng chứng cụ thể;
- Reload lại server hay không;
    - Việc reload yêu cầu 1 lý do cụ thể;
    - Server sẽ được reload về bản lưu gần đây nhất;

# Tìm hiểu:
 ### `Docker`, `docker-composer` là gì ?
	

> Việc setup và deploy application lên một hoặc nhiều server rất vất vả
> từ việc phải cài đặt các công cụ, môi trường cần cho application đến
> việc chạy được ứng dụng chưa kể việc không đồng nhất giữa các môi
> trường trên nhiều server khác nhau. Chính vì lý do đó `Docker` được ra
> đời để giải quyết vấn đề này.

- **Docker** là một nền tảng cho developers và sysadmin để develop, deploy và run application với container. Nó cho phép tạo các môi trường độc lập và tách biệt để khởi chạy và phát triển ứng dụng và môi trường này được gọi là container. Khi cần deploy lên bất kỳ server nào chỉ cần run container của Docker thì application của bạn sẽ được khởi chạy ngay lập tức.
	- **Docker compose** là công cụ dùng để định nghĩa và run multi-container cho Docker application. Với compose bạn sử dụng file YAML để config các services cho application của bạn. Sau đó dùng command để create và run từ những config đó. Sử dụng cũng khá đơn giản chỉ với ba bước:

			Khai báo app’s environment trong Dockerfile.
			Khai báo các services cần thiết để chạy application trong file docker-compose.yml.
			Run docker-compose up để start và run app.

### `Linux` vs `Unix` vs `BSD` hay `*nix` ? `macOS` thuộc loại nào ?
- **Unix** là một hệ điều hành vốn ra đời đã từ rất lâu, tại phòng thí nghiệm Bell Labs của AT&T. Dự án được dẫn dắt bởi Ken Thompson và Dennis Ritchie, 2 nhà khoa học máy tính nổi tiếng. Công việc phát triển Unix chính thức được bắt đầu vào mùa hè năm 1969, và phiên bản đầu tiên của Unix được ra đời vào tháng 3 năm 1971, tiếp đó là phiên bản thứ 2 ra đời năm 1972.
- Những năm sau của thập niên 70, AT&T chia sẻ Unix cho những tổ chức giáo dục, hay tổ chức thương mại bên ngoài, từ đó dẫn đến sự ra đời của nhiều phiên bản Unix khác nhau. Nổi bật nhất trong số đó là phiên bản giáo dục được xây dựng bởi Computer Systems Research Group thuộc đại học California, Berkeley. Phiên bản này được biết đến rộng rãi với cái tên Berkeley Software Distribution, hay **BSD**.. Tên này cũng được sử dụng cho các bản phân phối sau này.
- Phiên bản thương mại, close source nổi tiếng, thành công nhất, có lẽ chính là **MacOS** đình đám của Apple. MacOS cũng như các hệ điều hành khác của Apple hiện nay là iOS, watchOS, và tvOS đều được dựa trên nền tảng của BSD. Và MacOS cũng là một trong số ít các hệ điều hành được coi là Unix-like(*nix), khi có được chứng nhận Single UNIX Specification. 
- Khái niệm ***nix** hay **Unix-like** vốn được dùng để chỉ những hệ điều hành có được chứng nhận Single UNIX Specification (SUS), và có thể sử dụng thương hiệu UNIX.
	> Tháng 9 năm 1983, Richard Stallman thông báo về sự ra đời của dự án **GNU** (GNU là viết tắt của từ GNU’s not Unix).
	 Mục tiêu của dự án GNU là tạo ra được một hệ điều hành miễn phí, giống Unix, nơi mà mọi người có quyền tự do copy, phát triển, chỉnh sửa và phân phối phần mềm, và việc tái phân phối là không bị giới hạn. (Nên nhớ, Unix và các phiên bản rẽ nhánh từ Unix ban đầu đều là close source và bị ràng buộc bản quyền)
Project GNU đã tạo ra được rất nhiều sản phẩm quan trọng như GNU Compiler Collection (gcc), GNU Debugger, GNU Emacs text editor (Emacs), GNU build automator (make) … Ngoài ra còn phải kể đến giấy phép nổi tiếng được sử dụng rộng rãi nhất hiện nay: GNU General Public License (GPL)
GNU Project đã đạt được nhiều thành tựu lớn, tạo ra được nhiều công cụ tương tự như những gì có trên Unix. Tuy nhiên, GNU vẫn thiếu một thành phần quan trọng, mảnh ghép cuối cùng để nó trở thành một hệ điều hành hoàn chỉnh. Đó chính là Kernel, phần thực hiện công việc điều khiển, giao tiếp với các thiết bị phần cứng (CPU, RAM, Devices …).

- Và Linus Torvalds xuất hiện, ông là cha để của **Linux** - bản chất là hạt nhân (kernel) của hệ điều hành. Sự kết hợp giữa nhân Linux, với các phần mềm của GNU đã tạo ra một hệ điều hành hoàn chỉnh, hệ điều hành hoàn toàn miễn phí đầu tiên. Nó được mang tên GNU/Linux và mọi người thường gọi ngắn gọn là hệ điều hành Linux.
Linux chỉ là phần Kernel, còn GNU cung cấp các công cụ cần thiết chạy trên Kernel đó. Tuy nhiên, việc config Kernel như thế nào, cài đặt, sử dụng các phần mềm nào thì ta có thể tự do quyết định.
Một số các tổ chức, công ty giúp chúng ta làm sẵn những việc đó với việc phối kết hợp Linux Kernel với các utilities, hay package manager để tạo ra một bản phân phối một hệ điều hành hoàn chỉnh. Chúng được gọi là Linux Distribution, hay Distro.
Ngày nay, có vô vàn các bản phân phối Linux, nhiều cái rất quen thuộc, phổ biến, và cũng có nhiều distro có thể bạn còn chưa được nghe tên bao giờ. Một số Distro được sử dụng nhiều nhất có thể kể ra như Ubuntu, Debian, CentOS, Fedora, Redhat, Linux Mint ….

*Vậy hệ điều hành Linux có phải một* **nix hay không ?*
Đáng tiếc câu trả lời là ***Không.***
Đã từng có dự án giúp Linux đạt được SUS, nhưng cuối cùng không đi đến đâu cả, và hiện tại các Distro Linux cũng không được phép sử dụng trademark UNIX.
### `Alpine` vs `Ubuntu` ?
- 	**Alpine Linux** là bản phân phối Linux dựa trên musl và BusyBox, được thiết kế bảo mật, đơn giản và hiệu quả về tài nguyên. Nó sử dụng OpenRC cho hệ thống `init`.
Alpine nổi lên sau khi Docker được phát triển bởi vì nó nhỏ và nhẹ, thường được sử dụng để làm docker image.
- **Ubuntu** là một hệ điều hành máy tính dựa trên Debian GNU/Linux, một bản phân phối Linux thông dụng. Tên của nó bắt nguồn từ "ubuntu" trong tiếng Zulu, có nghĩa là "tình người", mô tả triết lý ubuntu: "Tôi được là chính mình nhờ có những người xung quanh," một khía cạnh tích cực của cộng đồng.
### VNC ?
- VNC, viết tắt của "Virtual Network Computing", là một hệ thống được sử dụng để chia sẻ màn hình giữa các thiết bị khác nhau với mục đích điều khiển từ xa. Điều này cho phép người dùng từ xa có thể xem và điều khiển màn hình, bàn phím và chuột của một máy tính khác như thể họ đang ngồi trước máy tính đó.
- VNC hoạt động dựa trên mô hình client/server. Máy tính cần được cài đặt thành một máy chủ VNC, trong khi máy tính khác muốn điều khiển từ xa cần cài đặt một trình xem VNC, hoặc còn gọi là client. Khi hai thành phần này được kết nối, máy chủ VNC sẽ chuyển gửi hình ảnh màn hình từ xa đến trình xem VNC.
- Ngoài việc xem màn hình từ xa, VNC cũng cho phép người dùng điều khiển máy tính từ xa bằng cách sử dụng bàn phím và chuột của thiết bị điều khiển. Điều này mang lại khả năng kiểm soát đầy đủ các hoạt động trên máy tính từ xa sau khi được cấp phép từ máy tính đó.
- VNC được phát triển tại Cambridge vào cuối những năm 1990 bởi những người sáng lập của RealVNC và đã trở thành một công nghệ phổ biến trong việc truy cập và điều khiển máy tính từ xa.

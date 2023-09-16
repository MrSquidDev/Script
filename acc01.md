let array_mess = [
    "alo",
                " xin chào ",
                " hihi ",
                " Hôm nay live sớm thế chị ",
                " Nay Live TFT à ",
                " Hôm nay Linh xinh quá ",
                " tft Rank gì rồi em? ",
                " Mùa Này Mordekaiser đang mạnh lắm đấy ",
                " Bọn Bilgewater mạnh zl ",
                " Sắp lên vàng chưa Linh? ",
                " Mạnh vậy ",
                " Nhìn giống top 8 lắm ",
                " Chơi đội hình gì đây Linh ơi ",
                " Dual Không Linh ? ",
                " Thuê Linh trên Playerduo hôm vừa rồi, nói chuyện cute cực ",
                " Bài này không hay đâu ",
                " Ủa sao không chơi BilgeWater ấy, đang mạnh lắm ",
                " Kèo top 1 1 cái hôn ",
                " Tưởng Là Mai Linh song chưởng cơ mà ? ",
                " Ủa chị này xinh thế anh em ",
                " Mùa mới em không biết chơi, chị dạy em chơi với ",
                " Mấy con Bilge Water dame to vãi nồi ",
                " Tầm bao lâu thì lên Cao Thủ hả chị ? ",
                " Anh mod kênh này dẹp trai quá, anh có người yêu chưa ạ ? ",
                " Fan Mai Linh 200 năm ",
                " chị chơi Auto Chess đi chị ",
                " Chị Linh ơi em xin Info anh Mod với ạ, em yêu ảnh mất rồi ",
                " Hello anh em ",
                " Chị này đánh TFT hay vlz vậy ? ",
                " Ủa rồi TF đâu ? ",
                " Bài này bài gì đây chị gái ? ",
                " Trông giống out tóp lắm ",
                " Cuối cùng tôi cũng tìm ra người chơi TFT gà hơn tôi ",
                " Bài này con gì carry thế chị Linh ? ",
                " Bài yếu vậy ? ",
                " Anh em đá mini map ít thôi ",
                " Linh thú này trông đẹp vãi  ",
                " sao trông nó lại ntn ",
                " chưa bao giờ tôi thấy hiện tượng này xảy ra cả ",
                " Này được độ rồi ",
                " Game kỹ năng chơi bằng nhân phẩm ",
                " Đù, ghê vậy ? ",
                " TOP 8, TOP 8 TOP 8 ",
                " hôm nay chị được những top gì rồi ? ",
                " Trông con kia nó đấm kinh vãi ",
                " Game lừa rồi ",
                " đen quá ",
                " đồ không đẹp lắm nhỉ ",
                " Mùa này hay vl ae ạ ",
                " Vợ tôi đánh hay vl ae ạ ",
                " Hnay chị được mấy cái top rồi ",
                " CHỊ NÀY LÀ CHỊ MAI LINH TEAM ĐỤT PHẢI K AE ",
                " hôm nay mùng 1 chắc cúng rồi nên bài mới ntn",
                " :V :V :V ",
                " NOn",
                " Gặp nhà top 2 là cút",
                " đi chợ nhặt được BF thì ngon ",
                " Nước mắt Linh rơi trò chơi kết thúc ",
                " Đen thôi đỏ quên đi ",
                " Tôi hết cái để nói rồi, viết tạm linh tinh vào đây vậy ",
                " có con Linh thú mới ocela vl ",
                " spamer à ",
                " được mấy cái top1 rồi ",
                " e live lâu chưa  ",
                " c ơi đừng chơi game nữa chơi e đi  ",
                " ôi sao trên onlive có người xinh ntn mà k biết nhỉ ",
                " em bao nhiêu tuổi r ",
               
];


function shuffleArray(array) {
    for (let i = array.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        [array[i], array[j]] = [array[j], array[i]];
    }
}

shuffleArray(array_mess); 

let currentIndex = 0;

function sendNextMessage() {
    if (currentIndex < array_mess.length) {
        let mess = array_mess[currentIndex];
        document.getElementById('write_area').innerHTML = mess;
        document.getElementById('btn_send').click();
        currentIndex++;
    } else {
        // All messages have been sent, reset and shuffle the array again
        currentIndex = 0;
        shuffleArray(array_mess);
    }
}

setInterval(sendNextMessage, 100000); 

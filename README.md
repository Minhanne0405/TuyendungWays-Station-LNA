<!DOCTYPE html>
<html lang="vi">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Ứng Tuyển Ways Station</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f9f9f9;
      margin: 0;
      padding: 0;
    }
    header {
      background-color: #007bff;
      color: white;
      padding: 30px;
      text-align: center;
    }
    main {
      max-width: 800px;
      margin: 30px auto;
      padding: 30px;
      background: white;
      border-radius: 10px;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    h2 {
      color: #007bff;
      margin-top: 30px;
    }
    ul {
      padding-left: 20px;
    }
    input, select, textarea {
      width: 100%;
      padding: 10px;
      margin-top: 10px;
      margin-bottom: 20px;
      border: 1px solid #ccc;
      border-radius: 6px;
    }
    button {
      background-color: #007bff;
      color: white;
      padding: 12px 25px;
      border: none;
      border-radius: 6px;
      font-size: 16px;
      cursor: pointer;
    }
    .thanks {
      display: none;
      text-align: center;
      margin-top: 40px;
      color: #28a745;
      font-weight: bold;
      font-size: 18px;
    }
    footer {
      text-align: center;
      margin-top: 50px;
      padding: 20px;
      background-color: #eee;
    }
  </style>
</head>
<body>

<header>
  <h1>Ứng Tuyển Ways Station</h1>
</header>

<main>
  <section>
    <h2>Giới thiệu</h2>
    <p>Ways Station LNA là cựu nhân viên tự mở. Chúng tôi đang tìm kiếm những bạn trẻ năng động để cùng phát triển mô hình kinh doanh gồm net, bida, và phòng gym.</p>
  </section>

  <section>
    <h2>Vị trí tuyển dụng</h2>
    <ul>
      <li>Phục vụ net</li>
      <li>Phục vụ bida</li>
      <li>Thu ngân net bida</li>
      <li>Giữ xe</li>
      <li>Phục vụ gym</li>
      <li>Thu ngân gym</li>
    </ul>
  </section>

  <section>
    <h2>Form Ứng Tuyển</h2>
    <form id="applyForm" onsubmit="showThanks(event)">
      <input type="text" name="name" placeholder="Họ và tên" required />
      <input type="tel" name="phone" placeholder="Số điện thoại" required />
      
      <label for="position">Vị trí ứng tuyển</label>
      <select name="position" required>
        <option value="">-- Chọn vị trí --</option>
        <option>Phục vụ net</option>
        <option>Phục vụ bida</option>
        <option>Thu ngân net bida</option>
        <option>Giữ xe</option>
        <option>Phục vụ gym</option>
        <option>Thu ngân gym</option>
      </select>

      <label for="shift">Ca làm</label>
      <select name="shift" required>
        <option value="">-- Chọn ca làm --</option>
        <option>Full time</option>
        <option>12 tiếng</option>
      </select>

      <textarea name="note" placeholder="Ghi chú thêm (không bắt buộc)" rows="4"></textarea>

      <button type="submit">Gửi đơn ứng tuyển</button>
    </form>

    <div class="thanks" id="thankYouMsg">
      🎉 Cảm ơn bạn đã ứng tuyển, chúng tôi sẽ liên hệ lại!
    </div>
  </section>

  <footer>
    Liên hệ: <strong>0399013426</strong>
  </footer>
</main>

<script>
  function showThanks(event) {
    event.preventDefault();
    document.getElementById("applyForm").style.display = "none";
    document.getElementById("thankYouMsg").style.display = "block";
  }
</script>

</body>
</html>

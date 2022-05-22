<head>
    <table></table>
    <link rel="stylesheet" href="https://pyscript.net/alpha/pyscript.css" />
    <script defer src="https://pyscript.net/alpha/pyscript.js"></script>
</head>
<html>
<body>

    <p class="title-detail-api">
        เลือกรูปภาพผลไม้ ด้วยเทคนิค Deep Learning
    </p>
  
<form action="?=$_SERVER['PHP_SELF'];?>" method="POST" enctype="multipart/form-data">
    <input type="file" name="file" accept="image/png, image/gif, image/jpeg" onchange="renderFile(event)">
</form>

<!-- img HTML -->
<img id="preview"/>

<!-- JavaScript -->
<script>
  var renderFile = function(event) {
    var r = new FileReader();
    r.onload = function(){
      var preview = document.getElementById('preview');
      preview.src = r.result;
    };
    r.readAsDataURL(event.target.files[0]);
  };
</script>

<h1>
  <button type="button"
onclick="document.getElementById('test').innerHTML = Date()">
วิเคราะห์.</button>
<script>
  function showMessage() {
      document.getElementById("message").innerHTML = "สวัสดี JavaScript";
  }
</script>
</h1>

</body>
</html>

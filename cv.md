---
layout: page
image: /assets/img/logo.png
description: >
  cv
hide_description: true
redirect_from:
  - /download/
---

<style>
  .password-lock {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    padding: 40px;
    border-radius: 10px;
    text-align: center;
    color: white;
    margin: 20px 0;
  }
  
  .password-lock h2 {
    color: white;
    margin-bottom: 10px;
  }
  
  .password-lock input {
    padding: 10px;
    border: none;
    border-radius: 5px;
    width: 200px;
    margin-right: 10px;
    font-size: 16px;
  }
  
  .password-lock button {
    padding: 10px 20px;
    background: white;
    color: #667eea;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-weight: bold;
    font-size: 16px;
  }
  
  .password-lock button:hover {
    opacity: 0.9;
  }
  
  .error-msg {
    color: #ff6b6b;
    display: none;
    margin-top: 10px;
    font-size: 14px;
  }
  
  .protected-content {
    display: none;
  }
  
  .logout-link {
    text-align: center;
    margin-top: 20px;
  }
  
  .logout-link a {
    color: #667eea;
    cursor: pointer;
    text-decoration: underline;
  }
</style>

<div class="password-lock" id="lockBox">
  <h2>🔒 此页面已加密</h2>
  <p>请输入密码查看</p>
  <input type="password" id="pwd" placeholder="输入密码" onkeypress="if(event.key==='Enter') unlock()">
  <button onclick="unlock()">解锁</button>
  <div class="error-msg" id="error">密码错误</div>
</div>

<div class="protected-content" id="content" markdown="1">

# CV

可点击下载[PDF](/assets/Resume.pdf).

![Resume PDF](/assets/img/blog/resume.png){:.lead width="368" height="515" loading="lazy"}

<div class="logout-link">
  <a onclick="logout()">退出登录</a>
</div>

</div>

<script>
  // ⚠️ 改这里：设置你的密码
  const PASSWORD = "123456";
  
  function unlock() {
    const input = document.getElementById('pwd').value;
    if (input === PASSWORD) {
      document.getElementById('lockBox').style.display = 'none';
      document.getElementById('content').style.display = 'block';
      document.getElementById('error').style.display = 'none';
    } else {
      document.getElementById('error').style.display = 'block';
      document.getElementById('pwd').value = '';
    }
  }
  
  function logout() {
    document.getElementById('lockBox').style.display = 'block';
    document.getElementById('content').style.display = 'none';
    document.getElementById('pwd').value = '';
    document.getElementById('error').style.display = 'none';
  }
</script>
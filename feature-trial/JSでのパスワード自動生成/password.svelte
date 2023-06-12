<script>
  let password_base =
    "1234567890abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ";
  let password;
  function genPassword(length = 20) {
    let password = "";
    for (let i = 0; i < length; i++) {
      password += password_base.charAt(
        Math.floor(Math.random() * password_base.length)
      );
    }
    return password;
  }
</script>

<button on:click={genPassword}>パスワードを生成する</button>
<p>{password}</p>

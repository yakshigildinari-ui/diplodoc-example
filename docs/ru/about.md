# Начинаем работу с QR-Passport
Эта инструкция – ваш помощник для начала работы. Интерфейс системы будет выглядеть по-разному в зависимости от прав доступа. Подробнее о правах доступа см. [Пользователи](company/users.md#anchor).

{% note info %}

Все примеры в инструкции носят справочный характер. 

{% endnote %}

Для начала работы с QR-Passport войдите в систему по [ссылке](https://qrpassport.app/admin). Используйте для входа имя пользователя и пароль, которые были отправлены на вашу электронную почту.

<img src="" id="theme-image" alt="Регистрация">

<script>
// Ждем загрузки DOM
document.addEventListener('DOMContentLoaded', function() {
  const img = document.getElementById('theme-image');
  
  // Функция для определения темы
  function getCurrentTheme() {
    // Проверяем все возможные индикаторы темы
    if (document.body.getAttribute('data-theme') === 'dark') return 'dark';
    if (document.body.classList.contains('theme-dark')) return 'dark';
    if (document.body.classList.contains('yfm-theme-dark')) return 'dark';
    if (document.body.classList.contains('dd-theme-dark')) return 'dark';
    
    // Проверяем кнопку переключения темы
    const themeToggle = document.querySelector('[data-theme-toggle]');
    if (themeToggle && themeToggle.getAttribute('data-theme') === 'dark') return 'dark';
    
    return 'light';
  }
  
  // Устанавливаем картинку
  if (getCurrentTheme() === 'dark') {
    img.src = './_images/login_dark.png';
  } else {
    img.src = './_images/login.png';
  }
  
  console.log('Текущая тема:', getCurrentTheme());
  console.log('Классы body:', document.body.className);
  console.log('Атрибуты body:', document.body.attributes);
});
</script>
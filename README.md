1)Заходим на страницу товара и нажимаем Check stock, перехватываем POST запрос, в котором есть xml вставка.
2)Создаем внешнюю сущность xxe, указывающую на сайт http://169.254.169.254/.
3)Вместо productId выводим &xxe и получаем ответ "Invalid product ID: latest". Добавляем latest/ к адресу в xxe.
4)Отправляем запрос и получаем "Invalid product ID: meta-data". Добавляем meta-data/ к адресу. И т.д. В конечном счете будем иметь адрес 
http://169.254.169.254/latest/meta-data/iam/security-credentials/admin. Именно по этому адресу находится секретный ключ админа.

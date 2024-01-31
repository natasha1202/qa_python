# qa_python
##Список файлов:
main.py - содержит тестируемый класс BooksCollector
tests.py - класс, содержащий юнит-тесты, проверяющие класс BooksCollector
conftest.py - класс, содержащий фикстуры, используемые тестами для создания тестовых данных

##Список тестов:
*test_add_new_book_add_two_books* - добавление двух новых книг в список, позитивная проверка
*test_add_new_book_too_long_name* - добавление в список книги со слишком длинным названием, негативная проверка

*test_set_book_genre_to_one_existing_book* - установление поля "жанр" для книги из списка, позитивная проверка

*test_get_book_genre_existing_book* - проверка корректности возвращаемого жанра для книги, для которой жанр определен, 
позитивная проверка

*test_get_books_with_specific_genre_books_from_existing_dict* - тест проверяет корректность работы метода, 
выводящего список книг определенного жанра, при условии, что список книг корректно задан в виде словаря

*test_get_books_genre_books_from_existing_dict* - проверка корректности возвращаемого списка книг с жанрами,
список книг и жанры заданы

*test_get_books_for_children_exist_books_for_children_in_dict* - проверка, что из заданного списка книг корректно 
возвращается список книг для детей

*test_add_book_in_favorites_add_one_book_from_existing_dict* - проверка корректности добавления книги в избранное,
книга из заданного списка, позитивная проверка

*test_add_book_in_favorites_add_one_book_not_from_dict* - тест проверяет, что если книги нет в списке, 
то ее нельзя добавить в избранное, негативная проверка

*test_add_book_in_favorites_book_already_in_favorites* - проверка, что нельзя дважды добавить одну и ту же книгу в
избранное, негативная проверка

*test_delete_book_from_favorites_book_from_favorites* - проверка, что книга корректно удаляется из списка избранного,
книга существует в списке, позитивная проверка

*test_get_list_of_favorites_books_existing_favorite_list* - проверка, что корректно возвращается список список 
избранных книг, если список задан, позитивная проверка

##Команды для запуска тестов
###Запустить все тесты
pytest -v tests.py

###Запустить один тест по имени
python -m pytest -s tests.py -k test_add_new_book_add_two_books
pytest -v tests.py -k test_add_new_book_add_two_books


# Endpoints

 1. [GET] http://3.85.10.166/movie/list \
Lista filmes
 2. [GET] http://3.85.10.166/user/list \
 Lista usuários
 3. [GET] http://3.85.10.166/movie/list/ {user_id : int} \ 
 Lista usuário por id
 4. [GET] http://3.85.10.166/movie/search?query= {query : string} \
Procura filme por título
5. [GET] http://3.85.10.166/movie/actor?query= {query : string} \
Procura ator por nome
6. [GET] http://3.85.10.166/movie/actor/ {actor_id : int} \
Procura ator por tmdb id
7. [POST] http://3.85.10.166/user/create \
Cria usuário
Corpo da requisição

    ```
    email: string
    password: string
    ```
8. [POST] http://3.85.10.166/user/favorite/add \
Adiciona um filme favorito
Corpo da requisição
	```
	user_id : int
	title:  str
	description:  str
	bannerUrl:  str
	tmdb_id:  int
	```
9. [POST] http://3.85.10.166/movie/actor/favorite/add \
Adiciona um ator favorito
Corpo da requisição
	```
	name:  str
	bio:  str
	profileUrl:  str
	user_id:  int
	tmdb_actor_id:  int
	```
10. [DELETE] http://3.85.10.166/user/delete/{user_id : int} \
Deleta usuário

11. [DELETE] http://3.85.10.166/user/favorite/remove/{user_id : int}?title={movie_name : string} \ 
Deleta filme favorito

12. [DELETE] http://3.85.10.166/movie/actor/favorite/remove/{user_id : int}?name={actor_name : string} \
Deleta ator favorito

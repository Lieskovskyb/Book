1:test get products
http://172.17.0.2:8080/api/products
get

pm.test("Status code is 200", function () {
pm.response.to.have.status(200);
});


2:test get products id 3
http://172.17.0.2:8080/api/products/3


pm.test("Status code is 200", function () {
pm.response.to.have.status(200);
});

3:test put product id 3 
http://172.17.0.2:8080/api/products/3

"id": 3,
"title": "4cycle456",  na "title": "4cycle444"

pm.test("Status code is 200", function () {
pm.response.to.have.status(200);
});

4:test get produkcts id 3 
http://172.17.0.2:8080/api/products/3

pm.test("Status code is 200", function () {
pm.response.to.have.status(200);
});

5:test post products
http://172.17.0.2:8080/api/products

"title": "MACBOOK",
"keywords": "Apple",

pm.test("Status code is 201", function () {
pm.response.to.have.status(201);
});


6:test delete products
http://172.17.0.2:8080/api/products

"title": "MACBOOK",
"keywords": "Apple",

pm.test("Status code is 204", () => {
pm.response.to.have.status(204);
});

7:test get products id
http://172.17.0.2:8080/api/products/id MACBOOK Apple

pm.test("Status code is 404", () => {
pm.response.to.have.status(404);
});

Tento test som robil v postman a prešiel
pekný deň
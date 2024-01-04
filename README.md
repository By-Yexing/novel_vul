Novel framework JWT authentication vulnerability
novel is a learning novel project based on the latest Java technology stack Spring Boot 3 + Vue 3. In the novel, because the jwt key is fixed, an attacker can use the key to construct a malicious JWT Token, thus bypassing the authentication mechanism.
In the application.yml file, the default key for the jwt is stored
![490f840222c32a433e05245909c555e](https://github.com/By-Yexing/novel_vul/assets/107806521/e6bea3a2-4cc7-4004-8fa1-868927f94e46)
The entire jwt parsing process is as follows:
![36c9c8742a020ffa10a2a0e756bce31](https://github.com/By-Yexing/novel_vul/assets/107806521/8e396134-caca-48a1-a15d-3a7a8d6fc7ed)
![1704376057073](https://github.com/By-Yexing/novel_vul/assets/107806521/2c21c2b4-b957-4061-8cf9-d85a38a28f75)
So, we can use this default key to forge the authentication field, thus bypassing authentication
![72346763740b46f46ad4edd299c8748](https://github.com/By-Yexing/novel_vul/assets/107806521/e351450a-cd1c-46c0-9155-85875cb6c3be)
![image](https://github.com/By-Yexing/novel_vul/assets/107806521/955ea9c6-2811-4d3e-bad8-9ac14e229bfd)

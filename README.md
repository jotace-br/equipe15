# Equipe 15 do projeto de APS sobre o framework VRaptor

## Começando com o VRaptor

O VRaptor 4 entrega alta produtividade para sua aplicação WEB Java em cima do CDI. VRaptor é um framework MVC opensource com uma comunidade enorme de desenvolvedores e usuários.

### Pré-requisitos

O VRaptor 4 depende diretamente do CDI versão 1.1, portanto só funcionará nos servidores que suportem essa versão do CDI ou superior como CDI 1.2. Também é necessário possuir JDK 1.7 ou superior. Se for usar Java 8, não deixe de conferir [isso](http://www.vraptor.org/en/docs/dependencies-and-prerequisites/#jdk-8)

Os Servidores de Aplicações já testados e suportados são:

- Glassfish 4
- WildFly 8

E os Servlet Containers suportados são:

- Tomcat 7 (+ Weld 2.x jars)
- Jetty 8 and 9 (+ Weld 2.x jars)

Ao usar um Servlet Container como o Tomcat ou Jetty, é preciso adicionar os jars do Weld 2.x, além do seguinte listener em seu web.xml, para que seja possível ativar o CDI:

```
<listener>
    <listener-class>org.jboss.weld.environment.servlet.Listener</listener-class>
</listener>
```
E o arquivo beans.xml, que é opcional se você estiver usando um Application Server, que deve estar dentro do WEB-INF de sua aplicação:

```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://xmlns.jcp.org/xml/ns/javaee"
    xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
    xsi:schemaLocation="http://xmlns.jcp.org/xml/ns/javaee http://xmlns.jcp.org/xml/ns/javaee/beans_1_1.xsd"
    version="1.1" bean-discovery-mode="all">
</beans>
```

Algumas dependências podem variar se você usa um Application Server ou um Servlet Container. Pacotes da especificação, como o CDI ou Bean Validation, não são necessários quando você usa um Application Server.


### Instalação

Basta acessar [este link](http://www.vraptor.org/pt/download/), onde ele explicará passo a passo como instalar e usar.

Assim como, só basta também adicionar a dependência do VRaptor em seu *pom.xml*:
```
<dependency>
    <groupId>br.com.caelum</groupId>
    <artifactId>vraptor</artifactId>
    <version>4.2.0-RC5</version>
</dependency>
```

## Feito com

* [TEMPLATED](https://templated.co/) - Template usado no site.
* [MOTIVAÇÃO](https://www.youtube.com/channel/UC_l6dh0591UQlh7Mo3xCaig) - Nosso motivador principal
* [FORÇA DE VONTADE](https://www.youtube.com/channel/UCTbW3P2M9fftdFiQojD8t5Q) - Por ensinar de forma curta e grossa que estudar vale a pena

## Autores

* **Júlio César** - *Instrutor, Programador Front-End e Contribuidor do Projeto* - [jotace-br](https://github.com/jotace-br)
* **Gabriel Ferreira** - *Contribuidor do Projeto e Programador Back-End* - [gabriel2448](https://github.com/gabriel2448)
* **Bruno Henrique** - *Contribuidor do Projeto e Programador Back-End* - [brunohenriquem](https://github.com/brunohenriquem)

## Licença

Este projeto está sobre a licença Apache License 2.0 - veja em [LICENSE.md](LICENSE.md) para mais detalhes.

## Agradecimentos

* Obrigado ao [Leonardo Fernandes](https://github.com/leofernandesmo) pelo apoio e ajuda em todas as vezes que pedimos, sem pestanejar uma vez sequer.
* Agradecemos também ao [Glauber Ferreira](https://github.com/glauberferreira) por sempre tirar nossas dúvidas e nos ensinar aquilo que fora necessário para esse projeto.

> O trabalho em equipe é mais rico, forte e por isso capaz de alcançar as metas mais difíceis!

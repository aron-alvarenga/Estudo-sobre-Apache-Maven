# 📝 Estudo sobre Apache Maven 👨‍💻

Estudo sobre o gerenciamento de dependências e build com Apache Maven.

## ⚙️ Ferramentas

- Java v. 11.0.12
- Apache Maven v. 3.8.2
- IDE IntelliJ IDEA Community Edition 2021.2.2

## 🛠️ Comandos Apache Maven

- ### Criando projeto

**-DgroupId -** Agrupamento do projeto;<br />**-DartifactId -** Nome do projeto;<br />**-Darchetype -** Nome do template.

```java
mvn archetype:generate -DgroupId=com.aronalvarenga -DartifactId=quick-start-maven -Darchetype=maven-archetype-quickstart -DinteractiveMode=false
```

- ### Compilando projeto
```java
mvn compile
```
Antes da compilação, foi preciso adicionar ao arquivo POM o seguinte código:

```java
<dependencies>
...
</dependencies>
<build>
    <plugins>
        <plugin>
            <groupId>org.apache.maven.plugins</groupId>
            <artifactId>maven-compiler-plugin</artifactId>
            <configuration>
                <source>1.8</source>
                <target>1.8</target>
            </configuration>
        </plugin>
    </plugins>
</build>
```
- ### Testando projeto

```java
mvn test
```
- ### Empacotando(Criando o JAR) projeto

Após este comando, é criado um arquivo .jar na pasta target

```java
mvn package
```

- ### Limpando diretório de trabalho do projeto

Após este comando, a pasta target é deletada

```java
mvn clean
```

## 🔎 Pesquisar por...
**“Maven archetype list”** para procurar por templates de personalização e construção de projeto usando Maven. Na documentação ([https://maven.apache.org/archetypes/](https://maven.apache.org/archetypes/)), é possível encontrar algumas opções.

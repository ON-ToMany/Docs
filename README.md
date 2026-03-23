<h1 align="center">
  <img src="https://github.com/ON-ToMany.png" width="80" align="center">
  <font <font size="6">ONEtoMany</font>
</h1>



<p align="center">
Sistemas desenvolvidos para <b>- Projeto Integrador</b>
</p>


# 📚 ESCOPO DOS PROJETOS

<div align="center">
  
| PROJETO | MODELO |
|-----|------------|
| 🚲 IonGuard |  Seguradora E-Bike  |
| 🥗 Friendly Food | App Delivery |
| 🌱 GreenTech | Sistema CRM |

</div>


# 👥 GRUPO 01

## Desenvolvedores 👨‍💻

- Álvaro Maximiano  
- Breno Nunes  
- José Rodrigues  
- Mayara Gonçalves  
- Maria Eduarda Gomes  
- Márcia Telles Fogaça  
- Mateus Santos Vieira  

---

# 3️ Descrição do Projeto

A **IonGuard** nasceu para proteger quem escolheu o futuro da mobilidade.

Especializada em seguros para **bicicletas elétricas (E-Bikes)**, oferecemos cobertura completa contra:

- 🔐 Roubo
- 🚨 Furto
- 🔧 Reparos de chassis
- 🔋 Problemas em baterias

Nosso objetivo é garantir que sua **bicicleta elétrica esteja sempre pronta para o próximo trajeto**.

---

O **Friendly Food** nasceu para combater a insegurança alimentar através da tecnologia. Nossa plataforma gerencia doações de alimentos, garantindo
Especializada em seguros para **bicicletas elétricas (E-Bikes)**, oferecemos cobertura completa contra:

- 🍎 Classificação de itens (Perecíveis)
- 📦 Controle rigoroso de estoque
- ⏳ Monitoramento de prazos de validade
- 🤝 Conexão direta com instituições receptoras

Aplicação para gestão e conexão entre **doadores e entidades beneficiadas.**

---

# 🛠 4 Tecnologias Utilizadas
<div align="center">
  
| Item | Tecnologia |
|-----|------------|
| 🖥 Servidor | Node.js |
| 💻 Linguagem | Typescript |
| ⚙ Framework | NestJS |
| 🗄 ORM | TypeORM |
| 🗃 Banco de Dados | MySQL 

</div>

# 📊 5 Diagrama Entidade-Relacionamento

<p align="center">
<img width="520" src="https://github.com/user-attachments/assets/438f3459-fb71-41ad-aa6c-3a9446c0a1ed">
</p>

<p align="center">
<img width="520" src="https://github.com/user-attachments/assets/438f3459-fb71-41ad-aa6c-3a9446c0a1ed">
</p>

---

# 🗄 6 Descrição das Tabelas e seus Atributos

**Banco de Dados:**  
- `db_seguradora_ion_guard` 
- `db_Delivery`

**SGBD:**  MySQL

## 📋 Tabela App IonGuard: `tb_apolice`
<div align="center">
  
| Atributo | Tipo | Descrição | Chave |
|---------|------|-----------|------|
| id | BIGINT | Suporta grande quantidade de cadastros de apólices | PK |
| tipo_seguro | VARCHAR(255) | Categoria do seguro contratado | NN |
| valor_plano | DECIMAL(5,2) | Valor do plano escolhido pelo cliente | NN |
| data_inicio | DATE | Data de início da vigência do plano | NN |
| data_fim | DATE | Data final da vigência do plano | NN |
| status_plano | VARCHAR(255) | Status do plano (Adimplente, Cancelado, Inadimplente) | NN |

</div>

## 📋 Tabela FriendlyFood: `tb_produto`
<div align="center">
  
| Atributo | Tipo | Descrição | Chave |
|---------|------|-----------|------|
| id | BIGINT | Identificador único do produto, gerado automaticamente pelo banco de dados | PK |
| nome | VARCHAR(255) | Nome do produto | NN |
| energia Kcal | DECIMAL(10,2) | Valor energético do produto por 100g, em quilocalorias. Usado como ponto negativo no cálculo do NutriScore| NN |
| gordura_saturada | DECIMAL(10,2) | Quantidade de gordura saturada por 100g. Ponto negativo no cálculo do NutriScore por impacto cardiovascular | NN |
| acucares | DECIMAL(10,2) |  Quantidade de açúcares totais por 100g. Ponto negativo no cálculo do NutriScore | NN |
| sodio_mg | DECIMAL(10,2) | Quantidade de sódio em miligramas por 100g. Ponto negativo no cálculo do NutriScore | NN |
| fibras | DECIMAL(10,2) | Quantidade de fibras alimentares por 100g. Ponto positivo no cálculo do NutriScore | NN |
| proteinas | DECIMAL(10,2) | Quantidade de proteínas por 100g. Ponto positivo no cálculo do NutriScore | NN |
| perc_frutas_vegetais | DECIMAL(10,2) | Percentual de frutas, legumes e vegetais no produto (0 a 100). Ponto positivo no NutriScore; padrão 0 quando não aplicável | NN |
| nutre_score | VARCHAR(255) | Resultado do cálculo NutriScore: A (melhor) a E (pior). Calculado automaticamente pelo service com base nos atributos nutricionais | NN |
| categoria_id | BIGINT | Referência à categoria à qual este produto pertence (ManyToOne) | FK |
| usuario_id | BIGINT | Referência ao usuário (doador) responsável por este produto (ManyToOne) | FK |

</div>

## 📋 Tabela FriendlyFood: `tb_categoria`
<div align="center">

| Atributo | Tipo | Descrição | Chave |
|---------|------|-----------|------|
|id |BIGINT|identificador único da categoria, gerado automaticamente pelo banco de dados.|PK |
|tipo|VARCHAR(255)|Tipo da categoria|NN|
|targetAudience|VARCHAR(255)|Público-alvo da categoria (ex: idosos, crianças, famílias em situação de vulnerabilidade).|NN|
|produto_id|BIGINT|Referência aos produtos pertencentes a esta categoria. Uma categoria pode conter vários produtos (OneToMany)|FK|
</div>

## 📋 Tabela FriendlyFood: `tb_usuario`
<div align="center">

| Atributo | Tipo | Descrição | Chave |
|---------|------|-----------|------|
|id|BIGINT|Identificador único do usuário, gerado automaticamente pelo banco de dados.|PK|
|nome|VARCHAR(255)|Nome do usuário|NN|
|usuario|VARCHAR(255)|Email do usuário|NN|
|senha|VARCHAR(255)|Senha do usuário|NN|
|produto_id|BIGINT|Produtos pertencentes ao usuário|FK|

</div>

# 🧩 7 Descrição das Entidades e seus Atributos

## Classe IonGuard: `apolice`
<div align="center">
  
| Atributo | Tipo | Descrição |
|---------|------|-----------|
| id | number | Identificador único da apólice |
| tipo_seguro | string | Tipo de seguro contratado |
| valor_plano | number | Valor do plano |
| data_inicio | date | Data de início da vigência |
| data_fim | date | Data final da vigência |
| status_plano | string | Status atual do plano (Ativo, Cancelado, Inadimplente) | 

</div>

## Classe FriendlyFood: `categoria`

<div align="center">
  
| Atributo | Tipo | Descrição |
|---------|------|-----------|
| id | number |Identificador único da categoria, mapeado como chave primária com auto-incremento via @PrimaryGeneratedColumn()|
| tipo | string | Tipo de doação. Mapeado com @Column() e armazenado como VARCHAR no banco |
| targetAudience | string | Público-alvo da categoria. Mapeado com @Column(). Permite filtrar doações por grupo beneficiário|
| produto | produto[] | Lista de produtos vinculados à categoria. Mapeado com @OneToMany(() => Produto, produto => produto.categoria) 

</div>

## Classe FriendlyFood: `produto`

<div align="center">

| Atributo | Tipo | Descrição |
|---------|------|-----------|
|id|number|Identificador único da categoria, mapeado como chave primária com auto-incremento via @PrimaryGeneratedColumn().|
|nome|string|Nome do produto. Mapeado com @Column().|
|energia_kcal|number|Calorias por 100g. Mapeado com @Column('decimal'). Ponto negativo do NutriScore.|
|gordura_saturada|number|Gordura saturada por 100g. Mapeado com @Column('decimal'). Ponto negativo do NutriScore.|
|acucares|number|Açúcares por 100g. Mapeado com @Column('decimal'). Ponto negativo do NutriScore.|
|sodio_mg|number|Sódio em mg por 100g. Mapeado com @Column('decimal'). Ponto negativo do NutriScore.|
|fibras|number|Fibras por 100g. Mapeado com @Column('decimal'). Ponto positivo do NutriScore.|
|proteinas|number|Proteínas por 100g. Mapeado com @Column('decimal'). Ponto positivo do NutriScore.|
|perc_frutas_veg|number|% de frutas/vegetais (0-100). Mapeado com @Column('decimal', { default: 0 }). Ponto positivo do NutriScore.|
|nutri_score|string|Letra A-E gerada pelo cálculo NutriScore. Mapeado com @Column(). Calculado no service antes de persistir.|
|categoria|Categoria|Categoria do produto. Mapeado com @ManyToOne(() => Categoria, categoria => categoria.produto).|
|usuario|Usuario|Usuário responsável pelo produto. Mapeado com @ManyToOne(() => Usuario, usuario => usuario.produto) 

</div>

## Classe FriendlyFood: `usuario`

<div align="center">
  
| Atributo | Tipo | Descrição |
|---------|------|-----------|
| id | number | Identificador único da categoria, mapeado como chave primária com auto-incremento via @PrimaryGeneratedColumn() |
| nome | string | Nome do usuário. Mapeado com @Column() |
| usuario | string | Nome do usuário. Mapeado com @Column(). |
| senha | string | Senha criptografada. Mapeado com @Column() |
| produto | Produto[] | Lista de produtos do usuário. Mapeado com @OneToMany(() => Produto, produto => produto.usuario) |
</div



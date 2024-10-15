Três etapas da modelagem de dados:

1. Modelo Conceitual
2. Modelo Lógico
3. Modelo Físico

Como converter um Modelo Conceitual em um Modelo Lógico?

Chave estrangeira: uma ponte entre entidades

```csharp
class Aluno 
{
	public long MatriculaId { get; set; }
	public long Id { get; set; }
}
```

## Modelo Lógico

Estabelecemos quais campos são necessários para estabelecer o vínculo entre entidades (chave estrangeira).

| Aluno          |
| -------------- |
| Matricula      |
| Nome           |
| Código Matéria |

| Matéria |
| ------- |
| Código  |
| Nome    |

## Algebra Relacional
Operações entre conjuntos (assim como na matemática) que permitem a execução de operações entre estes conjuntos de entidades

- Seleção
- Projeção
- União
- Diferença
- Intersecção
- Produto Cartesiano
- Junção
- Operadores
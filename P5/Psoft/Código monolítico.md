---

tipo: anotacao

periodo: 5

disciplina: Psoft

trilhas:

- Engenharia de Software

---
## O que é:

**Código monolítico**, no contexto do [[Bridge]], é uma base de código em que partes diferentes estão tão misturadas e dependentes umas das outras que mudar uma exige entender ou alterar várias outras. Não é sinônimo de aplicação monolítica: uma aplicação pode ser um único sistema e ainda ter código bem organizado em módulos.

## Problema:

Imagine uma aplicação com interfaces para usuários e administradores, cada uma com condições espalhadas pelo código para lidar com Windows, Linux e macOS. Adicionar uma plataforma pode exigir mudanças em várias telas; uma alteração em uma tela pode afetar outras combinações. Isso dificulta a manutenção e aumenta o risco de erros.

## Como evitar:

Separe responsabilidades e defina como as partes se comunicam. No [[Bridge]], a interface cuida da interação com o usuário e delega operações específicas da plataforma a uma implementação. Assim, uma nova plataforma não exige reescrever cada interface.

Uma [[Classe monolítica|classe monolítica]] concentra responsabilidades em **uma classe**; código monolítico descreve o acoplamento de **uma base de código** ou de uma parte maior dela.

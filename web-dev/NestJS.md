# Nest JS

## COMANDOS NEST CLI

Obs.:
- A execução de comandos Nest CLI depende da devDependencie "@nestjs/cli".
- Pode haver problemas em executar pelo powershell; Se ocorrer, usar o cmd.

Para gerar arquivos baseados em esquemas:
   <code>  nest generate <esquema> <nome> [options] </code>
  OU nest g <schema> <nome> [options]
Ex.:
nest g resource teste //já cria module, controller e service

Documentação: https://docs.nestjs.com/cli/usages

<br><br><br>

## DOCUMENTAÇÃO COM SWAGGER

### Para agrupar APIs no Swagger:
no controller, usar @ApiTags antes do @Controller
Ex.:
@ApiTags('nome')
@Controller('nome')

### Para exibir informações adicionais da API no Swagger (resumo, descrição...):
no controller, usar @ApiOperation() depois do método
Ex:
@Get('adm/ee')
@ApiOperation({ 
summary: 'Meu resumo...',
description: `Minha descrição...`
})

O plugin adiciona o seguinte exemplo de trecho de código a stack CDK:

```typescript
  const snsSimpleAction = new stkHandler.SnsSimpleAction(stack, 'actionX', {
    actionBasedRule: handlerCore.successRule,
    lambdaName: 'actionLambda',
  });
  handlerCore.addAction(snsSimpleAction);
```

O qual também gera uma lambda no diretório `src` das lambdas no subdiretório padrão `actions` com o nome da lambda informado na aplicação do plugin ex:

```dir
src/actions/actionLambda.ts
```


<h1 align=center> Componentes do fluxo de github </h1>
![2-branching](https://github.com/user-attachments/assets/d0cb2f28-752d-430f-bb9b-3ff45acd87aa)


### Branches

Os branches são uma parte essencial para a experiência do GitHub, pois são onde podemos fazer alterações sem afetar todo o projeto em que estamos trabalhando.
Seu branch é um lugar seguro para experimentar novos recursos ou correções. Se você cometer um erro, poderá reverter suas alterações ou efetuar push das alterações adicionais para corrigir o erro. Suas alterações não serão atualizadas no branch padrão até que você mescle seu branch.

### Commits

uma alteração em um ou mais arquivos de um branch. Toda vez que uma confirmação é criada, é atribuído a ela uma ID exclusiva, que é rastreada juntamente com o tempo e o colaborador. Os commits fornecem uma trilha de auditoria clara para qualquer pessoa que revise o histórico de um arquivo ou item vinculado, como um problema ou uma solicitação de pull.

### Solicitação de Pull (pull request)

Uma solicitação de pull é o mecanismo usado para sinalizar que as confirmações de um branch estão prontas para serem mescladas em outro branch.

O membro da equipe que envia a solicitação pull pede a um ou mais revisores para verificar o código e aprovar a mesclagem. Esses revisores têm a oportunidade de comentar sobre as alterações, adicionar as próprias ou usar a solicitação de pull para uma discussão adicional.

Depois que as alterações forem aprovadas (se necessário), o branch de origem da solicitação de pull (o branch de comparação) será mesclado ao branch base.



O fluxo do GitHub pode ser definido como um fluxo de trabalho leve que permite a experimentação segura. Você pode testar novas ideias e colaboração com sua equipe usando branching, solicitações de pull e mesclagens. Percorrendo o fluxo do GitHub e os respectivos componentes:

1. Comece criando uma ramificação para que as alterações, recursos e correções que você criar não afetem a ramificação principal.
2.Em seguida, faça suas alterações. Recomendamos implantar alterações no branch do recurso antes de mesclar no branch principal. Fazer isso garante que as alterações sejam válidas em um ambiente de produção.
3. Agora, crie uma solicitação de pull para pedir feedback aos colaboradores. A revisão de pull request é tão valiosa que alguns repositórios exigem uma revisão de aprovação antes que os pull requests possam ser mesclados.
4. Em seguida, revise e implemente o feedback dos seus colaboradores.
5.Quando você se sentir satisfeito com suas alterações, é hora de aprovar sua solicitação de pull e mesclá-la ao branch principal.
6. Por fim, você pode excluir sua ramificação. Excluir sua ramificação sinaliza que seu trabalho nela foi concluído e evita que você ou outras pessoas usem ramificações antigas acidentalmente.
Pronto, você passou por um ciclo de fluxo do GitHub!

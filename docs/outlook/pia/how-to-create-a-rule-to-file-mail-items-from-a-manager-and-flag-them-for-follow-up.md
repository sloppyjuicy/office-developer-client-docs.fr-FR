---
title: Création d’une règle pour classer les éléments de courrier provenant d’un manager et les marquer pour le suivi
TOCTitle: Create a rule to file mail items from a manager and flag them for follow-up
ms:assetid: c50578c2-15de-4d5f-87d9-d6162034f083
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424477(v=office.15)
ms:contentKeyID: 55119880
ms.date: 07/24/2014
mtps_version: v=office.15
ms.openlocfilehash: 2fc6f5fe60b2f643590e8f7545804cf6d8a4c11c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25405986"
---
# <a name="create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up"></a>Création d’une règle pour classer les éléments de courrier provenant d’un manager et les marquer pour le suivi

Cet exemple montre comment configurer une règle pour classer les éléments de courrier provenant de l’utilisateur et les marquer pour assurer leur suivi.

## <a name="example"></a>Exemple

> [!NOTE] 
> L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).

Les règles d'Outlook peuvent fonctionner côté serveur ou côté client, selon le type de compte et de règle. Vous pouvez implémenter des règles de nombreuses façons différentes pour appliquer vos propres schémas organisationnels lorsque vous organisez des éléments dans votre boîte aux lettres. Par exemple, vous pouvez créer une hiérarchie de sous-dossiers qui organise le courrier non lu et le courrier lu selon le domaine de l'objet. Vous pouvez aussi créer une hiérarchie de sous-dossiers qui correspond à l'expéditeur du message. Vous pouvez également catégoriser votre courrier, puis utiliser des dossiers de recherche pour agréger le courrier par catégorie.

Le modèle objet **Rules**, qui comprend un objet [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) représentant une règle dans Outlook, vous permet de créer des règles par programmation pour appliquer un certain schéma organisationnel, de créer une règle spécifique à votre solution ou de vous assurer que certaines règles sont déployées auprès d'un groupe d'utilisateurs. À l'aide du modèle objet **Rules**, vous pouvez ajouter, modifier et supprimer des règles par programmation. À l'aide de la collection [Rules](https://msdn.microsoft.com/library/bb622788\(v=office.15\)) et de l'objet **Rule**, vous pouvez aussi accéder à, ajouter et supprimer des règles définies pour une session. 

Un objet **Rule** a une propriété [RuleType](https://msdn.microsoft.com/library/bb645613\(v=office.15\)) qui indique si la règle est une règle d'envoi ou de réception. Lorsqu'une règle est créée, la propriété **RuleType** est spécifiée et ne peut pas être modifiée sans supprimer puis recréer la règle avec une propriété **RuleType** différente. Les objets [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) et [RuleCondition](https://msdn.microsoft.com/library/bb612469\(v=office.15\)) , les objets de leurs collections et les objets d'action et de condition dérivés sont également utilisés pour une prise en charge plus avancée de la modification des actions de règle et des conditions de règle.

Le modèle objet **Rules** ne prend pas en charge toutes les règles que vous pouvez créer à l'aide de l'Assistant Règles et alertes dans l'interface utilisateur d'Outlook, mais il prend en charge les actions et les conditions de règles les plus fréquemment utilisées. Toutes les règles créées à l'aide de l'Assistant Règles et alertes qui sont appliquées à des messages, qui incluent des éléments de courrier, des demandes de réunion, des demandes de tâche, des documents, des accusés de réception, des accusés de lecture, des réponses au vote et des notifications d'absence du bureau, peuvent aussi être créées par programmation.

Une règle peut s’exécuter sur le serveur Exchange ou sur le client Outlook, à condition que la boîte aux lettres de l’utilisateur actuel soit hébergée sur un serveur Exchange. La propriété [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) de l'objet **Rule** retourne **true** pour indiquer que la règle s'exécute sur un client, et Outlook doit être en cours d'exécution pour que la règle s'exécute. Si la règle s'exécute sur le serveur, Outlook ne doit pas être en cours d'exécution pour que les conditions de règle soient évaluées et que les actions de règle soient effectuées.

> [!NOTE]
> Il n'existe pas de collection distincte représentant les conditions d'exception des règles. Utilisez la propriété [Exceptions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._rule.exceptions?view=outlook-pia) de l'objet **Rule** pour obtenir une collection [RuleConditions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.ruleconditions?view=outlook-pia) qui représente les conditions d'exception des règles.

Pour créer des règles via le modèle objet Outlook, procédez selon les étapes suivantes :

1.  Obtenez la collection **Rules** auprès de la propriété [DefaultStore](https://msdn.microsoft.com/library/bb623164\(v=office.15\)) de l'objet [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) en appelant la méthode [GetRules()](https://msdn.microsoft.com/library/bb609979\(v=office.15\)) sur l'objet [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) par défaut. Utilisez un bloc **try…catch** pour prendre en compte le fait que le client est hors connexion ou déconnecté du serveur Exchange. Ceci empêche Outlook de générer une erreur.

2.  Appelez la méthode [Create(String, OlRuleType)](https://msdn.microsoft.com/library/bb643857\(v=office.15\)) sur l’objet **Rules** pour créer une variable d’instance ou un objet **Rule**, en spécifiant les paramètres Name et [OlRuleType](https://msdn.microsoft.com/library/bb645776\(v=office.15\)).

3.  Utilisez les collections [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) et [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) pour permettre les actions, les conditions et les exceptions sur l'objet **Rule**. Notez que toute condition activée dans la collection **RuleConditions**, retournée par la propriété [Exceptions](https://msdn.microsoft.com/library/bb609880\(v=office.15\)) , est traitée en tant que condition d'exception de règle, et que des actions ou des conditions personnalisées intégrées supplémentaires ne peuvent pas être ajoutées à la collection.

4.  Définissez la propriété [Enabled](https://msdn.microsoft.com/library/bb609147\(v=office.15\)) à **true** pour que toute action, condition ou exception de règle donnée soit opérationnelle. Certaines actions ou conditions, telles que la propriété [Folder](https://msdn.microsoft.com/library/bb646755\(v=office.15\)) , requièrent la définition de propriétés supplémentaires sur l'action ou la condition pour enregistrer l'objet **Rule** sans erreur.

5.  Enfin, appelez la méthode [Save(Object)](https://msdn.microsoft.com/library/bb610738\(v=office.15\)) sur la collection **Rules** pour enregistrer les règles créées ou modifiées. Placez la méthode **Save** dans un bloc **try…catch** pour gérer les exceptions.

Dans l’exemple de code suivant, CreateManagerRule implémente les étapes précédemment décrites. CreateManagerRule vérifie d’abord si la propriété [CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\)) représente un objet [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)), indiquant si l’utilisateur actuel est un utilisateur Exchange. Si c’est le cas, CreateManagerRule obtient le manager de l’utilisateur actuel en appelant la méthode [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) sur l’objet **ExchangeUser** de la propriété **CurrentUser** de l’objet **NameSpace**. Une règle de réception est ensuite créée pour déplacer les messages reçus dans un sous-dossier de la Boîte de réception selon les conditions suivantes :

- Le message provient du manager de l’utilisateur.

- Le destinataire est indiqué sur la ligne **À :** du message.

- Le message n’est pas une demande de réunion ou une mise à jour.

Enfin, le message est marqué pour un suivi le jour même. CreateManagerRule montre également une gestion appropriée des erreurs pour les conditions susceptibles de générer une exception, par exemple dans le cas où l’utilisateur est hors connexion ou déconnecté en mode Exchange mis en cache. 

Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**. L'instruction **d’utilisation** ne doit pas se produire juste avant les fonctions de l'exemple de code, mais doit être ajoutée avant la déclaration publique. La ligne de code suivante montre comment effectuer l’importation et la tâche dans C\#.

```csharp
using Outlook = Microsoft.Office.Interop.Outlook;
```


```csharp
private void CreateManagerRule()
{
    Outlook.ExchangeUser manager;
    Outlook.Folder managerFolder;
    Outlook.AddressEntry currentUser =
        Application.Session.CurrentUser.AddressEntry;
    if (currentUser.Type == "EX")
    {
        try
        {
            manager = currentUser.
                GetExchangeUser().GetExchangeUserManager();
        }
        catch
        {
            Debug.WriteLine("Could not obtain user's manager.");
            return;
        }
        Outlook.Rules rules;
        try
        {
            rules = Application.Session.DefaultStore.GetRules();
        }
        catch
        {
            Debug.WriteLine("Could not obtain rules collection.");
            return;
        }
        if (manager != null)
        {
            string displayName = manager.Name;
            Outlook.Folders folders =
                Application.Session.GetDefaultFolder(
                Outlook.OlDefaultFolders.olFolderInbox).Folders;
            try
            {
                managerFolder =
                    folders[displayName] as Outlook.Folder;
            }
            catch
            {
                managerFolder =
                    folders.Add(displayName, Type.Missing)
                    as Outlook.Folder;
            }
            Outlook.Rule rule = rules.Create(displayName,
                Outlook.OlRuleType.olRuleReceive);

            // Rule conditions
            // From condition
            rule.Conditions.From.Recipients.Add(
                manager.PrimarySmtpAddress);
            rule.Conditions.From.Recipients.ResolveAll();
            rule.Conditions.From.Enabled = true;

            // Sent only to me
            rule.Conditions.ToMe.Enabled = true;

            // Rule exceptions
            // Meeting invite or update
            rule.Exceptions.MeetingInviteOrUpdate.Enabled = true;

            // Rule actions
            // MarkAsTask action
            rule.Actions.MarkAsTask.MarkInterval =
                Outlook.OlMarkInterval.olMarkToday;
            rule.Actions.MarkAsTask.FlagTo = "Follow-up";
            rule.Actions.MarkAsTask.Enabled = true;

            // MoveToFolder action
            rule.Actions.MoveToFolder.Folder = managerFolder;
            rule.Actions.MoveToFolder.Enabled = true;
            try
            {
                rules.Save(true);
            }
            catch (Exception ex)
            {
                Debug.WriteLine(ex.Message);
            }
        }
    }
}
```

## <a name="see-also"></a>Voir aussi

- [Règles](rules.md)


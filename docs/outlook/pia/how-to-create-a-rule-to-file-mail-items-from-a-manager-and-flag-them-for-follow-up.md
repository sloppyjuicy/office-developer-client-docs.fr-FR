---
title: Création d’une règle pour classer les éléments de courrier provenant d’un manager et les marquer pour le suivi
TOCTitle: Create a rule to file mail items from a manager and flag them for follow-up
ms:assetid: c50578c2-15de-4d5f-87d9-d6162034f083
ms:mtpsurl: https://msdn.microsoft.com/library/Ff424477(v=office.15)
ms:contentKeyID: 55119880
ms.date: 07/24/2014
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: dba46c851050c3f948ec829ae2340e0492ca135f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360402"
---
# <a name="create-a-rule-to-file-mail-items-from-a-manager-and-flag-them-for-follow-up"></a><span data-ttu-id="c01fe-102">Création d’une règle pour classer les éléments de courrier provenant d’un manager et les marquer pour le suivi</span><span class="sxs-lookup"><span data-stu-id="c01fe-102">Create a rule to file mail items from a manager and flag them for follow-up</span></span>

<span data-ttu-id="c01fe-103">Cet exemple montre comment configurer une règle pour classer les éléments de courrier provenant de l’utilisateur et les marquer pour assurer leur suivi.</span><span class="sxs-lookup"><span data-stu-id="c01fe-103">This example shows how to set up a rule to file mail items from the user’s manager and flag them for follow up.</span></span>

## <a name="example"></a><span data-ttu-id="c01fe-104">Exemple</span><span class="sxs-lookup"><span data-stu-id="c01fe-104">Example</span></span>

> [!NOTE] 
> <span data-ttu-id="c01fe-105">L’exemple de code suivant est un extrait de [programmation d’Applications pour Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span><span class="sxs-lookup"><span data-stu-id="c01fe-105">The following code example is an excerpt from [Programming Applications for Microsoft Office Outlook 2007](https://www.amazon.com/gp/product/0735622493?ie=UTF8&tag=msmsdn-20&linkCode=as2&camp=1789&creative=9325&creativeASIN=0735622493).</span></span>

<span data-ttu-id="c01fe-p101">Les règles d'Outlook peuvent fonctionner côté serveur ou côté client, selon le type de compte et de règle. Vous pouvez implémenter des règles de nombreuses façons différentes pour appliquer vos propres schémas organisationnels lorsque vous organisez des éléments dans votre boîte aux lettres. Par exemple, vous pouvez créer une hiérarchie de sous-dossiers qui organise le courrier non lu et le courrier lu selon le domaine de l'objet. Vous pouvez aussi créer une hiérarchie de sous-dossiers qui correspond à l'expéditeur du message. Vous pouvez également catégoriser votre courrier, puis utiliser des dossiers de recherche pour agréger le courrier par catégorie.</span><span class="sxs-lookup"><span data-stu-id="c01fe-p101">Outlook rules can operate either server-side or client-side, depending on the type of account and rule. There are many ways you can implement rules to enforce your own organizational schemes when you organize items in your mailbox. For example, you can create a subfolder hierarchy that organizes unread mail and read mail by subject area. Or, you can create a subfolder hierarchy that corresponds to the sender of the message. You can also categorize your mail and then use search folders to aggregate the mail by category.</span></span>

<span data-ttu-id="c01fe-111">Le modèle objet **Rules**, qui comprend un objet [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) représentant une règle dans Outlook, vous permet de créer des règles par programmation pour appliquer un certain schéma organisationnel, de créer une règle spécifique à votre solution ou de vous assurer que certaines règles sont déployées auprès d'un groupe d'utilisateurs.</span><span class="sxs-lookup"><span data-stu-id="c01fe-111">The **Rules** object model, which includes a [Rule](https://msdn.microsoft.com/library/bb647152\(v=office.15\)) object that represents a rule in Outlook, allows you to create rules programmatically to enforce a certain organizational scheme, create a specific rule that is unique to your solution, or ensure that certain rules are deployed to a group of users.</span></span> <span data-ttu-id="c01fe-112">À l'aide du modèle objet **Rules**, vous pouvez ajouter, modifier et supprimer des règles par programmation.</span><span class="sxs-lookup"><span data-stu-id="c01fe-112">By using the **Rules** object model, you can programmatically add, edit, and delete rules.</span></span> <span data-ttu-id="c01fe-113">À l'aide de la collection [Rules](https://msdn.microsoft.com/library/bb622788\(v=office.15\)) et de l'objet **Rule**, vous pouvez aussi accéder à, ajouter et supprimer des règles définies pour une session.</span><span class="sxs-lookup"><span data-stu-id="c01fe-113">By using the [Rules](https://msdn.microsoft.com/library/bb622788\(v=office.15\)) collection and the **Rule** object, you can also access, add, and delete rules defined for a session.</span></span> 

<span data-ttu-id="c01fe-114">Un objet **Rule** a une propriété [RuleType](https://msdn.microsoft.com/library/bb645613\(v=office.15\)) qui indique si la règle est une règle d'envoi ou de réception.</span><span class="sxs-lookup"><span data-stu-id="c01fe-114">A **Rule** object has a [RuleType](https://msdn.microsoft.com/library/bb645613\(v=office.15\)) property that indicates whether the rule is a send or receive rule.</span></span> <span data-ttu-id="c01fe-115">Lorsqu'une règle est créée, la propriété **RuleType** est spécifiée et ne peut pas être modifiée sans supprimer puis recréer la règle avec une propriété **RuleType** différente.</span><span class="sxs-lookup"><span data-stu-id="c01fe-115">When a rule is created, the **RuleType** property is specified, and cannot be changed without deleting and re-creating the rule with a different **RuleType** property.</span></span> <span data-ttu-id="c01fe-116">Les objets [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) et [RuleCondition](https://msdn.microsoft.com/library/bb612469\(v=office.15\)) , les objets de leurs collections et les objets d'action et de condition dérivés sont également utilisés pour une prise en charge plus avancée de la modification des actions de règle et des conditions de règle.</span><span class="sxs-lookup"><span data-stu-id="c01fe-116">The [RuleAction](https://msdn.microsoft.com/library/bb644297\(v=office.15\)) and [RuleCondition](https://msdn.microsoft.com/library/bb612469\(v=office.15\)) objects, their collection objects, and derived action and condition objects are also used to further support editing rule actions and rule conditions.</span></span>

<span data-ttu-id="c01fe-p104">Le modèle objet **Rules** ne prend pas en charge toutes les règles que vous pouvez créer à l'aide de l'Assistant Règles et alertes dans l'interface utilisateur d'Outlook, mais il prend en charge les actions et les conditions de règles les plus fréquemment utilisées. Toutes les règles créées à l'aide de l'Assistant Règles et alertes qui sont appliquées à des messages, qui incluent des éléments de courrier, des demandes de réunion, des demandes de tâche, des documents, des accusés de réception, des accusés de lecture, des réponses au vote et des notifications d'absence du bureau, peuvent aussi être créées par programmation.</span><span class="sxs-lookup"><span data-stu-id="c01fe-p104">The **Rules** object model does not support all rules that you can create by using the Rules and Alert Wizard in the Outlook user interface, but it supports the most commonly used rule actions and conditions. Any rules created by using the Rules and Alerts Wizard that are applied to messages, which include mail items, meeting requests, task requests, documents, delivery receipts, read receipts, voting responses, and out-of-office notices, can also be created programmatically.</span></span>

<span data-ttu-id="c01fe-119">Une règle peut s’exécuter sur le serveur Exchange ou sur le client Outlook, à condition que la boîte aux lettres de l’utilisateur actuel soit hébergée sur un serveur Exchange.</span><span class="sxs-lookup"><span data-stu-id="c01fe-119">A rule can execute on the Exchange server or on the Outlook client, provided that the current user’s mailbox is hosted on an Exchange server.</span></span> <span data-ttu-id="c01fe-120">La propriété [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) de l'objet **Rule** retourne **true** pour indiquer que la règle s'exécute sur un client, et Outlook doit être en cours d'exécution pour que la règle s'exécute.</span><span class="sxs-lookup"><span data-stu-id="c01fe-120">The [IsLocalRule](https://msdn.microsoft.com/library/bb647386\(v=office.15\)) property of the **Rule** object returns **true** to indicate that the rule executes on a client, and Outlook must be running for the rule to execute.</span></span> <span data-ttu-id="c01fe-121">Si la règle s'exécute sur le serveur, Outlook ne doit pas être en cours d'exécution pour que les conditions de règle soient évaluées et que les actions de règle soient effectuées.</span><span class="sxs-lookup"><span data-stu-id="c01fe-121">If the rule executes on the server, Outlook does not have to be running for the rule conditions to be evaluated and the rule actions to be completed.</span></span>

> [!NOTE]
> <span data-ttu-id="c01fe-p106">Il n'existe pas de collection distincte représentant les conditions d'exception des règles. Utilisez la propriété [Exceptions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._rule.exceptions?view=outlook-pia) de l'objet **Rule** pour obtenir une collection [RuleConditions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.ruleconditions?view=outlook-pia) qui représente les conditions d'exception des règles.</span><span class="sxs-lookup"><span data-stu-id="c01fe-p106">There is no separate collection that represents rule exception conditions. Use the [Exceptions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook._rule.exceptions?view=outlook-pia) property of the **Rule** object to get a [RuleConditions](https://docs.microsoft.com/dotnet/api/microsoft.office.interop.outlook.ruleconditions?view=outlook-pia) collection that represents rule exception conditions.</span></span>

<span data-ttu-id="c01fe-124">Pour créer des règles via le modèle objet Outlook, procédez selon les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="c01fe-124">To create rules through the Outlook object model, follow these steps:</span></span>

1.  <span data-ttu-id="c01fe-p107">Obtenez la collection **Rules** auprès de la propriété [DefaultStore](https://msdn.microsoft.com/library/bb623164\(v=office.15\)) de l'objet [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) en appelant la méthode [GetRules()](https://msdn.microsoft.com/library/bb609979\(v=office.15\)) sur l'objet [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) par défaut. Utilisez un bloc **try…catch** pour prendre en compte le fait que le client est hors connexion ou déconnecté du serveur Exchange. Ceci empêche Outlook de générer une erreur.</span><span class="sxs-lookup"><span data-stu-id="c01fe-p107">Get the **Rules** collection from the [DefaultStore](https://msdn.microsoft.com/library/bb623164\(v=office.15\)) property of the [NameSpace](https://msdn.microsoft.com/library/bb645857\(v=office.15\)) object by calling the [GetRules()](https://msdn.microsoft.com/library/bb609979\(v=office.15\)) method on the default [Store](https://msdn.microsoft.com/library/bb609139\(v=office.15\)) object. Use a **try…catch** block to account for the user being offline or disconnected from the Exchange server. This prevents Outlook from raising an error.</span></span>

2.  <span data-ttu-id="c01fe-128">Appelez la méthode [Create(String, OlRuleType)](https://msdn.microsoft.com/library/bb643857\(v=office.15\)) sur l’objet **Rules** pour créer une variable d’instance ou un objet **Rule**, en spécifiant les paramètres Name et [OlRuleType](https://msdn.microsoft.com/library/bb645776\(v=office.15\)).</span><span class="sxs-lookup"><span data-stu-id="c01fe-128">Call the [Create(String, OlRuleType)](https://msdn.microsoft.com/library/bb643857\(v=office.15\)) method on the **Rules** object to create an instance variable or a **Rule** object, specifying a Name and a [OlRuleType](https://msdn.microsoft.com/library/bb645776\(v=office.15\)) parameter.</span></span>

3.  <span data-ttu-id="c01fe-p108">Utilisez les collections [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) et [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) pour permettre les actions, les conditions et les exceptions sur l'objet **Rule**. Notez que toute condition activée dans la collection **RuleConditions**, retournée par la propriété [Exceptions](https://msdn.microsoft.com/library/bb609880\(v=office.15\)) , est traitée en tant que condition d'exception de règle, et que des actions ou des conditions personnalisées intégrées supplémentaires ne peuvent pas être ajoutées à la collection.</span><span class="sxs-lookup"><span data-stu-id="c01fe-p108">Use the [RuleActions](https://msdn.microsoft.com/library/bb610113\(v=office.15\)) and [RuleConditions](https://msdn.microsoft.com/library/bb610965\(v=office.15\)) collections to enable actions, conditions, and exceptions on the **Rule** object. Note that any condition enabled in the **RuleConditions** collection, returned by the [Exceptions](https://msdn.microsoft.com/library/bb609880\(v=office.15\)) property, is treated as a rule exception condition, and additional built-in custom actions or conditions cannot be added to the collection.</span></span>

4.  <span data-ttu-id="c01fe-p109">Définissez la propriété [Enabled](https://msdn.microsoft.com/library/bb609147\(v=office.15\)) à **true** pour que toute action, condition ou exception de règle donnée soit opérationnelle. Certaines actions ou conditions, telles que la propriété [Folder](https://msdn.microsoft.com/library/bb646755\(v=office.15\)) , requièrent la définition de propriétés supplémentaires sur l'action ou la condition pour enregistrer l'objet **Rule** sans erreur.</span><span class="sxs-lookup"><span data-stu-id="c01fe-p109">Set the [Enabled](https://msdn.microsoft.com/library/bb609147\(v=office.15\)) property to **true** for any given rule action, condition, or exception to be operational. Some actions or conditions, such as the [Folder](https://msdn.microsoft.com/library/bb646755\(v=office.15\)) property, require that you set additional properties on the action or condition to save the **Rule** object without an error.</span></span>

5.  <span data-ttu-id="c01fe-p110">Enfin, appelez la méthode [Save(Object)](https://msdn.microsoft.com/library/bb610738\(v=office.15\)) sur la collection **Rules** pour enregistrer les règles créées ou modifiées. Placez la méthode **Save** dans un bloc **try…catch** pour gérer les exceptions.</span><span class="sxs-lookup"><span data-stu-id="c01fe-p110">Finally, call the [Save(Object)](https://msdn.microsoft.com/library/bb610738\(v=office.15\)) method on the **Rules** collection to save the created or modified rules. Enclose the **Save** method in a **try…catch** block to handle exceptions.</span></span>

<span data-ttu-id="c01fe-135">Dans l’exemple de code suivant, CreateManagerRule implémente les étapes précédemment décrites.</span><span class="sxs-lookup"><span data-stu-id="c01fe-135">In the following code example, CreateManagerRule implements the steps previously described.</span></span> <span data-ttu-id="c01fe-136">CreateManagerRule vérifie d’abord si la propriété [CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\)) représente un objet [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)), indiquant si l’utilisateur actuel est un utilisateur Exchange.</span><span class="sxs-lookup"><span data-stu-id="c01fe-136">CreateManagerRule first verifies whether the [CurrentUser](https://msdn.microsoft.com/library/bb622574\(v=office.15\)) property represents an [ExchangeUser](https://msdn.microsoft.com/library/bb609574\(v=office.15\)) object, indicating that the current user is an Exchange user.</span></span> <span data-ttu-id="c01fe-137">Si c’est le cas, CreateManagerRule obtient le manager de l’utilisateur actuel en appelant la méthode [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) sur l’objet **ExchangeUser** de la propriété **CurrentUser** de l’objet **NameSpace**.</span><span class="sxs-lookup"><span data-stu-id="c01fe-137">If the current user is an Exchange user, CreateManagerRule gets the current user’s manager by calling the [GetExchangeUserManager()](https://msdn.microsoft.com/library/bb646656\(v=office.15\)) method on the **ExchangeUser** object of the **CurrentUser** property of the **NameSpace** object.</span></span> <span data-ttu-id="c01fe-138">Une règle de réception est ensuite créée pour déplacer les messages reçus dans un sous-dossier de la Boîte de réception selon les conditions suivantes :</span><span class="sxs-lookup"><span data-stu-id="c01fe-138">A receive rule is then created to move received messages to a subfolder of the Inbox for the following conditions:</span></span>

- <span data-ttu-id="c01fe-139">Le message provient du responsable de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="c01fe-139">The message is from the user’s manager.</span></span>

- <span data-ttu-id="c01fe-140">Le destinataire se trouve sur la ligne **À :** du message.</span><span class="sxs-lookup"><span data-stu-id="c01fe-140">The recipient is on the **To:** line of the message.</span></span>

- <span data-ttu-id="c01fe-141">Le message n’est pas une demande de réunion ou une mise à jour.</span><span class="sxs-lookup"><span data-stu-id="c01fe-141">The message is not a meeting request or update.</span></span>

<span data-ttu-id="c01fe-p112">Enfin, le message est marqué pour un suivi le jour même. CreateManagerRule montre également une gestion appropriée des erreurs pour les conditions susceptibles de générer une exception, par exemple dans le cas où l’utilisateur est hors connexion ou déconnecté en mode Exchange mis en cache. </span><span class="sxs-lookup"><span data-stu-id="c01fe-p112">Finally, the message is flagged for follow-up today. CreateManagerRule also illustrates appropriate error handling for conditions that could raise an exception such as the user being offline or disconnected in cached Exchange mode.</span></span>

<span data-ttu-id="c01fe-144">Si vous utilisez Visual Studio pour tester cet exemple de code, vous devez d’abord ajouter une référence au composant Bibliothèque d’objets Microsoft Outlook 15.0 et spécifier la variable lorsque vous importez l’espace de noms **Microsoft.Office.Interop.Outlook**.</span><span class="sxs-lookup"><span data-stu-id="c01fe-144">If you use Visual Studio to test this code example, you must first add a reference to the Microsoft Outlook 15.0 Object Library component and specify the Outlook variable when you import the **Microsoft.Office.Interop.Outlook** namespace.</span></span> <span data-ttu-id="c01fe-145">L’instruction **using** ne doit pas se produire juste avant les fonctions de l’exemple de code, mais doit être ajoutée avant la déclaration publique.</span><span class="sxs-lookup"><span data-stu-id="c01fe-145">The **using** statement must not occur directly before the functions in the code example but must be added before the public Class declaration.</span></span> <span data-ttu-id="c01fe-146">Le code suivant illustre l’importation et l’affectation dans C\#.</span><span class="sxs-lookup"><span data-stu-id="c01fe-146">The following line of code shows how to do the import and assignment in C\#.</span></span>

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

## <a name="see-also"></a><span data-ttu-id="c01fe-147">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c01fe-147">See also</span></span>

- [<span data-ttu-id="c01fe-148">Règles</span><span class="sxs-lookup"><span data-stu-id="c01fe-148">Rules</span></span>](rules.md)


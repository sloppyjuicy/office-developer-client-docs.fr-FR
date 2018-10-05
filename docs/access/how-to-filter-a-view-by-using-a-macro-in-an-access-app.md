---
title: Filtrage d’une vue à l’aide d’une macro dans l’application Access
manager: kelbow
ms.date: 08/18/2017
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: db4dbb71-1b22-4dfd-bc07-5f7d694fc038
description: Apprenez à filtrer une vue dans une application Access à l’aide de l’action de macro RequeryRecords et une macro de données.
ms.openlocfilehash: 7ce65ef0c04fe91334d00649810c608cdab2f310
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390407"
---
# <a name="filter-a-view-by-using-a-macro-in-an-access-app"></a>Filtrage d’une vue à l’aide d’une macro dans l’application Access

Apprenez à filtrer une vue dans une application Access à l’aide de l’action de macro RequeryRecords et une macro de données.
  
> [!IMPORTANT]
> Microsoft ne recommande plus la création et l'utilisation d'applications web Access dans SharePoint. En guise d'alternative, vous pouvez utiliser [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) pour générer des solutions d'entreprise sans code pour le web et les appareils mobiles. 

L’affichage de liste par défaut dans une application Access vous permet de filtrer les problèmes sur les valeurs contenues dans les champs. Il peut arriver dans lequel vous souhaitez filtrer une vue basée sur un ensemble de conditions plutôt qu’en correspondance d’une valeur. Pour faire que vous devez créer une macro. Cet article vous montre comment créer une macro qui filtrer une vue pour afficher les tâches qui ont dépassé une échéance ou d’échéance dans les 7 prochains jours.
  
## <a name="prerequisites-for-building-an-app-with-access"></a>Conditions requises pour la création d’une application avec Access
<a name="Access2013FilterViewByUsingMacro_Prerequisites"> </a>

Pour suivre les étapes décrites dans cet exemple, vous devez :
  
- Access 2013
- Un environnement de développement SharePoint 2013
    
> [!NOTE]
> Pour plus d'informations sur la configuration de votre environnement de développement SharePoint, consultez [Configurer un environnement de développement général pour SharePoint 2013](https://msdn.microsoft.com/library/08e4e4e1-d960-43fa-85df-f3c279ed6927%28Office.15%29.aspx). Pour plus d'informations sur l'obtention de Access 2013 et SharePoint 2013, consultez [Téléchargements](https://msdn.microsoft.com/office/apps/fp123627). 
  
## <a name="create-the-app"></a>Création de l'application
<a name="Access2013FilterViewByUsingMacro_CreateApp"> </a>

Supposons que vous souhaitez créer une application Access qui effectue le suivi des tâches de votre entreprise. Avant de commencer la création de tables et l’affichage, vous devez rechercher un modèle de schéma.
  
### <a name="to-create-the-task-tracking-app"></a>Pour créer l’application de suivi de tâches

1. Ouvrez Access, puis sélectionnez **Application web personnalisée**.
    
2. Entrez un nom et un emplacement web pour votre application. Vous pouvez également sélectionner un emplacement dans la liste **Emplacements**, puis sélectionner **Créer**.
    
3. Tapez **tâches** dans la zone **Rechercher** , puis appuyez sur ENTRÉE. 
    
    Une liste de modèles qui peuvent être utiles pour le suivi des tâches s’affiche dans la Figure 1.
    
   **La figure 1. Modèles correspondant à la recherche de tâches**

   ![Modèles appropriés pour la recherche des problèmes](media/odc_Access15_CreateAndCustomizeWebApp_Figure01.JPG "Modèles appropriés pour la recherche des problèmes")
  
4. Cliquez sur **tâches**.
    
Access crée un ensemble de tables et d'affichages.
  
Entrez plusieurs exemples de tâches et employés dans votre application. Pour ce faire, choisissez **Lancer l’application** pour ouvrir l’application dans votre navigateur web. Entrez une valeur dans le champ **Date d’échéance** pour chaque tâche. Lorsque vous avez terminé, retournez dans Access. 
  
## <a name="plan-the-customizations"></a>Planifier les personnalisations
<a name="Access2013FilterViewByUsingMacro_PlanCustomizations"> </a>

Vous avez maintenant une application qui contient plusieurs tâches. L’affichage par défaut permet de rechercher les tâches à l’aide des éléments qui sont stockés dans les champs affichés dans l’affichage. Par exemple, vous pouvez rechercher pour les problèmes de haute priorité ou en cours. Supposons que vous souhaitez définir la priorité de votre travail, en affichant les problèmes actifs qui arrive à échéance dans la semaine à venir. Pour ce faire, vous devez créer une macro de l’interface utilisateur.
  
La commande de macro d’interface utilisateur que vous pouvez utiliser pour filtrer l’affichage est l' [Action de Macro RequeryRecords (accès web personnalisé application)](requeryrecords-macro-action-access-custom-web-app.md). L’action de macro **RequeryRecords** filtre l’affichage en fonction de l’argument *où* , qui est fourni sous la forme d’une clause WHERE SQL. Pour filtrer l’affichage, vous devez fournir plusieurs faits dans un format spécifique pour filtrer l’affichage. 
  
Les faits pertinents sont les suivants :
  
- L’ou les champs à comparer
    
- Comment faire référence à la date du jour
    
- Comment faire référence à un jour donné par rapport à la date du jour
    
- Comment déterminer lequel des tâches sont en cours
    
Le champ **Date d’échéance** fournit des informations sur lorsqu’une tâche est due. Le champ **état** fournit des informations d’état relatives à chaque tâche. Pour faire référence à un champ dans une macro, utilisez le format **[*TableName*]. [ *FieldName*]**. Utilisez **[tâches]. [ Date d’échéance]** pour faire référence au champ **Date d’échéance** et **[tâches]. [ État]** pour faire référence au champ **d’état** . 
  
La fonction de la [Fonction aujourd'hui (accès personnalisé web app)](today-function-access-custom-web-app.md) renvoie la date du jour. La fonction [DateAdd (accès personnalisé web app)](dateadd-function-access-custom-web-app.md) peut servir à calculer une date est un certain nombre de jours après la date spécifiée. 
  
Le champ **état** contient plusieurs valeurs possibles. Une valeur **terminé** indique que la tâche n’est plus active. 
  
Ces éléments peuvent être combinés dans la clause WHERE SQL suivante.
  
```sql
[Tasks].[Due Date]<DateAdd(Day,7,Today()) AND [Tasks].[Status]<>"Completed"
```

Cette clause SQL WHERE permet de filtrer l’affichage pour afficher les problèmes actifs qui arrive à échéance dans les 7 prochains jours ou retard dans la macro.
  
Pour exécuter la macro d’interface utilisateur, il doit être joint à un élément ou d’un événement qui se produit dans l’affichage. La **Barre d’Action** est un emplacement pratique pour ajouter une commande personnalisée à l’affichage. La **Barre d’Action** est une barre d’outils personnalisable qui s’affiche en haut de chaque mode d’affichage. Par défaut, la **Barre d’Action** contient des boutons pour ajouter, modifier, enregistrer, supprimer et annuler les modifications. Vous pouvez ajouter des boutons qui exécutent des actions personnalisées, telles que le filtrage de la vue. 
  
Si l’affichage contient les enregistrements qui répondent aux critères spécifiés, **RequeryRecords** filtre l’affichage. Toutefois, si l’affichage ne contient pas tous les enregistrements qui répondent aux critères, à un nouvel enregistrement vide s’affiche. Si vous ne souhaitez pas un enregistrement vide s’affiche si aucune tâche n’est due la semaine suivante, vous devez trouver une méthode pour vérifier les tâches avant d’appeler l’action de macro **RequeryRecords** . Pour ce faire, créez une macro de données pour vérifier les enregistrements qui répondent aux critères. 
  
La macro d’interface utilisateur appelle la macro de données, qui tente de trouver une tâche due la semaine prochaine. Si la macro de données détecte la tâche, puis personnaliser l’application.
  
## <a name="customize-the-app"></a>Personnalisation de l'application
<a name="Access2013FilterViewByUsingMacro_CustomizeApp"> </a>

Maintenant que vous avez déterminé les personnalisations, les implémenter. La macro de données doit être créée en premier. Certaines macros de données sont connectées directement à des tables. Toutefois, cette macro de données est une macro de données autonome.
  
### <a name="to-create-the-data-macro"></a>Pour créer la macro de données

1. Ouvrez l'application dans Access.
    
2. Dans le groupe **Créer**, sélectionnez **Avancé**, puis **Macro de données**.
    
    Une macro de données vide s’ouvre en mode Création de macro.
    
3. Dans la zone de liste **Ajouter une nouvelle Action** , sélectionnez **RechercherEnregistrement**.
    
4. Dans la zone de liste **Rechercher un enregistrement dans** , sélectionnez **tâches**.
    
5. Dans la zone **Condition Where** , entrez **[tâches]. [ Date d’échéance]\<DateAdd(Day,7,Today()) et [tâches]. [État] \< \>« Completed »**. 
    
6. Dans la liste déroulante **Ajouter une nouvelle Action** , sélectionnez **SetReturnVar** . 
    
    > [!NOTE]
    > Vous verrez deux zones de liste **Ajouter une nouvelle Action** , un dans le bloc **RechercherEnregistrement** et l’autre en dehors du bloc **RechercherEnregistrement** . Vous devez choisir la zone de liste **Ajouter une nouvelle Action** dans le bloc **RechercherEnregistrement** , comme le montre la Figure 1. 
  
   **La figure 1. Ajouter la zone de liste d’une nouvelle Action**

   ![Liste déroulante Ajouter une nouvelle Action](media/odc_Access2013_FilterFormByUsingMacro_Figure01.jpg "Liste déroulante Ajouter une nouvelle action")
  
7. Dans la zone **nom** , entrez **TaskFound**. 
    
8. Dans la zone **Expression** , entrez **« Oui »**. 
    
9. Cliquez sur **Enregistrer**. Entrez **TasksDueSoon** dans la zone **Nom de la Macro** , puis choisissez **OK**.
    
    La macro doit ressembler celle illustrée à la Figure 2.
    
   **La figure 2. Macro de données TasksDueSoon**

   ![Macro de données TasksDueSoon] (media/odc_Access2013_FilterFormByUsingMacro_Figure02.jpg "Macro de données TasksDueSoon")
  
10. Fermez l'affichage Création de macros.
    
À présent, nous sommes prêts à ajouter un bouton personnalisé à la barre d’Action.
  
### <a name="to-add-a-custom-button-to-the-action-bar"></a>Pour ajouter un bouton personnalisé à la barre d’Action

1. Choisissez le tableau des **tâches** . Il choisit le formulaire de liste de tâches. 
    
2. Dans le sélecteur d'affichage, sélectionnez **Liste**, l'icône **Paramètres/Action**, puis **Modifier**.
    
    L’affichage est ouvert en mode Création.
    
3. À présent, nous sommes prêts à ajouter un bouton personnalisé à la barre d’Action. Pour ce faire, choisissez **Ajouter une action personnalisée** , comme indiqué dans la Figure 3. 
    
   **La figure 3. Ajouter le bouton d’action personnalisée**

   ![Bouton Ajoutez une action personnalisée] (media/odc_Access2013_FilterFormByUsingMacro_Figure03.jpg "Bouton Ajoutez une action personnalisée")
  
    La nouvelle action est affichée comme un bouton avec une icône en étoile, comme le montre la Figure 4.
    
   **La figure 4. Nouveau bouton de barre d’Action**

   ![Bouton nouvelle barre d’Action] (media/odc_Access2013_FilterFormByUsingMacro_Figure04.jpg "Bouton nouvelle barre d’Action")
  
4. Cliquez sur le bouton de barre d’Action personnalisée, puis cliquez sur l’icône de **données** . 
    
    La boîte de dialogue **données** s’affiche. 
    
5. Dans la zone **Nom du contrôle** , entrez **FilterTasks**. 
    
6. Dans la zone **info-bulle** , entrez **l’affichage tâches au-delà d’échéance ou d’échéance de la semaine suivante**. 
    
À présent, nous sommes prêts à créer la macro d’interface utilisateur qui filtre l’affichage.
  
### <a name="to-create-the-ui-macro-to-filter-the-view"></a>Pour créer la macro d’interface utilisateur pour filtrer l’affichage

1. Dans la boîte de dialogue **données** , choisissez **En cliquant sur** comme indiqué dans la Figure 5. 
    
   **La figure 5. Boîte de dialogue données**

   ![Boîte de dialogue données] (media/odc_Access2013_FilterFormByUsingMacro_Figure05.jpg "Boîte de dialogue données")
  
    Une macro d’interface utilisateur vide est ouvert en mode Création de macro.
    
2. Dans la liste **Ajouter une nouvelle Action** , sélectionnez **ExécuterMacroDonnées**. 
    
3. Dans la zone Nom de la Macro, entrez **TasksDueSoon**. 
    
    Dans le champ **DéfinirVarLocale** , entrez **FilterRecords**. 
    
    L’action **ExécuterMacroDonnées** appelle la macro de données **TasksDueSoon** créés précédemment et stocke le résultat dans une variable nommée **FilterRecords**. 
    
4. Dans la zone de liste **Ajouter une nouvelle Action** , choisissez **Si**. 
    
5. Dans la zone **Si** , entrez **[FilterRecords] = « Yes »**. 
    
6. Dans la zone de liste **Ajouter une nouvelle Action** , choisissez **RequeryRecords**. 
    
    > [!NOTE]
    > Vous verrez deux zones de liste **Ajouter une nouvelle Action** , un dans le bloc **If** et une autre à l’extérieur du bloc **If** . Vous devez choisir la zone de liste **Ajouter une nouvelle Action** dans le bloc **If** , comme le montre la Figure 6. 
  
   **La figure 6. Ajouter la zone de liste d’une nouvelle Action**

   ![Liste déroulante Ajouter une nouvelle Action](media/odc_Access2013_FilterFormByUsingMacro_Figure06.jpg "Liste déroulante Ajouter une nouvelle action")
  
7. Dans la zone **où** , entrez **[tâches]. [ Date d’échéance]\<DateAdd(Day,7,Today()) et [tâches]. [État] \< \>« Completed »**. 
    
8. Dans la zone **Order By** , entrez **[Date d’échéance]**. 
    
9. Cliquez sur le lien **Ajouter un autre** qui s’affiche à droite de la zone **Ajouter une nouvelle Action** , comme le montre la Figure 7. 
    
   **La figure 7. Lien Ajouter Sinon**

   ![Ajouter un autre lien] (media/odc_Access2013_FilterFormByUsingMacro_Figure07.jpg "Ajouter un autre lien")
  
    Une clause Else est ajoutée au si bloc.
    
10. Dans la zone de liste **Ajouter une nouvelle Action** , choisissez **contrôle zonemessage.**. 
    
11. Dans la boîte de **Message** , entrez **aucune tâche n’est en retard ou arrivant à échéance dans les 7 prochains jours !**. 
    
12. Cliquez sur **Enregistrer**.
    
    La macro doit ressembler celle illustrée à la figure 8.
    
    **La figure 8. Macro d’interface utilisateur pour filtrer l’affichage**

    ![Macro d’interface utilisateur pour filtrer l’affichage] (media/odc_Access2013_FilterFormByUsingMacro_Figure08.jpg "Macro d’interface utilisateur pour filtrer l’affichage")
  
13. Fermez l'affichage Création de macros.
    
À ce stade, nous avons créé la macro d’interface utilisateur qui permet de filtrer l’affichage de liste de tâches pour afficher les tâches urgentes. Il n’est pas poli laisser l’affichage dans un état filtré sans fournir une méthode pour supprimer le filtre. Pour ce faire, ajoutez un autre bouton de barre d’Action et Macro d’interface utilisateur.
  
### <a name="to-add-an-action-bar-button-to-remove-the-filter"></a>Pour ajouter un bouton de barre d’Action pour supprimer le filtre

1. Choisissez **Ajouter une action personnalisée**.
    
    La nouvelle action est affichée comme un bouton avec une icône en étoile
    
2. Cliquez sur le bouton de barre d’Action personnalisé, puis cliquez sur l’icône de **données** . 
    
    La boîte de dialogue **données** s’affiche. 
    
3. Dans la zone **Nom du contrôle** , entrez **RemoveFilter**. 
    
4. Dans la zone **info-bulle** , entrez **Supprimer tous les filtres appliqués à l’affichage**. 
    
À présent, nous sommes prêts à créer la macro d’interface utilisateur qui permet de supprimer le filtre l’affichage.
  
### <a name="to-create-the-ui-macro-to-remove-the-filter-from-the-view"></a>Pour créer la macro d’interface utilisateur pour supprimer le filtre de l’affichage

1. Dans la boîte de dialogue **données** , choisissez **En cliquant sur**.
    
    Une macro d’interface utilisateur vide est ouvert en mode Création de macro.
    
2. Dans la zone de liste **Ajouter une nouvelle Action** , choisissez **RequeryRecords**. 
    
    Cette fois-ci, nous allons laissez les zones **où** et **Order By** vide. L’action **RequeryRecords** est appelée sans aucun paramètre, tous les filtres sont supprimés de l’affichage. 
    
3. Cliquez sur **Enregistrer**.
    
4. Fermez l'affichage Création de macros.
    
5. Fermez l’affichage de liste de tâches. Lorsque vous êtes invité à enregistrer vos modifications, sélectionnez **Oui**. 
    
À présent, nous sommes prêts à la personnalisation de texte. Choisissez **Lancer l’application** à ouvrir l’application dans votre navigateur web, puis choisissez le bouton de barre d’Action FilterTasks personnalisé. Toutes les tâches après l’échéance ou arrivant à échéance dans les 7 prochains jours sont affichés. Un message s’affiche si l’application ne contient aucune tâche urgents. 
  
## <a name="conclusion"></a>Conclusion

Vous pouvez utiliser l’action de macro **RequeryRecords** dans une macro d’interface utilisateur pour filtrer l’affichage en fonction des critères que vous choisissez. Selon le comportement que vous le souhaitez, vous souhaiterez peut-être créer une macro de données pour vérifier qu’un enregistrement répond aux critères avant d’utiliser l’action de macro **RequeryRecords** . 
  
## <a name="see-also"></a>Voir aussi

- [Nouveautés d’Access 2013 pour les développeurs](https://msdn.microsoft.com/library/df778f51-d65e-4c30-b618-65003ceb39b3%28Office.15%29.aspx)
    


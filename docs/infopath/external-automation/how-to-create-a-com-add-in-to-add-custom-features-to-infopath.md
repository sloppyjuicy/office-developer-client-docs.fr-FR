---
title: Créer un complément COM pour ajouter des fonctionnalités personnalisées à InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2007, création de compléments COM, InfoPath 2007, ajout de fonctionnalités personnalisées, compléments COM [InfoPath 2007]
localization_priority: Normal
ms.assetid: af0b0bc9-20ef-4503-8b3b-8f2a97b671a2
description: Microsoft InfoPath prend en charge les compléments COM pour étendre l’expérience utilisateur lors de la modification. Bien que la prise en charge des compléments COM ait été ajoutée pour la première fois dans InfoPath, les autres applications Office, telles que Microsoft Office Word et Microsoft Office Excel, comportent des compléments COM pris en charge depuis Office 2000.
ms.openlocfilehash: f8dd16b161c4ea862cf3b15e56e26a2547c1fc4c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303786"
---
# <a name="create-a-com-add-in-to-add-custom-features-to-infopath"></a>Créer un complément COM pour ajouter des fonctionnalités personnalisées à InfoPath

Microsoft InfoPath prend en charge les compléments COM pour étendre l’expérience utilisateur lors de la modification. Bien que la prise en charge des compléments COM ait été ajoutée pour la première fois dans InfoPath, les autres applications Office, telles que Microsoft Office Word et Microsoft Office Excel, comportent des compléments COM pris en charge depuis Office 2000.
  
La prise en charge des compléments COM dans InfoPath est disponible pour l'environnement d'édition de formulaire. L'environnement de création de formulaire ne peut pas être étendu à l'aide de compléments COM.
  
## <a name="the-idtextensibility2-interface"></a>Interface IDTExtensibility2

L'environnement d'édition InfoPath fournit la prise en charge de l'interface **IDTExtensibility2** , qui doit être implémentée par les développeurs de compléments COM. **IDTExtensibility2** est un objet double interface qui fournit cinq méthodes qui agissent comme des événements au sein de l'environnement d'édition. Ces méthodes permettent au complément COM de répondre aux conditions de démarrage et d'arrêt de l'environnement, indiquées dans le tableau suivant. 
  
|**Interface**|**Description**|
|:-----|:-----|
|**OnAddInsUpdate (ByVal Custom () As Variant)** <br/> |Se produit lorsqu'un complément est chargé ou déchargé dans l'environnement.  <br/> |
|**OnBeginShutdown (ByVal Custom () As Variant)** <br/> |Se produit lors de l'arrêt de l'environnement.  <br/> |
|**OnConnection (application ByVal en tant qu'objet, ByVal ConnectMode en tant que ext_ConnectMode, ByVal AddInInst As Object, ByVal Custom () As Variant)** <br/> |Se produit lorsqu'un complément est chargé dans l'environnement.  <br/> |
|**OnDisconnection (ByVal RemoveMode en tant que ext_DisconnectMode, ByVal Custom () As Variant)** <br/> |Se produit lorsqu'un complément est déchargé de l'environnement.  <br/> |
|**OnStartupComplete (ByVal Custom () As Variant)** <br/> |Se produit à la fin du démarrage de l'environnement.  <br/> |
   
## <a name="registering-com-add-ins"></a>Inscription de compléments COM

Toutes les applications Office, y compris InfoPath, utilisent le registre pour répertorier les compléments dans la collection de compléments COM, pour stocker l'état de connexion et pour stocker les informations de charge de démarrage ou de demande. Pour les compléments COM InfoPath, le nom de chaque complément apparaît sous la clé suivante:
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\InfoPath\AddIns\`
  
Pour les compléments COM installés pour être utilisés par tous les utilisateurs de l'ordinateur client, la clé de Registre se trouve dans la ruche de Registre HKLM:
  
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\InfoPath\AddIns\`
  
Le nom de la clé de registre correspond au **ProgIdAttribute** du complément et contient les valeurs suivantes. 
  
|**Name**|**Type**|**Description**|
|:-----|:-----|:-----|
|**FriendlyName** <br/> |**String** <br/> |Nom affiché dans la boîte de dialogue **compléments COM** et répertorié dans la page compléments **** du centre de gestion de la **confidentialité**.  <br/> |
|**Description** <br/> |**String** <br/> |La chaîne qui est affichée lorsque le complément est sélectionné dans le centre de gestion de la **confidentialité**.  <br/> |
|**LoadBehavior** <br/> |**COMPLÉTER** <br/> |Indique la façon dont le complément COM est chargé. La valeur peut être une combinaison de 0, 1, 2, 8 et 16. Pour plus d'informations, consultez le tableau ci-dessous.  <br/> |
   
La valeur **DWORD** de **LoadBehavior** doit contenir une valeur décrivant la façon dont le complément COM se charge dans l'environnement d'édition. La valeur peut être extraite du tableau ci-dessous ou une combinaison de valeurs de la table. Par exemple, un complément COM créé dans Visual Studio 2005 aura un **LoadBehavior** «3» chargé au démarrage de l'application et sera connecté. 
  
|**Value**|**Description**|
|:-----|:-----|
|0  <br/> |Rompu. Le complément apparaît comme inactif dans la boîte de dialogue **complément COM** .  <br/> |
|0,1  <br/> |Connecté. Le complément s'affiche comme étant actif dans la boîte de dialogue **complément COM** .  <br/> |
|n°2  <br/> |Charger au démarrage. Le complément est chargé et connecté au démarrage de l'application hôte.  <br/> |
|8bits  <br/> |Charger à la demande. Le complément est chargé et connecté lorsque l'application hôte l'exige, par exemple lorsqu'un utilisateur clique sur un bouton qui utilise la fonctionnalité dans le complément.  <br/> |
|Seiz  <br/> |Connecter la première fois. Le complément sera chargé et connecté la première fois que l'utilisateur exécutera l'application hôte après avoir inscrit le complément.  <br/> |
   
## <a name="creating-a-managed-com-add-in-with-visual-studio-2005-or-visual-studio-2008"></a>Création d'un complément COM géré avec Visual Studio 2005 ou Visual Studio 2008

Pour créer un complément COM géré à l'aide de Microsoft Visual Studio 2005 ou de Visual Studio 2008, créez un projet de complément partagé comme suit: 
  
1. Démarrez Visual Studio.
    
2. Dans le menu **Fichier**, cliquez sur **Nouveau projet**.
    
3. Dans le volet **types de projets** de la boîte de dialogue **nouveau projet** , cliquez sur le dossier **autres types de projets** , puis cliquez sur **extensibilité**.
    
4. Dans le volet **modèles** , cliquez sur **complément partagé**.
    
5. Dans la zone **nom** , tapez un nom pour le projet. 
    
6. Dans la zone **emplacement** , tapez un chemin d'accès à un dossier ou cliquez sur **Parcourir** et sélectionnez un chemin d'accès au dossier, puis cliquez sur **OK**. L' **Assistant Complément partagé** apparaît. 
    
7. Cliquez sur **suivant** dans l' **Assistant Complément partagé**. La page **Sélectionner un langage de programmation** apparaît. 
    
8. Cliquez sur **créer un complément à l'aide de Visual Basic**, puis cliquez sur **suivant**. La page **Sélectionner une application hôte** apparaît. 
    
9. Désactivez les cases à cocher en regard de chaque application à l'exception de **Microsoft InfoPath**, puis cliquez sur **suivant**. La page **entrer un nom et une description** s'affiche. 
    
10. Dans la zone **quel est le nom de votre complément** , tapez le nom de votre complément COM. 
    
11. Dans la zone **quelle est la description de votre complément** , tapez la description de votre complément COM, puis cliquez sur **suivant**. La page **choisir les options du complément** s'affiche. 
    
12. Cochez la case **je souhaite que mon complément soit chargé en même charge que l'application hôte** et **mon complément doit être accessible à tous les utilisateurs de l'ordinateur sur lequel il a été installé, et pas seulement à la personne qui l'installe** . 
    
13. Cliquez sur **suivant** pour passer en revue la page **récapitulative** , puis cliquez sur **Terminer**.
    
Une fois le projet créé par Visual Studio, deux projets s'affichent dans la fenêtre Explorateur de solutions. Le premier projet est le projet pour le complément COM; le deuxième projet est un projet de configuration pour le déploiement du complément COM. L' **Assistant Complément partagé** insère uniquement une référence à la **bibliothèque d'objets Microsoft Office 14,0**, c'est pourquoi il est nécessaire d'insérer une référence à la bibliothèque d'objets InfoPath en procédant comme suit:
  
1. Double-cliquez sur **mon projet** pour afficher les propriétés du projet de complément. Cliquez sur l'onglet **références** pour afficher les références automatiquement ajoutées au projet. 
    
2. Cliquez sur le bouton **Ajouter** pour afficher la boîte de dialogue **Ajouter une référence** . 
    
3. Dans l'onglet **com** , double-cliquez sur **bibliothèque de types Microsoft. InfoPath 2,0**, puis cliquez sur **OK**.
    
4. L'ajout d'une référence à la **bibliothèque de types 3,0 de Microsoft InfoPath** ajoute également des références à trois assemblys qui doivent être supprimés: **ADODB**, **mshtml**et **msxml2**. Dans l' **Explorateur de solutions** , sous **références**, cliquez avec le bouton droit sur chacune de ces références, puis cliquez sur **supprimer**.
    
## <a name="viewing-the-registry-settings"></a>Affichage des paramètres du Registre

Pour afficher les paramètres de Registre qui seront créés lors de l'installation du complément COM, procédez comme suit:
  
1. Cliquez avec le bouton droit sur le nœud racine du projet de configuration dans l' **Explorateur de solutions**, cliquez sur **affichage**, puis sur **éditeur**, puis sur **Registre**.
    
2. Dans le volet de gauche, cliquez sur le signe plus pour développer **HKEY_LOCAL_MACHINE**, **Software**, **Microsoft**, **InfoPath**, Then **AddIns**.
    
3. Cliquez sur le nom correspondant au **ProgID**de votre projet de complément partagé.
    
Pour modifier l'une de ces propriétés, cliquez avec le bouton droit sur la propriété, cliquez sur **fenêtre Propriétés**, puis modifiez la zone **valeur** dans la **fenêtre Propriétés**.
  
## <a name="compiling-and-distributing-the-shared-add-in"></a>Compilation et distribution du complément partagé

Pour compiler le complément COM géré à des fins de test sur l'ordinateur sur lequel le projet de complément partagé a été développé, cliquez avec le bouton droit sur le nœud racine du projet de complément partagé dans l'Explorateur de solutions, puis cliquez sur générer. Si le projet est généré sans erreur, vous pouvez démarrer l'environnement d'édition InfoPath et commencer à utiliser le complément COM géré. Si une instance d'InfoPath est en cours d'exécution, fermez-la avant de générer le projet. Il peut également s'avérer nécessaire d'ouvrir la boîte de dialogue Compléments COM pour vérifier que le complément COM est enregistré. Pour ouvrir la boîte de dialogue Compléments COM, procédez comme suit:
  
1. Ouvrez l'environnement d'édition InfoPath. La méthode la plus simple consiste à ouvrir un modèle de formulaire existant, qui crée un nouveau formulaire basé sur ce modèle de formulaire.
    
2. Cliquez sur Centre de gestion de la **confidentialité** dans le menu **Outils** . 
    
3. Cliquez sur **** la catégorie compléments à gauche. 
    
4. Dans la **section gérer** située en bas de la boîte de dialogue **Centre** de gestion de la confidentialité, sélectionnez **compléments COM** dans la liste, puis cliquez sur le bouton **OK** . 
    
5. Dans la boîte de dialogue **compléments COM** , vous verrez le nom de votre complément récemment généré et il doit y avoir une case à cocher en regard. S'il n'y a aucune case à cocher en regard, le chargement du complément COM a échoué en raison d'une erreur, qui figure dans la section **comportement du chargement** de la boîte de dialogue. 
    
Pour compiler le complément COM géré afin de l'utiliser sur un ordinateur autre que celui sur lequel le projet de complément partagé a été développé, vous devez suivre des étapes supplémentaires pour sécuriser votre code. Pour plus d'informations sur la sécurisation des projets de complément partagé à utiliser sur d'autres ordinateurs, consultez les trois articles suivants:
  
- [Déploiement de compléments COM gérés dans Office XP](https://go.microsoft.com/fwlink/?LinkID=73473)
  
- [Utilisation de la solution de shim de complément COM pour déployer des compléments COM managés dans Office XP](https://go.microsoft.com/fwlink/?LinkID=73474)
  
- [Isolation des extensions Office à l'aide de l'Assistant shim COM](https://go.microsoft.com/fwlink/?LinkID=73475)
  
> [!IMPORTANT]
> Ne pas isoler le complément COM peut entraîner des fuites de mémoire et une instabilité de l'application. 
  
> [!NOTE]
> Si le .NET Framework ou d'autres assemblys requis à partir du projet d'installation ne sont pas déjà installés sur les ordinateurs cibles, le fichier. msi risque de ne pas s'installer correctement. En outre, vous ne pouvez pas distribuer le fichier. msi, puis essayer d'installer le fichier. msi. Vous devez également distribuer les autres fichiers de prise en charge dans le même dossier que le fichier. msi d'origine généré par Visual Studio. 
  
## <a name="coding-in-the-com-add-in"></a>Codage dans le complément COM

Les événements d'application qui se produisent dans l'environnement d'édition de formulaires InfoPath peuvent être capturés par un complément COM. Les événements suivants de l'objet [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) peuvent être utilisés par le complément com pour répondre aux actions de l'utilisateur: 
  
|**Event**|**Description**|
|:-----|:-----|
|[NewXDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.NewXDocument.aspx) Évènement  <br/> |Se produit lorsqu'un nouveau formulaire est créé.  <br/> |
|[Quitter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.Quit.aspx) Évènement  <br/> |Se produit lorsque l’utilisateur quitte InfoPath.  <br/> |
|[WindowActivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowActivate.aspx) Évènement  <br/> |Se produit lors de l'activation d'une fenêtre de document.  <br/> |
|[WindowDeactivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowDeactivate.aspx) Évènement  <br/> |Se produit lors de la désactivation d'une fenêtre de document.  <br/> |
|[Windows](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowSize.aspx) Évènement  <br/> |Se produit lorsqu’une fenêtre de document est redimensionnée ou déplacée.  <br/> |
|[XDocumentBeforeClose](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeClose.aspx) Évènement  <br/> |Se produit immédiatement avant la fermeture d'un document.  <br/> |
|[XDocumentBeforePrint](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforePrint.aspx) Évènement  <br/> |Se produit juste avant l’impression d’un des documents ouverts.  <br/> |
|[XDocumentBeforeSave](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeSave.aspx) Évènement  <br/> |Se produit juste avant l’enregistrement d’un des documents ouverts.  <br/> |
|[XDocumentChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentChange.aspx) Évènement  <br/> |Se produit lorsqu’un formulaire est créé, lorsqu’un formulaire est ouvert ou lorsqu’un autre formulaire est activé.  <br/> |
|[XDocumentOpen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentOpen.aspx) Évènement  <br/> |Se produit à l'ouverture d'un document.  <br/> |
   
Pour capturer ces événements dans le complément COM, vous devez déclarer les variables de niveau classe suivantes dans votre classe **Connect** : 
  
```vb
InfoPathApplication = DirectCast( _
   application, Microsoft.Office.Interop.InfoPath._Application3)
InfoPathApplicationEvents = DirectCast( _
   InfoPathApplication.Events, _
   Microsoft.Office.Interop.InfoPath.ApplicationEvents)
```

```cs
InfoPathApplication =
   (Microsoft.Office.Interop.InfoPath._Application3)application;
InfoPathApplicationEvents =
   (Microsoft.Office.Interop.InfoPath.ApplicationEvents)
   InfoPathApplication.Events;
```

La première ligne reconvertit l' **objet** d'application générique reçu par le complément vers l'objet [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.aspx) . La deuxième ligne reconvertit [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.Events.aspx) la propriété Events de l'objet **_Application3** (représenté par la variable **InfoPathApplication** ) en objet [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) . 
  
Pour créer des gestionnaires d'événements, sélectionnez **InfoPathApplicationEvents** dans la zone de liste déroulante nom de la **classe** en haut de la fenêtre Visual Studio, puis sélectionnez l'événement que vous souhaitez gérer dans la zone de liste déroulante nom de la **méthode** située en haut de l'élément visuel Fenêtre Studio. Par exemple, si vous devez contrôler quand un formulaire est enregistré, vous gérez l'événement **XDocumentBeforeSave** . Si vous sélectionnez **XDocumentBeforeSave** dans la liste déroulante nom de la **méthode** , la procédure suivante est automatiquement insérée: 
  
```vb
Private Sub InfoPathApplicationEvents_XDocumentBeforeSave( _
   ByVal pDocument As Microsoft.Office.Interop.InfoPath._XDocument, _
   ByRef pfCancel As Boolean) _
   Handles InfoPathApplicationEvents.XDocumentBeforeSave
End Sub
```

```cs
private void InfoPathApplicationEvents_XDocumentBeforeSave(
   Microsoft.Office.Interop.InfoPath._XDocument pDocument, ref bool pfCancel)
{
}

```

Les événements de l'objet **ApplicationEvents** peuvent être gérés par le complément COM à l'aide de la même méthode. 
  
## <a name="see-also"></a>Voir aussi

- [Création d'un complément COM Microsoft Office 2000](https://go.microsoft.com/fwlink/?LinkID=73468) 
- [Création de compléments COM gérés par Office avec Visual Studio .NET](https://go.microsoft.com/fwlink/?LinkID=73470)
- [Utilisation des procédures événementielles IDTExtensibility2](https://go.microsoft.com/fwlink/?LinkID=73471)
- [Créer un complément COM Office à l'aide de Visual Basic .NET](https://go.microsoft.com/fwlink/?LinkID=73469)
- [Créer un complément COM Office à l'aide de Visual C# .NET](https://support.microsoft.com/en-us/help/302901/how-to-build-an-office-com-add-in-by-using-visual-c-net)
- [Création de compléments InfoPath 2007 à l'aide des outils Visual Studio 2005 pour Office System SE](https://msdn.microsoft.com/library/bb968857%28office.12%29.aspx)


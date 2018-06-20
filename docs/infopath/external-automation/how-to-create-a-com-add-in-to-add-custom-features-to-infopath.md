---
title: Créer un complément COM pour ajouter des fonctionnalités personnalisées à InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- InfoPath 2007, création de compléments com, InfoPath 2007, ajout de fonctionnalités personnalisées, des compléments COM [InfoPath 2007]
localization_priority: Normal
ms.assetid: af0b0bc9-20ef-4503-8b3b-8f2a97b671a2
description: Microsoft InfoPath prend en charge des compléments COM pour l’extension de l’expérience utilisateur d’édition de formulaires. Bien que prise en charge des compléments COM a été ajouté tout d’abord, dans InfoPath, les autres applications Office, telles que Microsoft Office Word et Microsoft Office Excel ont pris en charge des compléments COM depuis Office 2000.
ms.openlocfilehash: 4c70dfb71cf7b15a0978b4567ffac02a8ba524c3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782259"
---
# <a name="create-a-com-add-in-to-add-custom-features-to-infopath"></a>Créer un complément COM pour ajouter des fonctionnalités personnalisées à InfoPath

Microsoft InfoPath prend en charge des compléments COM pour l’extension de l’expérience utilisateur d’édition de formulaires. Bien que prise en charge des compléments COM a été ajouté tout d’abord, dans InfoPath, les autres applications Office, telles que Microsoft Office Word et Microsoft Office Excel ont pris en charge des compléments COM depuis Office 2000.
  
COM Add-prise en charge dans InfoPath est disponible pour l’environnement d’édition de formulaires. L’environnement de création de formulaire ne peut pas être étendu à l’aide de compléments COM.
  
## <a name="the-idtextensibility2-interface"></a>L’Interface IDTExtensibility2

InfoPath prend en charge l’environnement d’édition de l’interface **IDTExtensibility2** , qui doit être implémentée par les développeurs de compléments COM **IDTExtensibility2** est un objet d’interface double qui fournit cinq méthodes agissant en tant qu’événements dans l’environnement d’édition. Ces méthodes permettent le complément COM répondre aux conditions démarrage et l’arrêt de l’environnement, répertoriées dans le tableau suivant. 
  
|**Interface**|**Description**|
|:-----|:-----|
|**OnAddInsUpdate (ByVal custom() comme variante)** <br/> |Se produit lorsqu’un complément est chargé ou déchargé dans l’environnement.  <br/> |
|**OnBeginShutdown (ByVal custom() comme variante)** <br/> |Se produit lorsque l’environnement est arrêté.  <br/> |
|**OnConnection (Application ByVal comme objet, ByVal ConnectMode comme ext_ConnectMode, ByVal AddInInst comme objet, ByVal custom() comme variante)** <br/> |Se produit lorsqu’un complément est chargé dans l’environnement.  <br/> |
|**OnDisconnection (ByVal RemoveMode comme ext_DisconnectMode, ByVal custom() comme variante)** <br/> |Se produit lorsqu’un complément est déchargé de l’environnement.  <br/> |
|**OnStartupComplete (ByVal custom() comme variante)** <br/> |Se produit lorsque l’environnement a terminé le démarrage.  <br/> |
   
## <a name="registering-com-add-ins"></a>Inscrire des compléments COM

Toutes les applications Office, y compris InfoPath, utilisent le Registre pour la liste des compléments dans la collection de compléments COM, pour stocker l’état de connexion et pour stocker les informations de charge au démarrage ou à la demande. Pour InfoPath compléments COM, le nom de chaque complément apparaît sous la clé suivante :
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\InfoPath\AddIns\`
  
Pour les compléments COM installés par chaque utilisateur de l’ordinateur client, la clé de Registre se trouve dans la ruche HKLM :
  
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\InfoPath\AddIns\`
  
Nom de la clé de Registre correspond à **ProgIdAttribute** de la macro complémentaire et contient les valeurs suivantes. 
  
|**Name**|**Type**|**Description**|
|:-----|:-----|:-----|
|**FriendlyName** <br/> |**Chaîne** <br/> |Le nom qui est affiché dans la boîte de dialogue **compléments COM** et répertorié dans la page **compléments** du **Centre de gestion de la confidentialité**.  <br/> |
|**Description** <br/> |**String** <br/> |Chaîne qui s’affiche lorsque le complément est sélectionné dans le **Centre de gestion de la confidentialité**.  <br/> |
|**LoadBehavior** <br/> |**VALEUR DWORD** <br/> |Spécifie la façon dont le COM Add-in est chargé. La valeur peut être une combinaison de 0, 1, 2, 8 et 16. Voir le tableau ci-dessous pour plus d’informations.  <br/> |
   
La valeur **DWORD** de **LoadBehavior** doit contenir une valeur décrivant comment le COM Add-in chargée dans l’environnement d’édition. La valeur peut être dans le tableau ci-dessous, ou une combinaison des valeurs de la table. Par exemple, un COM Add-in créé dans Visual Studio 2005 aura un **LoadBehavior** « 3 » chargé au démarrage de l’application et être connecté. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Déconnecté. Le complément apparaît comme inactif dans la boîte de dialogue **COM Add-in** .  <br/> |
|1  <br/> |Connecté. Le complément apparaît comme actif dans la boîte de dialogue **COM Add-in** .  <br/> |
|2  <br/> |Charger au démarrage. Le complément est chargé et connecté au démarrage de l’application hôte.  <br/> |
|8  <br/> |Charger à la demande. Le complément est chargé et connecté lorsque l’application hôte requiert, par exemple lorsqu’un utilisateur clique sur un bouton qui utilise les fonctionnalités de la macro complémentaire.  <br/> |
|16  <br/> |Connecter la première fois. Le complément est chargé et connecté la première fois que l’utilisateur exécute l’application hôte après avoir inscrit le complément.  <br/> |
   
## <a name="creating-a-managed-com-add-in-with-visual-studio-2005-or-visual-studio-2008"></a>Création d’un complément COM géré avec Visual Studio 2005 ou Visual Studio 2008

Pour créer une COM géré complément à l’aide de Microsoft Visual Studio 2005 ou Visual Studio 2008, créez un projet de complément partagé comme suit : 
  
1. Démarrez Visual Studio.
    
2. Dans le menu **fichier** , cliquez sur **Nouveau projet**.
    
3. Dans le volet **Types de projets** de la boîte de dialogue **Nouveau projet** , cliquez sur le dossier **d’Autres Types de projets** , puis cliquez sur **l’extensibilité**.
    
4. Dans le volet **modèles** , cliquez sur **Complément partagé**.
    
5. Dans la zone **nom** , tapez un nom pour le projet. 
    
6. Dans la zone **emplacement** , tapez un chemin d’accès du dossier ou cliquez sur **Parcourir** et sélectionnez un chemin d’accès du dossier, puis cliquez sur **OK**. L' **Assistant Complément partagé** apparaît. 
    
7. Cliquez sur **suivant** dans l' **Assistant Complément partagé**. La page **Sélectionner un langage de programmation** apparaît. 
    
8. Cliquez sur **créer un complément à l’aide de Visual Basic**, puis cliquez sur **suivant**. La page **Sélectionner une Application hôte** apparaît. 
    
9. Désactivez les cases en regard de chaque application, à l’exception de **Microsoft InfoPath**, puis cliquez sur **suivant**. La page **entrer un nom et une Description** apparaît. 
    
10. Dans la zone **Quel est le nom de votre complément** , tapez le nom de votre COM Add-in. 
    
11. Dans la zone **Quelle est la description de votre complément** , tapez la description de votre COM Add-in, cliquez sur **suivant**. La page **Choisir les Options du complément** apparaît. 
    
12. Vérifiez les zones de **mon complément doit être accessible à tous les utilisateurs de l’ordinateur, qu'il a été installé, pas seulement la personne qui installe** et **je souhaite que mon complément chargé en même temps que l’application hôte** . 
    
13. Cliquez sur **suivant** pour passer en revue la page **Résumé** , puis cliquez sur **Terminer**.
    
Une fois que le projet est créé par Visual Studio, vous verrez deux projets dans la fenêtre de l’Explorateur de solutions. Le premier projet est le projet pour le COM Add-in ; le second projet est un projet d’installation pour le déploiement de la COM Add-in. L' **Assistant Complément partagé** insère uniquement une référence à la **Bibliothèque d’objets Microsoft Office 14.0**, afin qu’il soit nécessaire d’insérer une référence à la bibliothèque d’objets InfoPath en suivant les étapes suivantes :
  
1. Double-cliquez sur **Mon projet** pour afficher les propriétés du projet de complément. Cliquez sur l’onglet **références** pour afficher les références automatiquement ajoutés au projet. 
    
2. Cliquez sur le bouton **Ajouter** pour afficher la boîte de dialogue **Ajouter une référence** . 
    
3. Sous l’onglet **COM** , double-cliquez sur **Bibliothèque de types Microsoft.InfoPath 2.0**, puis cliquez sur **OK**.
    
4. Ajout d’une référence à la **Bibliothèque de Type Microsoft InfoPath 3.0** ajoute également les références aux trois assemblys qui doivent être supprimés : **ADODB** **MSHTML**et **MSXML2**. Dans **L’Explorateur de solutions** , sous **références**, cliquez sur chacune de ces références, puis cliquez sur **Supprimer**.
    
## <a name="viewing-the-registry-settings"></a>Afficher les paramètres de Registre

Pour afficher les paramètres de Registre qui seront créés lorsque le COM Add-in est installé, procédez comme suit :
  
1. Avec le bouton droit du nœud racine du projet d’installation dans l' **Explorateur de solutions**, cliquez sur **affichage**, puis **éditeur**, puis cliquez sur **Registre**.
    
2. Dans le volet gauche, cliquez sur le signe plus pour développer **HKEY_LOCAL_MACHINE**, **Software**, **Microsoft**, **InfoPath**, puis **AddIns**.
    
3. Cliquez sur le nom correspondant à du votre complément projet partagé **ProgID**.
    
Pour modifier un de ces propriétés, avec le bouton droit de la propriété, cliquez sur **Fenêtre Propriétés**et la zone **valeur** , dans la **Fenêtre Propriétés**.
  
## <a name="compiling-and-distributing-the-shared-add-in"></a>Compilation et distribution du complément partagé

Pour compiler le gérée COM Add-in de test sur l’ordinateur sur lequel le projet Complément partagé a été développé, cliquez sur le nœud racine du projet Complément partagé dans l’Explorateur de solutions, puis cliquez sur Générer. Si le projet est généré sans erreur, vous pouvez démarrer l’environnement d’édition InfoPath et commencer à utiliser le gérée COM Add-in. Si vous avez une instance d’InfoPath en cours d’exécution, fermez-le avant de générer le projet. Il peut également être nécessaire d’ouvrir la boîte de dialogue Compléments COM pour vérifier que le COM Add-in est enregistré. Pour ouvrir la boîte de dialogue Compléments COM, procédez comme suit :
  
1. Ouvrez l’environnement d’édition InfoPath. La plus simple consiste à ouvrir un modèle de formulaire existant, qui crée un nouveau formulaire basé sur ce modèle de formulaire.
    
2. Dans le menu **Outils** , cliquez sur **Centre de gestion de la confidentialité** . 
    
3. Cliquez sur la catégorie **compléments** sur la gauche. 
    
4. Dans la section **Gérer** au bas de la boîte de dialogue **Centre de gestion de la confidentialité** , sélectionnez **compléments COM** dans la liste, cliquez sur le bouton **OK** . 
    
5. Dans la boîte de dialogue **compléments COM** , vous verrez le nom de votre complément récemment généré, il doit y avoir une case à cocher située en regard. S’il n’existe aucune case à cocher située en regard, le COM Add-in chargement a échoué en raison d’une erreur qui apparaît dans la section **Comportement** de la boîte de dialogue. 
    
Pour compiler le complément COM géré pour une utilisation sur un ordinateur autre que l’ordinateur sur lequel le projet Complément partagé a été développé, vous devez suivre des étapes supplémentaires pour sécuriser votre code. Pour plus d’informations sur la sécurisation des projets complément partagé pour une utilisation sur d’autres ordinateurs, consultez les trois articles suivants :
  
- [Déploiement de compléments COM gérés dans Office XP](http://go.microsoft.com/fwlink/?LinkID=73473)
  
- [À l’aide de la Solution de Shim pour complément COM pour déployer des compléments COM gérés dans Office XP](http://go.microsoft.com/fwlink/?LinkID=73474)
  
- [Isolement d’Extensions Office avec l’Assistant COM Shim](http://go.microsoft.com/fwlink/?LinkID=73475)
  
> [!IMPORTANT]
> Ne pas isoler le COM Add-in peut entraîner des fuites de mémoire et instabilité de l’application. 
  
> [!NOTE]
> Si le .NET Framework ou autres assemblys requis du projet de configuration ne sont pas déjà installés sur les ordinateurs cibles, le fichier .msi risque de ne pas être installé correctement. En outre, vous ne peut pas distribuer le fichier .msi et tenter d’installer le fichier .msi. Vous devez également distribuer les autres fichiers de prise en charge dans le même dossier que le fichier .msi d’origine généré par Visual Studio. 
  
## <a name="coding-in-the-com-add-in"></a>Codage dans le complément COM

Événements d’application qui se produisent dans l’environnement d’édition de formulaires InfoPath peuvent être capturés par un COM Add-in. Les événements suivants de l’objet [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) peuvent être utilisés par le COM Add-in pour répondre aux actions de l’utilisateur : 
  
|**Événement**|**Description**|
|:-----|:-----|
|[NewXDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.NewXDocument.aspx) Événement  <br/> |Se produit lorsqu'un nouveau formulaire est créé.  <br/> |
|[Quitter](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.Quit.aspx) Événement  <br/> |Se produit lorsque l’utilisateur quitte InfoPath.  <br/> |
|[WindowActivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowActivate.aspx) Événement  <br/> |Se produit lors de l'activation d'une fenêtre de document.  <br/> |
|[WindowDeactivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowDeactivate.aspx) Événement  <br/> |Se produit lors de la désactivation d'une fenêtre de document.  <br/> |
|[WindowSize](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowSize.aspx) Événement  <br/> |Se produit lorsqu’une fenêtre de document est redimensionnée ou déplacée.  <br/> |
|[XDocumentBeforeClose](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeClose.aspx) Événement  <br/> |Se produit immédiatement avant la fermeture d'un document.  <br/> |
|[XDocumentBeforePrint](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforePrint.aspx) Événement  <br/> |Se produit juste avant l’impression d’un des documents ouverts.  <br/> |
|[XDocumentBeforeSave](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeSave.aspx) Événement  <br/> |Se produit juste avant l’enregistrement d’un des documents ouverts.  <br/> |
|[XDocumentChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentChange.aspx) Événement  <br/> |Se produit lorsqu’un formulaire est créé, lorsqu’un formulaire est ouvert ou lorsqu’un autre formulaire est activé.  <br/> |
|[XDocumentOpen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentOpen.aspx) Événement  <br/> |Se produit à l'ouverture d'un document.  <br/> |
   
Pour capturer ces événements dans le COM Add-in, vous devez déclarer les variables de niveau classe suivantes dans votre classe **Connect** : 
  
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

La première ligne effectue un cast de l’application générique **objet** reçu par le complément à l’objet [_Application3](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.aspx) . La deuxième ligne effectue un cast de la propriété [d’événements](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.Events.aspx) de l’objet **_Application3** (représenté par la variable **InfoPathApplication** ) à l’objet [ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) . 
  
Pour créer des gestionnaires d’événements, sélectionnez **InfoPathApplicationEvents** dans la zone de liste déroulante **Nom de classe** en haut de la fenêtre de Visual Studio, puis sélectionnez l’événement que vous souhaitez gérer dans la zone de liste déroulante **Nom de la méthode** dans la partie supérieure de l’objet visuel Fenêtre Studio. Par exemple, si vous avez besoin contrôler quand un formulaire est enregistré, vous gérez l’événement **XDocumentBeforeSave** . Sélection automatique des **XDocumentBeforeSave** à partir de la liste déroulante **Nom de la méthode** insère la procédure suivante : 
  
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

Les événements de l’objet **ApplicationEvents** peuvent être gérés par le COM Add-in à l’aide de la même méthode. 
  
## <a name="see-also"></a>Voir aussi

- [Création d’un Microsoft Office 2000 complément COM](http://go.microsoft.com/fwlink/?LinkID=73468) 
- [Création d’Office géré des compléments COM avec Visual Studio .NET](http://go.microsoft.com/fwlink/?LinkID=73470)
- [Utilisation des procédures événementielles IDTExtensibility2](http://go.microsoft.com/fwlink/?LinkID=73471)
- [Créer un complément COM pour Office avec Visual Basic .NET](http://go.microsoft.com/fwlink/?LinkID=73469)
- [Créer un complément COM pour Office avec Visual c# .NET](http://go.microsoft.com/fwlink/?LinkID=73472)
- [Création de compléments InfoPath 2007 à l’aide de Visual Studio 2005 Tools pour Office System SE](http://msdn.microsoft.com/en-us/library/bb968857%28office.12%29.aspx)


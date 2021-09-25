---
title: Créer un module complémentaire COM pour ajouter des fonctionnalités personnalisées à InfoPath
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- infopath 2007, création de compl?ments com,InfoPath 2007, ajout de fonctions personnalisées, compl?ments COM [InfoPath 2007]
ms.localizationpriority: medium
ms.assetid: af0b0bc9-20ef-4503-8b3b-8f2a97b671a2
description: Microsoft InfoPath prend en charge les compléments COM pour étendre l’expérience utilisateur lors de la modification. Bien que la prise en charge des modules complémentaires COM a été ajoutée pour la première fois dans InfoPath, d’autres applications Office telles que Microsoft Office Word et Microsoft Office Excel ont pris en charge les modules complémentaires COM depuis Office 2000.
ms.openlocfilehash: b53d14f637b8f2bd6b8accdf45a331f674a7d91a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552114"
---
# <a name="create-a-com-add-in-to-add-custom-features-to-infopath"></a>Créer un module complémentaire COM pour ajouter des fonctionnalités personnalisées à InfoPath

Microsoft InfoPath prend en charge les compléments COM pour étendre l’expérience utilisateur lors de la modification. Bien que la prise en charge des modules complémentaires COM a été ajoutée pour la première fois dans InfoPath, d’autres applications Office telles que Microsoft Office Word et Microsoft Office Excel ont pris en charge les modules complémentaires COM depuis Office 2000.
  
La prise en charge des compl?ments COM dans InfoPath est disponible pour l’environnement d’édition de formulaire. L’environnement de conception de formulaires ne peut pas être étendu à l’aide de compl?ments COM.
  
## <a name="the-idtextensibility2-interface"></a>The IDTExtensibility2 Interface

L’environnement d’édition InfoPath fournit la prise en charge de l’interface **IDTExtensibility2,** qui doit être implémentée par les développeurs de modules complémentaires COM. **IDTExtensibility2** est un objet à interface double qui fournit cinq méthodes qui agissent comme des événements dans l’environnement d’édition. Ces méthodes permettent au add-in COM de répondre aux conditions de démarrage et d’arrêt de l’environnement, répertoriées dans le tableau suivant. 
  
|**Interface**|**Description**|
|:-----|:-----|
|**OnAddInsUpdate (ByVal custom() As Variant)** <br/> |Se produit lorsqu’un add-in est chargé ou déchargé dans l’environnement.  <br/> |
|**OnBeginShutdown (ByVal custom() As Variant)** <br/> |Se produit lorsque l’environnement est en cours d’arrêt.  <br/> |
|**OnConnection(ByVal Application As Object, ByVal ConnectMode As ext_ConnectMode, ByVal AddInInst As Object, ByVal custom() As Variant)** <br/> |Se produit lorsqu’un add-in est chargé dans l’environnement.  <br/> |
|**OnDisconnection (ByVal RemoveMode As ext_DisconnectMode, ByVal custom() As Variant)** <br/> |Se produit lorsqu’un add-in est déchargé de l’environnement.  <br/> |
|**OnStartupComplete (ByVal custom() As Variant)** <br/> |Se produit lorsque le démarrage de l’environnement est terminé.  <br/> |
   
## <a name="registering-com-add-ins"></a>Inscription de compl?ments COM

Toutes les applications Office, y compris InfoPath, utilisent le Registre pour lister les modules complémentaires dans la collection Add-Ins COM, stocker l’état de connexion et stocker les informations de chargement de démarrage ou de demande. Pour les compl?ments COM InfoPath, le nom de chaque compl?ment s’affiche sous la clé suivante :
  
`HKEY_CURRENT_USER\Software\Microsoft\Office\InfoPath\AddIns\`
  
Pour les add-ins COM installés pour être utilisés par chaque utilisateur de l’ordinateur client, la clé de Registre se trouve dans la ruche du Registre HKLM :
  
`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Office\InfoPath\AddIns\`
  
Le nom de la clé de Registre correspond au **ProgIdAttribute** du add-in et contient les valeurs suivantes. 
  
|**Name**|**Type**|**Description**|
|:-----|:-----|:-----|
|**FriendlyName** <br/> |**String** <br/> |Nom affiché dans la boîte de dialogue Des applications **COM** et répertorié dans la **page** Des applications du Centre de **confiance.**  <br/> |
|**Description** <br/> |**String** <br/> |Chaîne qui s’affiche lorsque le module est sélectionné dans le Centre **de confiance.**  <br/> |
|**LoadBehavior** <br/> |**DWORD** <br/> |Spécifie le mode de chargement du compl?ment COM. La valeur peut être une combinaison de 0, 1, 2, 8 et 16. Pour plus d’informations, voir le tableau ci-dessous.  <br/> |
   
La **valeur DWORD** pour **LoadBehavior** doit contenir une valeur décrivant le chargement du compl?ment COM dans l’environnement d’édition. La valeur peut être à partir du tableau ci-dessous ou d’une combinaison de valeurs du tableau. Par exemple, un add-in COM créé dans Visual Studio 2005 aura un **LoadBehavior** de « 3 » chargé au démarrage de l’application et connecté. 
  
|**Valeur**|**Description**|
|:-----|:-----|
|0  <br/> |Déconnecté. Le compl?ment s’affiche comme inactif dans la **boîte de dialogue Compl?ment COM.**  <br/> |
|1  <br/> |Connecté. Le compl?ment s’affiche comme actif dans la boîte **de dialogue Compl?ment COM.**  <br/> |
|2  <br/> |Charger au démarrage. Le add-in est chargé et connecté au démarrage de l’application hôte.  <br/> |
|8   <br/> |Charger à la demande. Le add-in est chargé et connecté lorsque l’application hôte l’exige, par exemple lorsqu’un utilisateur clique sur un bouton qui utilise les fonctionnalités du module.  <br/> |
|16   <br/> |Connecter la première fois. Le add-in est chargé et connecté la première fois que l’utilisateur exécute l’application hôte après avoir inscrit le module.  <br/> |
   
## <a name="creating-a-managed-com-add-in-with-visual-studio-2005-or-visual-studio-2008"></a>Création d’un compl?ment COM géré avec Visual Studio 2005 ou Visual Studio 2008

Pour créer un add-in COM géré à l’aide de Microsoft Visual Studio 2005 ou Visual Studio 2008, créez un projet Add-In partagé comme suit : 
  
1. Démarrez Visual Studio.
    
2. Dans le menu **Fichier**, cliquez sur **Nouveau projet**.
    
3. Dans le **Project Types de** la boîte de dialogue Nouveau **Project,** cliquez sur le dossier Autres **types** de projets, puis cliquez sur **Extensibilité.**
    
4. Dans le **volet Modèles,** cliquez sur **Ajouter partagé.**
    
5. Dans la **zone** Nom, tapez un nom pour le projet. 
    
6. Dans la **zone Emplacement,** tapez un chemin d’accès de dossier ou cliquez sur **Parcourir** et sélectionnez un chemin d’accès de dossier, puis cliquez sur **OK**. **L’Assistant De ment partagé s’affiche.** 
    
7. Cliquez **sur Suivant** dans **l’Assistant De ment partagé.** La page **Sélectionner un langage de** programmation s’affiche. 
    
8. Cliquez **sur Créer un Visual Basic,** puis sur **Suivant.** La page **Sélectionner un hôte d’application** s’affiche. 
    
9. Décochez les cases en dehors de chaque application **à l’exception de Microsoft InfoPath,** puis cliquez sur **Suivant**. La page **Entrer un nom et une description s’affiche.** 
    
10. Dans la **zone Quel est le nom de** votre compl?ment, tapez le nom de votre compl?ment COM. 
    
11. Dans la **zone Quelle est la description de** votre compl?ment, tapez la description de votre compl?ment COM, puis cliquez sur **Suivant**. La page **Choisir Add-In options s’affiche.** 
    
12. Vérifiez que je souhaite que mon **add-in** soit chargé lors du chargement de l’application hôte et que Mon application soit disponible pour tous les utilisateurs de l’ordinateur sur qui il a été **installé,** et pas seulement la personne qui l’installe. 
    
13. Cliquez **sur Suivant** pour passer en revue la page **Résumé,** puis cliquez sur **Terminer.**
    
Une fois le projet créé par Visual Studio, vous verrez deux projets dans la fenêtre Explorateur de solutions. Le premier projet est le projet pour le compl?ment COM ; le deuxième projet est un projet d’installation pour le déploiement du compl?ment COM. L’Assistant De 2013 insère uniquement une référence à la bibliothèque d’objets **Microsoft Office 14.0.** Il est donc nécessaire d’insérer une référence à la bibliothèque d’objets InfoPath en suivant les étapes **ci-après** :
  
1. Double-cliquez **sur My Project** pour afficher les propriétés du projet de add-in. Cliquez sur **l’onglet Références** pour afficher les références ajoutées automatiquement au projet. 
    
2. Cliquez sur le **bouton** Ajouter pour afficher la boîte de dialogue **Ajouter une** référence. 
    
3. Sous **l’onglet COM,** double-cliquez sur Bibliothèque de types **Microsoft.InfoPath 2.0,** puis cliquez sur **OK**.
    
4. L’ajout d’une référence à la bibliothèque de types **Microsoft InfoPath 3.0** ajoute également des références à trois assemblys qui doivent être supprimés : **ADODB,** **MSHTML** et **MSXML2**. Dans **l’Explorateur** de solutions, sous **Références,** cliquez avec le bouton droit sur chacune de ces références, puis cliquez sur **Supprimer.**
    
## <a name="viewing-the-registry-settings"></a>Affichage du registre Paramètres

Pour afficher les paramètres de Registre qui seront créés lors de l’installation du compl?ment COM, suivez les étapes ci-après :
  
1. Cliquez avec le bouton droit sur le nœud racine du projet d’installation dans l’Explorateur de **solutions,** cliquez sur **Afficher,** puis Sur **Éditeur,** puis cliquez sur **Registre.**
    
2. Dans le volet de gauche, cliquez sur le plus pour développer HKEY_LOCAL_MACHINE **,** **Logiciel,** **Microsoft,** **InfoPath,** puis **AddIns**.
    
3. Cliquez sur le nom correspondant au **ProgID** de votre projet de add-in partagé.
    
Pour modifier l’une de ces propriétés, cliquez avec  le bouton droit sur la propriété, cliquez sur Fenêtre Propriétés **et** modifiez la zone Valeur dans la fenêtre **Propriétés.**
  
## <a name="compiling-and-distributing-the-shared-add-in"></a>Compilation et distribution des Add-In

Pour compiler le add-in COM géré pour le test sur l’ordinateur sur lequel le projet Add-In partagé a été développé, cliquez avec le bouton droit sur le nœud racine du projet Add-In partagé dans l’Explorateur de solutions, puis cliquez sur Créer. Si le projet est build sans erreur, vous pouvez démarrer l’environnement d’édition InfoPath et commencer à utiliser le compl?ment COM géré. Si une instance d’InfoPath est en cours d’exécution, fermez-la avant de créer le projet. Il peut également être nécessaire d’ouvrir la boîte de dialogue Des compl?ments COM pour vérifier que le compl?ment COM est inscrit. Pour ouvrir la boîte de dialogue Des applications COM, suivez les étapes suivantes :
  
1. Ouvrez l’environnement d’édition InfoPath. Le moyen le plus simple de le faire consiste à ouvrir un modèle de formulaire existant, qui crée un formulaire basé sur ce modèle de formulaire.
    
2. Cliquez **sur Centre de gestion de** la confiance dans le menu **Outils.** 
    
3. Cliquez sur **la catégorie Des add-ins** sur la gauche. 
    
4. Dans la section **Gérer** au  bas de la boîte de dialogue Centre de gestion de la relation, sélectionnez les applications **COM** dans la liste, puis cliquez sur **le bouton** Aller. 
    
5. Dans la boîte de dialogue Des compl?ments **COM,** vous verrez le nom de votre compl?ment récemment construit et une case doit cocher en regard de celui-ci. S’il n’y a pas de case à cocher en regard, le chargement du compl?ment COM n’a pas t chargé en raison d’une erreur, qui sera listée dans la **section** Comportement de chargement de la boîte de dialogue. 
    
Pour compiler le complément COM géré à utiliser sur un ordinateur autre que l’ordinateur sur lequel le projet Add-In partagé a été développé, vous devez suivre des étapes supplémentaires pour sécuriser votre code. Pour plus d’informations sur la sécurisation des projets Add-In partagés pour une utilisation sur d’autres ordinateurs, voir les trois articles suivants :
  
- [Déploiement de composants COM gérés Add-Ins dans Office XP](https://go.microsoft.com/fwlink/?LinkID=73473)
  
- [Utilisation de la solution SHIM de compl?ment COM pour déployer des compl?ments COM gérés dans Office XP](https://go.microsoft.com/fwlink/?LinkID=73474)
  
- [Isolation des extensions Office avec l’Assistant Shim COM](https://go.microsoft.com/fwlink/?LinkID=73475)
  
> [!IMPORTANT]
> Le fait de ne pas isoler le compl?ment COM peut provoquer des fuites de m moir et l’instabilité de l’application. 
  
> [!NOTE]
> Si le .NET Framework ou d’autres assemblys requis du projet d’installation ne sont pas déjà installés sur les ordinateurs cibles, il se peut que le fichier .msi ne s’installe pas correctement. En outre, vous ne pouvez pas distribuer le fichier .msi puis essayer d’installer le .msi fichier. Vous devez également distribuer les autres fichiers de support dans le même dossier que le fichier .msi d’origine généré par Visual Studio. 
  
## <a name="coding-in-the-com-add-in"></a>Codage dans le compl?ment COM

Les événements d’application qui se produisent dans l’environnement d’édition de formulaires InfoPath peuvent être capturés par un compl?ment COM. Les événements [suivants de l’objet ApplicationEvents](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) peuvent être utilisés par le compl?ment COM pour répondre aux actions de l’utilisateur : 
  
|**Event**|**Description**|
|:-----|:-----|
|[NewXDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.NewXDocument.aspx) Événement  <br/> |Se produit lorsqu'un nouveau formulaire est créé.  <br/> |
|[Quit](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.Quit.aspx) Événement  <br/> |Se produit lorsque l’utilisateur quitte InfoPath.  <br/> |
|[WindowActivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowActivate.aspx) Événement  <br/> |Se produit lors de l'activation d'une fenêtre de document.  <br/> |
|[WindowDeactivate](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowDeactivate.aspx) Événement  <br/> |Se produit lors de la désactivation d'une fenêtre de document.  <br/> |
|[WindowSize](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.WindowSize.aspx) Événement  <br/> |Se produit lorsqu’une fenêtre de document est redimensionnée ou déplacée.  <br/> |
|[XDocumentBeforeClose](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeClose.aspx) Événement  <br/> |Se produit immédiatement avant la fermeture d'un document.  <br/> |
|[XDocumentBeforePrint](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforePrint.aspx) Événement  <br/> |Se produit juste avant l’impression d’un des documents ouverts.  <br/> |
|[XDocumentBeforeSave](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentBeforeSave.aspx) Événement  <br/> |Se produit juste avant l’enregistrement d’un des documents ouverts.  <br/> |
|[XDocumentChange](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentChange.aspx) Événement  <br/> |Se produit lorsqu’un formulaire est créé, lorsqu’un formulaire est ouvert ou lorsqu’un autre formulaire est activé.  <br/> |
|[XDocumentOpen](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._ApplicationEvents_Event.XDocumentOpen.aspx) Événement  <br/> |Se produit à l'ouverture d'un document.  <br/> |
   
Pour capturer ces événements dans le compl?ment COM, vous devez d déclarer les variables de niveau de classe suivantes dans **Connecter** classe : 
  
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

La première ligne caste  l’objet d’application générique reçu par le _Application3 [objet.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.aspx) La deuxième ligne caste la propriété [Events](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath._Application3.Events.aspx) de **l’objet _Application3** (représenté par la variable **InfoPathApplication)** vers l’objet [ApplicationEvents.](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.ApplicationEvents.aspx) 
  
Pour créer des handlers d’événements, sélectionnez  **InfoPathApplicationEvents** dans la zone de liste verte Nom de classe  en haut de la fenêtre Visual Studio, puis sélectionnez l’événement que vous souhaitez gérer dans la zone de liste rouge Nom de la méthode en haut de la fenêtre Visual Studio. Par exemple, si vous devez contrôler quand un formulaire est enregistré, vous devez gérer l’événement **XDocumentBeforeSave.** La sélection **de XDocumentBeforeSave** dans la liste drop-down **Nom** de la méthode insère automatiquement la procédure suivante : 
  
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

Tous les événements de **l’objet ApplicationEvents** peuvent être gérés par le add-in COM à l’aide de la même méthode. 
  
## <a name="see-also"></a>Voir aussi

- [Création d Microsoft Office 2000 COM](https://go.microsoft.com/fwlink/?LinkID=73468) 
- [Création de Office com géré Add-Ins avec Visual Studio .NET](https://go.microsoft.com/fwlink/?LinkID=73470)
- [Working with the IDTExtensibility2 Event Procedures](https://go.microsoft.com/fwlink/?LinkID=73471)
- [Créer un Office COM avec Visual Basic .NET](https://go.microsoft.com/fwlink/?LinkID=73469)
- [Créer un Office COM à l’aide de Visual C# .NET](https://support.microsoft.com/en-us/help/302901/how-to-build-an-office-com-add-in-by-using-visual-c-net)
- [Création d'Add-Ins InfoPath 2007 à l’aide Visual Studio Outils 2005 pour Office système SE](https://msdn.microsoft.com/library/bb968857%28office.12%29.aspx)


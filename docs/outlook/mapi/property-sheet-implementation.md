---
title: Implémentation de feuille de propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f3475206-0237-4b5b-8efd-abd5d5e0b6c3
ms.openlocfilehash: 11e81890c3ea781405456bc31f55d5df36ac7c84
ms.sourcegitcommit: 518845d053a009b11c8d907a33822161c0b6bc96
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/08/2022
ms.locfileid: "63378183"
---
# <a name="property-sheet-implementation"></a>Implémentation de feuille de propriétés

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une feuille de propriétés est une boîte de dialogue qui affiche les propriétés d’un objet. Les propriétés peuvent être en lecture seule, ce qui permet à l’utilisateur de les afficher uniquement, ou en lecture/écriture, ce qui lui permet d’apporter des modifications. Une feuille de propriétés contient une ou plusieurs fenêtres enfants superposées appelées pages. Chaque page contient des fenêtres de contrôle pour définir un groupe de propriétés connexes. Les utilisateurs naviguent d’une page à l’autre en sélectionnant un onglet qui place la page correspondante au premier plan de la feuille des propriétés.
  
Les fournisseurs de services doivent implémenter une feuille de propriétés qui affiche un ensemble minimal de propriétés liées à la configuration dans le service de messagerie. Si vous autorisez la modification de ces propriétés de service de message, vous pouvez autoriser les utilisateurs d’applications clientes, telles que le Panneau de contrôle, à apporter les modifications ou à implémenter les modifications par programme. L’implémentation de feuilles de propriétés pour afficher et modifier d’autres types de propriétés est facultative. 
  
En règle générale, vous devez afficher une feuille de propriétés dans les situations suivantes :
  
- Lorsqu’un client appelle la méthode [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) de votre objet d’état. 
    
- Lorsque MAPI appelle la méthode d’accès de votre objet fournisseur.
    
- Lorsque MAPI appelle la fonction de point d’entrée pour le service de messagerie de votre fournisseur.
    
Les fournisseurs de transport implémentent également des feuilles de propriétés pour afficher les propriétés liées aux options de message, et les fournisseurs de carnets d’adresses implémentent des feuilles de propriétés pour afficher et modifier des informations détaillées sur les utilisateurs de messagerie et les listes de distribution, les critères de recherche avancés et les modèles permettant d’entrer de nouveaux utilisateurs.
  
Vous pouvez utiliser l’une des trois techniques suivantes pour créer une feuille de propriétés :
  
- Manuellement, comme vous le feriez dans n’importe quelle boîte de dialogue.
    
- À l’aide du contrôle commun de feuille de propriétés fourni dans Windows SDK.
    
- À l’aide d’un tableau d’affichage MAPI.
    
Les fournisseurs doivent choisir la dernière option (créer une feuille de propriétés à l’aide d’un tableau d’affichage). Il s’agit de l’option la plus simple, car elle élimine la nécessité d’utiliser l’interface Windows’utilisateur. 
  
Pour implémenter une feuille de propriétés construite à partir d’un tableau d’affichage pour les propriétés de votre service de message, utilisez la procédure suivante :
  
1. [Appelez IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) pour ouvrir une section dans le profil actuel. Passez votre [MAPIUID](mapiuid.md) ou NULL pour ouvrir la section de profil de votre fournisseur. 
    
2. [Appelez CreateIProp pour](createiprop.md) créer un objet de données de propriété. 
    
3. Appelez la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) de la section de profil pour copier toutes les propriétés de la section dans l’objet de données de propriété. 
    
4. Créez un tableau d’affichage en construisant une ou plusieurs structures [DTPAGE](dtpage.md) qui décrivent les contrôles à afficher dans la feuille des propriétés et en appelant la [fonction BuildDisplayTable](builddisplaytable.md) , ou en implémentant du code personnalisé. 
    
5. Appelez [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) pour afficher une feuille de propriétés qui possède les propriétés copiées. Passez un pointeur vers l’objet de données de propriété en tant que paramètre  _lpConfigData_ et un pointeur vers le tableau d’affichage en tant que paramètre  _lpDisplayTable_ . Si vous souhaitez remplacer le mode d’accès par défaut pour cette feuille de propriétés, ne définissez pas l’indicateur DT_EDITABLE pour chaque contrôle du tableau d’affichage qui représente une propriété en lecture seule. 
    
6. Lorsque toutes les modifications ont été apportées dans la feuille des propriétés, appelez la méthode **IMAPIProp::CopyTo** de l’objet de données de propriété pour copier les propriétés modifiées dans la section de profil. 
    
Pour une vue d’ensemble des tableaux d’affichage, voir [Tableaux d’affichage](display-tables.md). 
  
Pour plus d’informations sur les tableaux d’affichage, voir [Implémentation de tableaux d’affichage](display-table-implementation.md). 
  
Pour plus d’informations sur l’implémentation d’un contrôle, voir [Control Object Implementation](control-object-implementation.md).
  
Pour récupérer l’index d’un contrôle qu’un utilisateur sélectionne dans une zone de liste de tableau d’affichage, patientez jusqu’à ce que l’utilisateur clique sur **OK** ou **Appliquer**. À ce stade, l’identificateur d’entrée de l’élément sélectionné est écrit dans l’interface [IMAPIProp : IUnknown](imapipropiunknown.md) en tant que valeur de la propriété spécifiée par le membre **ulPRSetProperty** dans la structure [DTBLLBX](dtbllbx.md) . 
  
Si vous devez pouvoir ajouter ou supprimer des éléments de votre zone de liste, l’utilisation d’un tableau d’affichage et de la méthode [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) ne fonctionne pas. Envisagez plutôt d’implémenter une feuille de propriétés avec l’API de feuille de propriétés Win32 contenue dans comdlg32.dll fichier. 
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)


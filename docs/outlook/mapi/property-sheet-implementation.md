---
title: Implémentation de la feuille de propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f3475206-0237-4b5b-8efd-abd5d5e0b6c3
description: 'Dernière modification : 23 juillet 2011'
ms.openlocfilehash: 3f1c6497a182231645691f669d8900d33b495503
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328524"
---
# <a name="property-sheet-implementation"></a>Implémentation de la feuille de propriétés

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Une feuille des propriétés est une boîte de dialogue qui affiche les propriétés d'un objet. Les propriétés peuvent être en lecture seule, ce qui permet à l'utilisateur de les afficher uniquement ou en lecture/écriture, ce qui permet à l'utilisateur d'y effectuer des modifications. Une feuille de propriétés contient une ou plusieurs fenêtres enfants superposées appelées pages. Chaque page contient des fenêtres de contrôle permettant de définir un groupe de propriétés connexes. Les utilisateurs naviguent d'une page à une page en sélectionnant un onglet qui place la page correspondante au premier plan de la feuille des propriétés.
  
Les fournisseurs de services doivent implémenter une feuille de propriétés qui affiche un ensemble minimal de propriétés liées à la configuration dans le service de messagerie. Si vous autorisez la modification de ces propriétés de service de message, vous pouvez autoriser les utilisateurs d'applications clientes, tels que le panneau de configuration, à effectuer les modifications ou à implémenter ces modifications par programme. L'implémentation des feuilles de propriétés pour afficher et modifier d'autres types de propriétés est facultative. 
  
En règle générale, vous devez afficher une feuille de propriétés dans les situations suivantes:
  
- Lorsqu'un client appelle la méthode [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) de l'objet d'État. 
    
- Lorsque MAPI appelle la méthode d'ouverture de session de l'objet fournisseur.
    
- Lorsque MAPI appelle la fonction de point d'entrée pour le service de messagerie de votre fournisseur.
    
Les fournisseurs de transport implémentent également des feuilles de propriétés pour afficher les propriétés associées aux options de message, et les fournisseurs de carnet d'adresses implémenter des feuilles de propriétés pour afficher et modifier des informations détaillées sur les utilisateurs de messagerie et les listes de distribution, recherche avancée des critères et des modèles pour la saisie de nouveaux utilisateurs.
  
Vous pouvez utiliser l'une des trois techniques suivantes pour créer une feuille de propriétés:
  
- Manuellement, comme vous le feriez pour n'importe quelle boîte de dialogue.
    
- À l'aide du contrôle commun de feuille de propriétés fourni dans le kit de développement logiciel (SDK) Windows.
    
- À l'aide d'une table d'affichage MAPI.
    
Les fournisseurs doivent choisir la dernière option (créer une feuille des propriétés à l'aide d'une table d'affichage). Il s'agit de l'option la plus simple, car elle élimine la nécessité d'utiliser l'interface utilisateur de Windows. 
  
Pour implémenter une feuille de propriétés construite à partir d'une table d'affichage pour vos propriétés de service de messagerie, procédez comme suit:
  
1. Appelez [IMAPISupport:: OpenProfileSection](imapisupport-openprofilesection.md) pour ouvrir une section dans le profil actuel. TransMettez votre [MAPIUID](mapiuid.md) ou null pour ouvrir la section de profil de votre fournisseur. 
    
2. Appelez [CreateIProp](createiprop.md) pour créer un objet de données de propriété. 
    
3. Appelez la méthode [IMAPIProp:: CopyTo](imapiprop-copyto.md) de la section profile pour copier toutes les propriétés de la section vers l'objet de données de la propriété. 
    
4. Créez une table d'affichage en créant une ou plusieurs structures [DTPAGE](dtpage.md) qui décrivent les contrôles à afficher sur la feuille de propriétés et en appelant la fonction [BuildDisplayTable](builddisplaytable.md) , ou en implémentant du code personnalisé. 
    
5. Appelez [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) pour afficher une feuille de propriétés qui a les propriétés copiées. TransMettez un pointeur vers l'objet de données de propriété en tant que paramètre _lpConfigData_ et un pointeur vers la table d'affichage en tant que paramètre _lpDisplayTable_ . Si vous souhaitez remplacer le mode d'accès par défaut pour cette feuille de propriétés, ne définissez pas l'indicateur DT_EDITABLE pour chaque contrôle de la table d'affichage qui représente une propriété en lecture seule. 
    
6. Lorsque toutes les modifications ont été apportées à la feuille de propriétés, appelez la méthode **IMAPIProp:: CopyTo** de l'objet de données de propriété pour recopier les propriétés modifiées dans la section profil. 
    
Pour une vue d'ensemble des tables d'affichage, voir [afficher les tables](display-tables.md). 
  
Pour plus d'informations sur les tables d'affichage, voir [Display table Implementation](display-table-implementation.md). 
  
Pour plus d'informations sur l'implémentation d'un contrôle, voir [Control Object Implementation](control-object-implementation.md).
  
Pour récupérer l'index d'un contrôle qu'un utilisateur sélectionne dans une liste de tables d'affichage, patientez jusqu'à ce que l'utilisateur clique sur **OK** ou sur **appliquer**. À ce stade, l'identificateur d'entrée de l'élément sélectionné est réécrit dans l'interface [IMAPIProp: IUnknown](imapipropiunknown.md) en tant que valeur de la propriété spécifiée par le membre **ulPRSetProperty** dans la structure [DTBLLBX](dtbllbx.md) . 
  
Si vous devez être en mesure d'ajouter ou de supprimer des éléments de votre zone de liste, l'utilisation d'une table d'affichage et de la [IMAPISupport::D oconfigpropsheet](imapisupport-doconfigpropsheet.md) ne fonctionnera pas. Au lieu de cela, envisagez d'implémenter une feuille de propriétés avec l'API de feuille de propriétés Win32 contenue dans le fichier comdlg32. dll. 
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)


---
title: Implémentation d’une feuille de propriétés
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f3475206-0237-4b5b-8efd-abd5d5e0b6c3
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: 9a0fad8fa20b2d94077f9fbdf8a3c595c0ab219e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580865"
---
# <a name="property-sheet-implementation"></a>Implémentation d’une feuille de propriétés

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Une feuille de propriétés est une boîte de dialogue pour afficher les propriétés d’un objet. Les propriétés peuvent être en lecture seule, l’activation de l’utilisateur uniquement pour les afficher, ou de lecture/écriture, permettant à l’utilisateur apporter des modifications. Une feuille de propriétés contient une ou plusieurs fenêtres enfants qui se chevauchent, appelés pages. Chaque page contient un contrôle windows pour définir un groupe de propriétés connexes. Les utilisateurs naviguer d’une page en sélectionnant un onglet qui affiche la page correspondante au premier plan de la feuille de propriétés.
  
Fournisseurs de services doivent implémenter une feuille de propriétés qui affiche un jeu de propriétés relatives à la configuration dans le service message minimal. Si vous autorisez ces propriétés de service de message à modifier, vous pouvez soit autoriser les utilisateurs du client applications, telles que le panneau, apportez les modifications ou appliquer les modifications apportées par programme. Feuilles de propriétés pour afficher et modifier d’autres types de propriétés est facultative. 
  
En règle générale, vous devrez afficher une feuille de propriétés dans les situations suivantes :
  
- Lorsqu’un client appelle la méthode [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) de l’objet de votre statut. 
    
- Lorsque MAPI appelle la méthode d’ouverture de session de l’objet de votre fournisseur.
    
- Lorsque MAPI appelle la fonction de point d’entrée pour le service de message de votre fournisseur.
    
Fournisseurs de transport implémentent également les feuilles de propriétés pour afficher les propriétés liées aux options de message et fournisseurs de carnet d’adresses implémentent des feuilles de propriétés pour afficher et modifier des informations détaillées sur les utilisateurs et les listes de distribution, recherche avancée de la messagerie critères et modèles pour la saisie de nouveaux utilisateurs.
  
Vous pouvez utiliser une des trois méthodes suivantes pour créer une feuille de propriétés :
  
- Manuellement, comme vous le feriez pour toute boîte de dialogue.
    
- À l’aide de la propriété contrôle de la feuille fourni dans le SDK de Windows.
    
- Afficher le tableau à l’aide d’une MAPI.
    
Fournisseurs doivent choisir la dernière option (créer une feuille de propriétés à l’aide d’un tableau d’affichage). Il s’agit de l’option la plus simple car elle élimine la nécessité de travailler avec l’interface utilisateur Windows. 
  
Pour implémenter une feuille de propriétés créée à partir d’un tableau d’affichage pour des propriétés de service de message, utilisez la procédure suivante :
  
1. Appelez [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) pour ouvrir une section dans le profil actif. Passez vos [MAPIUID](mapiuid.md) ou la valeur NULL pour ouvrir la section de profil de votre fournisseur. 
    
2. Appelez [CreateIProp](createiprop.md) pour créer un objet de données de propriété. 
    
3. Appeler la méthode [IMAPIProp::CopyTo](imapiprop-copyto.md) de la section profil pour copier toutes les propriétés de la section à l’objet de données de propriété. 
    
4. Créer un tableau d’affichage en créant une ou plusieurs structures [DTPAGE](dtpage.md) qui décrivent les contrôles qui doit apparaître sur la feuille des propriétés et appeler la fonction [BuildDisplayTable](builddisplaytable.md) , ou en implémentant un code personnalisé. 
    
5. Appelez [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) pour afficher une feuille de propriétés qui possède les propriétés copiées. Passer un pointeur vers l’objet de données de propriété en tant que le paramètre _lpConfigData_ et un pointeur vers le tableau de l’affichage en tant que paramètre _lpDisplayTable_ . Si vous souhaitez remplacer le mode d’accès par défaut pour cette feuille de propriétés, ne définissez pas l’indicateur DT_EDITABLE pour chaque contrôle dans le tableau d’affichage qui représente une propriété en lecture seule. 
    
6. Lorsque toutes les modifications ont été apportées dans la feuille des propriétés, appelez la méthode de **IMAPIProp::CopyTo** de l’objet de données de propriété pour copier les propriétés modifiées à la section de profil. 
    
Pour une vue d’ensemble des tables d’affichage, voir [Afficher les Tables](display-tables.md). 
  
Pour plus d’informations sur les tables d’affichage, voir [Implémentation de Table afficher](display-table-implementation.md). 
  
Pour plus d’informations sur l’implémentation d’un contrôle, voir [Implémentation d’objet de contrôle](control-object-implementation.md).
  
Pour récupérer l’index d’un contrôle sélectionné par un utilisateur dans une zone de liste affichage tableau, attendez que l’utilisateur clique sur **OK** ou sur **Appliquer**. À ce stade, l’identificateur d’entrée de l’élément sélectionné est réécrit dans la [IMAPIProp : IUnknown](imapipropiunknown.md) interface comme valeur de la propriété spécifiée par le membre **ulPRSetProperty** de la structure [DTBLLBX](dtbllbx.md) . 
  
Si vous devez être en mesure d’ajouter ou supprimer des éléments de votre zone de liste, l’à l’aide d’un tableau d’affichage et la méthode [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) ne fonctionnera pas. Au lieu de cela, envisagez d’implémenter une feuille de propriétés avec l’API de feuille de propriétés Win32 contenue dans le fichier comdlg32.dll. 
  
## <a name="see-also"></a>Voir aussi



[Fournisseurs de services MAPI](mapi-service-providers.md)


---
title: Ajout ou suppression de fournisseurs dans un service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44bb4d34-ca96-4d5a-93fe-85e09bd7971d
description: 'Derniére modification : samedi 23 juillet 2011'
ms.openlocfilehash: ed5ea8bdfcbdaaa6b6abd81a39f0e8df50d3b314
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433422"
---
# <a name="adding-or-deleting-providers-in-a-message-service"></a>Ajout ou suppression de fournisseurs dans un service de messagerie

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Pour ajouter ou supprimer des fournisseurs de services dans un service de messagerie, utilisez l'interface [IProviderAdmin: IUnknown](iprovideradminiunknown.md) . Vous pouvez récupérer un pointeur **IProviderAdmin** en appelant [IMsgServiceAdmin:: AdminProviders](imsgserviceadmin-adminproviders.md). La table du fournisseur, accessible via [IProviderAdmin:: GetProviderTable](iprovideradmin-getprovidertable.md), répertorie les informations sur les fournisseurs de services actuellement installés dans le service de messagerie. Les clients et les fournisseurs de services peuvent utiliser la table des fournisseurs pour accéder au nom du fichier DLL du fournisseur, par exemple, à l' **MAPIUID**, au nom d'affichage et au type du fournisseur, ainsi qu'à des informations sur le service de messagerie. Pour plus d'informations, consultez la rubrique [tables du fournisseur](provider-tables.md).
  
 **Pour ajouter ou supprimer un fournisseur de services dans un service de messagerie**
  
1. Appelez la méthode **AdminServices** pour accéder à un objet d'administration de service de messagerie. 
    
2. Appelez [IMsgServiceAdmin:: GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) pour accéder à la table des services de messagerie. 
    
3. Créer une restriction de propriété à l'aide d'une structure [SPropertyRestriction](spropertyrestriction.md) qui correspond à **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ou **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) avec le nom du service de messagerie à utiliser modifié. 
    
4. Appelez la méthode [IMAPITable:: FindRow](imapitable-findrow.md) du tableau service de messages pour localiser la ligne dans le tableau qui représente le service de messagerie ciblé. 
    
5. Appelez [IMsgServiceAdmin:: AdminProviders](imsgserviceadmin-adminproviders.md) pour récupérer un pointeur **IProviderAdmin** . TransMettez la colonne **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) à partir de la ligne du tableau de service de message en tant que paramètre _lpUID_ . 
    
6. Appelez [IProviderAdmin:: GetProviderTable](iprovideradmin-getprovidertable.md) pour accéder à la table des fournisseurs. 
    
7. Générez une restriction de propriété à l'aide d'une structure SPropertyRestriction qui correspond à **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ou **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)), avec le nom du fournisseur de services à ajouté ou supprimé. 
    
8. Appelez la méthode [IMAPITable:: FindRow](imapitable-findrow.md) de la table fournisseur pour localiser la ligne dans le tableau qui représente le fournisseur de services ciblé. 
    
9. Appelez [IProviderAdmin:: CreateProvider](iprovideradmin-createprovider.md) pour ajouter le fournisseur ou [IProviderAdmin::D eleteprovider](iprovideradmin-deleteprovider.md) pour le supprimer du service de messagerie. Pour **CreateProvider**, transmettez la propriété **PR_DISPLAY_NAME** du fournisseur en tant que paramètre _lpszProvider_ . Pour les deux méthodes, transmettez la propriété **PR_SERVICE_UID** du fournisseur en tant que paramètre _lpUID_ . Une fois que le fournisseur de services a été ajouté ou supprimé, la modification ne sera visible qu'après la création d'une nouvelle session. 
    
Une autre technique pour l'ajout d'un fournisseur de services, en particulier un fournisseur de banque de messages, à un profil implique la création d'un identificateur d'entrée pour le fournisseur. Étant donné que la création d'un identificateur d'entrée nécessite une connaissance de son format, cette technique peut être utilisée uniquement si le fournisseur de services a effectué le format d'identificateur d'entrée public. 
  
Avec l'identificateur d'entrée qui vient d'être construit, un client peut appeler [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md). MAPI crée automatiquement une section de profil dans le profil du fournisseur de services, mais ne l'ajoute pas à un service de messagerie. 
  
Certains services de messagerie n'autorisent pas ce type de modification dynamique; le service de messagerie peut être pris en charge ou non. La possibilité d'accéder directement aux sections de profil privé d'un service de messagerie est une autre fonctionnalité qui peut ou non être prise en charge. Si le service de messagerie que vous utilisez autorise un tel accès, il publiera le **GUID** qui représente la section privée dans MAPISVC. inf. Vous pouvez transmettre ce **GUID** dans un appel à [IProviderAdmin:: OpenProfileSection](iprovideradmin-openprofilesection.md) pour accéder à la section profil. 
  


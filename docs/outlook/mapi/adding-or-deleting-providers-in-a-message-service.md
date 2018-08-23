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
ms.openlocfilehash: 569c9d8a7ed3f56d88d83ea6fdac4477d39e50a2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569483"
---
# <a name="adding-or-deleting-providers-in-a-message-service"></a>Ajout ou suppression de fournisseurs dans un service de messagerie

  
  
**S’applique à**: Outlook 2013 | Outlook 2016 
  
Pour ajouter ou supprimer des fournisseurs de services dans un service de message, utilisez la [IProviderAdmin : IUnknown](iprovideradminiunknown.md) interface. Vous pouvez récupérer un pointeur **IProviderAdmin** en appelant [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md). Le tableau de fournisseur, accessible par le biais [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md), répertorie les informations sur les fournisseurs de services actuellement installée dans le service de message. Clients et fournisseurs de services peuvent utiliser la table des fournisseurs de d’accéder au nom du fournisseur fichier DLL, par exemple, ou **MAPIUID**, nom complet et du type du fournisseur, ainsi que les informations sur le service de message. Pour plus d’informations, voir [Les Tables de fournisseur](provider-tables.md).
  
 **Pour ajouter ou supprimer un fournisseur de services dans un service de message**
  
1. Appelez la méthode **AdminServices** pour accéder à un objet de l’administration de service de message. 
    
2. Appelez [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) pour accéder à la table de service de message. 
    
3. Créer une restriction de propriété à l’aide d’une structure [SPropertyRestriction](spropertyrestriction.md) qui correspond à **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ou **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) avec le nom du service de message à modifié. 
    
4. Appeler la méthode [IMAPITable::FindRow](imapitable-findrow.md) de la table de service de message pour localiser la ligne dans la table qui représente le service message ciblé. 
    
5. Appelez [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) pour récupérer un pointeur **IProviderAdmin** . Passez la colonne **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) à partir de la ligne de tableau de service de message en tant que paramètre _lpUID_ . 
    
6. Appelez [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) pour accéder à la table des fournisseurs. 
    
7. Créer une restriction de propriété à l’aide d’une structure SPropertyRestriction qui correspond à **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ou **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) avec le nom du fournisseur de services à ajouté ou supprimé. 
    
8. Appeler la méthode [IMAPITable::FindRow](imapitable-findrow.md) de la table fournisseur pour localiser la ligne dans la table qui représente le fournisseur de services ciblé. 
    
9. Appelez [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md) pour ajouter le fournisseur ou [IProviderAdmin::DeleteProvider](iprovideradmin-deleteprovider.md) en supprimer le service de message. Pour **CreateProvider**, passez la propriété **PR_DISPLAY_NAME** du fournisseur en tant que paramètre _lpszProvider_ . Pour des méthodes, transmettez propriété **PR_SERVICE_UID** du fournisseur en tant que paramètre _lpUID_ . Une fois que le fournisseur de services a été ajouté ou supprimé, la modification ne sera pas apparente jusqu'à ce qu’une nouvelle session est créée. 
    
Une autre technique à l’ajout d’un fournisseur de services, notamment un fournisseur de magasin de message, à un profil implique la construction d’un identificateur d’entrée pour le fournisseur. Étant donné que la construction d’un identificateur d’entrée nécessite une connaissance de son format, cette technique peut uniquement être utilisée si le fournisseur de services a effectué son format d’identificateur d’entrée public. 
  
Avec l’identificateur d’entrée nouvellement construit, un client peut appeler [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md). MAPI crée une section de profil dans le profil pour le fournisseur de services automatiquement, mais ne l’ajoute pas à un service de message. 
  
Certains services message ne permettent pas de ce type de modification dynamique ; Si elle est prise en charge dépend du service de message. Une autre fonctionnalité qui peut ou ne peut pas être pris en charge est la possibilité d’accéder directement aux sections de profil privé d’un service de message. Si vous utilisez le service de message permet ce type d’accès, il sera publier le **GUID** qui représente la section privée dans MAPISVC.INF. Vous pouvez passer ce **GUID** dans un appel à [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) pour accéder à la section de profil. 
  


---
title: Ajout ou suppression de fournisseurs dans un service de messagerie
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 44bb4d34-ca96-4d5a-93fe-85e09bd7971d
ms.openlocfilehash: da5671d536155211e789d8037cdb08d8386703a5
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63522927"
---
# <a name="adding-or-deleting-providers-in-a-message-service"></a>Ajout ou suppression de fournisseurs dans un service de messagerie

**S’applique à** : Outlook 2013 | Outlook 2016
  
Pour ajouter ou supprimer des fournisseurs de services dans un service de messagerie, utilisez l’interface [IProviderAdmin : IUnknown](iprovideradminiunknown.md) . Vous pouvez récupérer un **pointeur IProviderAdmin** en appelant [IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md). La table fournisseur, accessible via [IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md), répertorie les informations sur les fournisseurs de services actuellement installés dans le service de messagerie. Les clients et les fournisseurs de services peuvent utiliser la table des fournisseurs pour accéder au nom du fichier DLL fournisseur, par exemple, ou au **MAPIUID**, au nom complet et au type du fournisseur, ainsi qu’aux informations sur le service de messagerie. Pour plus d’informations, voir [Tables des fournisseurs](provider-tables.md).
  
## <a name="to-add-or-delete-a-service-provider-in-a-message-service"></a>Pour ajouter ou supprimer un fournisseur de services dans un service de messagerie
  
1. Appelez la **méthode AdminServices pour** accéder à un objet d’administration de service de message.

2. [Appelez IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) pour accéder à la table de service de message.

3. Créez une restriction de propriété à l’aide d’une structure [SPropertyRestriction](spropertyrestriction.md) qui correspond à **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ou **PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md)) avec le nom du service de message à modifier.

4. Appelez la méthode [IMAPITable::FindRow](imapitable-findrow.md) de la table de service de message pour localiser la ligne dans le tableau qui représente le service de message ciblé.

5. [Appelez IMsgServiceAdmin::AdminProviders](imsgserviceadmin-adminproviders.md) pour récupérer un **pointeur IProviderAdmin**. Passez la colonne **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) à partir de la ligne de table de service de message en tant que paramètre _lpUID_ .

6. [Appelez IProviderAdmin::GetProviderTable](iprovideradmin-getprovidertable.md) pour accéder à la table du fournisseur.

7. Créez une restriction de propriété à l’aide d’une structure SPropertyRestriction qui correspond à **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) ou **PR_PROVIDER_DISPLAY** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md)) avec le nom du fournisseur de services à ajouter ou à supprimer.

8. Appelez la méthode [IMAPITable::FindRow](imapitable-findrow.md) de la table fournisseur pour localiser la ligne dans le tableau qui représente le fournisseur de services ciblé.

9. Appelez [IProviderAdmin::CreateProvider](iprovideradmin-createprovider.md) pour ajouter le fournisseur ou [IProviderAdmin::D eleteProvider](iprovideradmin-deleteprovider.md) pour le supprimer du service de message. Pour **CreateProvider**, passez la propriété **PR_DISPLAY_NAME fournisseur en** tant que _paramètre lpszProvider_ . Pour l’une ou l’autre méthode, passez la **propriété PR_SERVICE_UID du** fournisseur en tant que _paramètre lpUID_ . Une fois que le fournisseur de services a été ajouté ou supprimé, la modification n’apparaît pas tant qu’une nouvelle session n’est pas créée.

Une autre technique d’ajout d’un fournisseur de services, en particulier un fournisseur de magasins de messages, à un profil implique la construction d’un identificateur d’entrée pour le fournisseur. Étant donné que la construction d’un identificateur d’entrée nécessite une connaissance de son format, cette technique ne peut être utilisée que si le fournisseur de services a rendu son format d’identificateur d’entrée public.
  
Avec l’identificateur d’entrée nouvellement créé, un client peut appeler [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md). MAPI crée automatiquement une section de profil dans le profil pour le fournisseur de services, mais ne l’ajoute pas à un service de messagerie.
  
Certains services de message n’autorisent pas ce type de modification dynamique ; le service de message doit décider s’il est pris en charge ou non. Une autre fonctionnalité prise en charge est la possibilité d’accéder directement aux sections de profil privé d’un service de message. Si le service de message que vous utilisez autorise un tel accès, il publiera le **GUID** qui représente la section privée dans MAPISVC.INF. Vous pouvez transmettre ce **GUID** dans un appel à [IProviderAdmin::OpenProfileSection](iprovideradmin-openprofilesection.md) pour accéder à la section de profil.
  
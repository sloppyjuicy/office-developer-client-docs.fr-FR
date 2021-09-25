---
title: Accès aux objets à l’aide de la session
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ecada707-2960-41ec-be7e-619cad257c57
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: da0ee486979d02f70f24fed2e6e63a5ce5277564
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59556979"
---
# <a name="accessing-objects-by-using-the-session"></a>Accès aux objets à l’aide de la session

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le pointeur de session que vous recevez de votre appel [à MAPILogonEx](mapilogonex.md) peut être utilisé pour accéder à un large éventail d’objets. Le tableau suivant répertorie les méthodes utilisées pour accéder à différents objets : 
  
|**Object**|**Méthode session**|
|:-----|:-----|
|Section Profil  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Magasin de messages  <br/> |[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) <br/> |
|Carnet d’adresses  <br/> |[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) <br/> |
|Objet d’administration du service de message  <br/> |[IMAPISession::AdminServices](imapisession-adminservices.md) <br/> |
|Dossier, message, conteneur de carnet d’adresses, liste de distribution ou utilisateur de messagerie  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
   
Avec la **méthode OpenEntry et** un identificateur d’entrée valide, vous pouvez ouvrir n’importe quel objet fournisseur de carnet d’adresses ou de magasin de messages. Il existe **d’autres méthodes OpenEntry** dans MAPI, en plus de la méthode **IMAPISession.** **OpenEntry est** implémenté dans les objets suivants : 
  
|**Object**|**Méthode**|
|:-----|:-----|
|Objet d’accès au fournisseur de carnet d’adresses  <br/> |[IABLogon::OpenEntry](iablogon-openentry.md) <br/> |
|Carnet d’adresses  <br/> |[IAddrBook::OpenEntry](iaddrbook-openentry.md) <br/> |
|Conteneur de carnet d’adresses  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Session  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
|Magasin de messages  <br/> |[IMsgStore::OpenEntry](imsgstore-openentry.md) <br/> |
|Objet d’ouverture de messagerie du fournisseur de magasins de messages  <br/> |[IMSLogon::OpenEntry](imslogon-openentry.md) <br/> |
|Folder  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Objet Support  <br/> |[IMAPISupport::OpenEntry](imapisupport-openentry.md) <br/> |
   
Certaines **méthodes OpenEntry** nécessitent l’ouverture d’un identificateur d’entrée de l’objet, tout comme **IMAPISession::OpenEntry**; d’autres méthodes permettent de spécifier la valeur NULL. Un identificateur d’entrée NULL est interprété différemment en fonction de l’objet. Par exemple, lorsque vous appelez **IAddrBook::OpenEntry** avec un identificateur d’entrée NULL, MAPI ouvre le conteneur racine du carnet d’adresses. La méthode **OpenEntry** de la boutique de messages se comporte de la même manière . il ouvre le dossier racine de la boutique de messages. **IMAPIContainer::OpenEntry**, implémenté par les conteneurs de dossiers et de carnet d’adresses, peut renvoyer MAPI_E_INVALID_PARAMETER ou le conteneur racine, en fonction de l’implémenteur. 
  
En plus de refuser une valeur NULL pour l’identificateur d’entrée, la méthode **OpenEntry** de la session diffère des autres méthodes **OpenEntry,** car son travail n’est pas d’ouvrir des objets. Au lieu de cela, il examine l’identificateur d’entrée et fait suivre l’appel à une autre méthode **OpenEntry** implémentée par le fournisseur de services approprié. Par exemple, si vous appelez **IMAPISession::OpenEntry** avec l’identificateur d’entrée d’un message, MAPI appelle la méthode **IMSLogon::OpenEntry** de la boutique de messages responsable du message. 
  
Outre l’utilisation de la session pour ouvrir des objets, les clients l’utilisent pour les comparer. La [méthode IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) compare les objets en comparant leurs identificateurs d’entrée. Si les structures [MAPIUID](mapiuid.md) contenues dans les identificateurs d’entrée appartiennent au même fournisseur de services, MAPI le fait. **CompareEntryIDs renvoie une** valeur d’erreur lorsque les deux identificateurs d’entrée ne correspondent pas. Bien que cette méthode puisse comparer les identificateurs d’entrée qui appartiennent à n’importe quel type d’objet, **CompareEntryIDs** fonctionne mieux pour les objets de niveau supérieur tels que les magasins de messages et les conteneurs de carnet d’adresses. Pour comparer des objets de niveau inférieur, comparez directement les clés de recherche des objets (**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))) ou les clés d’enregistrement (**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))). 
  
Comme **OpenEntry**, **CompareEntryIDs** est implémenté par plusieurs objets. Choisissez la **méthode OpenEntry** et **CompareEntryID** à utiliser en fonction de la quantité d’informations que vous avez sur l’objet ou les objets à ouvrir ou à comparer. Utilisez les instructions suivantes lors du choix de la méthode d’interface à appeler : 
  
- Si vous n’avez aucune information sur les objets cibles, appelez [IMAPISession::OpenEntry](imapisession-openentry.md) ou [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md). Cette approche permet d’accéder à n’importe quel objet, mais elle est la plus lente des trois.
    
- Si vous savez que les objets cibles sont des entrées de carnet d’adresses plutôt que, par exemple, des dossiers, appelez la méthode [IAddrBook::OpenEntry](iaddrbook-openentry.md) ou [IAddrBook::CompareEntryIDs.](iaddrbook-compareentryids.md) **IAddrBook::OpenEntry** ouvre le conteneur racine du carnet d’adresses lorsque NULL est spécifié en tant qu’objet cible. Cette approche permet d’accéder à n’importe quel objet de carnet d’adresses et est plus rapide que d’utiliser **IMAPISession,** mais plus lente que d’utiliser **IMAPIContainer**.
    
- Si l’identificateur d’entrée utilisé est un identificateur d’entrée à court terme ou si vous savez que les objets cibles appartiennent à un conteneur ou dossier de carnet d’adresses particulier, appelez la méthode [IMAPIContainer::OpenEntry.](imapicontainer-openentry.md) Cette approche permet d’obtenir les performances les plus rapides, mais permet d’accéder uniquement aux objets d’un conteneur ou d’un dossier spécifique. 
    


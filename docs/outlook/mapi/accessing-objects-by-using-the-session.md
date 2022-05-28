---
title: Accès aux objets à l’aide de la session
description: Décrit comment accéder aux objets à l’aide du pointeur de session reçu de l’appel à MAPILogonEx.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: ecada707-2960-41ec-be7e-619cad257c57
ms.openlocfilehash: 18c14760c210f923c7dfd7d87fc660e75a37b4ea
ms.sourcegitcommit: 8c8e4ac05a6612dd5c815ab18ba40e56a6ba839d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/28/2022
ms.locfileid: "65769553"
---
# <a name="accessing-objects-by-using-the-session"></a>Accès aux objets à l’aide de la session

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le pointeur de session que vous recevez de votre appel à [MAPILogonEx](mapilogonex.md) peut être utilisé pour accéder à un large éventail d’objets. Le tableau suivant répertorie les méthodes utilisées pour accéder à différents objets : 
  
|**Object**|**Méthode de session**|
|:-----|:-----|
|Section Profil  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Magasin de messages  <br/> |[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) <br/> |
|Carnet d’adresses  <br/> |[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) <br/> |
|Objet d’administration du service message  <br/> |[IMAPISession::AdminServices](imapisession-adminservices.md) <br/> |
|Dossier, message, conteneur de carnet d’adresses, liste de distribution ou utilisateur de messagerie  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
   
Avec la méthode **OpenEntry** et un identificateur d’entrée valide, vous pouvez ouvrir n’importe quel objet fournisseur de carnet d’adresses ou de magasin de messages. Il existe d’autres méthodes **OpenEntry** dans MAPI, en plus de la méthode **IMAPISession** . **OpenEntry** est implémenté dans les objets suivants : 
  
|**Object**|**Méthode**|
|:-----|:-----|
|Objet d’ouverture de session du fournisseur de carnet d’adresses  <br/> |[IABLogon::OpenEntry](iablogon-openentry.md) <br/> |
|Carnet d’adresses  <br/> |[IAddrBook::OpenEntry](iaddrbook-openentry.md) <br/> |
|Conteneur de carnet d’adresses  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Session  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
|Magasin de messages  <br/> |[IMsgStore::OpenEntry](imsgstore-openentry.md) <br/> |
|Objet d’ouverture de session du fournisseur du magasin de messages  <br/> |[IMSLogon::OpenEntry](imslogon-openentry.md) <br/> |
|Folder  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Objet support  <br/> |[IMAPISupport::OpenEntry](imapisupport-openentry.md) <br/> |
   
Certaines méthodes **OpenEntry** nécessitent l’ouverture d’un identificateur d’entrée de l’objet, tout comme **IMAPISession::OpenEntry** ; d’autres méthodes permettent de spécifier null. Un identificateur d’entrée NULL est interprété différemment en fonction de l’objet. Par exemple, lorsque vous appelez **IAddrBook::OpenEntry** avec un identificateur d’entrée NULL, MAPI ouvre le conteneur racine du carnet d’adresses. La méthode **OpenEntry** du magasin de messages se comporte de la même façon ; il ouvre le dossier racine du magasin de messages. **IMAPIContainer::OpenEntry**, implémenté par les dossiers et les conteneurs de carnets d’adresses, peut retourner MAPI_E_INVALID_PARAMETER ou le conteneur racine, en fonction de l’implémenteur. 
  
En plus de désallouer une valeur NULL pour l’identificateur d’entrée, la méthode **OpenEntry** de la session diffère des autres méthodes **OpenEntry** , car son travail n’est pas d’ouvrir des objets. Au lieu de cela, il examine l’identificateur d’entrée et transfère l’appel à une autre méthode **OpenEntry** implémentée par le fournisseur de services approprié. Par exemple, si vous appelez **IMAPISession::OpenEntry** avec l’identificateur d’entrée d’un message, MAPI appelle la méthode **IMSLogon::OpenEntry** du magasin de messages responsable du message. 
  
En plus d’utiliser la session pour ouvrir des objets, les clients l’utilisent pour les comparer. La méthode [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) compare les objets en comparant leurs identificateurs d’entrée. Si les structures [MAPIUID](mapiuid.md) contenues dans les identificateurs d’entrée appartiennent au même fournisseur de services, MAPI transfère l’appel à ce fournisseur. **CompareEntryIDs** retourne une valeur d’erreur lorsque les deux identificateurs d’entrée ne correspondent pas. Bien que cette méthode puisse comparer les identificateurs d’entrée qui appartiennent à n’importe quel type d’objet, **CompareEntryIDs** fonctionne mieux pour les objets de niveau supérieur tels que les magasins de messages et les conteneurs de carnets d’adresses. Pour comparer des objets de niveau inférieur, comparez directement les clés de recherche des objets (**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))) ou les clés d’enregistrement (**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))). 
  
Comme **OpenEntry**, **CompareEntryIDs** est implémenté par plusieurs objets. Choisissez la méthode **OpenEntry** et **CompareEntryID** à utiliser en fonction de la quantité d’informations dont vous disposez sur l’objet ou les objets à ouvrir ou à comparer. Utilisez les instructions suivantes lors de la décision de la méthode d’interface à appeler : 
  
- Si vous n’avez aucune information sur les objets cibles, appelez [IMAPISession::OpenEntry](imapisession-openentry.md) ou [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md). Cette approche permet d’accéder à n’importe quel objet, mais est la plus lente des trois.
    
- Si vous savez que les objets cibles sont des entrées de carnet d’adresses plutôt que, par exemple, des dossiers, appelez la méthode [IAddrBook::OpenEntry](iaddrbook-openentry.md) ou [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) . **IAddrBook::OpenEntry** ouvre le conteneur racine du carnet d’adresses lorsque NULL est spécifié comme objet cible. Cette approche permet d’accéder à n’importe quel objet de carnet d’adresses et est plus rapide que l’utilisation **d’IMAPISession**, mais plus lente que l’utilisation **d’IMAPIContainer**.
    
- Si l’identificateur d’entrée utilisé est un identificateur d’entrée à court terme ou si vous savez que les objets cibles appartiennent à un conteneur ou un dossier de carnet d’adresses particulier, appelez la méthode [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) . Cette approche génère les performances les plus rapides, mais permet d’accéder uniquement aux objets d’un conteneur ou d’un dossier spécifique. 
    


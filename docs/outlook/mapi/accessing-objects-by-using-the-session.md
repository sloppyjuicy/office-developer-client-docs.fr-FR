---
title: Accès aux objets à l'aide de la session
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ecada707-2960-41ec-be7e-619cad257c57
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: a76397b74642aedf9ad5c9704735d869f61db7e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410538"
---
# <a name="accessing-objects-by-using-the-session"></a>Accès aux objets à l'aide de la session

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Le pointeur de session que vous recevez de votre appel à [MAPILogonEx](mapilogonex.md) peut être utilisé pour accéder à un large éventail d'objets. Le tableau suivant répertorie les méthodes utilisées pour accéder à divers objets: 
  
|**Object**|**Session, méthode**|
|:-----|:-----|
|Section Profil  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Banque de messages  <br/> |[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) <br/> |
|Carnet d’adresses  <br/> |[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) <br/> |
|Objet d'administration du service de messagerie  <br/> |[IMAPISession::AdminServices](imapisession-adminservices.md) <br/> |
|Dossier, message, conteneur de carnet d'adresses, liste de distribution ou utilisateur de messagerie  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
   
Avec la méthode **OpenEntry** et un identificateur d'entrée valide, vous pouvez ouvrir un objet de carnet d'adresses ou de fournisseur de banque de messages. Il existe d'autres méthodes **OpenEntry** dans MAPI, en plus de la méthode **IMAPISession** . **OpenEntry** est implémenté dans les objets suivants: 
  
|**Object**|**Méthode**|
|:-----|:-----|
|Objet de connexion du fournisseur de carnet d'adresses  <br/> |[IABLogon::OpenEntry](iablogon-openentry.md) <br/> |
|Carnet d’adresses  <br/> |[IAddrBook::OpenEntry](iaddrbook-openentry.md) <br/> |
|Conteneur de carnet d'adresses  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Session  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
|Banque de messages  <br/> |[IMsgStore::OpenEntry](imsgstore-openentry.md) <br/> |
|Objet de connexion du fournisseur de banque de messages  <br/> |[IMSLogon::OpenEntry](imslogon-openentry.md) <br/> |
|Folder  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Objet support  <br/> |[IMAPISupport::OpenEntry](imapisupport-openentry.md) <br/> |
   
Certaines méthodes **OpenEntry** nécessitent l'ouverture d'un identificateur d'entrée de l'objet, comme le fait **IMAPISession:: OpenEntry**; d'autres méthodes permettent de spécifier NULL. Un identificateur d'entrée NULL est interprété différemment en fonction de l'objet. Par exemple, lorsque vous appelez **IAddrBook:: OpenEntry** avec un identificateur d'entrée null, MAPI ouvre le conteneur racine du carnet d'adresses. La méthode **OpenEntry** de la Banque de messages se comporte de la même manière; il ouvre le dossier racine de la Banque de messages. **IMAPIContainer:: OpenEntry**, implémenté par les dossiers et les conteneurs du carnet d'adresses, peut renvoyer MAPI_E_INVALID_PARAMETER ou le conteneur racine, en fonction de l'implémentation. 
  
En plus de n'autoriser aucune valeur NULL pour l'identificateur d'entrée, la méthode **OpenEntry** de la session diffère des autres méthodes **OpenEntry** , car sa tâche n'ouvre pas les objets. Au lieu de cela, il examine l'identificateur d'entrée et transfère l'appel à une autre méthode **OpenEntry** implémentée par le fournisseur de services approprié. Par exemple, si vous appelez **IMAPISession:: OpenEntry** avec l'identificateur d'entrée d'un message, MAPI appelle la méthode **IMSLogon:: OpenEntry** de la Banque de messages responsable du message. 
  
En plus de l'utilisation de la session pour ouvrir des objets, les clients l'utilisent pour les comparer. La méthode [IMAPISession:: CompareEntryIDs](imapisession-compareentryids.md) compare les objets en comparant leurs identificateurs d'entrée. Si les structures [MAPIUID](mapiuid.md) contenues dans les identificateurs d'entrée appartiennent au même fournisseur de services, MAPI transmet l'appel à ce fournisseur. **CompareEntryIDs** renvoie une valeur d'erreur lorsque les deux identificateurs d'entrée ne correspondent pas. Bien que cette méthode puisse comparer des identificateurs d'entrée appartenant à n'importe quel type d'objet, **CompareEntryIDs** fonctionne mieux pour les objets de niveau supérieur tels que les magasins de messages et les conteneurs de carnet d'adresses. Pour comparer les objets de niveau inférieur, comparez directement les clés de recherche des objets (**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))) ou les clés d'enregistrement (**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))). 
  
Comme **OpenEntry**, **CompareEntryIDs** est implémenté par plusieurs objets. Choisissez la méthode **OpenEntry** et **CompareEntryID** à utiliser en fonction de la quantité d'informations que vous avez sur l'objet ou les objets à ouvrir ou à comparer. Suivez les instructions ci-dessous pour choisir la méthode d'interface à appeler: 
  
- Si vous n'avez aucune information sur les objets cibles, appelez [IMAPISession:: OpenEntry](imapisession-openentry.md) ou [IMAPISession:: CompareEntryIDs](imapisession-compareentryids.md). Cette approche permet d'accéder à n'importe quel objet, mais est le plus lent parmi les trois.
    
- Si vous êtes certain que les objets cibles sont des entrées de carnet d'adresses et non, par exemple, des dossiers, appelez la méthode [IAddrBook:: OpenEntry](iaddrbook-openentry.md) ou [IAddrBook:: CompareEntryIDs](iaddrbook-compareentryids.md) . **IAddrBook:: OpenEntry** ouvre le conteneur racine du carnet d'adresses lorsque null est spécifié en tant qu'objet cible. Cette approche permet d'accéder à n'importe quel objet de carnet d'adresses et est plus rapide que l'utilisation de **IMAPISession**, mais plus lente que l'utilisation de **IMAPIContainer**.
    
- Si l'identificateur d'entrée utilisé est un identificateur d'entrée à court terme ou si vous êtes sûr que les objets cibles appartiennent à un conteneur ou dossier de carnet d'adresses particulier, appelez la méthode [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md) . Cette approche offre les performances les plus rapides, mais autorise uniquement l'accès aux objets d'un conteneur ou d'un dossier spécifique. 
    


---
title: Accès aux objets à l’aide de la Session
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ecada707-2960-41ec-be7e-619cad257c57
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ee20e73e5bc7bb6854b956da541d3a318a267d0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19782886"
---
# <a name="accessing-objects-by-using-the-session"></a>Accès aux objets à l’aide de la Session

  
  
**S’applique à**: Outlook 
  
Le pointeur de session provenant de l’appel de [MAPILogonEx](mapilogonex.md) peut être utilisé pour accéder à une grande variété d’objets. Le tableau suivant répertorie les méthodes qui permettent d’accéder aux objets différents : 
  
|**Objet**|**Méthode de session**|
|:-----|:-----|
|Section de profil  <br/> |[IMAPISession::OpenProfileSection](imapisession-openprofilesection.md) <br/> |
|Banque de messages  <br/> |[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) <br/> |
|Carnet d’adresses  <br/> |[IMAPISession::OpenAddressBook](imapisession-openaddressbook.md) <br/> |
|Objet d’administration de service de message  <br/> |[IMAPISession::AdminServices](imapisession-adminservices.md) <br/> |
|Dossier, message, conteneur de carnet d’adresses, liste de distribution ou utilisateur de messagerie  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
   
Avec la méthode **OpenEntry** et un identificateur d’entrée valide, vous pouvez ouvrir n’importe quel objet de fournisseur de magasin de message ou de carnet d’adresses. Il existe d’autres méthodes **OpenEntry** MAPI, en plus de la méthode **IMAPISession** . **OpenEntry** est implémentée dans les objets suivants : 
  
|**Objet**|**M?thode**|
|:-----|:-----|
|Objet d’ouverture de session du fournisseur de carnet d’adresses  <br/> |[IABLogon::OpenEntry](iablogon-openentry.md) <br/> |
|Carnet d’adresses  <br/> |[IAddrBook::OpenEntry](iaddrbook-openentry.md) <br/> |
|Conteneur de carnet d’adresses  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Session  <br/> |[IMAPISession::OpenEntry](imapisession-openentry.md) <br/> |
|Banque de messages  <br/> |[IMsgStore::OpenEntry](imsgstore-openentry.md) <br/> |
|Objet d’ouverture de session du fournisseur de banque de messages  <br/> |[IMSLogon::OpenEntry](imslogon-openentry.md) <br/> |
|Folder  <br/> |[IMAPIContainer::OpenEntry](imapicontainer-openentry.md) <br/> |
|Objet de prise en charge  <br/> |[IMAPISupport::OpenEntry](imapisupport-openentry.md) <br/> |
   
Certaines méthodes **OpenEntry** nécessitent un identificateur d’entrée de l’objet à ouvrir, comme **IMAPISession::OpenEntry**; autres méthodes autorisent NULL doit être spécifié. Un identificateur d’entrée NULL est interprété différemment en fonction de l’objet. Par exemple, lorsque vous appelez **IAddrBook::OpenEntry** avec un identificateur d’entrée NULL, MAPI ouvre le conteneur racine du carnet d’adresses. Méthode de **OpenEntry** de la banque de messages se comporte de la même façon ; Il ouvre le dossier racine de la banque de messages. **IMAPIContainer::OpenEntry**, implémentée par les dossiers et les conteneurs de carnet d’adresses, peut retourner MAPI_E_INVALID_PARAMETER ou le conteneur racine, en fonction de l’implémentation. 
  
Outre la désactivation d’une valeur NULL pour l’identificateur d’entrée, **OpenEntry** méthode de la session est différente autres méthodes **OpenEntry** car sa tâche n’est ne pas à ouvrir des objets. Au lieu de cela, elle examine l’identificateur d’entrée et transfère l’appel vers une autre méthode **OpenEntry** implémentée par le fournisseur de services approprié. Par exemple, si vous appelez **IMAPISession::OpenEntry** avec l’identificateur d’entrée d’un message, MAPI appelle la méthode **IMSLogon::OpenEntry** de la banque de messages responsable pour le message. 
  
Outre l’utilisation de la session à ouvrir des objets, clients utilisent pour les comparer. La méthode [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) compare des objets en comparant les identificateurs d’entrée. Si les structures [MAPIUID](mapiuid.md) contenues dans les identificateurs d’entrée appartiennent au même fournisseur de services, MAPI transfère l’appel à ce fournisseur. **CompareEntryIDs** renvoie une valeur d’erreur lorsque les identificateurs de deux entrée ne correspondent pas. Bien que cette méthode peut comparer les identificateurs d’entrée qui appartiennent à n’importe quel type d’objet, **CompareEntryIDs** est idéale pour les objets de niveau supérieur tels que les banques de messages et les conteneurs de carnet d’adresses. Pour comparer des objets de niveau inférieur, comparer directement les clés de recherche des objets (**clé PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))) ou sur Enregistrer (**PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))). 
  
Comme **OpenEntry**, **CompareEntryIDs** est implémentée par plusieurs objets. Choisir la méthode à utiliser en fonction de la quantité d’informations que vous avez sur l’ou les objets d’être ouvert ou par rapport **OpenEntry** et **CompareEntryID** . Utilisez les instructions suivantes lorsque vous décidez de la méthode d’interface à appeler : 
  
- Si vous ne disposez aucun informations sur les objets cibles, appelez [IMAPISession::OpenEntry](imapisession-openentry.md) ou [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md). Cette approche permet d’accéder à n’importe quel objet, mais est la plus lente des trois.
    
- Si vous savez que les objets cibles sont des entrées de carnet d’adresses plutôt que, par exemple, les dossiers, appelez la méthode [IAddrBook::OpenEntry](iaddrbook-openentry.md) ou [IAddrBook::CompareEntryIDs](iaddrbook-compareentryids.md) . **IAddrBook::OpenEntry** ouvre le conteneur racine du carnet d’adresses lorsque NULL est spécifiée en tant que l’objet cible. Cette approche permet d’accéder à n’importe quel objet du carnet d’adresses et est plus rapide que **IMAPISession**, mais plus lente qu’avec **IMAPIContainer**.
    
- Si l’identificateur d’entrée utilisé est un identificateur d’entrée à court terme, ou si vous savez que les objets cibles appartiennent à un conteneur de carnet d’adresses spécifique ou un dossier, appelez la méthode [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) . Cette approche offre les meilleures performances, mais autorise l’accès uniquement aux objets dans un conteneur spécifique ou un dossier. 
    


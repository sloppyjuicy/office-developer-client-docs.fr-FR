---
title: CrawlSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CrawlSourceSupportMask
api_type:
- COM
ms.assetid: d0a2f7ea-df6a-89e8-18c2-ac92e0a20edc
description: CrawlSourceSupportMask spécifie si Outlook doit analyser les dossiers d’une magasin, y compris les dossiers Contacts, Calendrier et Tâches, au démarrage pour remplir le volet de navigation.
ms.openlocfilehash: 81b5cc0d6ed45119c962b66b51cdbe840bf75447
ms.sourcegitcommit: 571b0c4770415afb62c4e9b35960ba51bc94893c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/16/2022
ms.locfileid: "63521560"
---
# <a name="crawlsourcesupportmask"></a>CrawlSourceSupportMask

**S’applique à** : Outlook 2013 | Outlook 2016
  
Spécifie si Microsoft Office Outlook doit analyser les dossiers d’une magasin, y compris les dossiers Contacts, Calendrier et Tâches, au démarrage pour remplir le volet de navigation.
  
## <a name="quick-info"></a>Informations rapides

|**Item**|**Valeur**|
|:-----|:-----|
|Exposé sur :  <br/> |[IMsgStore : objet IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Créé par :  <br/> |Fournisseur du Store  <br/> |
|Accessible par :  <br/> |Outlook clients et autres clients  <br/> |
|Type de propriété :  <br/> |PT_LONG  <br/> |
|Type d’accès :  <br/> |En lecture seule ou en lecture/écriture en fonction du fournisseur du magasin  <br/> |

## <a name="remarks"></a>Remarques

Pour fournir l’une des fonctionnalités du magasin, le fournisseur de magasin doit implémenter [IMAPIProp : IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour l’une de ces propriétés transmises à un appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Lorsque la balise de propriété de l’une de ces propriétés est transmise à [IMAPIProp::GetProps](imapiprop-getprops.md), le fournisseur de magasins doit également renvoyer la valeur de propriété correcte. Les fournisseurs du Store peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés.
  
Pour récupérer la valeur de cette propriété, le client doit d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifier cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur. Lorsque vous appelez [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d’entrée _lppPropNames_ :
  
|**Item**|**Valeur**|
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind :  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName :  <br/> |L"CrawlSourceSupportMask »  <br/> |

Cette propriété permet aux fournisseurs de magasins de spécifier si Outlook doit analyser différents dossiers dans une boutique. Il est utilisé au démarrage lorsque Outlook les dossiers existants sur chaque magasin ouvert pour **remplir le volet** de navigation . Outlook la présence et la valeur de cette propriété dans une boutique avant de lancer l’analyse.
  
Par défaut, cette propriété n’est pas exposée dans une boutique, ce qui signifie Outlook pouvez analyser les dossiers de la boutique. Si la propriété est exposée, les valeurs possibles sont les suivantes :
  
```

enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

CSM_DEFAULT
  
- Outlook pouvez analyser les dossiers de la boutique.

CSM_DO_NOT_CRAWL
  
- Outlook ne doit pas analyser les dossiers de la boutique.

CSM_CLIENT_DO_NOT_CHANGE
  
- N’autorisez pas les clients à modifier cette propriété sur le store. Notez que la constante **est CSM_CLIENT_DO_NOT_CHANGE** référence future et n’est pas implémentée actuellement. Pour l’instant, un magasin peut empêcher les clients de modifier cet indicateur en encodant en dur la valeur que la boutique renvoie pour cette propriété.

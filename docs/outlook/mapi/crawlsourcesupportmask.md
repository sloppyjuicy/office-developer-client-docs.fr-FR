---
title: CrawlSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CrawlSourceSupportMask
api_type:
- COM
ms.assetid: d0a2f7ea-df6a-89e8-18c2-ac92e0a20edc
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: cc3fcedb73b4acbd85529615d857403b4c268f3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420912"
---
# <a name="crawlsourcesupportmask"></a>CrawlSourceSupportMask

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique si Microsoft Office Outlook doit analyser les dossiers d'une banque, y compris les dossiers contacts, calendrier et tâches, au démarrage pour renseigner le volet de navigation.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exposé sur:  <br/> |[IMsgStore: objet IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Créé par:  <br/> |Fournisseur de magasin  <br/> |
|Accès par:  <br/> |Outlook et d'autres clients  <br/> |
|Type de propriété:  <br/> |PT_LONG  <br/> |
|Type d'accès:  <br/> |Lecture seule ou lecture/écriture en fonction du fournisseur de la Banque  <br/> |
   
## <a name="remarks"></a>Remarques

Pour fournir l'une des fonctionnalités de magasin, le fournisseur de banque doit implémenter [IMAPIProp: IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour l'une des propriétés transmises à un appel [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) . Lorsque la balise de propriété de l'une de ces propriétés est transmise à [IMAPIProp:: GetProps](imapiprop-getprops.md), le fournisseur Store doit également renvoyer la valeur de propriété correcte. Les fournisseurs de magasins peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés. 
  
Pour récupérer la valeur de cette propriété, le client doit d'abord utiliser [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifier cette balise de propriété dans [IMAPIProp:: GetProps](imapiprop-getprops.md) pour obtenir la valeur. Lors de l'appel de [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d'entrée _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind. lpwstrName:  <br/> |L "CrawlSourceSupportMask"  <br/> |
   
Cette propriété permet aux fournisseurs de magasins de spécifier si Outlook doit analyser les différents dossiers d'une banque. Elle est utilisée au démarrage quand Outlook analyse les dossiers existants sur chaque banque ouverte pour remplir le volet de **navigation** ; Outlook vérifie la présence et la valeur de cette propriété sur un magasin avant de lancer l'analyse. 
  
Par défaut, cette propriété n'est pas exposée sur un magasin, ce qui signifie qu'Outlook peut analyser les dossiers de la Banque. Si la propriété est exposée, les valeurs possibles sont les suivantes:
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

CSM_DEFAULT
  
- Outlook peut analyser les dossiers de la Banque.
    
CSM_DO_NOT_CRAWL
  
- Outlook ne doit pas analyser les dossiers de la Banque.
    
CSM_CLIENT_DO_NOT_CHANGE
  
- Ne pas autoriser les clients à modifier cette propriété sur le magasin. Notez que la constante **CSM_CLIENT_DO_NOT_CHANGE** est destinée à des fins de référence ultérieure et qu'elle n'est pas actuellement implémentée. Pour le moment, un magasin peut empêcher les clients de modifier cet indicateur en codage en dur la valeur renvoyée par la Banque pour cette propriété. 
    


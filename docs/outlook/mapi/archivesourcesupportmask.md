---
title: ArchiveSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ArchiveSourceSupportMask
api_type:
- COM
ms.assetid: e35216e0-c23f-70f2-0d5f-1ac5dc00fd8c
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 6fc5e8eb74d79d0a30ae6a423772ce741dee4562
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281591"
---
# <a name="archivesourcesupportmask"></a>ArchiveSourceSupportMask

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Indique si Microsoft Office Outlook doit analyser les dossiers d'une banque et les archiver automatiquement.
  
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
|Kind. lpwstrName:  <br/> |L "ArchiveSourceSupportMask"  <br/> |
   
Cette propriété permet aux fournisseurs de magasin de spécifier si Outlook doit analyser les dossiers d'une banque et les archiver automatiquement.
  
Par défaut, cette propriété n'est pas exposée sur un magasin, ce qui signifie qu'Outlook peut analyser les dossiers de la Banque. Si la propriété est exposée, les valeurs possibles sont les suivantes:
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

ASM_DEFAULT
  
- Outlook peut analyser les dossiers de la Banque.
    
ASM_DO_NOT_ARCHIVE
  
- Outlook ne doit pas analyser les dossiers de la Banque.
    
ASM_CLIENT_DO_NOT_CHANGE
  
- Ne pas autoriser les clients à modifier cette propriété sur le magasin. Notez que la constante **ASM_CLIENT_DO_NOT_CHANGE** est destinée à des fins de référence ultérieure et qu'elle n'est pas actuellement implémentée. Pour le moment, un magasin peut empêcher les clients de modifier cet indicateur en codage en dur la valeur renvoyée par la Banque pour cette propriété. 
    


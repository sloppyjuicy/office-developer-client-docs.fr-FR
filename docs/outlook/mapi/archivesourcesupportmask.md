---
title: ArchiveSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ArchiveSourceSupportMask
api_type:
- COM
ms.assetid: e35216e0-c23f-70f2-0d5f-1ac5dc00fd8c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2afdfffe3af123fd9ab3a2c7b06f386bd253bdae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567850"
---
# <a name="archivesourcesupportmask"></a>ArchiveSourceSupportMask

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Spécifie si Microsoft Office Outlook doit analyser les dossiers d’une boutique et les archiver automatiquement.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exposé sur :  <br/> |[IMsgStore : objet IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Créé par :  <br/> |Fournisseur du Store  <br/> |
|Accessible par :  <br/> |Outlook clients et autres clients  <br/> |
|Type de propriété :  <br/> |PT_LONG  <br/> |
|Type d’accès :  <br/> |En lecture seule ou en lecture/écriture en fonction du fournisseur du magasin  <br/> |
   
## <a name="remarks"></a>Remarques

Pour fournir l’une des fonctionnalités du magasin, le fournisseur de magasin doit implémenter [IMAPIProp : IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour l’une de ces propriétés transmises à un appel [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) Lorsque la balise de propriété pour l’une de ces propriétés est transmise à [IMAPIProp::GetProps](imapiprop-getprops.md), le fournisseur de magasin doit également renvoyer la valeur de propriété correcte. Les fournisseurs du Store peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés. 
  
Pour récupérer la valeur de cette propriété, le client doit d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifier cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur. Lorsque vous appelez [IMAPIProp::GetIDsFromNames,](imapiprop-getidsfromnames.md)spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) pointée par le paramètre d’entrée  _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind :  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName :  <br/> |L"ArchiveSourceSupportMask »  <br/> |
   
Cette propriété permet aux fournisseurs de magasins de spécifier si Outlook doivent analyser les dossiers d’une boutique et les archiver automatiquement.
  
Par défaut, cette propriété n’est pas exposée dans une boutique, ce qui signifie Outlook pouvez analyser les dossiers de la boutique. Si la propriété est exposée, les valeurs possibles sont les suivantes :
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

ASM_DEFAULT
  
- Outlook pouvez analyser les dossiers de la boutique.
    
ASM_DO_NOT_ARCHIVE
  
- Outlook ne doit pas analyser les dossiers de la boutique.
    
ASM_CLIENT_DO_NOT_CHANGE
  
- N’autorisez pas les clients à modifier cette propriété sur le store. Notez que la constante **ASM_CLIENT_DO_NOT_CHANGE** est à des références futures et n’est pas implémentée actuellement. Pour l’instant, un magasin peut empêcher les clients de modifier cet indicateur en encodant en dur la valeur que la boutique renvoie pour cette propriété. 
    


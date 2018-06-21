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
ms.openlocfilehash: 1e0c099783b4d44b1aaf746b07c77981c135ca9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/21/2018
ms.locfileid: "19782933"
---
# <a name="archivesourcesupportmask"></a>ArchiveSourceSupportMask

  
  
**S’applique à**: Outlook 
  
Indique si Microsoft Office Outlook doit analyser les dossiers dans un magasin et les archiver automatiquement.
  
## <a name="quick-info"></a>Informations rapides

|||
|:-----|:-----|
|Exposée sur :  <br/> |[IMsgStore : IMAPIProp](imsgstoreimapiprop.md) objet  <br/> |
|Créé par :  <br/> |Fournisseur de banque  <br/> |
|Accessible par :  <br/> |Outlook et autres clients  <br/> |
|Type de propriété :  <br/> |PT_LONG  <br/> |
|Type d’accès :  <br/> |En lecture seule ou en lecture/écriture, selon le fournisseur de banque  <br/> |
   
## <a name="remarks"></a>Remarques

Pour fournir une des fonctionnalités de magasin, le fournisseur de banque doit implémenter [IMAPIProp : IUnknown](imapipropiunknown.md) et renvoyer une balise de propriété valide pour une de ces propriétés passées à un appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Lorsque la balise de propriété pour une de ces propriétés est transmise à [IMAPIProp::GetProps](imapiprop-getprops.md), le fournisseur de banque doit également retourner la valeur de la propriété adéquate. Fournisseurs de magasins peuvent appeler [HrGetOneProp](hrgetoneprop.md) et [HrSetOneProp](hrsetoneprop.md) pour obtenir ou définir ces propriétés. 
  
Pour récupérer la valeur de cette propriété, le client doit d’abord utiliser [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) pour obtenir la balise de propriété, puis spécifiez cette balise de propriété dans [IMAPIProp::GetProps](imapiprop-getprops.md) pour obtenir la valeur. Lors de l’appel [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), spécifiez les valeurs suivantes pour la structure [MAPINAMEID](mapinameid.md) sur laquelle pointé le paramètre d’entrée _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid :  <br/> |PSETID_Common  <br/> |
|ulKind :  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName :  <br/> |L « ArchiveSourceSupportMask »  <br/> |
   
Cette propriété permet de spécifier si Outlook doit analyser les dossiers dans un magasin et les archiver automatiquement les fournisseurs de magasins.
  
Par défaut, cette propriété n’est pas exposée dans une banque, ce qui signifie qu’Outlook peut analyser les dossiers sur le magasin. Si la propriété est exposée, les valeurs possibles sont les éléments suivants :
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

ASM_DEFAULT
  
- Outlook peut analyser les dossiers sur le magasin.
    
ASM_DO_NOT_ARCHIVE
  
- Outlook n’a pas doit analyser les dossiers sur le magasin.
    
ASM_CLIENT_DO_NOT_CHANGE
  
- Ne pas autoriser les clients à modifier cette propriété dans le magasin. Notez que constante **ASM_CLIENT_DO_NOT_CHANGE** est pour servir ultérieurement de référence et n’est pas implémenté actuellement. À ce stade, un magasin peut empêcher les clients cet indicateur à coder la valeur de cette propriété renvoie le magasin. 
    


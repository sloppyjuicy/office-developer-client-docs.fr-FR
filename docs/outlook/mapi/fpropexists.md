---
title: FPropExists
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FPropExists
api_type:
- COM
ms.assetid: 33c00752-cdc1-4cbe-8fca-6b06c78bd362
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: ccfb503f62ef039700f79cd8852883685f329dfe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783369"
---
# <a name="fpropexists"></a>FPropExists

  
  
**S’applique à**: Outlook 
  
Recherche une balise de propriété donnée d’une interface ou d’une interface [IMAPIProp](imapipropiunknown.md) dérivé **IMAPIProp**, tels que [IMessage](imessageimapiprop.md) ou [IMAPIFolder](imapifolderimapicontainer.md). 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Paramètres

 _pobj_
  
> [in] Pointeur vers l’interface **IMAPIProp** ou une interface dérivée **IMAPIProp** dans laquelle rechercher la balise de propriété. 
    
 _ulPropTag_
  
> [in] Balise de propriété à rechercher.
    
## <a name="return-value"></a>Valeur renvoy�e

TRUE 
  
> Une correspondance de la balise de propriété donné a été trouvée. 
    
FALSE 
  
> Une correspondance de la balise de propriété donnée est introuvable.
    
## <a name="remarks"></a>Remarques

Si la balise de propriété dans le paramètre _ulPropTag_ a type PT_UNSPECIFIED, la fonction **FPropExists** recherche une correspondance basée uniquement sur l’identificateur de propriété. Dans le cas contraire, la correspondance est pour la balise de propriété entière, y compris le type. 
  


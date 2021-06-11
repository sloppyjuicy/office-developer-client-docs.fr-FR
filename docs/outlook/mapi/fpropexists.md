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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 7190065c687524302bae362a2e25d3848e17d1bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429487"
---
# <a name="fpropexists"></a>FPropExists

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recherche une balise de propriété donnée dans une interface [IMAPIProp](imapipropiunknown.md) ou une interface dérivée **d’IMAPIProp,** telle que [IMessage](imessageimapiprop.md) ou [IMAPIFolder](imapifolderimapicontainer.md). 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
BOOL FPropExists(
  LPMAPIPROP pobj,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Parameters

 _pobj_
  
> [in] Pointeur vers l’interface ou l’interface **IMAPIProp** dérivée **d’IMAPIProp** dans laquelle rechercher la balise de propriété. 
    
 _ulPropTag_
  
> [in] Balise de propriété pour laquelle effectuer une recherche.
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Une correspondance a été trouvée pour la balise de propriété donnée. 
    
FALSE 
  
> Une correspondance pour la balise de propriété donnée n’a pas été trouvée.
    
## <a name="remarks"></a>Remarques

Si la balise de propriété dans le paramètre  _ulPropTag_ possède un type PT_UNSPECIFIED, la fonction **FPropExists** recherche une correspondance basée uniquement sur l’identificateur de propriété. Sinon, la correspondance est pour la balise de propriété entière, y compris le type. 
  


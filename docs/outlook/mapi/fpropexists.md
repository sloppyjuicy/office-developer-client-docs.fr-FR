---
title: FPropExists
description: Décrit FPropExists et fournit la syntaxe, les paramètres et la valeur de retour.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MAPI.FPropExists
api_type:
- COM
ms.assetid: 33c00752-cdc1-4cbe-8fca-6b06c78bd362
ms.openlocfilehash: 4e153cc2081e0787ab319fb9c596512d5182ef32
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65815225"
---
# <a name="fpropexists"></a>FPropExists

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recherche une balise de propriété donnée dans une interface [IMAPIProp](imapipropiunknown.md) ou une interface dérivée **d’IMAPIProp**, comme [IMessage](imessageimapiprop.md) ou [IMAPIFolder](imapifolderimapicontainer.md). 
  
|Propriété|Valeur|
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

## <a name="parameters"></a>Paramètres

 _pobj_
  
> [in] Pointeur vers l’interface ou l’interface **IMAPIProp** dérivée **d’IMAPIProp** dans laquelle rechercher la balise de propriété. 
    
 _ulPropTag_
  
> [in] Balise de propriété pour laquelle effectuer une recherche.
    
## <a name="return-value"></a>Valeur renvoyée

TRUE 
  
> Une correspondance pour la balise de propriété donnée a été trouvée. 
    
FALSE 
  
> Une correspondance pour la balise de propriété donnée est introuvable.
    
## <a name="remarks"></a>Remarques

Si la balise de propriété dans le paramètre _ulPropTag_ a un type PT_UNSPECIFIED, la fonction **FPropExists** recherche une correspondance basée uniquement sur l’identificateur de propriété. Sinon, la correspondance concerne l’ensemble de la balise de propriété, y compris le type. 
  


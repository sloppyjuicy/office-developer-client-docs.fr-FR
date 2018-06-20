---
title: HrGetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrGetOneProp
api_type:
- HeaderDef
ms.assetid: 8d0a381a-e714-4663-9a57-b0e1cdbd6ba7
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 4dcdce72781669988a0cb15eb9b3a7cd73494bfb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19783561"
---
# <a name="hrgetoneprop"></a>HrGetOneProp

  
  
**S’applique à**: Outlook 
  
Extrait la valeur d’une propriété unique à partir d’une interface de propriété, autrement dit, une interface dérivée de [IMAPIProp](imapipropiunknown.md). 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Les applications clientes et des fournisseurs de services  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a>Paramètres

 _nous procure_
  
> [in] Pointeur vers l’interface [IMAPIProp](imapipropiunknown.md) à partir de laquelle la valeur de la propriété doit être récupérée. 
    
 _ulPropTag_
  
> [in] Balise de propriété de la propriété à récupérer. 
    
 _ppprop_
  
> [out] Pointeur vers un pointeur vers la structure [SPropValue](spropvalue.md) retournée définissant la valeur de la propriété extraite. 
    
## <a name="return-value"></a>Valeur renvoy�e

MAPI_E_NOT_FOUND 
  
> La propriété demandée n’est pas disponible à partir de l’interface spécifiée.
    
## <a name="remarks"></a>Remarques

Contrairement à la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) , la fonction **HrGetOneProp** ne retourne jamais aucun avertissement. Car il récupère une seule propriété, il suffit réussit ou échoue. Pour extraire plusieurs propriétés, **GetProps** est plus rapide. 
  
Vous pouvez définir ou modifier une propriété unique avec la fonction [HrSetOneProp](hrsetoneprop.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour des exemples de code MFCMAPI, voir le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetMAPIObjectType  <br/> |MFCMAPI utilise la méthode **HrGetOneProp** pour récupérer le type d’un objet.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)


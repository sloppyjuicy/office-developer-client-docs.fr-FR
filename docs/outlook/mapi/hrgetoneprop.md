---
title: HrGetOneProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- HrGetOneProp
api_type:
- HeaderDef
ms.assetid: 8d0a381a-e714-4663-9a57-b0e1cdbd6ba7
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 84685b6d1cc48861da6202f38628330b5ebd0156
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59576169"
---
# <a name="hrgetoneprop"></a>HrGetOneProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Extrait la valeur d’une propriété unique à partir d’une interface de propriété, c’est-à-dire une interface dérivée [d’IMAPIProp](imapipropiunknown.md). 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
HRESULT HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a>Paramètres

 _pmp_
  
> [in] Pointeur vers [l’interface IMAPIProp](imapipropiunknown.md) à partir de laquelle la valeur de propriété doit être récupérée. 
    
 _ulPropTag_
  
> [in] Balise de propriété de la propriété à récupérer. 
    
 _ppprop_
  
> [out] Pointeur vers un pointeur vers la structure [SPropValue renvoyée](spropvalue.md) définissant la valeur de propriété récupérée. 
    
## <a name="return-value"></a>Valeur renvoyée

MAPI_E_NOT_FOUND 
  
> La propriété demandée n’est pas disponible à partir de l’interface spécifiée.
    
## <a name="remarks"></a>Remarques

Contrairement à [la méthode IMAPIProp::GetProps,](imapiprop-getprops.md) la fonction **HrGetOneProp** ne renvoie jamais d’avertissement. Étant donné qu’elle récupère une seule propriété, elle réussit ou échoue simplement. Pour récupérer plusieurs propriétés, **GetProps** est plus rapide. 
  
Vous pouvez définir ou modifier une propriété unique avec [la fonction HrSetOneProp.](hrsetoneprop.md) 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetMAPIObjectType  <br/> |MFCMAPI utilise la **méthode HrGetOneProp** pour récupérer le type d’un objet.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)


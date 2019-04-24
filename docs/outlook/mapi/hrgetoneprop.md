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
ms.openlocfilehash: e5adc7d0c317d8b803645d78227777998d7d241f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347837"
---
# <a name="hrgetoneprop"></a>HrGetOneProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Récupère la valeur d'une propriété unique à partir d'une interface de propriété, c'est-à-dire une interface dérivée de [IMAPIProp](imapipropiunknown.md). 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
HrGetOneProp(
  LPMAPIPROP pmp,
  ULONG ulPropTag,
  LPSPropValue FAR * ppprop
);
```

## <a name="parameters"></a>Paramètres

 _PMP_
  
> dans Pointeur vers l'interface [IMAPIProp](imapipropiunknown.md) à partir de laquelle la valeur de propriété doit être récupérée. 
    
 _ulPropTag_
  
> dans Balise de propriété de la propriété à récupérer. 
    
 _ppprop_
  
> remarquer Pointeur vers un pointeur vers la structure [SPropValue](spropvalue.md) renvoyée qui définit la valeur de la propriété récupérée. 
    
## <a name="return-value"></a>Valeur renvoyée

MAPI_E_NOT_FOUND 
  
> La propriété demandée n'est pas disponible à partir de l'interface spécifiée.
    
## <a name="remarks"></a>Remarques

Contrairement à la méthode [IMAPIProp:: GetProps](imapiprop-getprops.md) , la fonction **HrGetOneProp** ne renvoie aucun avertissement. Étant donné qu'elle récupère une seule propriété, elle réussit ou échoue. Pour récupérer plusieurs propriétés, **GetProps** est plus rapide. 
  
Vous pouvez définir ou modifier une seule propriété à l'aide de la fonction [HrSetOneProp](hrsetoneprop.md) . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |GetMAPIObjectType  <br/> |MFCMAPI utilise la méthode **HrGetOneProp** pour récupérer le type d'un objet.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)


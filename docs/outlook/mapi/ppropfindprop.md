---
title: PpropFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PpropFindProp
api_type:
- HeaderDef
ms.assetid: f23dd6f4-915b-4fe8-ab3f-6d625c7d6061
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: 97021128f92af0486af1ba3125c7843eaa357648
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350729"
---
# <a name="ppropfindprop"></a>PpropFindProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recherche une propriété spécifiée dans un jeu de propriétés.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil. h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Applications clientes et fournisseurs de services  <br/> |
   
```cpp
LPSPropValue PpropFindProp(
  LPSPropValue rgprop,
  ULONG cprop,
  ULONG ulPropTag
);
```

## <a name="parameters"></a>Paramètres

 _rgprop_
  
> dans Tableau de structures [SPropValue](spropvalue.md) qui définissent les propriétés à rechercher. 
    
 _cprop_
  
> dans Nombre de propriétés dans l'ensemble de propriétés indiqué par le paramètre _rgprop_ . 
    
 _ulPropTag_
  
> dans Balise de propriété de la propriété à rechercher dans le jeu de propriétés indiqué par le paramètre _rgprop_ . 
    
## <a name="return-value"></a>Valeur renvoyée

 **PpropFindProp** renvoie une structure [SPropValue](spropvalue.md) définissant la propriété qui correspond à la balise de la propriété Input ou null s'il n'y a aucune correspondance. 
  
## <a name="remarks"></a>Remarques

Si la balise de propriété donnée indique une propriété de type PT_UNSPECIFIED, la fonction **PpropFindProp** recherche une correspondance uniquement pour l'identificateur de propriété dans la balise. Dans le cas contraire, elle trouve une correspondance pour l'intégralité de la balise de propriété, y compris le type de propriété, et renvoie la propriété identifiée. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl. cpp  <br/> |CContentsTableListCtrl:: BuildDataItem  <br/> |MFCMAPI utilise la méthode **PpropFindProp** pour rechercher les propriétés d'un jeu de propriétés ajouté à la liste.  <br/> |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)


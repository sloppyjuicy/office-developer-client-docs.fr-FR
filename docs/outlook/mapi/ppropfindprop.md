---
title: PpropFindProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PpropFindProp
api_type:
- HeaderDef
ms.assetid: f23dd6f4-915b-4fe8-ab3f-6d625c7d6061
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 32b7f70f2d3e976d38e638fda7ee0feb2af4e8b1
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62787645"
---
# <a name="ppropfindprop"></a>PpropFindProp

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Recherche une propriété spécifiée dans un jeu de propriétés.
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapiutil.h  <br/> |
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
  
> [in] Tableau de [structures SPropValue](spropvalue.md) qui définissent les propriétés à rechercher. 
    
 _cprop_
  
> [in] Nombre de propriétés dans le jeu de propriétés indiqué par le  _paramètre rgprop_ . 
    
 _ulPropTag_
  
> [in] Balise de propriété de la propriété à rechercher dans le jeu de propriétés indiqué par le  _paramètre rgprop_ . 
    
## <a name="return-value"></a>Valeur renvoyée

 **PpropFindProp** renvoie une structure [SPropValue](spropvalue.md) définissant la propriété qui correspond à la balise de propriété d’entrée, ou NULL en l’absence de correspondance. 
  
## <a name="remarks"></a>Remarques

Si la balise de propriété donnée indique une propriété de type PT_UNSPECIFIED, la fonction **PpropFindProp** trouve une correspondance uniquement pour l’identificateur de propriété dans la balise. Sinon, il trouve une correspondance pour l’ensemble de la balise de propriété, y compris le type de propriété, et renvoie la propriété identifiée. 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|ContentsTableListCtrl.cpp  <br/> |CContentsTableListCtrl::BuildDataItem  <br/> |MFCMAPI utilise la **méthode PpropFindProp** pour rechercher les propriétés d’un jeu de propriétés ajouté à la liste. |
   
## <a name="see-also"></a>Voir aussi



[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)


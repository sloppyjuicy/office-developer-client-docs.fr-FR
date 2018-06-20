---
title: ValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParms
api_type:
- COM
ms.assetid: 3ede1a35-4acc-4b8f-a1bd-027f35798a37
description: 'Derni�re modification�: lundi 9 mars 2015'
ms.openlocfilehash: a22f7628b306707474e4ffb6fdf4525e00bf0771
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19787481"
---
# <a name="validateparms"></a>ValidateParms

  
  
**S’applique à**: Outlook 
  
Appelle une fonction interne pour vérifier que les applications clientes de paramètres transmis à des fournisseurs de services. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémentée par :  <br/> |MAPI  <br/> |
|Appelée par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Paramètres

 _eMethod_
  
> [in] Spécifie, par l’énumération, la méthode à valider. 
    
 _Premier_
  
> [in] Pointeur vers le premier argument dans la pile.
    
## <a name="return-value"></a>Valeur renvoy�e

S_OK 
  
> Tous les paramètres sont valides. 
    
MAPI_E_CALL_FAILED 
  
> Un ou plusieurs des paramètres ne sont pas valides.
    
## <a name="remarks"></a>Remarques

Paramètres passés entre MAPI et service fournisseurs sont supposés être correct et sont soumis à la validation de débogage uniquement avec la macro [CheckParms](checkparms.md) . Fournisseurs doivent vérifier tous les paramètres passés par les applications clientes, mais les clients doivent supposer que MAPI et le fournisseur de paramètres sont corrects. Utilisez la macro **HR_FAILED** pour tester les valeurs de retour. 
  
 **ValidateParms** est appelé différemment selon que le code appelant est C ou C++. C++ transmet un paramètre implicite appelé _cette_ à chaque appel de méthode, qui est explicite dans C et l’adresse de l’objet. Le premier paramètre, _eMethod_, est un énumérateur à partir de l’interface et la méthode en cours de validation et indique quels paramètres s’attendent à trouver sur la pile. Le deuxième paramètre est différent de C et C++. En C++, elle est appelée _premier_, et il est le premier paramètre à la méthode en cours de validation. Le deuxième paramètre de la langue C, _ppThis_, est l’adresse du premier paramètre à la méthode qui est toujours un pointeur d’objet. Dans les deux cas, le deuxième paramètre donne l’adresse de début de la liste des paramètres de la méthode et en fonction de _eMethod_, déplace vers le bas de la pile et valide les paramètres. 
  
Fournisseurs d’implémentation des interfaces courants tels que **IMAPITable** et **IMAPIProp** doivent toujours vérifier les paramètres à l’aide de la fonction **ValidateParms** afin d’assurer cohérence entre tous les fournisseurs. Fonctions de validation de paramètre supplémentaire ont été définies pour certains types de paramètre complexe à la place, selon le cas. Consultez les rubriques de référence pour les fonctions suivantes : 
  
- [FBadColumnSet](fbadcolumnset.md)
    
- [FBadEntryList](fbadentrylist.md)
    
- [FBadProp](fbadprop.md)
    
- [FBadProp](fbadprop.md)
    
- [FBadRestriction](fbadrestriction.md)
    
- [FBadRestriction](fbadrestriction.md)
    
- [FBadRglpszW](fbadrglpszw.md)
    
- [FBadRow](fbadrow.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
Méthodes héritées utilisent la validation de la même paramètre que l’interface à partir de laquelle ils héritent. Par exemple, la vérification des paramètres des **IMessage** et **IMAPIProp** doivent être la même. 
  
## <a name="see-also"></a>Voir aussi



[UlValidateParms](ulvalidateparms.md)


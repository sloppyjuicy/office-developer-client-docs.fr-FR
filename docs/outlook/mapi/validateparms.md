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
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: f2669f703827924493387c4beac0b64b25672860
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436802"
---
# <a name="validateparms"></a>ValidateParms

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Appelle une fonction interne pour vérifier les paramètres que les applications clientes ont transmis aux fournisseurs de services. 
  
|||
|:-----|:-----|
|Fichier d’en-tête :  <br/> |Mapival.h  <br/> |
|Implémenté par :  <br/> |MAPI  <br/> |
|Appelé par :  <br/> |Fournisseurs de services  <br/> |
   
```cpp
HRESULT ValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Paramètres

 _eMethod_
  
> [in] Spécifie, par l’éumération, la méthode à valider. 
    
 _First_
  
> [in] Pointeur vers le premier argument de la pile.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Tous les paramètres sont valides. 
    
MAPI_E_CALL_FAILED 
  
> Un ou plusieurs paramètres ne sont pas valides.
    
## <a name="remarks"></a>Remarques

Les paramètres transmis entre MAPI et les fournisseurs de services sont supposés corrects et ne subissent une validation de débogage qu’avec la macro [CheckParms.](checkparms.md) Les fournisseurs doivent vérifier tous les paramètres transmis par les applications clientes, mais les clients doivent supposer que les paramètres MAPI et fournisseur sont corrects. Utilisez la macro **HR_FAILED** pour tester les valeurs de retour. 
  
 **ValidateParms est** appelé différemment selon que le code appelant est C ou C++. C++ transmet un paramètre implicite appelé « this  _»_ à chaque appel de méthode, qui devient explicite en C et qui est l’adresse de l’objet. Le premier paramètre,  _eMethod,_ est un éumérateur effectué à partir de l’interface et de la méthode en cours de validation et indique les paramètres à rechercher sur la pile. Le deuxième paramètre est différent pour C et C++. En C++, il s’agit du premier paramètre de la méthode en cours de validation. Le deuxième paramètre du langage C,  _ppThis_, est l’adresse du premier paramètre de la méthode qui est toujours un pointeur d’objet. Dans les deux cas, le deuxième paramètre donne l’adresse du début de la liste des paramètres de la méthode et, en fonction de  _eMethod,_ descend la pile et valide les paramètres. 
  
Les fournisseurs implémentant des interfaces courantes telles que **IMAPITable** et **IMAPIProp** doivent toujours vérifier les paramètres à l’aide de la fonction **ValidateParms** afin de s’assurer de la cohérence entre tous les fournisseurs. Des fonctions de validation de paramètre supplémentaires ont été définies pour certains types de paramètres complexes à utiliser à la place. Consultez les rubriques de référence pour les fonctions suivantes : 
  
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
    
Les méthodes héritées utilisent la même validation de paramètre que l’interface dont elles héritent. Par exemple, la vérification des **paramètres IMessage** et **IMAPIProp** doit être identique. 
  
## <a name="see-also"></a>Voir aussi



[UlValidateParms](ulvalidateparms.md)


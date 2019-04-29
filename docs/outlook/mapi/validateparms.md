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
  
Appelle une fonction interne pour vérifier les paramètres que les applications clientes ont transmises aux fournisseurs de services. 
  
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
  
> dans Spécifie, par énumération, la méthode à valider. 
    
 _First_
  
> dans Pointeur vers le premier argument de la pile.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Tous les paramètres sont valides. 
    
MAPI_E_CALL_FAILED 
  
> Un ou plusieurs paramètres ne sont pas valides.
    
## <a name="remarks"></a>Remarques

Les paramètres transmis entre MAPI et les fournisseurs de services sont supposés être corrects et soumis à la validation de débogage uniquement avec la macro [CheckParms](checkparms.md) . Les fournisseurs doivent vérifier tous les paramètres transmis par les applications clientes, mais les clients doivent supposer que les paramètres MAPI et de fournisseur sont corrects. Utilisez la macro **HR_FAILED** pour tester les valeurs renvoyées. 
  
 **ValidateParms** est appelé différemment selon que le code appelant est C ou C++. C++ transmet un paramètre implicite appelé _This_ à chaque appel de méthode, qui devient explicite dans C et est l'adresse de l'objet. Le premier paramètre, _eMethod_, est un énumérateur créé à partir de l'interface et de la méthode en cours de validation et indique les paramètres à rechercher dans la pile. Le deuxième paramètre est différent pour C et C++. En C++, il est appelé en _premier_, et il s'agit du premier paramètre de la méthode en cours de validation. Le deuxième paramètre de la langue C, _ppThis_, est l'adresse du premier paramètre de la méthode qui est toujours un pointeur d'objet. Dans les deux cas, le deuxième paramètre indique l'adresse du début de la liste des paramètres de la méthode et s'appuie sur _eMethod_, se déplace vers le bas de la pile et valide les paramètres. 
  
Les fournisseurs qui implémentent des interfaces communes, telles que **IMAPITable** et **IMAPIProp** , doivent toujours vérifier les paramètres à l'aide de la fonction **ValidateParms** afin de s'assurer de la cohérence entre tous les fournisseurs. Des fonctions de validation de paramètres supplémentaires ont été définies pour certains types de paramètres complexes à utiliser à la place, le cas échéant. Consultez les rubriques de référence pour les fonctions suivantes: 
  
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
    
Les méthodes héritées utilisent la même validation de paramètre que l'interface dont elles héritent. Par exemple, le contrôle de paramètre pour **IMessage** et **IMAPIProp** doit être le même. 
  
## <a name="see-also"></a>Voir aussi



[UlValidateParms](ulvalidateparms.md)


---
title: IMAPIPropGetPropList
description: Décrit la syntaxe, les paramètres et la valeur de retour d’IMAPIPropGetPropList, qui retourne des balises de propriété pour toutes les propriétés.
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.GetPropList
api_type:
- COM
ms.assetid: 0069c223-32bb-4286-b763-39fd45dc263b
ms.openlocfilehash: 71efb9887688dba9aba143f455419eef68030f39
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65816289"
---
# <a name="imapipropgetproplist"></a>IMAPIProp::GetPropList

**S’applique à** : Outlook 2013 | Outlook 2016
  
Retourne des balises de propriété pour toutes les propriétés.
  
```cpp
HRESULT GetPropList(
  ULONG ulFlags,
  LPSPropTagArray FAR * lppPropTagArray
);
```

## <a name="parameters"></a>Paramètres

 _ulFlags_
  
> [in] Masque de bits des indicateurs qui contrôle le format des chaînes dans les balises de propriété retournées. L’indicateur suivant peut être défini :

MAPI_UNICODE
  
> Les chaînes retournées sont au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, les chaînes sont au format ANSI.

 _lppPropTagArray_
  
> [out] Pointeur vers un pointeur vers le tableau de balises de propriétés qui contient des balises pour toutes les propriétés de l’objet.

## <a name="return-value"></a>Valeur renvoyée

S_OK
  
> Toutes les balises de propriété ont été retournées avec succès.

MAPI_E_BAD_CHARWIDTH
  
> Soit l’indicateur MAPI_UNICODE a été défini et l’implémentation ne prend pas en charge Unicode, soit MAPI_UNICODE n’a pas été défini et l’implémentation prend uniquement en charge Unicode.

## <a name="remarks"></a>Remarques

La méthode **IMAPIProp::GetPropList** récupère la balise de propriété pour chaque propriété actuellement prise en charge par un objet. Si l’objet ne prend actuellement en charge aucune propriété, **GetPropList** retourne un tableau de balises de propriétés avec le membre **cValues** défini sur 0.
  
L’étendue des propriétés retournées par **GetPropList** varie d’un fournisseur à l’autre. Certains fournisseurs de services excluent les propriétés auxquelles l’appelant n’a pas accès. Tous les fournisseurs retournent des propriétés de type **PT_OBJECT**.
  
Si l’objet ne prend pas en charge Unicode, **GetPropList** retourne MAPI_E_BAD_CHARWIDTH, même s’il n’existe aucune propriété de chaîne définie pour l’objet.
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Les fournisseurs de transport distant implémentent **GetPropList** exactement comme spécifié ici. Il n’y a pas de préoccupations particulières. Bien entendu, votre implémentation doit retourner la même liste de propriétés que celle prise en charge par la méthode [IMAPIProp::GetProps](imapiprop-getprops.md) .
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Appelez la fonction [MAPIFreeBuffer](mapifreebuffer.md) pour libérer le tableau de balises de propriétés pointé par _lppPropTagArray_.
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI utilise la méthode **IMAPIProp::GetPropList** pour obtenir une liste de propriétés à passer à **GetProps**. |

## <a name="see-also"></a>Voir aussi

[IMAPIProp::GetProps](imapiprop-getprops.md)  
[MAPIFreeBuffer](mapifreebuffer.md)  
[IMAPIProp : IUnknown](imapipropiunknown.md)
 [MFCMAPI en tant qu’exemple de code](mfcmapi-as-a-code-sample.md)

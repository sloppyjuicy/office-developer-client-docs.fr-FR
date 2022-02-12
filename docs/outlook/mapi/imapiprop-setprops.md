---
title: IMAPIPropSetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.SetProps
api_type:
- COM
ms.assetid: 49f007c9-42e5-4391-8b83-988c9b0ebdba
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 2f8c0d742fd0c3bdd46750124d13f8114fc8a01e
ms.sourcegitcommit: c0fae34cd3a9c75a7cffcf9ae8e417ddde07a989
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/12/2022
ms.locfileid: "62770786"
---
# <a name="imapipropsetprops"></a>IMAPIProp::SetProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Met à jour une ou plusieurs propriétés.
  
```cpp
HRESULT SetProps(
  ULONG cValues,
  LPSPropValue lpPropArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Paramètres

 _cValues_
  
> [in] Nombre de valeurs de propriétés pointées par  _le paramètre lpPropArray_ . Le  _paramètre cValues_ ne doit pas être 0. 
    
 _lpPropArray_
  
> [in] Pointeur vers un tableau de structures [SPropValue](spropvalue.md) qui contiennent des valeurs de propriété à mettre à jour. 
    
 _lppProblems_
  
> [in, out] Lors de l’entrée, un pointeur vers un pointeur vers une structure [SPropProblemArray](spropproblemarray.md) ; Dans le cas contraire, NULL, indiquant qu’il n’est pas nécessaire d’obtenir des informations sur l’erreur. Si  _lppProblems est_ un pointeur valide sur l’entrée, **SetProps** renvoie des informations détaillées sur les erreurs de mise à jour d’une ou plusieurs propriétés. 
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les propriétés ont été correctement mises à jour.
    
Les valeurs suivantes peuvent être renvoyées dans la structure **SPropProblemArray** , mais pas en tant que valeurs de retour **pour SetProps** :
  
MAPI_E_BAD_CHARWIDTH 
  
> L’indicateur MAPI_UNICODE a été définie et l’implémentation ne prend pas en charge Unicode, ou MAPI_UNICODE n’a pas été définie et l’implémentation prend uniquement en charge Unicode.
    
MAPI_E_COMPUTED 
  
> La propriété ne peut pas être mise à jour, car elle est en lecture seule, calculée par le fournisseur de services responsable de l’objet.
    
MAPI_E_INVALID_TYPE 
  
> Le type de propriété n’est pas valide.
    
MAPI_E_NO_ACCESS 
  
> Une tentative de modification d’un objet en lecture seule ou d’accès à un objet pour lequel l’utilisateur dispose d’autorisations insuffisantes a été tentée.
    
MAPI_E_NOT_ENOUGH_MEMORY 
  
> La propriété ne peut pas être mise à jour car elle est supérieure à la taille de la mémoire tampon d’appel de procédure distante (RPC).
    
MAPI_E_UNEXPECTED_TYPE 
  
> Le type de propriété n’est pas le type attendu par l’implémentation d’appel.
    
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Ignorez **la PR_NULL** de propriété ([PidTagNull](pidtagnull-canonical-property.md)) et toutes les propriétés avec un type de **PT_ERROR**. Ne pas apporter de modifications ni signaler de problèmes dans la structure **SPropProblemArray** . 
  
Renvoyer MAPI_E_INVALID_PARAMETER si une propriété de type **PT_OBJECT** est incluse dans le tableau de valeurs de propriété. Renvoyer également cette erreur si une propriété à valeurs multiples est incluse dans le tableau et que son membre **cValues** est définie sur 0. 
  
Si l’appel réussit globalement mais qu’il y a des problèmes avec la définition de certaines propriétés, renvoyez S_OK et placez des informations sur les problèmes dans l’entrée appropriée de la structure **SPropProblemArray** vers qui pointe le paramètre  _lppProblems_ . 
  
## <a name="notes-to-callers"></a>Remarques pour les appelants

Selon le fournisseur de services, vous pouvez également modifier le type de propriété en passant une balise de propriété qui contient un type différent de celui précédemment utilisé avec un identificateur de propriété donné.
  
Si vous incluez une balise de propriété pour une propriété qui n’est pas pris en compte par l’objet et que l’implémentation de **SetProps** permet la création de nouvelles propriétés, la propriété est ajoutée à l’objet. Toute valeur précédente stockée avec l’identificateur de propriété utilisé pour la nouvelle propriété est ignorée. 
  
Notez que la S_OK valeur de retour ne garantit pas que toutes les propriétés ont été correctement mises à jour. Certains fournisseurs cachent les appels **SetProps** jusqu’à ce qu’ils reçoivent un appel nécessitant une intervention du fournisseur, tel que [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ou [IMAPIProp::GetProps](imapiprop-getprops.md). Par conséquent, il est possible de recevoir des valeurs d’erreur liées à l’appel **SetProps** avec les appels ultérieurs. 
  
Si **SetProps renvoie** S_OK, vérifiez la structure **SPropProblemArray** pointée par  _lppProblems_ pour les problèmes de mise à jour des propriétés individuelles. Si **SetProps renvoie** une erreur, ne vérifiez pas le tableau des problèmes de propriété. Appelez plutôt la méthode [IMAPIProp::GetLastError](imapiprop-getlasterror.md) de l’objet. 
  
Lors de la mise à jour de propriétés de grande taille, **SetProps** peut échouer et renvoyer des MAPI_E_NOT_ENOUGH_MEMORY. Il n’existe aucune taille maximale pour les propriétés, et différents objets peuvent avoir des limites différentes. Si vous traitez des propriétés potentiellement importantes, soyez prêt à appeler la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) avec IID_IStream comme identificateur d’interface si **SetProps** renvoie cette valeur d’erreur. 
  
Appelez la [fonction MAPIFreeBuffer](mapifreebuffer.md) pour libérer la structure **SPropProblemArray** . 
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|PropertyEditor.cpp  <br/> |CPropertyEditor::WriteSPropValueToObject  <br/> |MFCMAPI utilise la méthode **IMAPIProp::SetProps** pour écrire une propriété dans un objet une fois la propriété modifiée. |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetLastError](imapiprop-getlasterror.md)
  
[IMAPIProp::GetProps](imapiprop-getprops.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[IMAPIProp::SaveChanges](imapiprop-savechanges.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


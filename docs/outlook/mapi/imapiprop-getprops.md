---
title: IMAPIPropGetProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IMAPIProp.GetProps
api_type:
- COM
ms.assetid: 1c7a9cd2-d765-4218-9aee-52df1a2aae6c
description: Dernière modification le 9 mars 2015
ms.openlocfilehash: 26ab8d67687038118c2dfbbf8d6fc6baddbdcccf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/24/2021
ms.locfileid: "59625532"
---
# <a name="imapipropgetprops"></a>IMAPIProp::GetProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Extrait la valeur de propriété d’une ou plusieurs propriétés d’un objet.
  
```cpp
HRESULT GetProps(
  LPSPropTagArray lpPropTagArray,
  ULONG ulFlags,
  ULONG FAR * lpcValues,
  LPSPropValue FAR * lppPropArray
);
```

## <a name="parameters"></a>Paramètres

 _lpPropTagArray_
  
> [in] Pointeur vers un tableau de balises de propriétés qui identifient les propriétés dont les valeurs doivent être récupérées. Le  _paramètre lpPropTagArray_ doit être NULL, indiquant que les valeurs de toutes les propriétés de l’objet doivent être renvoyées ou pointer vers une structure [SPropTagArray](sproptagarray.md) qui contient une ou plusieurs balises de propriété. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui indique le format des propriétés qui ont le type PT_UNSPECIFIED. L’indicateur suivant peut être définie :
    
MAPI_UNICODE 
  
> Les valeurs de chaîne de ces propriétés doivent être renvoyées au format Unicode. Si l’MAPI_UNICODE n’est pas définie, les valeurs de chaîne doivent être renvoyées au format ANSI.
    
 _lpcValues_
  
> [out] Pointeur vers un nombre de valeurs de propriétés pointées par _le paramètre lppPropArray._ Si  _lppPropArray_ est NULL, le contenu du paramètre  _lpcValues_ est zéro. 
    
 _lppPropArray_
  
> [out] Pointeur vers un pointeur vers les valeurs de propriété récupérées.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les valeurs de propriété ont été récupérées avec succès.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi globalement, mais une ou plusieurs propriétés n’ont pas été accessibles. Le **membre aulPropTag** de la valeur de propriété pour chaque propriété non disponible possède un type de propriété PT_ERROR un identificateur de zéro. Lorsque cet avertissement est renvoyé, l’appel doit être traité comme réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED.** Pour plus d’informations, voir [Utilisation de macros pour la gestion des erreurs.](using-macros-for-error-handling.md)
    
MAPI_E_INVALID_PARAMETER 
  
> Zéro a été transmis dans le membre **cValues** de la structure **SPropTagArray** pointée par  _lpPropTagArray_.
    
## <a name="remarks"></a>Remarques

La **méthode IMAPIProp::GetProps** obtient les valeurs de propriété d’une ou plusieurs propriétés d’un objet. 
  
Les valeurs des propriétés sont renvoyées dans le même ordre que celui demandé (autrement dit, l’ordre des propriétés dans le tableau de balises de propriétés pointés par  _lpPropTagArray_ correspond à l’ordre dans le tableau des structures de valeurs de propriétés pointées par  _lppPropArray_). 
  
Les types de propriété spécifiés dans les membres **aulPropTag** du tableau de balises de propriété indiquent le type de valeur qui doit être renvoyé dans le membre **Value** de chaque structure de valeurs de propriété. Toutefois, si l’appelant ne connaît pas le type d’une propriété, le type dans le membre **aulPropTag** peut être définie à la place sur PT_UNSPECIFIED. Lors de la récupération de la valeur, **GetProps** définit le type correct dans le membre **aulPropTag** de la structure de valeurs de propriété pour la propriété. 
  
Si les types de propriété sont spécifiés dans **l’array SPropTagarray** dans  _lpPropTagArray_, les valeurs de propriété dans **la valeur SPropValue renvoyée** dans  _lppPropArray_ ont des types qui correspondent exactement aux types demandés, sauf si une valeur d’erreur est renvoyée à la place. 
  
Les propriétés de chaîne peuvent avoir l’un des deux types de propriétés : PT_UNICODE pour représenter le format Unicode et PT_STRING8 pour représenter le format ANSI. Si l’MAPI_UNICODE est définie dans le paramètre  _ulFlags,_ chaque fois que **GetProps** ne peut pas déterminer le format approprié pour une propriété de chaîne, il renvoie sa valeur au format Unicode. **GetProps ne** peut pas déterminer un type de propriété de chaîne exact dans les situations suivantes : 
  
- Le  _paramètre lpPropTagArray_ est définie sur NULL pour demander toutes les propriétés. 
    
- Le **membre aulPropTag inclut** la valeur PT_UNSPECIFIED comme type de propriété dans le tableau de balises de propriétés. 
    
Si le  _paramètre lpPropTagArray_ est définie sur NULL pour récupérer toutes les propriétés de l’objet et qu’il n’existe aucune propriété, **GetProps** : 
  
- Renvoie S_OK.
    
- Définit la valeur de nombre dans le membre **cValues** de la structure de valeurs de propriété sur 0. 
    
- Définit le contenu de  _lpcValues_ sur 0. 
    
- Définit  _lppPropArray_ sur NULL. 
    
 **GetProps ne doit** pas renvoyer de propriétés à valeurs multiples avec **des valeurs définies** sur 0. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Appelez la [fonction MAPIAllocateBuffer](mapiallocatebuffer.md) pour allouer initialement de la mémoire pour la structure [SPropValue](spropvalue.md) pointée par  _lpPropTagArray_; appelez [MAPIAllocateMore pour](mapiallocatemore.md) allouer toute mémoire supplémentaire nécessaire aux membres de la structure. 
  
Renvoyer MAPI_W_ERRORS_RETURNED si vous ne pouvez pas récupérer la valeur d’une ou plusieurs des propriétés demandées. Dans la structure de valeurs de propriété, définissez le type dans le membre **aulPropTag** sur PT_ERROR et le membre **Valeur** sur un code d’état qui décrit l’erreur. Par exemple, si vous devez convertir une chaîne en Unicode et ne pas prendre en charge Unicode, définissez le membre **Value** sur MAPI_E_BAD_CHARWIDTH. Si la propriété est trop grande, définissez-la sur MAPI_E_NOT_ENOUGH_MEMORY. Si l’objet ne prend pas en charge la propriété, définissez-la sur MAPI_E_NOT_FOUND. 
  
L’implémentation de la méthode **GetProps** par un fournisseur de transport distant doit renvoyer les valeurs de propriétés du dossier pour les propriétés demandées par l’appelant. Votre implémentation doit : 
  
- Allouez un tableau de valeurs de propriétés à renvoyer à l’appelant et stockez son adresse dans le paramètre de pointeur de valeur de propriété transmis à cet effet.
    
- Copiez les balises de propriété des propriétés du dossier dans les balises de propriété dans le tableau des valeurs de propriété en fonction du tableau des balises de propriété transmises **à GetProps**.
    
- Assurez-vous que le type de propriété est définie pour toutes les balises de propriété transmises **à GetProps**. L’appelant peut transmettre un type de propriété PT_UNSPECIFIED, auquel cas **GetProps** doit définir le type de propriété correct pour cette balise de propriété. 
    
- Définissez la valeur de chaque propriété dans le tableau de valeurs de propriétés en fonction de sa balise. Par exemple, si la balise de propriété demandée par l’appelant **est PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** peut définir la valeur sur MAPI_FOLDER. 
    
- Si l’appelant transmet des balises de propriété que votre implémentation ne gère pas, vous pouvez définir la balise de propriété sur PT_ERROR pour ces propriétés et définir la valeur de la propriété sur MAPI_E_NOT_FOUND.
    
- Renvoyer S_OK si aucune erreur ne s’est produite MAPI_W_ERRORS_RETURNED si des erreurs se sont produites.
    
L’implémentation de la méthode **GetProps** par un fournisseur de transport distant doit au minimum prendre en charge les propriétés suivantes : 
  
- **PR_ACCESS** ([PidTagAccess](pidtagaccess-canonical-property.md))
    
- **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))
    
- **PR_ASSOC_CONTENT_COUNT** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))
    
- **PR_CONTENT_COUNT** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))
    
- **PR_CREATION_TIME** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))
    
- **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))
    
- **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))
    
- **PR_FOLDER_TYPE** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))
    
- **PR_OBJECT_TYPE**
    
- **PR_SUBFOLDERS** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))
    
## <a name="notes-to-callers"></a>Remarques pour les appelants

Pour les propriétés de type PT_OBJECT, appelez la méthode [IMAPIProp::OpenProperty](imapiprop-openproperty.md) au lieu de **GetProps**. 
  
Pour les propriétés sécurisées, ne vous attendez pas à les récupérer en appelant **GetProps** avec  _le paramètre lppPropTagArray_ définie sur NULL. Vous devez définir explicitement l’identificateur d’une propriété sécurisée dans le membre **aulPropTag** de son tableau de balises de propriétés lorsque vous appelez **GetProps**. Le fournisseur de services doit savoir quand et comment une propriété sécurisée est disponible. 
  
Libérez la structure **SPropValue renvoyée** en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) uniquement si **GetProps** renvoie S_OK ou MAPI_W_ERRORS_RETURNED. 
  
Si **GetProps renvoie** MAPI_W_ERRORS_RETURNED car il n’a pas pu accéder à une ou plusieurs propriétés, vérifiez les balises des propriétés renvoyées. Les propriétés qui ont échoué auront les valeurs suivantes définies dans leur structure de valeurs de propriété : 
  
- Type de propriété dans le **membre aulPropTag** définie sur PT_ERROR. 
    
- La valeur de la propriété dans le **membre Value** est définie sur un code d’état pour l’erreur, par exemple MAPI_E_NOT_FOUND. 
    
Les propriétés qui échouent parce qu’elles sont trop  grandes pour être renvoyées dans la structure de valeurs de propriété ont leur membre Value MAPI_E_NOT_ENOUGH_MEMORY. En règle générale, cela se produit avec des chaînes ou des propriétés binaires de type PT_STRING8, PT_UNICODE ou PT_BINARY lorsque la valeur de la propriété est supérieure ou supérieure à 4 Ko. Appelez **IMAPIProp::OpenProperty pour** récupérer des propriétés de grande taille. 
  
Toutes les implémentations de **GetProps** ne peuvent pas prendre en charge les formats Unicode et ANSI pour les chaînes de caractères. Lorsqu’une propriété particulière nécessite une conversion de format de chaîne et **que GetProps** ne peut pas la prendre en charge, le membre **Value** de la propriété est MAPI_E_BAD_CHARWIDTH. 
  
Pour vérifier si un PST est un PST SharePoint, montez le PST à l’aide de [IMAPISession::OpenMsgStore,](imapisession-openmsgstore.md)puis appelez **GetProps** sur l’objet de la boutique de messages demandant cette propriété. S’il existe, vous pouvez supposer que le PST a été configuré pour SharePoint ; si ce n’est pas le cas, le PST n’a pas été configuré comme SharePoint PST. 
  
Pour plus d’informations sur l’utilisation de **GetProps** pour accéder aux propriétés, voir [Récupération des propriétés MAPI.](retrieving-mapi-properties.md)
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI utilise la méthode **IMAPIProp::GetProps** pour obtenir toutes les propriétés d’un objet en passant null ou le tableau renvoyé par la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) dans le paramètre _lpPropTagArray._  <br/> |
   
## <a name="see-also"></a>Voir aussi



[IMAPIProp::GetPropList](imapiprop-getproplist.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)
  
[MAPIAllocateBuffer](mapiallocatebuffer.md)
  
[MAPIAllocateMore](mapiallocatemore.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropTagArray](sproptagarray.md)
  
[SPropValue](spropvalue.md)
  
[IMAPIProp : IUnknown](imapipropiunknown.md)


[MFCMAPI comme un exemple de Code](mfcmapi-as-a-code-sample.md)
  
[Récupération des propriétés MAPI](retrieving-mapi-properties.md)
  
[Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md)


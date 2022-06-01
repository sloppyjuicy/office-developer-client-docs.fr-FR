---
title: IMAPIPropGetProps
description: Décrit la syntaxe, les paramètres et la valeur de retour d’IMAPIPropGetProps, qui récupère la valeur de propriété d’une ou plusieurs propriétés d’un objet.
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
ms.openlocfilehash: 160c8d1f23ee8fd67c4b1b29b3a2026b4d2ca4cd
ms.sourcegitcommit: f872848fbeb5b2353179ad4bf4eab23f61f87666
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/01/2022
ms.locfileid: "65817843"
---
# <a name="imapipropgetprops"></a>IMAPIProp::GetProps

  
  
**S’applique à** : Outlook 2013 | Outlook 2016 
  
Récupère la valeur de propriété d’une ou plusieurs propriétés d’un objet.
  
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
  
> [in] Pointeur vers un tableau de balises de propriétés qui identifient les propriétés dont les valeurs doivent être récupérées. Le paramètre  _lpPropTagArray_ doit être NULL, indiquant que les valeurs de toutes les propriétés de l’objet doivent être retournées, ou pointer vers une structure [SPropTagArray](sproptagarray.md) qui contient une ou plusieurs balises de propriété. 
    
 _ulFlags_
  
> [in] Masque de bits d’indicateurs qui indique le format des propriétés qui ont le type PT_UNSPECIFIED. L’indicateur suivant peut être défini :
    
MAPI_UNICODE 
  
> Les valeurs de chaîne de ces propriétés doivent être retournées au format Unicode. Si l’indicateur MAPI_UNICODE n’est pas défini, les valeurs de chaîne doivent être retournées au format ANSI.
    
 _lpcValues_
  
> [out] Pointeur vers un nombre de valeurs de propriété pointées par le paramètre  _lppPropArray_ . Si  _lppPropArray_ a la valeur NULL, le contenu du paramètre  _lpcValues_ est égal à zéro. 
    
 _lppPropArray_
  
> [out] Pointeur vers un pointeur vers les valeurs de propriété récupérées.
    
## <a name="return-value"></a>Valeur renvoyée

S_OK 
  
> Les valeurs de propriété ont été récupérées avec succès.
    
MAPI_W_ERRORS_RETURNED 
  
> L’appel a réussi dans l’ensemble, mais une ou plusieurs propriétés n’ont pas pu être consultées. Le membre **aulPropTag** de la valeur de propriété pour chaque propriété indisponible a un type de propriété de PT_ERROR et un identificateur égal à zéro. Lorsque cet avertissement est retourné, l’appel doit être traité comme ayant réussi. Pour tester cet avertissement, utilisez la macro **HR_FAILED** . Pour plus d’informations, consultez [Utilisation de macros pour la gestion des erreurs](using-macros-for-error-handling.md).
    
MAPI_E_INVALID_PARAMETER 
  
> Zéro a été passé dans le membre **cValues** de la structure **SPropTagArray** pointée par  _lpPropTagArray_.
    
## <a name="remarks"></a>Remarques

La méthode **IMAPIProp::GetProps** obtient les valeurs de propriété d’une ou plusieurs propriétés d’un objet. 
  
Les valeurs de propriété sont retournées dans le même ordre que celui demandé (autrement dit, l’ordre des propriétés dans le tableau de balises de propriétés pointé par  _lpPropTagArray_ correspond à l’ordre dans le tableau des structures de valeurs de propriétés pointées par  _lppPropArray_). 
  
Les types de propriétés spécifiés dans les membres **aulPropTag** du tableau de balises de propriétés indiquent le type de valeur qui doit être retourné dans le membre **Valeur** de chaque structure de valeur de propriété. Toutefois, si l’appelant ne connaît pas le type d’une propriété, le type dans le membre **aulPropTag** peut être défini à la place sur PT_UNSPECIFIED. Lors de la récupération de la valeur, **GetProps** définit le type correct dans le membre **aulPropTag** de la structure de valeur de propriété pour la propriété. 
  
Si les types de propriétés sont spécifiés dans **le SPropTagArray** dans  _lpPropTagArray_, les valeurs de propriété dans **SPropValue** retournées dans  _lppPropArray_ ont des types qui correspondent exactement aux types demandés, sauf si une valeur d’erreur est retournée à la place. 
  
Les propriétés de chaîne peuvent avoir l’un des deux types de propriétés : PT_UNICODE pour représenter le format Unicode et PT_STRING8 pour représenter le format ANSI. Si l’indicateur MAPI_UNICODE est défini dans le paramètre _ulFlags_ , chaque fois que **GetProps** ne peut pas déterminer le format approprié pour une propriété de chaîne, il retourne sa valeur au format Unicode. **GetProps** ne peut pas déterminer un type de propriété de chaîne exact dans les situations suivantes : 
  
- Le paramètre  _lpPropTagArray_ a la valeur NULL pour demander toutes les propriétés. 
    
- Le membre **aulPropTag** inclut la valeur PT_UNSPECIFIED comme type de propriété dans le tableau de balises de propriétés. 
    
Si le paramètre  _lpPropTagArray_ a la valeur NULL pour récupérer toutes les propriétés de l’objet et qu’aucune propriété n’existe, **GetProps** effectue les opérations suivantes : 
  
- Retourne S_OK.
    
- Définit la valeur de nombre dans le membre **cValues** de la structure de valeurs de propriété sur 0. 
    
- Définit le contenu de  _lpcValues sur_ 0. 
    
- Définit  _lppPropArray sur_ NULL. 
    
 **GetProps** ne doit pas retourner de propriétés à valeurs multiples avec **des valeurs cValues définies** sur 0. 
  
## <a name="notes-to-implementers"></a>Remarques pour les responsables de l’implémentation

Appelez la fonction [MAPIAllocateBuffer](mapiallocatebuffer.md) pour allouer la mémoire initialement pour la structure [SPropValue](spropvalue.md) pointée par  _lpPropTagArray_ ; appelez [MAPIAllocateMore](mapiallocatemore.md) pour allouer toute mémoire supplémentaire nécessaire pour les membres de la structure. 
  
Retournez MAPI_W_ERRORS_RETURNED si vous ne pouvez pas récupérer la valeur d’une ou plusieurs des propriétés demandées. Dans la structure des valeurs de propriété, définissez le type dans le membre **aulPropTag** sur PT_ERROR et le membre **Value** sur un code d’état qui décrit l’erreur. Par exemple, si vous devez convertir une chaîne en Unicode et que vous ne prenez pas en charge Unicode, définissez le membre **Value** sur MAPI_E_BAD_CHARWIDTH. Si la propriété est trop grande, définissez-la sur MAPI_E_NOT_ENOUGH_MEMORY. Si l’objet ne prend pas en charge la propriété, définissez-la sur MAPI_E_NOT_FOUND. 
  
L’implémentation de la méthode **GetProps** par un fournisseur de transport distant doit retourner les valeurs de propriété du dossier pour les propriétés demandées par l’appelant. Votre implémentation doit effectuer les opérations suivantes : 
  
- Allouez un tableau de valeurs de propriétés pour revenir à l’appelant et stocker son adresse dans le paramètre de pointeur de valeur de propriété passé à cet effet.
    
- Copiez les balises de propriété des propriétés du dossier dans les balises de propriété du tableau de valeurs de propriétés en fonction du tableau d’étiquettes de propriétés passé à **GetProps**.
    
- Vérifiez que le type de propriété est défini pour toutes les balises de propriété passées à **GetProps**. L’appelant peut passer un type de propriété de PT_UNSPECIFIED, auquel cas **GetProps** doit définir le type de propriété correct pour cette balise de propriété. 
    
- Définissez la valeur de chaque propriété dans le tableau de valeurs de propriété en fonction de sa balise. Par exemple, si la balise de propriété demandée par l’appelant est **PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md)), **GetProps** peut définir la valeur sur MAPI_FOLDER. 
    
- Si l’appelant transmet des balises de propriété que votre implémentation ne gère pas, vous pouvez définir la balise de propriété sur PT_ERROR pour ces propriétés et définir la valeur de propriété sur MAPI_E_NOT_FOUND.
    
- Retournez S_OK si aucune erreur ne s’est produite ou MAPI_W_ERRORS_RETURNED s’il y a eu des erreurs.
    
L’implémentation de la méthode **GetProps** par un fournisseur de transport distant doit prendre en charge au minimum les propriétés suivantes : 
  
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
  
Pour les propriétés sécurisées, ne vous attendez pas à les récupérer en appelant **GetProps** avec le paramètre  _lppPropTagArray_ défini sur NULL. Vous devez définir explicitement l’identificateur d’une propriété sécurisée dans le membre **aulPropTag** de son tableau de balises de propriétés lorsque vous appelez **GetProps**. Quand et comment une propriété sécurisée est disponible est à la disposition du fournisseur de services. 
  
Libérez la structure **SPropValue** retournée en appelant la fonction [MAPIFreeBuffer](mapifreebuffer.md) uniquement si **GetProps** retourne S_OK ou MAPI_W_ERRORS_RETURNED. 
  
Si **GetProps** retourne MAPI_W_ERRORS_RETURNED parce qu’il n’a pas pu accéder à une ou plusieurs propriétés, vérifiez les balises de propriété des propriétés retournées. Les valeurs suivantes sont définies dans les propriétés ayant échoué dans leur structure de valeurs de propriété : 
  
- Type de propriété dans le membre **aulPropTag** défini sur PT_ERROR. 
    
- Valeur de propriété dans le membre **Valeur** définie sur un code d’état pour l’erreur, par exemple MAPI_E_NOT_FOUND. 
    
Les propriétés qui échouent parce qu’elles sont trop volumineuses pour être facilement retournées dans la structure de valeur de propriété ont leur membre **Value** défini sur MAPI_E_NOT_ENOUGH_MEMORY. En règle générale, cela se produit avec des propriétés de type chaîne ou binaire de type PT_STRING8, PT_UNICODE ou PT_BINARY lorsque la valeur de la propriété est supérieure ou égale à 4 Ko. Appelez **IMAPIProp::OpenProperty** pour récupérer des propriétés volumineuses. 
  
Toutes les implémentations de **GetProps ne prennent** pas en charge les formats Unicode et ANSI pour les chaînes de caractères. Lorsqu’une propriété particulière nécessite une conversion de format de chaîne et que **GetProps** ne peut pas la prendre en charge, le membre **Value** de la propriété est défini sur MAPI_E_BAD_CHARWIDTH. 
  
Pour vérifier si un PST est un SharePoint PST, montez le PST à l’aide [d’IMAPISession::OpenMsgStore](imapisession-openmsgstore.md), puis appelez **GetProps** sur l’objet du magasin de messages demandant cette propriété. S’il existe, vous pouvez supposer que le PST a été configuré pour SharePoint ; sinon, le PST n’a pas été configuré en tant que SharePoint PST. 
  
Pour plus d’informations sur l’utilisation de **GetProps** pour accéder aux propriétés, consultez [Récupération des propriétés MAPI](retrieving-mapi-properties.md).
  
## <a name="mfcmapi-reference"></a>Référence MFCMAPI

Pour voir un exemple de code MFCMAPI, consultez le tableau suivant.
  
|**Fichier**|**Fonction**|**Commentaire**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |GetPropsNULL  <br/> |MFCMAPI utilise la méthode **IMAPIProp::GetProps** pour obtenir toutes les propriétés d’un objet en passant null ou le tableau retourné par la méthode [IMAPIProp::GetPropList](imapiprop-getproplist.md) dans le paramètre _lpPropTagArray_ . |
   
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

